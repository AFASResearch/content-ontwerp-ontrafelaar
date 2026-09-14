---
name: rapporten
description: 'Breng de rapport-impact van een ontwerp in kaart: welke rapportlayouts en standaardrapporten in Profit, InSite of OutSite nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: welke rapporten zijn nodig, rapportlayout aanpassen, standaardrapport, afdrukken, rapportage-impact.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Rapporten-analyse

> **Status: skelet.** De inhoud wordt nog samen uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **rapporten en rapportlayouts** een ontwerp raakt en wat daarvoor ingericht of aangevuld moet worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Rapport** | rapport, rapportage, standaardrapport |
| **Rapportlayout** | rapportlayout, layout, afdruklayout |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Afdrukken of uitvoeren** | "de gebruiker drukt het overzicht af" |
| **Nieuwe velden in rapportage** | "veld X moet ook in het rapport" |
| **Controle- of verantwoordingsbehoefte** | "de accountant moet kunnen aantonen…" |
| **Periodieke output** | "maandelijks wordt een overzicht opgeleverd" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Rapportnaam** | Naam van het rapport of de rapportlayout |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad waar het rapport te vinden is |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Velden/gegevens** | Welke gegevens toegevoegd of gewijzigd worden, of `nader te bepalen` |
| **Gegevensbron** | Gegevensverzameling waarop het rapport rust, of `nader te bepalen` |
| **Doelgroep** | Voor wie het rapport bedoeld is |
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
- Analyses en gegevensverzamelingen (valt onder skill `analyses`)
- Documenten en brieven (valt onder skill `documentsjabloon`)
- Weergaven (valt onder skill `weergaven`) en boekingslayouts (valt onder skill `boekingslayouts`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaand rapport uitgebreid of komt er een nieuw rapport?
- Welke velden staan standaard op het rapport?
- Voor welke doelgroep leveren we het rapport standaard uit?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welk rapport gebruik je waarvoor?"**
- **"Waar vind ik het?"** — menupad
- **"Welke gegevens staan erin?"**

---

## Kwaliteitscriteria

- [ ] Elk rapport heeft kanaal, vindplaats en doelgroep
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupad voor rapportbeheer in Profit
- Onderscheid tussen rapport, rapportlayout en afdrukvorm
- Welke rapporten standaard worden uitgeleverd
