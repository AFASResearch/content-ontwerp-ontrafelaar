---
name: documentsjabloon
description: 'Breng de documentsjabloon-impact van een ontwerp in kaart: moet er een brief, document of correspondentiesjabloon gebouwd worden, welke gegevensverzameling en velden komen erin, en wat bestaat al in Profit versus wat moet de programmeur nieuw toevoegen. Gebruik bij vragen als: welke documentsjablonen zijn nodig, briefsjabloon, correspondentie, document genereren, pdf uit Profit, bijlage bij een mail.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Documentsjabloon-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Moet er een documentsjabloon gebouwd worden?** (of moet een bestaand sjabloon worden aangepast)
2. **Welke gegevensverzameling en welke velden komen als tag in het document?**
3. **Wat bestaat al in Profit en wat moet de programmeur nieuw toevoegen?**

Vraag 3 bepaalt of dit een contenttaak is die wij zelf kunnen inrichten, of een afhankelijkheid richting de programmeur.

---

## Documentsjabloon of berichtsjabloon?

Deze twee worden vaak door elkaar gehaald. Bepaal altijd eerst welke van de twee het is — of allebei.

| | **Documentsjabloon** | **Berichtsjabloon** |
|---|---|---|
| **Wat het is** | Een brief of document (bijvoorbeeld pdf) | Een **mail** |
| **Wat je vastlegt** | Opmaak, tekst en tags van het document | Op het tabblad **E-mail**: **Titel**, **bijlage** en **inhoud** van het bericht |
| **Skill** | Deze skill | Skill `berichtsjabloon` |

> **Het raakvlak:** een documentsjabloon wordt vaak **als bijlage meegestuurd** bij een berichtsjabloon. Zie je dat in het ontwerp, lever dan beide taken op: het document hier, en de mail (titel, bijlage, inhoud) via de skill `berichtsjabloon`.

---

## Waar een documentsjabloon uit bestaat

| # | Onderdeel | Toelichting |
|---|-----------|-------------|
| 1 | **Omschrijving** | De naam van het sjabloon |
| 2 | **Gegevensverzameling** | Levert de velden die je als **tag** in het document plaatst |
| 3 | **De documenttekst** | De vaste tekst met de tags op de juiste plek, per taal |

---

## Stap 1 — Scan het ontwerp: moet er een document komen?

### A) Harde trigger

| Term | Varianten |
|------|-----------|
| **Documentsjabloon** | documentsjabloon, briefsjabloon, Word-sjabloon |
| **Correspondentie** | correspondentie, brief, uitnodiging, bevestiging, verklaring |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Document als uitkomst** | "er wordt een contract gegenereerd", "de gebruiker downloadt een pdf" |
| **Formele vastlegging** | "de afspraak wordt schriftelijk bevestigd" |
| **Bijlage bij een mail** | "de medewerker ontvangt het overzicht als bijlage" |
| **Nieuwe gegevens in een document** | "het document bevat voortaan ook veld X" |

Bij alleen een impliciet signaal: markeer `te weinig info` en zet het door als vraag aan de ontwerper.

---

## Stap 2 — Output per documentsjabloon

### Blok A — Sjabloon (kop)

| Veld | Inhoud |
|------|--------|
| **Omschrijving** | Naam van het documentsjabloon |
| **Gevraagde actie** | `nieuw bouwen + inchecken` / `aanpassen` / `controleren` |
| **Kanaal** | Profit / InSite / OutSite |
| **Aanleiding** | Welke gebeurtenis of processtap het document oplevert |
| **Ontvanger** | Wie het document ontvangt |
| **Verzendwijze** | Download, afdruk of **bijlage bij een berichtsjabloon** (zie raakvlak hierboven) |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok B — Gegevensverzameling en tags

| Veld | Inhoud |
|------|--------|
| **Gegevensverzameling** | Naam van de ggv, of `te weinig info` |
| **Nieuwe ggv nodig** | ja / nee / `te weinig info` |
| **Te gebruiken velden (tags)** | Per veld: waarvoor je het in het document gebruikt en of het al bestaat |
| **Ontbrekende velden** | Velden die de tekst nodig heeft maar die (nog) niet in de ggv zitten |

Werk de velden altijd zo uit:

| Veld | Waarvoor in het document | Bestaat in Profit |
|------|--------------------------|-------------------|
| … | aanhef / adressering / inhoudelijke regel / ondertekening | Zie Stap 3 |

