---
name: informatiebolletje
description: 'Breng de informatiebolletje-impact van een ontwerp in kaart: welke velden in Profit, InSite of OutSite een informatiebolletje (veldtoelichting) nodig hebben of moeten worden aangepast. Gebruik bij vragen als: welke informatiebolletjes zijn nodig, wat zijn de veldinfo-wijzigingen, maak de informatiebolletje-paragraaf, veldinfo content, veldtoelichting.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Informatiebolletje-analyse

## Doel

Volledig in kaart brengen welke **informatiebolletjes** een ontwerp vereist — zowel expliciet benoemde als impliciet noodzakelijke veldinformatie — voor Profit, InSite en/of OutSite.

Een informatiebolletje is een toelichting die verschijnt wanneer een gebruiker op het icoontje bij een veld klikt.

Lever het resultaat altijd op in drie blokken: **Wel doen**, **Niet doen** en **Twijfel**. Niet elk geraakt veld krijgt een bolletje; de skill maakt die keuze expliciet en motiveert hem.

---

## Waar vul je het informatiebolletje?

1. Open de omgeving en zet de **consultancy-modus** aan.
2. Ga naar **Consultancy / Anta Taal / Veldinfo content (informatiebolletje)**.
3. Zoek het veld en open de regel. Er zijn twee weergaven: één met de velden waarvan het bolletje gevuld is en één met **Alle velden**. Zie je het veld niet? Kijk dan bij `Alle velden`.
4. Vul de tekst bij de eigenschappen en sla op. De wijziging is nog niet direct zichtbaar in de weergave; open de regel opnieuw om hem te zien.
5. Push op de normale manier. Onder SQL2XML staat het veld onder `Veldinfo content`.

### Vaste regels

- **Content is eigenaar van de Nederlandse tekst.** Elke wijziging in de Nederlandse tekst loopt via de content-afdeling.
- **Een veld kan op meerdere plekken worden gebruikt.** Controleer altijd via de weergave `Alle velden` waar het veld nog meer voorkomt. Is het veld gedeeld, houd de tekst dan generiek of laat het bolletje ongemoeid en zet de uitleg in de help.
- **Elke wijziging maakt een nieuw ResId.** Ook bij het aanpassen van een bestaand bolletje. De tekst staat één à twee dagen later in de Vertaaltool en gaat automatisch mee in het reguliere vertaalproces. Je hoeft hiervoor geen aparte vertaaltaak op te voeren.
- **Maximale lengte is niet gedocumenteerd.** Hanteer korte zinnen en een compacte tekst. Noem bij twijfel expliciet dat de limiet onbekend is.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

Markeer altijd als informatiebolletje-taak wanneer een van de volgende termen letterlijk voorkomt:

| Term | Varianten |
|------|-----------|
| **Informatiebolletje** | informatiebolletje, info-bolletje |
| **Veldhelp** | veldhelp, veld-help |
| **Veldinfo** | veldinfo, veld-info |
| **Veldinfo content** | veldinfo content, veldinformatie |
| **Tooltip** | tooltip |

### B) Impliciete signalen

Markeer ook als informatiebolletje-taak wanneer uit de tekst blijkt dat een veld toelichting nodig heeft, ook al wordt de term "informatiebolletje" niet gebruikt. Herken dit aan:

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld** | "krijgt een nieuw veld X", "op scherm Y komt veld X" |
| **Verplaatst veld** | "de instelling verhuist van A naar B" |
| **Gewijzigde betekenis** | "het veld wordt voortaan gevuld met…" |
| **Toelichting bij veld** | "het veld X behoeft uitleg", "een toelichting op veld X is gewenst" |
| **Gebruiksinstructie bij invoer** | "de gebruiker moet weten dat…", "uitleg over hoe het veld te gebruiken" |
| **Betekenis van waarden** | "de codes staan voor…", "dit veld bevat drie mogelijke waarden: …" |
| **Voorwaardelijke zichtbaarheid** | "het veld is zichtbaar afhankelijk van…" |
| **Complexe invoereis** | "het formaat is…", "de waarde mag alleen…" |
| **Verwijzing naar externe context** | "zie ook…", "conform CAO…" — als dit bij een veld staat |

---

## Stap 2 — Deel elk gevonden veld in: wel doen, niet doen of twijfel

Bepaal per veld in welk blok het hoort. Gebruik deze criteria.

### Wel doen

Plaats het veld hier als minstens één punt geldt:

- Het veld is nieuw of staat nieuw op dit scherm.
- Het veld heeft meerdere keuzewaarden met een verschillend effect.
- Het gedrag of de betekenis van het veld wijzigt aantoonbaar door dit ontwerp.
- Het ontwerp vraagt expliciet om een informatiebolletje.

### Niet doen

Plaats het veld hier als minstens één punt geldt:

- Het veld is breed gedeeld en de betekenis blijft gelijk; alleen het gebruik verandert.
- De uitleg gaat over een proces of uitkomst in plaats van over het veld zelf. Die hoort in de help.
- Het gaat om zichtbaarheidsregels, validaties of conversiegevolgen.
- Een specifieke tekst maakt het bolletje op een andere plek onjuist.

Motiveer elk `niet doen` in één zin, zodat de keuze toetsbaar is.

### Twijfel

Plaats het veld hier als je een vraag moet beantwoorden voordat je bouwt, bijvoorbeeld:

- Onduidelijk of het veld blijft bestaan of vervalt.
- Onduidelijk of het veld een regel heeft in `Veldinfo content`.
- Onduidelijk of de bestaande tekst nog klopt na de wijziging.
- Het ontwerp noemt een groep velden zonder ze te benoemen.

Formuleer de openstaande vraag, niet je vermoeden. Noem wie hem beantwoordt. Lever de concepttekst alvast mee voor het geval de twijfel de kant van `wel doen` op valt.

---

## Stap 3 — Output samenstellen

Gebruik **geen tabellen**. Werk per veld met een kop en een opsomming, zodat de lezer blokken los kan kopiëren naar Word of OneNote.

Begin met een korte inleiding van maximaal drie regels: ontbrekende bronbestanden, betrouwbaarheid van paginanummers en een telzin (bijvoorbeeld: "Bouw vier bolletjes, laat drie velden met rust en zoek vijf punten uit").

Gebruik daarna de blokken `WEL DOEN`, `NIET DOEN` en `TWIJFEL`, in die volgorde. Nummer de velden doorlopend over de blokken heen.

Lever per veld deze regels op:

- **Veldnaam** als kop
- **Bestand/scherm**: waar het veld staat, met het volledige pad in Profit. Noteer het als `Menu / submenu / scherm / tabblad`, bijvoorbeeld `HRM / Payroll / Cao / [cao] / Loonschaal / Eigenschappen loonschaal`. Ken je het pad niet zeker? Geef het beste pad en zet erachter `(pad controleren in de omgeving)`. Bij InSite of OutSite noteer je portal, pagina en paginaonderdeel.
- **Kanaal**: alleen opnemen bij InSite, OutSite of meerdere kanalen. Laat deze regel weg als het ontwerp uitsluitend Profit raakt; meld dat dan één keer in de inleiding.
- **Type signaal**: `expliciet` (term staat erin) of `impliciet` (veld heeft aantoonbaar toelichting nodig)
- **Gevraagde actie**: `nieuw` / `aanpassen` / `verwijderen` / `geen actie`
- **Gedeeld veld**: `nee` / `ja, tekst generiek houden` / `onbekend, controleren via weergave Alle velden`
- **Vertaalgevolg**: `ja, nieuw ResId` bij elke nieuwe of gewijzigde Nederlandse tekst
- **Status**: `komt voor` / `te weinig info` (+ wat ontbreekt)
- **Bron (ontwerp)**: Hoofdstuk/§ | Pagina | (anker: "ankerzin/titel")
- **Waarom wel** (blok Wel doen), **Waarom niet** (blok Niet doen) of **Uit te zoeken** (blok Twijfel)
- **Beoogde inhoud**: concrete concepttekst als blockquote, of `nader te bepalen` als het ontwerp dit niet specificeert

In het blok `Niet doen` laat je `Gevraagde actie` op `geen actie` staan en sla je de concepttekst over.

Gebruik één blok per veld. Heeft hetzelfde veld in meerdere kanalen een ander informatiebolletje nodig? Gebruik dan een apart blok per kanaal en noem het kanaal dan wel.

Sluit altijd af met de sectie **Waar vul je het informatiebolletje?**, zodat de lezer het pad en de vaste regels bij de hand heeft.

### Concepttekst schrijven

Pas de skill `schrijfwijzer` toe op elke concepttekst:

