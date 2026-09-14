---
name: weergaven
description: 'Breng in kaart welke weergaven een ontwerp raakt: nieuwe of gewijzigde kolommen, filters en sorteringen in overzichten in Profit, InSite of OutSite. Gebruik bij vragen als: welke weergaven zijn nodig, kolom toevoegen aan weergave, filter, sortering, overzicht aanpassen.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Weergaven-analyse

> **Status: skelet.** De inhoud wordt nog samen uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **weergaven** een ontwerp raakt: welke kolommen, filters of sorteringen nieuw zijn, wijzigen of gecontroleerd moeten worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Weergave** | weergave, overzicht |
| **Kolom** | kolom, kolommen |
| **Filter** | filter, selectie |
| **Sortering** | sortering, sorteren, volgorde |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld dat zichtbaar moet zijn** | "veld X moet in het overzicht te zien zijn" |
| **Zoeken of filteren** | "de gebruiker kan filteren op status" |
| **Behoefte aan overzicht** | "de gebruiker ziet alle openstaande aanvragen" |
| **Nieuwe status of kenmerk** | een nieuw kenmerk dat je in een lijst wilt herkennen |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Weergave** | Naam van de weergave |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad of object waar de weergave hoort |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Kolommen/velden** | Welke kolommen toegevoegd, verwijderd of verplaatst worden |
| **Filter/sortering** | Standaardfilter of -sortering, of `nader te bepalen` |
| **Doelgroep** | Voor wie de weergave bedoeld is |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Klantspecifieke eigen weergaven
- Technische performance van weergaven
- Boekings- en invoerlayouts (valt onder skill `boekingslayouts`)
- Autorisatie op weergaven (valt onder skill `autorisatie`)
- Rapporten (valt onder skill `rapporten`) en analyses (valt onder skill `analyses`)
- Veldzichtbaarheid per profiel (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaande weergave uitgebreid of komt er een nieuwe standaardweergave?
- Welke kolommen staan standaard aan?
- Welk filter of welke sortering is standaard actief?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat zie je in deze weergave?"**
- **"Waar vind je de weergave?"** — menupad
- **"Hoe pas je de weergave aan?"**

---

## Kwaliteitscriteria

- [ ] Elke weergave heeft kanaal en vindplaats
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupad voor weergavebeheer
- Welke weergaven standaard worden uitgeleverd
- Regels voor standaardkolommen en -filters
