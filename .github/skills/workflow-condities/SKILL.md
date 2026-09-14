---
name: workflow-condities
description: 'Breng de workflow-impact van een ontwerp in kaart: welke workflows, processtappen, acties en condities nieuw zijn, wijzigen of gecontroleerd moeten worden in Profit, InSite of OutSite. Gebruik bij vragen als: welke workflow is nodig, workflow-impact, conditie, processtap, goedkeuringsstroom, InSite-workflow.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Workflow / condities-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **workflows en condities** een ontwerp raakt: nieuwe of gewijzigde processtappen, acties, bestemmingen en voorwaarden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Workflow** | workflow, workflowdefinitie, processtroom |
| **Conditie** | conditie, voorwaarde, regel |
| **Processtap** | processtap, stap, actie, bestemming |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Goedkeuring** | "de leidinggevende keurt goed", "na akkoord van HR" |
| **Statusovergang** | "de aanvraag krijgt status Ingediend" |
| **Voorwaardelijke route** | "bij een bedrag boven € 500 gaat het naar…" |
| **Terugkoppeling naar indiener** | "bij afkeuring kan de medewerker aanpassen" |
| **Automatische afhandeling** | "als aan X is voldaan, wordt het automatisch goedgekeurd" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Workflow** | Naam van de workflow of workflowdefinitie |
| **Kanaal** | Profit / InSite / OutSite / Pocket |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Processtappen** | Welke stappen toegevoegd of gewijzigd worden |
| **Conditie** | De voorwaarde waaronder een stap of route geldt, of `nader te bepalen` |
| **Bestemming** | Wie de taak krijgt (rol, functie, persoon) |
| **Acties** | Welke acties de gebruiker heeft (goedkeuren, afkeuren, terugsturen) |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Gebruik één blok per workflow. Noem de stappen in volgorde.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische implementatie van de workflow-engine
- Klantspecifieke workflowvarianten
- Autorisatie op workflowtaken (valt onder skill `autorisatie`)
- Berichten die de workflow verstuurt (valt onder skill `berichtsjabloon`)
- Signalen die een workflow starten (valt onder skill `signalen`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wie is de bestemming van elke stap als het ontwerp dit niet benoemt?
- Welke conditie bepaalt de route, en welke grenswaarde geldt?
- Wordt een bestaande workflow uitgebreid of komt er een nieuwe workflow?
- Wat gebeurt er bij afkeuring of bij uitblijven van actie?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke stappen doorloopt de aanvraag?"**
- **"Wie doet wat in welke stap?"**
- **"Wanneer geldt welke route?"** — de condities
- **"Waar richt je de workflow in?"** — menupad

---

## Kwaliteitscriteria

- [ ] Elke workflow heeft stappen, bestemming en acties
- [ ] Elke conditie is concreet benoemd of gemarkeerd als `te weinig info`
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupaden voor workflowbeheer in Profit
- Hoe condities technisch worden vastgelegd
- Standaardworkflows die worden uitgeleverd