- Schrijf op B1-niveau, actief en in de tweede persoon (`je`).
- Begin met de actie van de gebruiker, niet met de systeemwerking.
- Licht keuzewaarden toe in een opsomming, één regel per waarde.
- Gebruik de vraagvorm voor uitzonderingen: "Is de medewerker jonger? Dan …".
- Houd de tekst kort; de maximale lengte is niet gedocumenteerd.

### Voorbeeldopzet van de output

Volg deze opzet letterlijk. Vervang de voorbeeldinhoud door de bevindingen uit het ontwerp.

```markdown
# Informatiebolletjes [projectnaam] — voorstel in drie delen

Dit ontwerp raakt uitsluitend Profit; InSite en OutSite komen niet voor. De deelprojectdocumenten staan niet in de workspace, dus toets dit voorstel daar nog tegen. Paginanummers zijn niet betrouwbaar beschikbaar; ik gebruik hoofdstuk plus ankerzin. Bouw vier bolletjes, laat drie velden met rust en zoek vijf punten uit.

Menupaden zijn gebaseerd op het ontwerp en de gangbare Profit-indeling. Controleer ze in de omgeving voordat je vult.

---

# WEL DOEN — [aantal] nieuwe bolletjes

## 1. [Veldnaam]

- Bestand/scherm: HRM / Payroll / Cao / [cao] / Loonschaal / Eigenschappen loonschaal (pad controleren in de omgeving)
- Type signaal: impliciet (verplaatst veld, betekenis van waarden)
- Gevraagde actie: nieuw
- Gedeeld veld: onbekend, controleren via weergave Alle velden
- Vertaalgevolg: ja, nieuw ResId
- Status: `komt voor`
- Bron (ontwerp): Hoofdstuk 4 | Pagina onbekend | (anker: "…")
- Waarom wel: [één zin]

Beoogde inhoud:

> [concepttekst]

---

# NIET DOEN — laat deze velden met rust

## 5. [Veldnaam]

- Bestand/scherm: HRM / Medewerker / [medewerker] / Arbeidsvoorwaarde / Rooster (pad controleren in de omgeving)
- Gevraagde actie: geen actie
- Status: `komt voor`
- Bron (ontwerp): Hoofdstuk 5 | Pagina onbekend | (anker: "…")
- Waarom niet: [één zin]

---

# TWIJFEL — eerst uitzoeken

## 8. [Veldnaam]

- Bestand/scherm: HRM / Payroll / Cao / [cao] / Eigenschappen cao (pad controleren in de omgeving)
- Type signaal: impliciet (gewijzigd gedrag)
- Gevraagde actie: aanpassen, afhankelijk van de uitkomst
- Gedeeld veld: onbekend, controleren via weergave Alle velden
- Vertaalgevolg: ja, nieuw ResId
- Status: `te weinig info`
- Bron (ontwerp): Hoofdstuk 7 | Pagina onbekend | (anker: "…")
- Uit te zoeken: [vraag] Vraag dit aan [team].

Beoogde inhoud bij aanpassing:

> [concepttekst]

---

## Waar vul je het informatiebolletje?

[vaste sectie]

## Buiten scope

[vaste sectie]
```

Let op bij het invullen:

- Nummer door over de drie blokken heen, zodat elk veld één uniek nummer heeft.
- In het blok `Niet doen` laat je `Type signaal`, `Gedeeld veld` en `Vertaalgevolg` weg; die voegen daar niets toe.
- Zet de concepttekst altijd als blockquote, zodat de bouwer hem los kan kopiëren.

---

## Stap 4 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item **Bron (ontwerp)** toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Als hoofdstuk/pagina **niet betrouwbaar beschikbaar** is:
- Vermeld dat expliciet.
- Gebruik **sectietitel of tekstfragment** als anker.

---

## Stap 5 — Buiten scope (altijd opnemen)

Sluit de volgende onderwerpen expliciet uit en benoem ze als "buiten scope":

- Helptext of documentatie buiten velden (bijv. procesbeschrijvingen, handleidingen)
- Verplichte veldvalidaties of foutmeldingen (die worden elders beheerd)
- Vrije tekstvelden op InSite-pagina's die geen veldkoppeling hebben
- Tooltips of popups die via maatwerk/custom code worden getoond en niet via `Veldinfo content` worden gevuld
- De vertaling naar ENG, DUI en FR — die loopt automatisch via de Vertaaltool en valt niet onder de skill `vertalingen`
