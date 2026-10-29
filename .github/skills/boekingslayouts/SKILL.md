---
name: boekingslayouts
description: 'Breng in kaart welke boekingslayouts en invoerlayouts een ontwerp raakt: moet er een layout gebouwd worden, welke velden en bronnen komen erin, en wat bestaat al in Profit versus wat moet de programmeur nieuw toevoegen. Gebruik bij vragen als: welke boekingslayouts zijn nodig, boekingslayout aanpassen, invoerlayout, invoervolgorde, boekingssoort, welke velden bij het boeken.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Boekingslayouts-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Moet er een boekingslayout gebouwd worden?** (of moet een bestaande layout worden aangepast)
2. **Welke velden komen erin, en uit welke bron komen ze?**
3. **Wat bestaat al in Profit en wat moet de programmeur nieuw toevoegen?**

Vraag 3 bepaalt of dit een contenttaak is die wij zelf kunnen inrichten, of een afhankelijkheid richting de programmeur.

---

## Wat is een boekingslayout?

Een boekingslayout bepaalt **wat de gebruiker ziet en invult tijdens het boeken**: welke velden zichtbaar zijn, in welke volgorde ze staan en welke verplicht zijn.

| # | Onderdeel | Toelichting |
|---|-----------|-------------|
| 1 | **Boekingssoort of dagboek** | Waar de layout aan hangt. Bepaalt welke velden überhaupt beschikbaar zijn |
| 2 | **Velden** | Elk veld heeft een rol: invoer, vaste waarde, alleen-lezen of niet tonen |
| 3 | **Volgorde en indeling** | De invoervolgorde en de groepering van velden op het scherm |

> **Een layout toont alleen velden die het boekingsscherm kent.** Komt een veld uit een andere bron, bijvoorbeeld een keuzelijst of een gegevensverzameling, benoem die bron expliciet — dan is er vrijwel altijd eerst werk voor de programmeur.

---

## Stap 1 — Scan het ontwerp: moet er een layout komen?

### A) Harde trigger

| Term | Varianten |
|------|-----------|
| **Boekingslayout** | boekingslayout, boekinglayout |
| **Invoerlayout** | invoerlayout, layout, invoerscherm |
| **Boeking** | boeking, boekingssoort, boekingsregel, dagboek |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw invoerveld** | "bij het boeken komt veld X erbij" |
| **Nieuwe invoervolgorde** | "de gebruiker vult eerst X in, dan Y" |
| **Nieuwe boekingssoort** | "er komt een nieuw boekingstype" |
| **Voorwaardelijke invoer** | "veld X is alleen zichtbaar bij soort Y" |
| **Vaste of voorgevulde waarde** | "het veld wordt automatisch gevuld met…" |

Bij alleen een impliciet signaal: markeer `te weinig info` en zet het door als vraag aan de ontwerper.

---

## Stap 2 — Output per boekingslayout

### Blok A — Layout (kop)

| Veld | Inhoud |
|------|--------|
| **Boekingslayout** | Naam van de boekings- of invoerlayout |
| **Gevraagde actie** | `nieuw bouwen + inchecken` / `aanpassen` / `controleren` |
| **Boekingssoort / dagboek** | Waar de layout aan hangt |
| **Vindplaats** | Menupad of proces, of `te weinig info` |
| **Doelgroep** | Wie ermee boekt |
| **Standaard uitleveren** | ja / nee / `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok B — Velden en herkomst

| Veld | Rol | Bron van de waarde | Conditie | Bestaat in Profit |
|------|-----|--------------------|----------|-------------------|
| … | `invoer` / `verplicht` / `vast gevuld` / `alleen-lezen` / `niet tonen` | Boekingsscherm, codetabel of gegevensverzameling | Wanneer het veld van toepassing is | Zie Stap 3 |

Regels bij dit blok:

- **Noem de invoervolgorde expliciet.** Zegt het ontwerp niets over volgorde: `te weinig info` + beslispunt. Gok geen volgorde.
- **Benoem per veld of het verplicht is.** Een verplicht veld dat niet gevuld kan worden, blokkeert het boeken.
- **Benoem de conditie** als een veld alleen bij een bepaalde soort of situatie zichtbaar is.
- **Gok veldnamen of codetabellen nooit.** Zoek ze op in de omgeving of markeer `te weinig info`.
- **Controleer of de voorgestelde invoer uitvoerbaar is**: is het veld op dat niveau wijzigbaar?

---

## Stap 3 — Bestaat het al in Profit, of moet de programmeur het bouwen?

Beantwoord dit **per layout en per veld**:

| Uitkomst | Wat het betekent | Wie pakt het op |
|----------|------------------|-----------------|
| `bestaat in Profit` | Layout en veld zijn er al en zijn bruikbaar | **Wij** — contenttaak, direct in te richten |
| `layout bestaat, veld ontbreekt` | De layout is er, het benodigde veld niet | **Programmeur** voegt het veld toe aan het boekingsscherm; onze taak wacht hierop |
| `nieuw te bouwen` | De boekingssoort of layout bestaat niet | **Programmeur** bouwt die; onze taak wacht hierop |
| `te weinig info` | Niet vast te stellen uit ontwerp of omgeving | Uitzoeken in de omgeving of navragen bij de ontwerper |

Regels:

- **Verifieer in de omgeving, niet alleen in het ontwerp.**
- **Elke regel `nieuw te bouwen` of `veld ontbreekt` is een afhankelijkheid** en hoort als beslispunt terug.
- **Hergebruik gaat voor nieuwbouw.** Een bestaande layout uitbreiden is vrijwel altijd beter dan een tweede layout die bijna hetzelfde doet.

---

## Stap 4 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 5 — Buiten scope (altijd opnemen)

- Klantspecifieke eigen boekingslayouts
- Technische veldvalidaties en foutmeldingen
- Het toevoegen van een veld aan het boekingsscherm zelf (programmeur)
- Weergaven en overzichten (valt onder skill `weergaven`)
- Autorisatie op boeken (valt onder skill `autorisatie`)
- Veldzichtbaarheid per profiel en context (valt onder skill `profielen-en-veldcontexten`)
- Veldtoelichting bij de invoervelden (valt onder skill `informatiebolletje`)

---

## Stap 6 — Beslispunten (altijd opnemen, minimaal 1)

- Wordt een bestaande boekingslayout uitgebreid of komt er een nieuwe?
- Welke velden moet de programmeur toevoegen voordat wij de layout kunnen inrichten?
- Welke velden zijn verplicht bij het boeken?
- Wat is de invoervolgorde als het ontwerp die niet benoemt?
- Geldt er een conditie per boekingssoort?

---

## Stap 7 — Content (altijd apart opnemen)

- **"Welke gegevens vul je in bij het boeken?"**
- **"Waar vind je de boekingslayout?"** — menupad
- **"Wanneer gebruik je welke layout?"**
- **"Welke velden zijn verplicht?"**

---

## Kwaliteitscriteria

- [ ] Per layout is expliciet beantwoord of die gebouwd moet worden
- [ ] Elk veld heeft een rol (invoer / verplicht / vast gevuld / alleen-lezen / niet tonen)
- [ ] Per veld staat de bron van de waarde
- [ ] Per layout en per veld staat of het al in Profit bestaat of door de programmeur gebouwd moet worden
- [ ] De invoervolgorde is benoemd of als `te weinig info` gemarkeerd
- [ ] Condities per boekingssoort zijn benoemd
- [ ] Elke afhankelijkheid richting de programmeur staat als beslispunt
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt
