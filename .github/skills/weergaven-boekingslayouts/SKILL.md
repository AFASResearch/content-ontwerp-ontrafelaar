---
name: weergaven-boekingslayouts
description: 'Breng in kaart welke weergaven en boekingslayouts een ontwerp raakt: nieuwe of gewijzigde kolommen, filters, sorteringen en invoerlayouts in Profit. Gebruik bij vragen als: welke weergaven zijn nodig, boekingslayout aanpassen, kolom toevoegen aan weergave, filter, invoerlayout.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Weergaven / Boekingslayouts-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **weergaven en boekingslayouts** een ontwerp raakt: welke kolommen, filters, sorteringen of invoerlayouts nieuw zijn, wijzigen of gecontroleerd moeten worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Weergave** | weergave, overzicht, kolom, filter, sortering |
| **Boekingslayout** | boekingslayout, invoerlayout, layout |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld dat zichtbaar moet zijn** | "veld X moet in het overzicht te zien zijn" |
| **Zoeken of filteren** | "de gebruiker kan filteren op status" |
| **Nieuwe invoervolgorde** | "de gebruiker vult eerst X in, dan Y" |
| **Nieuwe boekingssoort of -regel** | "er komt een nieuw boekingstype" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Weergave/layout** | Naam van de weergave of boekingslayout |
| **Type** | Weergave / boekingslayout |
| **Vindplaats** | Menupad of object waar de weergave hoort |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Kolommen/velden** | Welke kolommen of velden toegevoegd, verwijderd of verplaatst worden |
| **Filter/sortering** | Standaardfilter of -sortering, of `nader te bepalen` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- Klantspecifieke eigen weergaven
- Technische performance van weergaven
- Autorisatie op weergaven (valt onder skill `autorisatie`)
- Rapporten en analyses (valt onder skill `documenten-rapporten-analyses`)
- Veldzichtbaarheid per profiel (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaande weergave uitgebreid of komt er een nieuwe standaardweergave?
- Welke kolommen staan standaard aan?
- Welk filter is standaard actief?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat zie je in deze weergave?"**
- **"Waar vind je de weergave?"** — menupad
- **"Hoe pas je de weergave aan?"**

---

## Kwaliteitscriteria

- [ ] Elke weergave heeft type en vindplaats
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Onderscheid tussen weergave, boekingslayout en invoerlayout
- Menupaden voor weergavebeheer
- Welke weergaven standaard worden uitgeleverd
