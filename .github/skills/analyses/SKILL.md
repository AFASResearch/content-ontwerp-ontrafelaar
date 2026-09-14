---
name: analyses
description: 'Breng de analyse-impact van een ontwerp in kaart: welke analyses en gegevensverzamelingen in Profit, InSite of OutSite nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: welke analyses zijn nodig, gegevensverzameling toevoegen, dataset, analyse-impact, stuurinformatie.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Analyses-analyse

> **Status: skelet.** De inhoud wordt nog samen uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **analyses en gegevensverzamelingen** een ontwerp raakt en wat daarvoor ingericht of aangevuld moet worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Analyse** | analyse, analyses |
| **Gegevensverzameling** | gegevensverzameling, ggv, dataset |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Behoefte aan inzicht** | "de manager wil kunnen zien hoeveel…" |
| **Nieuwe gegevens beschikbaar stellen** | "de gegevens worden beschikbaar voor analyse" |
| **Filteren of groeperen** | "uitgesplitst per afdeling" |
| **Gegevensbron voor ander onderdeel** | een signaal, rapport of berichtsjabloon dat een gegevensverzameling nodig heeft |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Naam** | Naam van de analyse of gegevensverzameling |
| **Type** | Analyse / gegevensverzameling |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Velden/gegevens** | Welke gegevens erin zitten of bijkomen, of `nader te bepalen` |
| **Gebruikt door** | Welk rapport, signaal of berichtsjabloon erop steunt |
| **Doelgroep** | Voor wie de analyse bedoeld is |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische performance en query-optimalisatie
- Klantspecifieke eigen analyses
- Rapporten en rapportlayouts (valt onder skill `rapporten`)
- Weergaven (valt onder skill `weergaven`) en boekingslayouts (valt onder skill `boekingslayouts`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Is een nieuwe gegevensverzameling nodig, of volstaat een bestaande?
- Welke velden nemen we op in de gegevensverzameling?
- Leveren we de analyse standaard uit?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke analyse gebruik je waarvoor?"**
- **"Waar vind ik het?"** — menupad
- **"Welke gegevens zitten erin?"**

---

## Kwaliteitscriteria

- [ ] Elke analyse heeft type, kanaal en vindplaats
- [ ] Bij elke gegevensverzameling staat welk onderdeel erop steunt
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Onderscheid tussen analyse en gegevensverzameling
- Menupad voor beheer van analyses en gegevensverzamelingen
- Welke analyses standaard worden uitgeleverd
