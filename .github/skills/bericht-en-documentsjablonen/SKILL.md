---
name: bericht-en-documentsjablonen
description: 'Breng de impact van een ontwerp op bericht- en documentsjablonen in kaart: nieuwe of gewijzigde e-mailberichten, brieven, documenten en correspondentiesjablonen in Profit, InSite of OutSite. Gebruik bij vragen als: welke sjablonen zijn nodig, moet er een berichtsjabloon aangepast, e-mailsjabloon, documentsjabloon, correspondentie, welke velden uit de gegevensverzameling als tag.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Bericht- & documentsjablonen-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Moet er een berichtsjabloon komen?** (of moet een bestaand sjabloon worden aangepast)
2. **Welke velden uit de gegevensverzameling gebruiken we als tag in de tekst?**
3. **Welke tekst komt erin — inclusief het onderwerp van de mail, per taal?**

Staat het woord **"berichtsjabloon"** in het ontwerp, dan is dat het signaal dat wij het sjabloon moeten **bouwen en inchecken**.

---

## Wat is een berichtsjabloon?

Een berichtsjabloon is in de praktijk **een mail**. Het bestaat uit drie onderdelen:

| # | Onderdeel | Toelichting |
|---|-----------|-------------|
| 1 | **Omschrijving** | De naam van het sjabloon, met **`(Profit)`** erachter. Voorbeeld: `Uitnodigen sollicitant (Profit)` |
| 2 | **Gegevensverzameling** | Levert de velden die je als **tag** in de tekst kunt plaatsen. Voorbeeld: `Roepnaam`, `Vacature`, `Omschrijving bericht`, `Telnr. werk`, `Mail werk` |
| 3 | **De e-mail zelf, per taal** | Per taalregel (**NL / ENG / DUI / FR**) vul je twee dingen: het veld **Onderwerp (mail)** en de **inhoud** in de berichtsjabloon-editor |

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Harde trigger

Staat het woord **berichtsjabloon** (of een variant) letterlijk in het ontwerp, dan is er **altijd** een taak: bouwen en inchecken.

| Term | Varianten |
|------|-----------|
| **Berichtsjabloon** | berichtsjabloon, e-mailsjabloon, mailsjabloon |
| **Documentsjabloon** | documentsjabloon, briefsjabloon, Word-sjabloon |
| **Correspondentie** | correspondentie, brief, uitnodiging, bevestiging |

### B) Impliciete signalen

Ook zonder het woord "berichtsjabloon" kan er een sjabloon nodig zijn:

| Signaal | Voorbeelden |
|---------|-------------|
| **Automatische verzending** | "de medewerker ontvangt een e-mail", "er wordt een bevestiging verstuurd" |
| **Workflowbericht** | "bij afkeuring krijgt de aanvrager bericht" |
| **Signaal met e-mail** | een signaaldefinitie die automatisch een e-mailbericht verstuurt |
| **Nieuwe gegevens in een bericht** | "het bericht bevat voortaan ook veld X" |
| **Document als uitkomst** | "er wordt een contract gegenereerd", "de gebruiker downloadt een pdf" |
| **Anderstalige ontvanger** | "ook voor buitenlandse vestigingen" |

Bij een impliciet signaal: markeer als `te weinig info` als het ontwerp niet expliciet om een berichtsjabloon vraagt, en zet het door als vraag aan de ontwerper.

---

## Stap 2 — Output per berichtsjabloon

Lever per sjabloon **drie blokken** op: eerst de kop, dan de velden, dan de teksten.

### Blok A — Sjabloon (kop)

| Veld | Inhoud |
|------|--------|
| **Omschrijving** | Naam van het sjabloon **inclusief `(Profit)`**, bijv. `Uitnodigen sollicitant (Profit)` |
| **Type** | Berichtsjabloon (e-mail) / documentsjabloon |
| **Gevraagde actie** | `nieuw bouwen + inchecken` / `aanpassen` / `controleren` |
| **Aanleiding** | Welke gebeurtenis, processtap of signaal het bericht triggert |
| **Ontvanger** | Wie de mail ontvangt |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok B — Gegevensverzameling en tags