### Blok C — Teksten per taal

| Taal | Documenttekst |
|------|---------------|
| NL | … |
| ENG | … |
| DUI | … |
| FR | … |

Regels voor dit blok:

- Lever **altijd** de **NL**-tekst uit. Dit is de brontekst.
- Beantwoord expliciet **welke talen** nodig zijn. Zegt het ontwerp hier niets over: `te weinig info` + vraag aan de ontwerper.
- De **vertalingen zelf** worden uitgewerkt door de skill `vertalingen`, met de tags ongewijzigd.
- **Tags wijzig of vertaal je nooit.** De tag moet overeenkomen met het veld in de gegevensverzameling.
- Is de tekst nog niet bekend: `nader te bepalen` + benoem wat de tekst moet overbrengen.
- Pas de skill `schrijfwijzer` toe: B1, actief, concreet.

---

## Stap 3 — Bestaat het al in Profit, of moet de programmeur het bouwen?

Beantwoord dit **per gegevensverzameling en per veld**:

| Uitkomst | Wat het betekent | Wie pakt het op |
|----------|------------------|-----------------|
| `bestaat in Profit` | De ggv of het veld is er al en is bruikbaar | **Wij** — contenttaak, direct in te richten |
| `ggv bestaat, veld ontbreekt` | De bron is er, het benodigde veld niet | **Programmeur** voegt het veld toe aan de ggv; onze taak wacht hierop |
| `nieuw te bouwen` | De gegevensverzameling bestaat niet | **Programmeur** bouwt de ggv; onze taak wacht hierop |
| `te weinig info` | Niet vast te stellen uit ontwerp of omgeving | Uitzoeken in de omgeving of navragen bij de ontwerper |

Regels:

- **Verifieer in de omgeving, niet alleen in het ontwerp.**
- **Elke regel `nieuw te bouwen` of `veld ontbreekt` is een afhankelijkheid** en hoort als beslispunt terug.
- **Hergebruik gaat voor nieuwbouw**, ook bij sjablonen: controleer eerst of een bestaand sjabloon volstaat met een extra tag.

---

## Stap 4 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 5 — Buiten scope (altijd opnemen)

- Huisstijl, beeldmateriaal en centrale opmaakrichtlijnen
- Klantspecifieke documentsjablonen
- Het bouwen van de gegevensverzameling zelf als die nieuw is (programmeur)
- De mail waarin het document als bijlage meegaat (valt onder skill `berichtsjabloon`)
- Rapportlayouts (valt onder skill `rapporten`)
- Het uitwerken van de vertalingen zelf (valt onder skill `vertalingen`)
- De workflowstap die het document genereert (valt onder skill `workflow-condities`)

---

## Stap 6 — Beslispunten (altijd opnemen, minimaal 1)

- Komt er een nieuw documentsjabloon of passen we een bestaand sjabloon aan?
- Is het een document, een mail, of allebei (document als bijlage)?
- Welke gegevensverzameling gebruiken we, en moet de programmeur die uitbreiden?
- Welke velden zetten we als tag in de tekst?
- In welke talen leveren we het sjabloon uit (NL / ENG / DUI / FR)?
- Wie is de ontvanger als het ontwerp dit niet benoemt?

---

## Stap 7 — Content (altijd apart opnemen)

- **"Welke tekst en gegevens komen in het document?"**
- **"Waar richt je het sjabloon in?"** — menupad
- **"Wanneer ontvangt de gebruiker dit document?"**
- **"In welke talen is het sjabloon beschikbaar?"**

---

## Kwaliteitscriteria

- [ ] Er staat expliciet of het een documentsjabloon, een berichtsjabloon of beide is
- [ ] Per sjabloon zijn blok A, B en C ingevuld
- [ ] De gegevensverzameling is benoemd, of gemarkeerd als `te weinig info`
- [ ] Elke tag is gekoppeld aan een plek in de documenttekst
- [ ] Per ggv en per veld staat of het al in Profit bestaat of door de programmeur gebouwd moet worden
- [ ] Elke afhankelijkheid richting de programmeur staat als beslispunt
- [ ] De benodigde talen zijn expliciet beantwoord en de NL-brontekst is geleverd
- [ ] Tags staan ongewijzigd en zijn doorgezet naar de skill `vertalingen`
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt
