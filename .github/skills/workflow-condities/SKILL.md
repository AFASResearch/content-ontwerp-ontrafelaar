---
name: workflow-condities
description: 'Breng de workflow-impact van een ontwerp in kaart: welke workflows, processtappen, acties, condities en profielen per taak nieuw zijn, wijzigen of gecontroleerd moeten worden in Profit, InSite of OutSite. Gebruik bij vragen als: welke workflow is nodig, workflow-impact, conditie, processtap, goedkeuringsstroom, afwijkend beoordelingsprofiel, rapport in de workflow.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Workflow / condities-analyse

## Doel

Volledig in kaart brengen welke **workflows en condities** een ontwerp raakt: nieuwe of gewijzigde processtappen, acties, bestemmingen, voorwaarden en het profiel waarmee elke stap wordt afgehandeld.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Workflow** | workflow, workflowdefinitie, processtroom |
| **Conditie** | conditie, voorwaarde, regel |
| **Processtap** | processtap, stap, actie, bestemming, taak |
| **Profiel in de workflow** | afwijkend profiel, beoordelingsprofiel, starten in aanpassen |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Goedkeuring** | "de leidinggevende keurt goed", "na akkoord van HR" |
| **Statusovergang** | "de aanvraag krijgt status Ingediend" |
| **Voorwaardelijke route** | "bij een bedrag boven € 500 gaat het naar…" |
| **Terugkoppeling naar indiener** | "bij afkeuring kan de medewerker aanpassen" |
| **Automatische afhandeling** | "als aan X is voldaan, wordt het automatisch goedgekeurd" |
| **Taak met andere velden dan de vorige** | "HR legt het antwoord vast" → die taak heeft een eigen beoordeelprofiel nodig |
| **Terugloopstap** | "bij afkeuring kan de medewerker aanpassen" → eigen context voor de instuurder |
| **Stuk genereren in de stap** | "de behandelaar genereert een rapport en voegt het als bijlage toe" |
| **Meerdere profielen, één workflow** | controleer of één workflow volstaat of dat er per profiel een eigen workflow komt |

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
| **Profiel per taak** | Per processtap: welk aanmaak-, beoordeel- of **afwijkend beoordeelprofiel** die taak gebruikt. Zie `profielen-en-veldcontexten` |
| **Rapport of document** | Wordt er in een stap een rapport gegenereerd? Zo ja: welk rapport en wat er met het resultaat gebeurt. Zie `rapporten` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Gebruik één blok per workflow. Noem de stappen in volgorde.

> **Tel de workflows expliciet.** Een ontwerp dat één workflow noemt voor twee profielen, levert in de praktijk vaak twee workflows op zodra de stappen of de bestemmingen verschillen. Benoem dat als beslispunt in plaats van het ontwerp te volgen.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische implementatie van de workflow-engine
- Klantspecifieke workflowvarianten
- Autorisatie op workflowtaken (valt onder skill `autorisatie-en-functionaliteiten`); de veldinstellingen per taak vallen onder `profielen-en-veldcontexten`
- Berichten die de workflow verstuurt (valt onder skill `berichtsjabloon`)
- Signalen die een workflow starten (valt onder skill `signalen`)
- De opmaak van het rapport dat in een stap wordt gegenereerd (valt onder skill `rapporten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wie is de bestemming van elke stap als het ontwerp dit niet benoemt?
- Welke conditie bepaalt de route, en welke grenswaarde geldt?
- Wordt een bestaande workflow uitgebreid of komt er een nieuwe workflow?
- Volstaat één workflow voor alle profielen, of komt er per profiel een eigen workflow?
- Welke taak gebruikt welk afwijkend beoordelingsprofiel?
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
- [ ] Elke processtap heeft een benoemd profiel, of staat op `te weinig info`
- [ ] Het aantal workflows is expliciet vastgesteld en niet klakkeloos uit het ontwerp overgenomen
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
