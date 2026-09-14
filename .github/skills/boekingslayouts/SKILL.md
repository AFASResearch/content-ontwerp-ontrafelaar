---
name: boekingslayouts
description: 'Breng in kaart welke boekingslayouts en invoerlayouts een ontwerp raakt: nieuwe of gewijzigde invoervelden, volgorde en indeling bij het boeken in Profit. Gebruik bij vragen als: welke boekingslayouts zijn nodig, boekingslayout aanpassen, invoerlayout, invoervolgorde, boekingssoort.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Boekingslayouts-analyse

> **Status: skelet.** De inhoud wordt nog samen uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **boekingslayouts en invoerlayouts** een ontwerp raakt: welke invoervelden, volgorde of indeling nieuw zijn, wijzigen of gecontroleerd moeten worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Boekingslayout** | boekingslayout, boekinglayout |
| **Invoerlayout** | invoerlayout, layout, invoerscherm |
| **Boeking** | boeking, boekingssoort, boekingsregel |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuwe invoervolgorde** | "de gebruiker vult eerst X in, dan Y" |
| **Nieuw invoerveld** | "bij het boeken komt veld X erbij" |
| **Nieuwe boekingssoort** | "er komt een nieuw boekingstype" |
| **Voorwaardelijke invoer** | "veld X is alleen zichtbaar bij soort Y" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Boekingslayout** | Naam van de boekings- of invoerlayout |
| **Vindplaats** | Menupad of proces waar de layout hoort |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Velden** | Welke invoervelden toegevoegd, verwijderd of verplaatst worden |
| **Volgorde/indeling** | Gewenste invoervolgorde of indeling, of `nader te bepalen` |
| **Conditie** | Wanneer een veld of layout van toepassing is |
| **Doelgroep** | Wie ermee boekt |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Klantspecifieke eigen boekingslayouts
- Technische veldvalidaties en foutmeldingen
- Weergaven en overzichten (valt onder skill `weergaven`)
- Autorisatie op boeken (valt onder skill `autorisatie`)
- Veldzichtbaarheid per profiel (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaande boekingslayout uitgebreid of komt er een nieuwe?
- Welke velden zijn verplicht bij het boeken?
- Wat is de standaard invoervolgorde als het ontwerp dit niet benoemt?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke gegevens vul je in bij het boeken?"**
- **"Waar vind je de boekingslayout?"** — menupad
- **"Wanneer gebruik je welke layout?"**

---

## Kwaliteitscriteria

- [ ] Elke layout heeft een vindplaats en gevraagde actie
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Onderscheid tussen boekingslayout en invoerlayout
- Menupad voor beheer van boekingslayouts
- Welke boekingslayouts standaard worden uitgeleverd
