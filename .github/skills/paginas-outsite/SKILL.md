---
name: paginas-outsite
description: 'Breng de OutSite-impact van een ontwerp in kaart: welke OutSite-paginas nieuw zijn of wijzigen, en of er OutSite-profielen beschikbaar zijn. Controleer altijd expliciet of er profielen zijn voor OutSite. Gebruik bij vragen als: welke OutSite-paginas zijn nodig, OutSite-impact, OutSite profielen, externe portal pagina.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Pagina's OutSite-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **OutSite-pagina's** een ontwerp raakt.

> **Vaste controle:** ga altijd expliciet na of er **profielen beschikbaar zijn voor OutSite**. Rapporteer die uitkomst ook als het ontwerp er niets over zegt — dan met status `te weinig info`.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **OutSite** | OutSite, OutSite-pagina, OutSite-portal |
| **Profiel** | OutSite-profiel, profiel |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Externe gebruiker** | "de sollicitant", "de klant", "de leverancier" |
| **Publiek toegankelijk proces** | "zonder inloggen", "via de website" |
| **Aanmelding of aanvraag van buitenaf** | "extern indienen van een aanvraag" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Pagina/onderdeel** | Naam van de OutSite-pagina of het paginaonderdeel |
| **Portal/sjabloon** | Bijbehorend portal of sjabloon |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Profiel aanwezig** | ja (welk profiel) / nee / `te weinig info` |
| **Doelgroep** | Welke externe gebruiker |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische hosting, domeinen en certificaten
- Autorisatierollen voor OutSite (valt onder skill `autorisatie`)
- InSite-portalpagina's (valt onder skill `portalpagina-insite`)
- Profielen en veldcontexten in algemene zin (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Is er al een OutSite-profiel, of moet er een nieuw profiel komen?
- Wordt de pagina standaard uitgeleverd of alleen op aanvraag?
- Welke gegevens mogen extern zichtbaar zijn?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat ziet de externe gebruiker?"**
- **"Waar vind je de pagina?"**
- **"Welk profiel is nodig?"**

---

## Kwaliteitscriteria

- [ ] Voor elke pagina is de profielcheck expliciet beantwoord
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Overzicht van bestaande OutSite-portals en -profielen
- Menupaden voor OutSite-beheer
- Regels voor wat extern zichtbaar mag zijn
