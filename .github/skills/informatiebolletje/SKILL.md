---
name: informatiebolletje
description: 'Breng de informatiebolletje-impact van een ontwerp in kaart: welke velden in Profit, InSite of OutSite een informatiebolletje (veldtoelichting) nodig hebben of moeten worden aangepast. Een tooltiptekst in een ontwerp is hetzelfde als een informatiebolletje en valt altijd onder deze skill. Gebruik bij vragen als: welke informatiebolletjes zijn nodig, tooltiptekst, tooltipteksten herschrijven, wat zijn de veldinfo-wijzigingen, maak de informatiebolletje-paragraaf, veldinfo content, veldtoelichting.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Informatiebolletje-analyse

## Doel

Volledig in kaart brengen welke **informatiebolletjes** een ontwerp vereist — zowel expliciet benoemde als impliciet noodzakelijke veldinformatie — voor Profit, InSite en/of OutSite.

Een informatiebolletje is een toelichting die verschijnt wanneer een gebruiker op het icoontje bij een veld klikt.

> **Let op: tooltiptekst = informatiebolletje.** Noemt een ontwerp een "tooltiptekst", "tooltipteksten", "tooltip", "veldhelp" of "veldinfo"? Dan gaat het over het informatiebolletje en valt het onder deze skill. Behandel die teksten altijd als concepttekst die je toetst en herschrijft.

Lever het resultaat altijd op in drie blokken: **Wel doen**, **Niet doen** en **Twijfel**. Niet elk geraakt veld krijgt een bolletje; de skill maakt die keuze expliciet en motiveert hem.

De output bevat **uitsluitend** die drie blokken, met per veld alleen de veldnaam, de plek en de tekst. Zie Stap 3.

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
| **Tooltip** | tooltip, tooltiptekst, tooltipteksten, tooltiptekstje, hovertekst |

Staat er in het ontwerp een paragraaf of tabel met tooltipteksten? Neem dan **elk** daarin genoemd veld op in de analyse. Die teksten zijn een concept van de ontwerper, geen eindtekst: toets ze en herschrijf ze volgens de skill `schrijfwijzer`.

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

De output is **altijd** dezelfde drie blokken, in deze volgorde: `WEL DOEN`, `NIET DOEN`, `TWIJFEL`. Niets ervoor, niets ertussen, niets erna.

Per veld lever je precies drie regels op, zonder tabel en zonder nummering:

1. **Veldnaam** — vet, exact zoals in het ontwerp.
2. **Waar** — kanaal plus plek, op één regel. In Profit: `Profit — scherm, tabblad, veldgroep`. In InSite of OutSite: portal, pagina en paginaonderdeel. Geldt hetzelfde veld in meerdere kanalen met dezelfde tekst? Noem ze dan samen op die ene regel.
3. **Tekst** — de informatiebolletjetekst als blockquote.

In het blok `NIET DOEN` vervang je de blockquote door één zin met de reden. In het blok `TWIJFEL` vervang je de blockquote door de openstaande vraag plus wie hem beantwoordt.

Scheid de drie blokken met een horizontale lijn. Gebruik één blok per veld; heeft hetzelfde veld per kanaal een andere tekst nodig, maak dan twee blokken.

### Wat je weglaat uit de output

Deze skill gebruikt onderstaande informatie wél om tot een oordeel te komen, maar zet die **niet** in de output:

- inleiding, telzin, samenvatting of toelichting op de werkwijze
- bronverwijzing, status, type signaal, gevraagde actie, gedeeld veld, vertaalgevolg
- de secties `Waar vul je het informatiebolletje?` en `Buiten scope`
- een verantwoording van de herschrijving of schrijftips

Vraagt de gebruiker expliciet om onderbouwing, bronverwijzing of schrijftips? Lever die dan pas ná de drie blokken.

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
# WEL DOEN

**[Veldnaam]**
Profit — [scherm], [tabblad], veldgroep [naam]
> [tekst van het informatiebolletje]

**[Veldnaam]**
Profit en InSite — [scherm], [tabblad], veldgroep [naam]
> [tekst van het informatiebolletje]

---

# NIET DOEN

**[Veldnaam of onderwerp]**
InSite — [portal / pagina / paginaonderdeel]
Geen bolletje. [Reden in één zin.]

---

# TWIJFEL

**[Veldnaam]**
Profit — [scherm], [tabblad]
[Openstaande vraag in één of twee zinnen.] Vraag dit aan [team].
```

Let op bij het invullen:

- Geen koppen per veld, geen nummering, geen opsommingstekens met metadata.
- Ken je het Profit-pad niet zeker? Zet `(pad controleren in de omgeving)` achter de plek.
- Zet de tekst altijd als blockquote, zodat de bouwer hem los kan kopiëren naar `Veldinfo content`.
- Staan de drie blokken leeg? Lever dan alleen het blok dat gevuld is; laat lege blokken weg.

---

## Stap 4 — Bronverwijzing (bijhouden, niet tonen)

Houd per veld bij waar je het vandaan hebt, in dit format:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, gebruik dan sectietitel of tekstfragment als anker.

Deze verwijzing staat **niet** in de standaardoutput. Lever hem alleen als de gebruiker erom vraagt of een bevinding betwist.

---

## Stap 5 — Buiten scope (bewaken, niet tonen)

Deze onderwerpen vallen buiten de skill. Neem velden die hieronder vallen niet op in `WEL DOEN`; hoort een veld thuis in `NIET DOEN`, benoem dan kort de reden.

- Helptext of documentatie buiten velden (bijv. procesbeschrijvingen, handleidingen)
- Verplichte veldvalidaties of foutmeldingen (die worden elders beheerd)
- Vrije tekstvelden op InSite-pagina's die geen veldkoppeling hebben
- Tooltips of popups die via maatwerk/custom code worden getoond en niet via `Veldinfo content` worden gevuld
- De vertaling naar ENG, DUI en FR — die loopt automatisch via de Vertaaltool en valt niet onder de skill `vertalingen`

---

## Kwaliteitscriteria

- [ ] De output bestaat uitsluitend uit de blokken `WEL DOEN`, `NIET DOEN` en `TWIJFEL`
- [ ] Elk veld heeft precies drie regels: veldnaam, waar, tekst
- [ ] Elke tekst staat als blockquote en is geschreven volgens de skill `schrijfwijzer`
- [ ] Tooltipteksten uit het ontwerp zijn allemaal opgepakt en herschreven, niet overgenomen
- [ ] Procesuitleg staat niet in het bolletje maar in de help
- [ ] Geen inleiding, geen samenvatting, geen metadata en geen schrijftips, tenzij gevraagd
