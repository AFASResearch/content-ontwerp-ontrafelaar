---
name: profielen-en-veldcontexten
description: 'Breng in kaart welke profielen en veldcontexten een ontwerp raakt: welke velden zichtbaar, verplicht of afgeschermd moeten zijn per profiel of context in Profit, InSite, OutSite en Pocket. Gebruik bij vragen als: welke profielen zijn nodig, veldcontext aanpassen, veldzichtbaarheid, profiel-impact.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Profielen en veldcontexten-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **profielen en veldcontexten** een ontwerp raakt: welke velden per profiel of context zichtbaar, verplicht, alleen-lezen of verborgen moeten zijn.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Profiel** | profiel, gebruikersprofiel, InSite-profiel, OutSite-profiel |
| **Veldcontext** | veldcontext, context, contextinrichting |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld** | elk nieuw veld vraagt om een keuze over zichtbaarheid per profiel |
| **Rolafhankelijke zichtbaarheid** | "alleen de leidinggevende ziet dit veld" |
| **Verplichtstelling** | "dit veld is verplicht bij…" |
| **Alleen-lezen** | "de gebruiker kan dit niet wijzigen" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Veld** | Naam van het veld |
| **Profiel/context** | Welk profiel of welke veldcontext geraakt wordt |
| **Kanaal** | Profit / InSite / OutSite / Pocket |
| **Gevraagde instelling** | zichtbaar / verborgen / verplicht / alleen-lezen |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Gebruik één rij per combinatie van veld en profiel/context.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische veldvalidaties en foutmeldingen
- Autorisatiegroepen en -rollen (valt onder skill `autorisatie`)
- Informatiebolletjes bij velden (valt onder skill `informatiebolletje`)
- Weergaven en boekinglayouts (valt onder skill `weergaven-boekinglayouts`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- In welke profielen wordt een nieuw veld standaard getoond?
- Is het veld verplicht, en voor wie?
- Moet er een nieuw profiel komen of passen we bestaande profielen aan?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke velden zie je in welk profiel?"**
- **"Waar pas je dit aan?"** — menupad
- **"Wat gebeurt er als het veld verborgen is?"**

---

## Kwaliteitscriteria

- [ ] Elk veld heeft profiel/context, kanaal en gevraagde instelling
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupaden voor profiel- en veldcontextbeheer
- Overzicht van standaardprofielen per kanaal
- Verhouding tussen profiel, veldcontext en autorisatie
