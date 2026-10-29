# Ontwerp RHR02201 — Uurloon (sub-ontwerp 2 van CAO & uurloon)

Dit is het ontwerp voor het meesturen van het **uurloon** van AFAS Profit naar Nedap Ons. Het uurloon wordt als veld (`hourlyWages`) opgenomen in het bestaande Extended Employee-snapshot van Medewerker- en contractbericht (RHR02197) en hergebruikt volledig het bericht-, aanleiding-, samenvoeg- en verzendmechanisme daarvan. Dit sub-ontwerp voegt twee dingen toe: een trigger op de salaris-/uurloonmutatie en een conditionele veldmapping van het uurloon, gestuurd door het vinkje **Uurloon verzenden** op werkgever/functie in combinatie met *Synchroniseren met Nedap Ons* op medewerker/functie.

**Versiehistorie:**

| Versie | Datum | Auteur | Status | Toelichting |
| :--- | :--- | :--- | :--- | :--- |
| 0.1 | 15-07-2026 | Niek Boeder | Concept | Eerste conceptversie op basis van het plan sub-ontwerp 2. |
| 1.0 | 16-07-2026 | Niek Boeder | Definitief | Reviewbevindingen verwerkt (BR-consistentie, verzendpeildatum/conditiedatum, upsert-opruimen en triggervarianten in US01), open punten afgehandeld en beslissingen opgeschoond. |
| 1.1 | 07-10-2026 | Niek Boeder | Definitief | Verwerking van feedback van de pilotklanten: het niveau waarop wordt bepaald of het uurloon wordt meegestuurd was niet werkbaar. De instelling per soort dienstbetrekking ("Rechten behorend bij soort dienstbetrekking") is volledig vervangen door het vinkje **Uurloon verzenden** op werkgever/functie. Het uurloon gaat nu alleen mee als dat vinkje aan staat **én** er op de begindatum van de salarisregel een medewerker/functie-regel met *Synchroniseren met Nedap Ons = Ja* bestaat. Er komt bewust geen uitzondering per medewerker/functie. De wijzigingen staan afzonderlijk in het delta-bestand v1.0 naar v1.1. |

---

## 1. Inleiding

### Aanleiding

Nedap Ons gebruikt het uurloon van een medewerker voor een aantal specifieke berekeningen: het omrekenen van geldvergoedingen naar tijd (en omgekeerd) bij bijvoorbeeld slaapdienst-, bereikbaarheids- en aanwezigheidsdiensten, en het indexeren van LFB-verlof binnen de GGZ. Zonder aanlevering vanuit Profit moet de klant het uurloon apart in Ons onderhouden, met dubbele invoer en kans op verschillen.

Met dit sub-ontwerp levert Profit het uurloon automatisch mee in het medewerkersnapshot dat al voor Medewerker- en contractbericht (RHR02197) wordt verstuurd. De klant bepaalt per werkgever/functie of het uurloon wordt meegestuurd, zodat alleen gegevens worden gedeeld die functioneel nodig zijn. Pilotklanten hechten sterk aan het voorkomen van onnodig meegestuurde uurlonen.

### Positionering ten opzichte van Medewerker- en contractbericht (RHR02197)

Dit is een **gerichte toevoeging op Medewerker- en contractbericht (RHR02197)**, geen zelfstandige koppeling. Daar was het uurloonmodel (`hourlyWages`) al als gereserveerde plek in de veldmapping opgenomen, maar buiten scope gehouden. Dit sub-ontwerp vult die plek in. Anders dan daar — waar de salarisregel bewust géén aanleiding vuurt — voegt dit ontwerp juist een trigger op de salaris-/uurloonmutatie toe.

### Vooronderzoek

Voor dit ontwerp is gebruikgemaakt van:

- de pilotoverleggen van 13-04-2026, 15-04-2026, 06-05-2026 en 10-06-2026 over de keuze van het instellingsniveau en de uurloondefinities;
- de feedback van de pilotklanten op v1.0: het instellingsniveau soort dienstbetrekking is niet werkbaar en moet een vinkje bij werkgever/functie worden;
- de voortgangsupdate van 01-06-2026 (uurloonbesluit, werkweek t.b.v. uurloon, AVG);
- de Nedap Extended Employee API-analyse voor de structuur van `hourlyWages`;
- de Nedap-velden op werkgever/functie en medewerker/functie uit Nedap-velden in Profit (RHR02186) en de gegevensverzameling die het uurloon berekent.

### Resultaat

Dit sub-ontwerp levert functioneel op:

- het automatisch klaarzetten van een aanleiding bij een relevante salaris-/uurloonmutatie van een gesynchroniseerde medewerker;
- het meesturen van het actuele en toekomstige uurloon per dienstverband in het medewerkersnapshot (`hourlyWages`);
- een vinkje **Uurloon verzenden** op werkgever/functie waarmee de klant bepaalt of het uurloon wordt meegestuurd (standaard Nee); het uurloon gaat alleen mee voor medewerkers die ook gesynchroniseerd worden;
- hergebruik van de bestaande weergave, foutafhandeling en geplande verzendtaak uit Medewerker- en contractbericht (RHR02197).

#### AI-functionaliteit

Voor dit sub-ontwerp wordt geen AI-functionaliteit toegevoegd.

### Afbakening

| In scope | Toelichting |
| :--- | :--- |
| Uurloon in het snapshot | Het actuele en toekomstige uurloon per dienstverband wordt als `hourlyWages` in het bestaande medewerkersnapshot opgenomen. |
| Trigger op salaris/uurloon | Een mutatie op de salarisregel die het uurloon raakt, zet een aanleiding klaar onder de openstaande berichtregel van de medewerker. |
| Conditie per werkgever/functie | Een nieuw vinkje "Uurloon verzenden" op werkgever/functie bepaalt, samen met "Synchroniseren met Nedap Ons" op medewerker/functie, of het uurloon wordt meegestuurd; standaard Nee. |
| Connector en import | Het vinkje is muteerbaar via de update-connector en de imports van werkgever/functie, onder de activering. |

| Buiten scope | Toelichting |
| :--- | :--- |
| Uitzondering per medewerker/functie | Er is bewust geen mogelijkheid om per medewerker/functie het uurloon wel of niet te verzenden. |

### Randvoorwaarden

- De activering "Koppeling Nedap Ons" moet actief zijn (Nedap-velden in Profit, RHR02186).
- Medewerker- en contractbericht (RHR02197) is gerealiseerd; dit sub-ontwerp bouwt op het snapshot-, aanleiding- en verzendmechanisme daarvan.
- De veldgroep "Nedap Ons" op werkgever/functie en het veld "Synchroniseren met Nedap Ons" op medewerker/functie (RHR02186) bestaan. Het veld op medewerker/functie is standaard niet-wijzigbaar (RHR02186 US05-BR2); alleen een applicatiebeheerder kan het per veldcontext wijzigbaar maken, wat het bijzondere geval in US03 mogelijk maakt.
- Voor een juist uurloon per cao vult de klant het veld "werkweek t.b.v. uurloon" (zie Begrippen); de werkwijze hiervoor wordt in de implementatiehandleiding beschreven.

### Begrippen

