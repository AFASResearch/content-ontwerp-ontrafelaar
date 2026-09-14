---
name: icoontjes
description: 'Breng in kaart welke icoontjes een ontwerp raakt: nieuwe of gewijzigde iconen bij menu-items, knoppen, tegels, processtappen of pagina-onderdelen in Profit, InSite, OutSite en Pocket. Gebruik bij vragen als: welke icoontjes zijn nodig, icoon-impact, nieuw icoon, tegelicoon, knopicoon.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Icoontjes-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **icoontjes** nieuw nodig zijn of gewijzigd moeten worden door nieuwe of gewijzigde functionaliteit.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Icoon** | icoon, icoontje, pictogram, symbool |
| **Tegel** | tegel, tile, snelkoppeling |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw menu-item** | elk nieuw menupad heeft een icoon nodig |
| **Nieuwe knop of actie** | "er komt een knop Omzetten" |
| **Nieuwe InSite/OutSite-tegel of processtap** | "op de startpagina komt een tegel" |
| **Statusaanduiding** | "goedgekeurd wordt met een vinkje getoond" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Element** | Menu-item / knop / tegel / processtap / status |
| **Kanaal** | Profit / InSite / OutSite / Pocket |
| **Vindplaats** | Menupad of pagina |
| **Gevraagde actie** | `nieuw icoon` / `bestaand icoon hergebruiken` / `wijzigen` |
| **Betekenis** | Wat het icoon moet uitdrukken |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- Huisstijl- en ontwerprichtlijnen die centraal vastliggen
- Technische levering van iconenbestanden en formaten
- Klantspecifieke logo's en branding

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Hergebruiken we een bestaand icoon of maken we een nieuw icoon?
- Welk icoon past bij de betekenis als het ontwerp dit niet benoemt?
- Moet hetzelfde icoon in alle kanalen gelijk zijn?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welk icoon hoort bij welke functie?"**
- **"Waar zie je het?"** — menupad of pagina
- **"Wat betekent het icoon?"**

---

## Kwaliteitscriteria

- [ ] Elk item heeft element, kanaal en vindplaats
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Waar iconen worden beheerd en aangevraagd
- Bestaande iconenset en hergebruikregels
- Verschillen tussen kanalen (Profit, InSite, OutSite, Pocket)