| Veld | Inhoud |
|------|--------|
| **Gegevensverzameling** | Naam van de gegevensverzameling, of `nader te bepalen` |
| **Nieuwe ggv nodig** | ja / nee / `te weinig info` |
| **Te gebruiken velden (tags)** | Opsomming van de velden die als tag in de tekst komen |
| **Ontbrekende velden** | Velden die de tekst nodig heeft maar die (nog) niet in de gegevensverzameling zitten |

Noem per veld waarvóór je het gebruikt, bijvoorbeeld: `Roepnaam` → aanhef, `Vacature` → verwijzing in de tekst, `Mail werk` → ondertekening.

### Blok C — Teksten per taal

| Taal | Onderwerp (mail) | Inhoud bericht |
|------|------------------|----------------|
| NL | … | … |
| ENG | … | … |
| DUI | … | … |
| FR | … | … |

Regels voor dit blok:

- Lever **altijd** de **NL**-tekst uit, inclusief onderwerp. Dit is de brontekst.
- Beantwoord per sjabloon expliciet **welke talen** nodig zijn. Zegt het ontwerp hier niets over: `te weinig info` + vraag aan de ontwerper.
- De **daadwerkelijke vertalingen** naar ENG, DUI en FR worden uitgewerkt door de skill `vertalingen`. Geef hier alleen aan welke talen nodig zijn en lever de NL-brontekst aan.
- Schrijf de tekst met de tags uit blok B op de plek waar ze horen.
- Is de tekst nog niet bekend: zet `nader te bepalen` en benoem wat de tekst moet overbrengen.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item een bronverwijzing toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische mailserver-/SMTP-instellingen
- Huisstijl, beeldmateriaal en centrale opmaakrichtlijnen
- Het uitwerken van de vertalingen zelf (valt onder skill `vertalingen`)
- Vertalingen van teksten buiten sjablonen (veldlabels, menunamen, meldingen)
- De signaaldefinitie die het bericht aanroept (valt onder skill `signalen`)
- De workflowstap die het bericht triggert (valt onder skill `workflow-condities`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Komt er een nieuw berichtsjabloon of passen we een bestaand sjabloon aan?
- Welke gegevensverzameling gebruiken we, en moet die worden uitgebreid?
- Welke velden zetten we als tag in de tekst?
- In welke talen leveren we het sjabloon uit (NL / ENG / DUI / FR)?
- Wie is de ontvanger als het ontwerp dit niet benoemt?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

Sluit af met een blok "Content" dat beantwoordt:

- **"Welk onderwerp en welke tekst komen in de mail?"**
- **"Welke gegevens vullen we automatisch in?"** — de tags
- **"Wanneer ontvangt de gebruiker dit bericht?"**
- **"In welke talen is het sjabloon beschikbaar?"**

---

## Kwaliteitscriteria

- [ ] Elke omschrijving eindigt op `(Profit)`
- [ ] Per sjabloon zijn blok A, B en C alle drie ingevuld
- [ ] De gegevensverzameling is benoemd, of gemarkeerd als `te weinig info`
- [ ] Elk gebruikt veld (tag) is gekoppeld aan een plek in de tekst
- [ ] Onderwerp (mail) is ingevuld voor elke benodigde taal
- [ ] De benodigde talen zijn expliciet beantwoord
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Exact menupad voor sjabloonbeheer in Profit
- Werkwijze en voorwaarden voor het inchecken van een sjabloon
- Standaardteksten en bouwstenen die hergebruikt kunnen worden (aanhef, ondertekening, links)
- Documentsjablonen: eigen opbouw en velden, nu nog beknopt beschreven