- **Uurloon:** het berekende uurbedrag van de medewerker op basis van de salarisregel (salarisbedrag, salarissoort en het aantal uren per week). Profit leidt dit af in een gegevensverzameling; het is geen los ingevoerd veld.
- **Werkweek t.b.v. uurloon:** de Payroll-werkweek waarmee het uurloon wordt berekend. Deze kan afwijken van de HRM-werkweek (uren per week voor verlof en bezetting) en vangt het bekende verschil tussen bijvoorbeeld 156 en 156,5 uur per maand op.
- **Werkgever/functie:** de functie van een organisatorische eenheid van de werkgever (`AfasKnOrgEmrFun`), waar de standaardinstellingen voor Nedap Ons worden vastgelegd (RHR02186). De waarden zijn niet tijdgebonden en gelden op de actuele stand.
- **Medewerker/functie:** de functie van een medewerker binnen een dienstverband (`AfasHrEmployeeDepFun`), gekoppeld aan een werkgever/functie, met een begin- en einddatum. Het veld "Synchroniseren met Nedap Ons" wordt hier bij aanmaak overgenomen van werkgever/functie.
- **Snapshot (upsert):** de volledige momentopname van de medewerker die Medewerker- en contractbericht (RHR02197) per medewerker naar de Extended Employee API verstuurt. Nedap Ons verwerkt het als volledige upsert: gegevens die niet (meer) in het snapshot staan, worden bij Ons opgeruimd.
- **Aanleiding:** de reden waarom een snapshot is klaargezet; opeenvolgende mutaties worden samengevoegd tot één openstaande berichtregel per medewerker.
- **Verzendpeildatum:** de systeemdatum waarop het snapshot wordt samengesteld; bepaalt welke uurloonperioden meegaan (de actuele en toekomstige; verlopen perioden niet).
- **Conditiedatum:** de begindatum van de salarisperiode (salarisregel). Op die datum wordt bepaald welke medewerker/functie-regel geldt: die moet *Synchroniseren met Nedap Ons = Ja* hebben en bepaalt via haar werkgever/functie welk vinkje "Uurloon verzenden" van toepassing is. Het vinkje zelf wordt op de actuele waarde beoordeeld bij het samenstellen van het snapshot.
- **Uurloon verzenden:** het vinkje op werkgever/functie dat bepaalt of het uurloon van medewerkers met die werkgever/functie mag worden meegestuurd naar Nedap Ons.

### § Bijlagen

| Bijlage | Titel |
| :--- | :--- |
| A | [Samenvatting voor klant](#bijlage-a--samenvatting-voor-klant) |
| B | [Open punten en beslissingen](#bijlage-b--open-punten-en-beslissingen) |
| C | [Content checklist](#bijlage-c--content-checklist) |

---

## 2. User stories

De user stories beschrijven het functionele verhaal: bij een salaris-/uurloonwijziging wordt een aanleiding klaargezet (US01), het snapshot bevat het uurloon volgens de veldmapping (US02), en de klant bepaalt per werkgever/functie of het uurloon wordt meegestuurd (US03). Berichtstatus, foutafhandeling en verzending zijn ongewijzigd overgenomen uit Medewerker- en contractbericht (RHR02197) en niet als aparte user story opgenomen.

### Overzicht

| Nr | User story | Toelichting |
| :--- | :--- | :--- |
| US01 | Aanleiding klaarzetten bij salaris-/uurloonmutatie | Bij een uurloonwijziging op een gesynchroniseerde medewerker wordt een aanleiding onder de openstaande berichtregel klaargezet |
| US02 | Uurloon meesturen in het snapshot | Het snapshot bevat het actuele en toekomstige uurloon per dienstverband, mits het vinkje "Uurloon verzenden" en "Synchroniseren met Nedap Ons" het meesturen toestaan |
| US03 | Uurloon verzenden per werkgever/functie | De beheerder bepaalt per werkgever/functie met een vinkje of het uurloon wordt meegestuurd (standaard Nee) |

---

### 2.1 US01 — Aanleiding klaarzetten bij salaris-/uurloonmutatie

Als HR-adviseur wil ik dat bij een wijziging van het uurloon van een gesynchroniseerde medewerker automatisch een aanleiding wordt klaargezet, zodat Nedap Ons bij de eerstvolgende verzending het actuele uurloon ontvangt.

#### Functionele uitwerking

- Een mutatie op de medewerker/salaris-regel die het uurloon raakt, zet de aanleiding "Salaris/uurloon gewijzigd" klaar. De trigger kent drie mutatievarianten:
  - Variant A — een nieuwe regel met een nieuwe begindatum: er ontstaat een nieuwe uurloonperiode (bijv. bij een schaal-/tredewijziging of een cao-verhoging die als nieuwe salarisregel wordt vastgelegd).
  - Variant B — een wijziging van een bestaande, actuele of toekomstige regel: de begindatum blijft gelijk en het uurloon van die periode verandert (bijv. een correctie op het bedrag of op de werkweek t.b.v. uurloon).
  - Variant C — het verwijderen van een bestaande, actuele of toekomstige regel: de bijbehorende uurloonperiode vervalt.
- In alle drie de gevallen wordt de aanleiding alleen klaargezet als het berekende uurloon van een actuele of toekomstige periode verandert (bij variant C vervalt die periode) én aan de overige voorwaarden is voldaan. Bestaat er al een openstaande berichtregel, dan komt er alleen een aanleiding bij (samenvoegregel, gelijk aan Medewerker- en contractbericht, RHR02197).
- In Medewerker- en contractbericht (RHR02197) vuurt de salarisregel bewust géén aanleiding. Dit sub-ontwerp voegt die trigger gericht toe; alle overige triggers en het snapshotmechanisme blijven ongewijzigd.
- De aanleiding wordt alleen klaargezet als aan de voorwaarden uit Medewerker- en contractbericht (RHR02197) is voldaan **én** het uurloon voor het dienstverband wordt meegestuurd (US03: vinkje "Uurloon verzenden" aan en synchroniserende medewerker/functie-regel). Zo levert een uurloonwijziging die toch niet wordt aangeleverd geen leeg snapshot op.
- De synchronisatiestatus wordt per salarisperiode bepaald: een salarisregel telt alleen mee als er op de **begindatum van die salarisregel** een medewerker/functie-regel met *Synchroniseren met Nedap = Ja* bestaat voor hetzelfde dienstverband. Het vinkje "Uurloon verzenden" van de werkgever/functie van die regel moet op de actuele stand aan staan.
- **Schaalsalaris zonder salarisregel-mutatie.** De trigger werkt alleen als er daadwerkelijk een medewerker/salaris-regel wordt vastgelegd, gewijzigd of verwijderd (variant A, B of C). Een schaalsalaris kan echter tussentijds wijzigen zonder dat een regel muteert (bijvoorbeeld een cao-verhoging binnen dezelfde schaal en trede die alleen in de schaaltabel verandert); dan vuurt er geen aanleiding en blijft het eerder geleverde uurloon in Ons staan. De klant moet dan zelf een nieuwe salarisregel vastleggen om het uurloon te actualiseren (beslissing B5).

#### Bedrijfsregels

- BR1. Een aanleiding wordt alleen klaargezet als de activering "Koppeling Nedap Ons" actief is.
- BR2. Een aanleiding wordt alleen klaargezet als op de begindatum van de gewijzigde salarisregel een medewerker/functie-regel met *Synchroniseren met Nedap = Ja* geldt voor het dienstverband (begindatum ≤ salaris-begindatum, einddatum leeg of ≥ salaris-begindatum).
- BR3. Een aanleiding wordt alleen klaargezet als het vinkje "Uurloon verzenden" van de werkgever/functie van de medewerker/functie-regel uit BR2 aan staat (leidende conditie: US03-BR2).
- BR4. Alleen mutaties op actuele of toekomstige salarisregels (einddatum leeg of ≥ systeemdatum) leiden tot een aanleiding; wijzigingen op verlopen regels niet.
- BR5. Bestaat er nog geen openstaande berichtregel voor de medewerker, dan maakt Profit die aan met de aanleiding "Salaris/uurloon gewijzigd"; bestaat die al, dan wordt alleen de aanleiding toegevoegd.
- BR6. Een cascade waarbij een nieuw contract of dienstverband een nieuwe salarisregel oplevert, vuurt de aanleiding alleen als het uurloon feitelijk wijzigt.
- BR7. Het wijzigen van het vinkje "Uurloon verzenden" zet zelf géén aanleiding klaar (zie US03).
- BR8. De aanleiding vuurt bij een nieuwe regel met een nieuwe begindatum (variant A), bij het wijzigen van een bestaande actuele of toekomstige regel (variant B) en bij het verwijderen daarvan (variant C); telkens alleen als het berekende uurloon van een actuele of toekomstige periode daardoor verandert of vervalt. Een wijziging of verwijdering op een verlopen regel vuurt niet (BR4).

#### Acceptatiecriteria

1. **US01-AC1** *Given* een gesynchroniseerde medewerker waarvan de werkgever/functie "Uurloon verzenden = Ja" heeft *When* de HR-adviseur het uurloon wijzigt via een nieuwe salarisregel met een nieuwe begindatum (variant A) en opslaat *Then* wordt een aanleiding "Salaris/uurloon gewijzigd" onder de openstaande berichtregel klaargezet.
2. **US01-AC2** *Given* een medewerker met een reeds openstaande berichtregel *When* een uurloonwijziging wordt opgeslagen *Then* wordt de aanleiding aan die bestaande berichtregel gekoppeld en wordt geen tweede berichtregel aangemaakt.
3. **US01-AC3** *Given* een medewerker waarvan de werkgever/functie "Uurloon verzenden = Nee" heeft *When* het uurloon wijzigt *Then* wordt geen aanleiding klaargezet.
4. **US01-AC4** *Given* een medewerker zonder synchroniserende medewerker/functie-regel op de begindatum van de salarisregel *When* het uurloon wijzigt *Then* wordt geen aanleiding klaargezet.
5. **US01-AC5** *Given* de activering "Koppeling Nedap Ons" staat uit *When* het uurloon wijzigt *Then* wordt geen aanleiding klaargezet.
6. **US01-AC6** *Given* een mutatie op een verlopen (historische) salarisregel *When* deze wordt opgeslagen *Then* wordt geen aanleiding klaargezet.
7. **US01-AC7** *Given* een nieuw contract dat via de cascade een nieuwe salarisregel met een gewijzigd uurloon oplevert *When* het contract wordt opgeslagen *Then* wordt de aanleiding "Salaris/uurloon gewijzigd" klaargezet.
8. **US01-AC8** *Given* een salarismutatie waarbij het uurloon ongewijzigd blijft (alleen een niet-uurloonveld wijzigt) *When* de regel wordt opgeslagen *Then* wordt geen aanleiding klaargezet.
9. **US01-AC9** *Given* een gesynchroniseerde medewerker waarvan de werkgever/functie "Uurloon verzenden = Ja" heeft *When* de HR-adviseur een bestaande actuele of toekomstige salarisregel wijzigt waardoor het berekende uurloon verandert (variant B) *Then* wordt een aanleiding "Salaris/uurloon gewijzigd" klaargezet.
10. **US01-AC10** *Given* een gesynchroniseerde medewerker waarvan de werkgever/functie "Uurloon verzenden = Ja" heeft en een eerder geleverde uurloonperiode *When* de HR-adviseur de bijbehorende actuele of toekomstige salarisregel verwijdert (variant C) *Then* wordt een aanleiding klaargezet en vervalt die uurloonperiode in het eerstvolgende snapshot.
11. **US01-AC11** *Given* een medewerker/functie-regel met "Synchroniseren met Nedap Ons = Ja" waarvan de werkgever/functie "Uurloon verzenden = Nee" heeft (afwijkende instelling op medewerker/functie, zie US03) *When* het uurloon wijzigt *Then* wordt geen aanleiding klaargezet.

---

### 2.2 US02 — Uurloon meesturen in het snapshot

Als HR-adviseur wil ik dat het snapshot het actuele en toekomstige uurloon van de medewerker bevat, zodat Nedap Ons de vergoedings- en indexatieberekeningen met het juiste uurloon kan uitvoeren.

#### Functionele uitwerking

- Het uurloon wordt per dienstverband meegestuurd als tijdafhankelijke reeks: per salarisperiode een regel met het uurloon en de ingangsdatum. Alleen actuele en toekomstige perioden gaan mee; verlopen perioden vervallen (gelijk aan Medewerker- en contractbericht, RHR02197).
- Het uurloon is het door Profit berekende uurloon (zie Begrippen). Voor de MVP wordt dit huidige uurloon as-is meegestuurd; het verbeteren van het uurloonbegrip is een apart vervolgproject.
- Per uurloonperiode geldt de conditie uit US03: de reeks bevat alleen perioden waarvoor op de begindatum van de salarisregel een medewerker/functie-regel met *Synchroniseren met Nedap Ons = Ja* bestaat en het vinkje "Uurloon verzenden" van de bijbehorende werkgever/functie aan staat. Bij meerdere dienstverbanden kan het uurloon voor het ene dienstverband wél en het andere niet meegaan.
- Uurlonen mogen elkaar in de tijd niet overlappen; Profit levert een aaneensluitende reeks per dienstverband.

#### Bedrijfsregels

- BR1. Het snapshot bevat per dienstverband de actuele en toekomstige uurloonperioden; de verzendpeildatum is de systeemdatum. Verlopen perioden gaan niet mee.
- BR2. Een uurloonperiode gaat alleen mee als op de begindatum van de salarisregel een medewerker/functie-regel met *Synchroniseren met Nedap Ons = Ja* geldt én het vinkje "Uurloon verzenden" van de werkgever/functie van die regel aan staat (leidende conditie: US03-BR2).
- BR3. Staat het vinkje uit, ontbreekt een medewerker/functie-regel op de begindatum van de salarisregel, of staat daarop *Synchroniseren met Nedap Ons* op Nee, dan blijft het uurloon voor die periode weg uit het snapshot.
- BR4. Het uurloon wordt in centen aangeleverd (het berekende bedrag maal honderd).
- BR5. Het snapshot is een volledige upsert: bevat het geen uurloon (meer) voor een dienstverband — doordat het vinkje op Nee staat, de medewerker/functie niet meer synchroniseert of de werkgever/functie wijzigt — dan ruimt Nedap Ons het eerder geleverde uurloon bij de eerstvolgende verzending op.

#### Acceptatiecriteria

1. **US02-AC1** *Given* een medewerker met "Uurloon verzenden = Ja" op de werkgever/functie, een synchroniserende medewerker/functie-regel en één lopende salarisperiode *When* het snapshot wordt samengesteld *Then* bevat het snapshot één uurloonregel met het berekende uurloon in centen en de ingangsdatum.
2. **US02-AC2** *Given* een medewerker met een lopende en een toekomstige salarisperiode *When* het snapshot wordt samengesteld *Then* bevat het snapshot beide perioden en geen verlopen perioden.
3. **US02-AC3** *Given* "Uurloon verzenden = Nee" voor de werkgever/functie *When* het snapshot wordt samengesteld *Then* bevat het snapshot geen uurloon.
4. **US02-AC4** *Given* een medewerker met een maandsalaris en een gevulde "werkweek t.b.v. uurloon" *When* het uurloon wordt berekend *Then* is het meegestuurde uurloon berekend op basis van die werkweek.
5. **US02-AC5** *Given* een medewerker met twee dienstverbanden waarvan de werkgever/functie van het ene "Uurloon verzenden = Ja" heeft en van het andere "Nee" *When* het snapshot wordt samengesteld *Then* bevat het snapshot alleen het uurloon van het dienstverband met Ja.
6. **US02-AC6** *Given* een medewerker/functie-regel met "Synchroniseren met Nedap Ons = Nee" bij een werkgever/functie met "Uurloon verzenden = Ja" *When* het snapshot wordt samengesteld *Then* bevat het snapshot geen uurloon voor die periode.

---

### 2.3 US03 — Uurloon verzenden per werkgever/functie

Als beheerder wil ik per werkgever/functie kunnen bepalen of het uurloon naar Nedap Ons wordt meegestuurd, zodat de klant voldoet aan de AVG-beginselen dataminimalisatie en doelbinding en alleen uurlonen deelt waar Ons ze functioneel nodig heeft.

#### Functionele uitwerking

- Er komt een nieuw vinkje **Uurloon verzenden** (ja/nee, standaard Nee) op werkgever/functie, in de bestaande veldgroep "Nedap Ons" (RHR02186).
- Het uurloon wordt alleen meegestuurd als aan **beide** voorwaarden is voldaan:
  1. het vinkje "Uurloon verzenden" staat aan bij de werkgever/functie van het dienstverband, **en**
  2. er bestaat op de begindatum van de salarisregel een medewerker/functie-regel met *Synchroniseren met Nedap Ons = Ja* voor het dienstverband.
- Er is **bewust geen mogelijkheid** om per medewerker/functie het uurloon wel of niet te verzenden. Het vinkje komt dus alleen op werkgever/functie en niet op medewerker/functie; de pilotklanten willen zeker weten dat er geen onnodige uurlonen worden meegestuurd. Zie beslissing B2 in Bijlage B.
- **Bijzonder geval.** Als de klant bewust afwijkt op medewerker/functie en daar *Synchroniseren met Nedap Ons* op Ja zet terwijl "Uurloon verzenden" bij de werkgever/functie uit staat, dan gaat de medewerker wél naar Nedap Ons maar het uurloon niet mee. Het vinkje op werkgever/functie is altijd leidend. Dit geval kan alleen voorkomen als de veldcontext van "Synchroniseren met Nedap Ons" op medewerker/functie wijzigbaar is gemaakt (RHR02186 US05-BR2).
- Het vinkje is niet tijdgebonden en wordt beoordeeld op de actuele waarde bij het samenstellen van het snapshot. Welke werkgever/functie van toepassing is, volgt uit de medewerker/functie-regel die geldt op de begindatum van de salarisregel.
- Standaard staat het vinkje op Nee. AFAS levert geen standaardwaarden per cao uit; de klant zet het vinkje zelf aan per werkgever/functie.
- Het vinkje is alleen zichtbaar en muteerbaar als "Synchroniseren met Nedap Ons" op de werkgever/functie op Ja staat, net als weekkaartprofiel en deskundigheid. Zet de beheerder "Synchroniseren met Nedap Ons" op Nee, dan wordt "Uurloon verzenden" automatisch op Nee gezet, zodat een verborgen vinkje nooit actief kan blijven. Dat geldt ook voor wijzigingen via de import en de update-connector.
- Een wijziging van het vinkje zet zelf géén aanleiding klaar en start geen hersynchronisatie. De nieuwe stand gaat mee bij de eerstvolgende reguliere verzending van een geraakte medewerker of via een handmatige re-sync (wizard uit Medewerker- en contractbericht, RHR02197). De bestaande informatieve melding op werkgever/functie bij wijziging in de veldgroep "Nedap Ons" (RHR02186 US02) geldt ook voor dit vinkje; er komt geen aparte melding.
- Bij een functiewijziging naar een andere werkgever/functie geldt voor het eerstvolgende snapshot het vinkje van de nieuwe werkgever/functie. Is dat Nee, dan valt het uurloon weg uit het snapshot (upsert-opruimen, US02-BR5).

> De vormgeving van het eigenschappenscherm en de nieuw-wizard van werkgever/functie met het nieuwe vinkje staan in §4 User interface.

#### Bedrijfsregels

- BR1. Het vinkje "Uurloon verzenden" staat per werkgever/functie, standaardwaarde Nee, en is niet verplicht.
- BR2. Het uurloon wordt alleen in het snapshot opgenomen als het vinkje "Uurloon verzenden" van de werkgever/functie aan staat **én** er op de begindatum van de salarisperiode een medewerker/functie-regel met *Synchroniseren met Nedap Ons = Ja* bestaat voor het dienstverband. Deze conditie is leidend voor US01-BR2/BR3 en US02-BR2.
- BR3. Een wijziging van het vinkje zet geen aanleiding klaar en raakt reeds gesynchroniseerde medewerkers niet direct; de nieuwe stand volgt bij de volgende reguliere verzending of een handmatige re-sync (zie ook US01-BR7).
- BR4. Bij wijziging van het vinkje toont Profit de bestaande informatieve melding op werkgever/functie (RHR02186 US02); bij import wordt die onderdrukt. Er is geen aparte uurloonmelding.
- BR5. Het vinkje is niet tijdgebonden en wordt op de actuele waarde beoordeeld.
- BR6. Het veld is alleen zichtbaar en muteerbaar onder de activering "Koppeling Nedap Ons".
- BR7. Er is geen vinkje of afwijking per medewerker/functie. Staat "Synchroniseren met Nedap Ons" op medewerker/functie op Ja bij een werkgever/functie met "Uurloon verzenden = Nee", dan gaat het uurloon niet mee.
- BR8. Staat het vinkje op Nee of ontbreekt een synchroniserende medewerker/functie-regel op de begindatum van de salarisperiode, dan valt het uurloon weg uit het eerstvolgende snapshot (upsert-opruimen, zie US02-BR5).
- BR9. Het vinkje is alleen zichtbaar en muteerbaar als "Synchroniseren met Nedap Ons" op de werkgever/functie op Ja staat. Staat dat veld op Nee, dan staat "Uurloon verzenden" altijd op Nee: het systeem zet het vinkje bij het opslaan op Nee, ook bij import en connector. Een medewerker/functie met *Synchroniseren = Ja* bij een werkgever/functie met *Synchroniseren = Nee* krijgt daardoor geen uurloon.

#### Acceptatiecriteria

1. **US03-AC1** *Given* een actieve Koppeling Nedap Ons *When* de beheerder het eigenschappenscherm van werkgever/functie opent *Then* is het vinkje "Uurloon verzenden" zichtbaar in de veldgroep "Nedap Ons" met standaardwaarde Nee.
2. **US03-AC2** *Given* "Uurloon verzenden = Ja" op de werkgever/functie en een medewerker/functie-regel met "Synchroniseren met Nedap Ons = Ja" op de begindatum van de salarisregel *When* de medewerker wordt gesynchroniseerd *Then* bevat het snapshot het uurloon.
3. **US03-AC3** *Given* "Uurloon verzenden = Nee" op de werkgever/functie *When* een medewerker met die werkgever/functie wordt gesynchroniseerd *Then* bevat het snapshot geen uurloon.
4. **US03-AC4** *Given* "Uurloon verzenden = Ja" op de werkgever/functie en "Synchroniseren met Nedap Ons = Nee" op de medewerker/functie-regel *When* het snapshot wordt samengesteld *Then* bevat het snapshot geen uurloon voor die periode.
5. **US03-AC5** *Given* "Uurloon verzenden = Nee" op de werkgever/functie en een medewerker/functie-regel waarop de beheerder bewust "Synchroniseren met Nedap Ons = Ja" heeft gezet *When* het snapshot wordt samengesteld *Then* gaat de medewerker mee naar Nedap Ons maar bevat het snapshot geen uurloon.
6. **US03-AC6** *Given* de beheerder wijzigt het vinkje van Nee naar Ja en slaat op via het eigenschappenscherm *Then* toont Profit de bestaande informatieve melding op werkgever/functie en wordt geen aanleiding klaargezet.
7. **US03-AC7** *Given* de beheerder wijzigt het vinkje via de import of de update-connector *When* de wijziging wordt verwerkt *Then* wordt de informatieve melding onderdrukt en wordt geen aanleiding klaargezet.
8. **US03-AC8** *Given* de activering "Koppeling Nedap Ons" staat uit *When* de beheerder werkgever/functie opent *Then* is het vinkje "Uurloon verzenden" niet zichtbaar.
9. **US03-AC9** *Given* het vinkje stond op Ja en wordt op Nee gezet *When* het volgende snapshot van een geraakte medewerker wordt verstuurd *Then* bevat dat snapshot geen uurloon meer en ruimt Nedap Ons het eerder geleverde uurloon op.
10. **US03-AC10** *Given* een medewerker met "Uurloon verzenden = Ja" op de huidige werkgever/functie en een eerder geleverd uurloon *When* een functiewijziging naar een werkgever/functie met "Uurloon verzenden = Nee" wordt vastgelegd en het snapshot wordt verstuurd *Then* bevat het snapshot geen uurloon meer.
11. **US03-AC11** *Given* een actieve Koppeling Nedap Ons *When* de beheerder het eigenschappenscherm van medewerker/functie opent *Then* bestaat er geen veld om het uurloon per medewerker/functie wel of niet te verzenden.
12. **US03-AC12** *Given* een werkgever/functie met "Synchroniseren met Nedap Ons = Nee" *When* de beheerder het eigenschappenscherm of de nieuw-wizard opent *Then* is het vinkje "Uurloon verzenden" niet zichtbaar.
13. **US03-AC13** *Given* een werkgever/functie met "Synchroniseren met Nedap Ons = Ja" *When* de beheerder het eigenschappenscherm of de nieuw-wizard opent *Then* is het vinkje "Uurloon verzenden" zichtbaar en wijzigbaar.
14. **US03-AC14** *Given* een werkgever/functie met "Synchroniseren met Nedap Ons = Ja" en "Uurloon verzenden = Ja" *When* de beheerder "Synchroniseren met Nedap Ons" op Nee zet en opslaat *Then* staat "Uurloon verzenden" op Nee.
15. **US03-AC15** *Given* een werkgever/functie met "Synchroniseren met Nedap Ons = Nee" *When* een import of connector "Uurloon verzenden = Ja" aanlevert *Then* staat "Uurloon verzenden" na het opslaan op Nee.
16. **US03-AC16** *Given* een medewerker/functie met "Synchroniseren met Nedap Ons = Ja" bij een werkgever/functie met "Synchroniseren met Nedap Ons = Nee" *When* het snapshot wordt samengesteld *Then* bevat het snapshot geen uurloon.

---

## 3. Datamodel

Het datamodel hergebruikt de generieke tabellen en codetabellen van Medewerker- en contractbericht (RHR02197) en voegt één aanleidingcode en één instellingveld toe.

### 3.1 Gedeelde codetabel Type aanleiding Nedap Ons bericht

De gedeelde codetabel met typen aanleiding (Medewerker- en contractbericht, RHR02197, codes 01 t/m 15) krijgt één nieuwe waarde:

| Code | Omschrijving | Bron (component) |
| :--- | :--- | :--- |
| 16 | Salaris/uurloon gewijzigd | Medewerker/salaris |

Code 16 volgt op de verzuimberichten 01 t/m 07 en het medewerker- en contractbericht 08 t/m 15. Sub-ontwerp CAO-instellingen gebruikt daarna code 17 **Individuele CAO-instelling gewijzigd** en code 18 **Werkgeversinstelling gewijzigd**. Normdagen voegt geen code toe en hergebruikt code 12 **Rooster gewijzigd**.

### 3.2 Veld "Uurloon verzenden" op werkgever/functie

In het scherm werkgever/functie (`AfasKnOrgEmrFun`, RHR02186 §3.2) komt één nieuw veld, in de bestaande veldgroep "Nedap Ons":

| Veld | Type | Standaard | Bijzonderheid |
| :--- | :--- | :--- | :--- |
| Uurloon verzenden | Ja/nee | Nee | Zichtbaar onder de activering; niet verplicht; niet tijdgebonden |

- **Waarom hier.** Werkgever/functie is het niveau waarop de overige Nedap Ons-instellingen (synchroniseren, weekkaartprofiel, deskundigheid) al worden vastgelegd. Pilotklanten gaven aan dat het niveau soort dienstbetrekking (v1.0) niet werkbaar is en dat het vinkje bij de werkgever/functie moet staan.
- **Vullogica.** Door de beheerder ingesteld per werkgever/functie; geen automatische vulling. Het veld wordt, anders dan "Synchroniseren met Nedap Ons", **niet** overgenomen naar medewerker/functie en heeft daar ook geen tegenhanger: er is bewust geen afwijking per medewerker/functie. Profit leest het vinkje via de werkgever/functie van de medewerker/functie-regel die geldt op de begindatum van de salarisregel.
- **Output.** Staat het vinkje aan en synchroniseert de medewerker/functie-regel, dan bevat het snapshot het uurloon (§5.3); staat het vinkje uit, dan blijft het uurloon weg.
- **Gedrag.** Een wijziging zet geen aanleiding klaar en raakt reeds gesynchroniseerde medewerkers niet direct (US03).
- **Geen mutatietabel, geen InSite.** Werkgever/functie is een beheerentiteit in Profit Windows zonder mutatietabel en zonder InSite-functionaliteit.

### 3.3 Update-connector en imports

Het veld is, onder de activering, beschikbaar in dezelfde update-connectoren en imports als de overige Nedap Ons-velden op werkgever/functie (RHR02186 §3.4 en §3.5):

| Route | Schrijft naar | Nieuw veld |
| :--- | :--- | :--- |
| Update-connector `KnOrgEmrFun` | Werkgever/functie | Uurloon verzenden |
| HRM > Beheer > Import HRM > Functie (nieuw) | Werkgever/functie | Uurloon verzenden |
| HRM > Beheer > Import HRM > Functie (mutatie) | Werkgever/functie | Uurloon verzenden |

De importmodules "Functie (nieuw)" en "Functie (mutatie)" bouwen hun importvelden op uit de tabelbeschrijving van werkgever/functie (`Kn/Oef`); het nieuwe veld is daardoor automatisch importeerbaar zodra het in de MDD staat. Bij "Functie (mutatie)" blijft een niet aangeleverd veld ongewijzigd. Er wordt geen aparte importmelding getoond. Staat de activering uit, dan is het veld niet importeerbaar en niet in het connector-schema opgenomen. De connectoren `KnEmployee` (element `AfasOrgunitFunction`, dat op medewerker/functie werkt) en `HrOnboarding` en de import Org. eenheid/functie op medewerker/functie krijgen géén nieuw veld.

### 3.4 Hergebruikte tabellen

De berichtregel- en aanleiding-tabellen en de foutafhandeling uit Medewerker- en contractbericht (RHR02197) worden ongewijzigd hergebruikt; dit sub-ontwerp voegt hieraan alleen de nieuwe aanleiding (code 16) toe.

### 3.5 Conversie

Er is geen dataconversie nodig. Bestaande werkgever/functie-regels krijgen bij oplevering de standaardwaarde **Nee** voor het nieuwe veld "Uurloon verzenden"; de klant zet het vinkje daarna zelf aan. De instelling per soort dienstbetrekking uit v1.0 is nog niet opgeleverd en wordt vervangen, dus er is niets om te converteren.

---

## 4. User interface

Dit sub-ontwerp voegt één veld toe aan bestaande UI-onderdelen van werkgever/functie: het eigenschappenscherm (§4.1) en de nieuw-wizard "Nieuwe functie" (§4.2). Er komen geen nieuwe menu-items, weergaven, meldingen of InSite-functionaliteiten bij; het betreft een beheerentiteit in Profit Windows (zie §3.2).

### 4.1 Eigenschappenscherm werkgever/functie

Het bestaande eigenschappenscherm van werkgever/functie (`AfasKnOrgEmrFun`) wordt uitgebreid met het ja/nee-veld **Uurloon verzenden** in de bestaande veldgroep **Nedap Ons** (RHR02186). Het scherm, de tabbladindeling en de overige velden blijven ongewijzigd.

**Eigenschappen**

| Eigenschap | Waarde |
| :--- | :--- |
| Bladeren | Nee (ongewijzigd) |
| Conditie | Het veld "Uurloon verzenden" is alleen zichtbaar en muteerbaar onder de activering "Koppeling Nedap Ons" |

**Veldgroep Nedap Ons**

| Veld | Wijzigbaar | Verplicht |
| :--- | :--- | :--- |
| Synchroniseren met Nedap Ons | Ja (ongewijzigd) | Nee |
| Weekkaartprofiel | Ja (ongewijzigd) | Verplicht als Synchroniseren = Ja |
| Deskundigheid | Ja (ongewijzigd) | Verplicht als Synchroniseren = Ja |
| Uurloon verzenden (nieuw) | Ja, alleen als Synchroniseren = Ja | Nee (standaardwaarde Nee) |

**Gedrag en wijzigbaarheid**

- Standaardwaarde Nee; het vinkje is niet tijdgebonden.
- Het veld is alleen zichtbaar en wijzigbaar als "Synchroniseren met Nedap Ons" op werkgever/functie op Ja staat (US03-BR9), gelijk aan weekkaartprofiel en deskundigheid. Wordt Synchroniseren op Nee gezet, dan zet Profit "Uurloon verzenden" op Nee. Het uurloon gaat daarnaast pas daadwerkelijk mee voor medewerkers waarvan de medewerker/functie-regel synchroniseert (US03).
- Bij wijziging van het vinkje toont Profit de bestaande informatieve melding bij wijziging in de veldgroep "Nedap Ons" op werkgever/functie (RHR02186 US02). Bij muteren via de import of connector wordt deze melding onderdrukt.

**Autorisatie**

De autorisatie volgt het bestaande scherm van werkgever/functie; er komt geen apart autorisatierecht bij.

### 4.2 Nieuw-wizard werkgever/functie

Het veld **Uurloon verzenden** verschijnt ook in de bestaande nieuw-wizard "Nieuwe functie" van werkgever/functie, in dezelfde veldgroep **Nedap Ons** als op het eigenschappenscherm (onder de activering). Standaardwaarde Nee. De weergave van werkgever/functie krijgt geen extra kolom, gelijk aan het bestaande veld "Adresgegevens meesturen".

---

## 5. Gegevensverwerking

### 5.1 Aanmaken bericht (klaarzetten aanleiding)

Een uurloonwijziging op de salarisregel zet — mits aan de voorwaarden is voldaan — de aanleiding "Salaris/uurloon gewijzigd" klaar onder de openstaande berichtregel van de medewerker. Dit geldt voor alle drie de mutatievarianten uit US01: een nieuwe regel met een nieuwe begindatum (A), een wijziging van een bestaande actuele of toekomstige regel (B) en het verwijderen daarvan (C). Het verdere klaarzetten en samenvoegen verloopt identiek aan Medewerker- en contractbericht (RHR02197).

Profit zet de aanleiding "Salaris/uurloon gewijzigd" alleen klaar als ná de uurloonwijziging aan alle onderstaande voorwaarden is voldaan. Zodra één voorwaarde niet klopt, gebeurt er niets (geen aanleiding):

1. De activering "Koppeling Nedap Ons" is actief.
2. Op de begindatum van de gewijzigde salarisregel bestaat er voor het dienstverband een medewerker/functie-regel met *Synchroniseren met Nedap = Ja*.
3. Het vinkje "Uurloon verzenden" staat aan bij de werkgever/functie van de medewerker/functie-regel uit voorwaarde 2 (actuele waarde).
4. De salarisregel is actueel of toekomstig (einddatum leeg of ≥ systeemdatum).

Is aan alle vier voldaan, dan zet Profit aanleiding 16 klaar onder de openstaande berichtregel van de medewerker; bestaat die berichtregel nog niet, dan maakt Profit hem eerst aan. Het op Nee zetten van het vinkje vuurt zelf geen aanleiding (US03-BR3); de gewijzigde stand gaat mee bij de eerstvolgende verzending van een geraakte medewerker of via een handmatige re-sync.

**Samenvoegregel.** Bestaat er al een openstaande berichtregel voor de medewerker, dan wordt de aanleiding daaraan gekoppeld; anders maakt Profit een nieuwe openstaande berichtregel aan. Het snapshot bevat altijd de volledige actuele stand, dus samenvoegen is inherent consistent.

### 5.2 Verzenden snapshot en verwerken respons

De verzending verloopt ongewijzigd via de geplande taak en de foutafhandeling van Medewerker- en contractbericht (RHR02197). Het uurloon wordt meegestuurd als onderdeel van hetzelfde medewerkersnapshot; er is geen apart bericht of endpoint. Per uurloonperiode geldt de conditie uit US03-BR2 (vinkje "Uurloon verzenden" aan én synchroniserende medewerker/functie-regel op de begindatum van de salarisregel). De handmatige re-sync en de initiële synchronisatie (wizard uit Medewerker- en contractbericht, RHR02197) stellen hetzelfde snapshot samen en nemen het uurloon mee onder dezelfde conditie. Er komen geen nieuwe signalen, weergaven of menu-items bij; de bestaande Nedap Ons-weergave toont ook de aanleiding "Salaris/uurloon gewijzigd".

### 5.3 Veldmapping — Uurloon (`hourlyWages`)

**Bron — het berekende uurloon.** Het uurloon is geen apart ingevoerd veld op de salarisregel, maar wordt door Profit **berekend** in de gegevensverzameling voor het salaris (`Vw_AfasHrEmployeeSalary01`, kolom `AfasHrHourlyWage` / veld `HrWg`). De berekening werkt in twee stappen:

1. **Is de salarissoort al een uurbedrag?** Bij soort salaris "per uur" is het uurloon gelijk aan het salarisbedrag van de salarisregel; er wordt niets omgerekend.
2. **Anders: periodesalaris omrekenen naar een uurbedrag.** Bij een maand-, week-, vierweken-, halvemaand- of kwartaalsalaris deelt Profit het salarisbedrag door het aantal uren in die periode. Dat aantal volgt uit het aantal uren per week maal het aantal weken in de periode:

| Salarisperiode | Omrekening naar uurloon |
| :--- | :--- |
| Per week | salarisbedrag / (uren per week) |
| Per twee weken | salarisbedrag / (uren per week × 2) |
| Per vier weken | salarisbedrag / (uren per week × 4) |
| Per halve maand | (salarisbedrag × 6) / (uren per week × 13) |
| Per maand | (salarisbedrag × 3) / (uren per week × 13) |
| Per kwartaal | salarisbedrag / (uren per week × 13) |

De factor 13 volgt uit het jaarritme: een jaar telt 52 weken, dus 13 weken per kwartaal; een maand is een derde van een kwartaal (13/3 weken).

**De rol van "Werkweek t.b.v. uurloon".** Het "aantal uren per week" in de omrekening hierboven is niet automatisch de reguliere werkweek. Profit gebruikt hiervoor het veld **"Werkweek t.b.v. uurloon"** (`AfasHrHoursPerWeekLoan`, de Payroll-werkweek) uit de standaard dagen en uren per regeling/arbeidsvoorwaarde. Is dat veld gevuld, dan rekent Profit daarmee; is het leeg, dan valt Profit terug op het reguliere veld **"Uren per week"** (`AfasHrHoursPerWeek`, de HRM-werkweek die ook voor verlof en bezetting geldt).

Zo kan de klant het uurloon afstemmen op de definitie van zijn cao, los van de HRM-werkweek. Voorbeeld bij een maandsalaris:

- Met een reguliere werkweek van **36 uur** wordt gedeeld door 36 × 13 / 3 = **156** uur per maand.
- Vult de klant "Werkweek t.b.v. uurloon" op **36,11538**, dan wordt gedeeld door 36,11538 × 13 / 3 ≈ **156,5** uur per maand.

Hiermee wordt het bekende verschil tussen 156 en 156,5 uur per maand tussen loonstrook en Ons opgevangen. De klant is verantwoordelijk voor het correct vullen van "Werkweek t.b.v. uurloon"; de implementatiehandleiding beschrijft dit (zie beslissing B6 en Bijlage C).

**Doel.** De uitwisseling gebruikt de uurloon-reeks van de Extended Employee API. Deze is tijdafhankelijk en mag niet overlappen.

| Profit-gegeven | API-veld | Verplicht | Toelichting |
| :--- | :--- | :--- | :--- |
| Berekend uurloon (in centen) | `wageInCents` | Nee | Berekend uurbedrag maal honderd (bijv. € 15,00 = 1500). Profit rekent al met twee decimalen, dus dit levert hele centen op. |
| Ingangsdatum salarisperiode | `beginDate` | Ja | Startdatum van de uurloonperiode |
| Einddatum salarisperiode | `endDate` | Nee | Leeg bij de actuele, lopende periode |
| Medewerker | `employeeNumber` | Nee* | Identificatie van de medewerker (uit Medewerker- en contractbericht, RHR02197) |
| Dienstverband | `employmentNumber` | Nee* | Onderscheidt dienstverbanden bij dezelfde medewerker |

> *Óf `employeeNumber` óf de interne Ons-referentie is verplicht; Profit levert `employeeNumber` + `employmentNumber`, gelijk aan Medewerker- en contractbericht (RHR02197).

**Voorbeeld.** Onderstaand `hourlyWages`-fragment hoort bij het medewerkersnapshot (§5.2) en is gebaseerd op testmedewerker 0013 (Floor van der Aar) uit de DM_ZW-omgeving — dezelfde medewerker als het voorbeeld van Medewerker- en contractbericht (RHR02197). De medewerker heeft twee gesynchroniseerde dienstverbanden; per dienstverband gaat de actuele uurloonperiode mee (verzendpeildatum = systeemdatum). Het maandsalaris van € 10.783 bij dienstverband 1 levert bij een werkweek van 36 uur (deler 156) een uurloon van € 69,12 = 6912 centen; verlopen perioden gaan niet mee.

```json
"hourlyWages": [
  {
    "employeeNumber": "0013",
    "employmentNumber": 1,
    "beginDate": "2026-07-01",
    "wageInCents": 6912
  },
  {
    "employeeNumber": "0013",
    "employmentNumber": 2,
    "beginDate": "2026-02-01",
    "wageInCents": 3146
  }
]
```

---

## Bijlage A — Samenvatting voor klant

### Wat verandert er?

AFAS Profit kan het uurloon van je medewerkers automatisch meesturen naar Nedap Ons, als onderdeel van het medewerkerbericht dat al wordt verstuurd. Ons gebruikt het uurloon voor berekeningen zoals vergoedingen voor slaap-, bereikbaarheids- en aanwezigheidsdiensten en voor het indexeren van LFB-verlof. Bij een wijziging van het uurloon zet Profit automatisch klaar dat er een nieuw bericht verstuurd moet worden.

### Wat wordt niet doorgegeven of ondersteund?

Het uurloon wordt alleen meegestuurd voor medewerkers van wie de werkgever/functie het vinkje "Uurloon verzenden" heeft aan staan en die zelf gesynchroniseerd worden met Nedap Ons. Je kunt dit niet per medewerker instellen. Zet je bij een medewerker bewust "Synchroniseren met Nedap Ons" aan terwijl het vinkje bij de werkgever/functie uit staat, dan gaat de medewerker wel naar Ons, maar het uurloon niet.

AFAS stuurt een nieuw uurloon alleen mee als er een **nieuwe salarisregel** (salarismutatie) wordt vastgelegd, bijvoorbeeld bij een schaal- of tredewijziging. Een schaalsalaris kan echter tussentijds wijzigen zonder dat er een nieuwe salarisregel ontstaat — bijvoorbeeld bij een cao-verhoging binnen dezelfde schaal en trede. In dat geval merkt de koppeling de wijziging niet automatisch op en blijft het eerder geleverde uurloon in Ons staan.

**Oplossing.** Voer bij zo'n tussentijdse wijziging — bijvoorbeeld een minimumloonupdate per 1 juli — de medewerker/salaris-mutaties op via een **import**. Elke geïmporteerde salarisregel is een nieuwe salarisregel en zet daarmee automatisch het geactualiseerde uurloon klaar voor verzending naar Ons. Zo actualiseer je in één keer alle betrokken medewerkers.

### Wat kun je monitoren of instellen?

- Je bepaalt **per werkgever/functie** met het vinkje **Uurloon verzenden** of het uurloon wordt meegestuurd (standaard staat dit uit).
- Voor een juist uurloon per cao vul je het veld **"werkweek t.b.v. uurloon"**. De implementatiehandleiding beschrijft hoe je dit doet en hoe het verschil tussen bijvoorbeeld 156 en 156,5 uur per maand wordt opgevangen.
- De status van de berichten en de foutafhandeling volg je in dezelfde weergave als de overige Nedap Ons-berichten.

### Wat valt buiten de eerste versie?

- Het verbeteren van het uurloonbegrip zelf (bruto/WML/cao-uurloon, deler per cao) is een apart vervolgproject.
- Het automatisch opmerken van uurloonwijzigingen die ontstaan door cao-/schaalwijzigingen zonder salarismutatie.

---

## Bijlage B — Open punten en beslissingen

### Open punten

Er zijn geen openstaande punten. De eerder genoemde punten zijn vastgesteld: de aanleidingcode is definitief 16 (beslissing B9), de uurloonberekening uit de salaris-gegevensverzameling inclusief "werkweek t.b.v. uurloon" is het uitgangspunt (beslissingen B1 en B6), en er is geen aanvullende afrondingsspecificatie nodig omdat het uurloon al met twee decimalen wordt berekend (zie §5.3).

### Beslissingen

| Nr | Beslissing |
| :--- | :--- |
| B1 | Voor de MVP wordt het huidige (berekende) uurloon as-is meegestuurd. Uit de pilotoverleggen en de voortgangsupdate van 01-06-2026 bleek dat er behoefte kan zijn aan een preciezer of anders gedefinieerd uurloonbegrip — bijvoorbeeld een bruto-, WML- of cao-uurloon met een eigen deler per cao. Zo'n verbetering vraagt eerst functionele afstemming (welk uurloon, welke deler per cao) en raakt meerdere klanten verschillend; daarom wordt ze als apart vervolgproject opgepakt en valt ze buiten dit sub-ontwerp. |
| B2 | De conditie "wel/niet uurloon verzenden" wordt vastgelegd met een vinkje op werkgever/functie (v1.1; in v1.0 per soort dienstbetrekking). Het uurloon gaat alleen mee als dat vinkje aan staat én de medewerker/functie-regel op de begindatum van de salarisregel *Synchroniseren met Nedap Ons = Ja* heeft. Pilotklanten vonden het niveau soort dienstbetrekking niet werkbaar. Er is bewust géén mogelijkheid om per medewerker/functie het uurloon wel of niet te verzenden: de klanten willen zeker weten dat er geen onnodige uurlonen worden meegestuurd. Bij een bewuste afwijking op medewerker/functie (synchroniseren Ja terwijl het vinkje bij de werkgever/functie uit staat) gaat het uurloon niet mee. |
| B3 | Het vinkje is niet tijdgebonden en wordt op de actuele waarde beoordeeld; alleen "Synchroniseren met Nedap Ons" op medewerker/functie wordt per begindatum van de salarisregel bepaald. Standaard Nee; AFAS levert geen standaardwaarden per cao uit. |
| B4 | De trigger vuurt alleen op de salaris-/uurloonmutatie en alleen als aan de conditie uit B2 is voldaan. Een wijziging van het vinkje triggert zelf geen (her)synchronisatie en toont de bestaande informatieve melding op werkgever/functie (RHR02186 US02). |
| B5 | Uurloon volgt de medewerker/salaris-regel. AFAS stuurt een geactualiseerd uurloon mee wanneer een medewerker/salaris-regel wordt vastgelegd, gewijzigd of verwijderd (varianten A, B en C in US01). Een schaalsalaris kan echter tussentijds wijzigen zonder dat een regel muteert (bijv. een cao-verhoging binnen dezelfde schaal en trede die alleen in de schaaltabel verandert); dan volgt geen aanlevering en moet de klant zelf een nieuwe salarisregel vastleggen om het uurloon te actualiseren. Bekende MVP-beperking, bevestigd in de pilotenquête (twee klanten) en het pm-overleg van 22-04-2026; de mutatieroutes zijn gecommuniceerd in de voortgangsupdate van 01-06-2026. |
| B6 | Het verschil tussen HRM- en Payroll-werkweek (bijv. 156/156,5) wordt opgevangen via het bestaande veld "werkweek t.b.v. uurloon". |
| B7 | Het snapshot is een volledige upsert. Het uurloon wordt als volledige stand meegestuurd; laat het snapshot voor een dienstverband geen (of geen actueel) uurloon meer zien, dan ruimt Nedap Ons het eerder geleverde uurloon op. Dit is het expliciete uitgangspunt van de koppeling, gelijk aan Medewerker- en contractbericht (RHR02197). |
| B8 | Uitzetten of verwijderen werkt niet met terugwerkende kracht op reeds geleverde gegevens. Het op Nee zetten van het vinkje zet zelf geen (her)synchronisatie in gang; het eerder geleverde uurloon wordt pas opgeruimd bij de eerstvolgende verzending van een geraakte medewerker of via een handmatige re-sync. Aanvaarde beperking, consistent met de AVG-motivatie van US03 en met beslissing B4. |
| B9 | De aanleidingcode voor "Salaris/uurloon gewijzigd" is definitief 16 (eerstvolgende vrije nummer in de gedeelde codetabel; zie §3.1). |
| B10 | Het vinkje "Uurloon verzenden" is alleen zichtbaar bij "Synchroniseren met Nedap Ons = Ja" op werkgever/functie, conform de bestaande velden `Adresgegevens meesturen`, weekkaartprofiel en deskundigheid. Anders dan bij die velden wordt de waarde bij Synchroniseren = Nee ook teruggezet naar Nee: een verborgen vinkje mag het uurloon niet onzichtbaar blijven vrijgeven, gezien de eis van de pilotklanten dat er geen onnodige uurlonen worden verzonden. |

---

## Bijlage C — Content checklist

| Onderdeel | Tekst / locatie | Status |
| :--- | :--- | :--- |
| Veldlabel | "Uurloon verzenden" in de bestaande veldgroep "Nedap Ons" op werkgever/functie | Nieuw — vertaling nodig |
| Veldgroeplabel | "Nedap Ons" (bestaande veldgroep op werkgever/functie, RHR02186) | Hergebruik bestaande term |
| Tooltip | Korte uitleg bij het veld "Uurloon verzenden" (waarvoor Ons het uurloon gebruikt; standaard uit; geldt alleen voor gesynchroniseerde medewerkers) | Nieuw — nog op te stellen |
| Informatieve melding | Bestaande melding bij wijziging in de veldgroep "Nedap Ons" op werkgever/functie (RHR02186 US02); geen aparte uurloonmelding meer | Hergebruik bestaande tekst |
| Codetabelwaarde | Aanleiding "Salaris/uurloon gewijzigd" (code 16) | Nieuw — vertaling nodig |
| Implementatiehandleiding | Uitleg "werkweek t.b.v. uurloon" en het 156/156,5-verschil | Aandachtspunt afdeling Content |
