---
name: documenten-rapporten-analyses
description: 'Breng in kaart welke documenten, rapporten en analyses een ontwerp raakt: nieuwe of gewijzigde rapportlayouts, standaardrapporten, analyses en gegevensverzamelingen die voor de eindgebruiker beschikbaar moeten komen. Gebruik bij vragen als: welke rapporten zijn nodig, rapportage-impact, analyse toevoegen, gegevensverzameling, rapportlayout.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Documenten / Rapporten / Analyses-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **documenten, rapporten en analyses** een ontwerp raakt en wat daarvoor ingericht of aangevuld moet worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Rapport** | rapport, rapportage, rapportlayout, overzicht afdrukken |
| **Analyse** | analyse, gegevensverzameling, dataset |
| **Document** | document, pdf, export, uitvoer |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Behoefte aan uitvoer** | "de gebruiker kan de gegevens exporteren" |
| **Nieuwe velden die zichtbaar moeten zijn in rapportage** | "veld X moet ook in het overzicht" |
| **Controle-/verantwoordingsbehoefte** | "de accountant moet kunnen aantonen…" |
| **Periodieke output** | "maandelijks wordt een overzicht opgeleverd" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Naam** | Rapport, analyse of document |
| **Type** | Rapport / analyse / gegevensverzameling / document |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad of pagina |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Velden/gegevens** | Welke gegevens toegevoegd of gewijzigd worden, of `nader te bepalen` |
| **Doelgroep** | Voor wie de uitvoer bedoeld is |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische performance en query-optimalisatie
- Klantspecifieke maatwerkrapportages
- Dashboards en cockpits
- Weergaven en boekingslayouts (valt onder skill `weergaven-boekingslayouts`)
- Documentsjablonen voor correspondentie (valt onder skill `bericht-en-documentsjablonen`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaand rapport uitgebreid of komt er een nieuw rapport?
- Welke velden zijn standaard zichtbaar als het ontwerp dit niet benoemt?
- Is een nieuwe gegevensverzameling nodig, of volstaat een bestaande?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welk rapport of welke analyse gebruik je waarvoor?"**
- **"Waar vind ik het?"** — menupad
- **"Welke gegevens staan erin?"**

---

## Kwaliteitscriteria

- [ ] Elk item heeft type, kanaal en vindplaats
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Onderscheid tussen rapport, analyse en gegevensverzameling
- Menupaden voor beheer van rapporten en analyses
- Wanneer iets standaard wordt uitgeleverd en wanneer niet
