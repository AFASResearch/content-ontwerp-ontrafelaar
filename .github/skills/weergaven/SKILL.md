---
name: weergaven
description: 'Breng in kaart welke weergaven een ontwerp raakt: moet er een weergave gebouwd worden, welke gegevensverzameling en velden heeft die nodig, en wat bestaat al in Profit versus wat moet de programmeur nieuw toevoegen. Gebruik bij vragen als: welke weergaven zijn nodig, kolom toevoegen aan weergave, filter, sortering, overzicht aanpassen, welke velden in de weergave.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Weergaven-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Moet er een weergave gebouwd worden?** (of moet een bestaande weergave worden aangepast)
2. **Welke gegevensverzameling en welke velden heeft die weergave nodig?**
3. **Wat bestaat al in Profit en wat moet de programmeur nieuw toevoegen?**

Vraag 3 bepaalt of dit een contenttaak is die wij zelf kunnen inrichten, of een afhankelijkheid richting de programmeur.

---

## Wat is een weergave?

Een weergave toont records uit een **gegevensverzameling** in een lijst. De gegevensverzameling levert de velden; de weergave bepaalt welke velden als kolom zichtbaar zijn, hoe er gefilterd wordt en in welke volgorde de regels staan.

| # | Onderdeel | Toelichting |
|---|-----------|-------------|
| 1 | **Gegevensverzameling** | De bron. Levert alle velden die je als kolom of filter kunt gebruiken |
| 2 | **Velden** | Elk veld heeft een rol: kolom, filter of sortering |
| 3 | **De weergave zelf** | Naam, kanaal, vindplaats (menupad of object) en doelgroep |

> **Geen veld in de gegevensverzameling = geen kolom.** Bepaal dus altijd eerst of het veld in de bron zit.

---

## Stap 1 — Scan het ontwerp: moet er een weergave komen?

### A) Harde trigger

| Term | Varianten |
|------|-----------|
| **Weergave** | weergave, overzicht, lijst |
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
| **Nieuw tabblad of object** | een nieuw tabblad toont vrijwel altijd een lijst |

Bij alleen een impliciet signaal: markeer `te weinig info` en zet het door als vraag aan de ontwerper.

---

## Stap 2 — Output per weergave

Lever per weergave **twee blokken** op: eerst de kop, dan de gegevensverzameling met velden.

### Blok A — Weergave (kop)

| Veld | Inhoud |
|------|--------|
| **Weergave** | Naam van de weergave |
| **Gevraagde actie** | `nieuw bouwen + inchecken` / `aanpassen` / `controleren` |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad of object + tabblad, of `te weinig info` |
| **Doelgroep** | Voor wie de weergave bedoeld is |
| **Standaard uitleveren** | ja / nee / `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok B — Gegevensverzameling en velden

| Veld | Inhoud |
|------|--------|
| **Gegevensverzameling** | Naam van de ggv waarop de weergave draait, of `te weinig info` |
| **Nieuwe ggv nodig** | ja / nee / `te weinig info` |
| **Velden** | Per veld: rol, waarvoor en of het al bestaat (zie tabel hieronder) |
| **Ontbrekende velden** | Velden die de weergave nodig heeft maar die (nog) niet in de ggv zitten |

Werk de velden altijd zo uit:

| Veld | Rol | Waarvoor | Bestaat in Profit |
|------|-----|----------|-------------------|
| … | `kolom` / `filter` / `sortering` | Wat het veld in de weergave doet | Zie Stap 3 |

Regels bij dit blok:

- **Noem de standaardstand.** Welke kolommen staan aan, welk filter is actief en op welk veld is gesorteerd. Zegt het ontwerp dit niet: `te weinig info` + beslispunt.
- **Toon omschrijvingen, geen codes.**
- **Beschrijf welke records het filter uitsluit.** Dat bepaalt wat de gebruiker níet ziet en hoort terug in de content.
- **Gok veldcodes en ggv-namen nooit.** Zoek ze op in de omgeving of markeer `te weinig info`.

---

## Stap 3 — Bestaat het al in Profit, of moet de programmeur het bouwen?

Beantwoord dit **per gegevensverzameling en per veld**:

| Uitkomst | Wat het betekent | Wie pakt het op |
|----------|------------------|-----------------|
| `bestaat in Profit` | De ggv of het veld is er al en is bruikbaar | **Wij** — contenttaak, direct in te richten |
| `ggv bestaat, veld ontbreekt` | De bron is er, het benodigde veld niet | **Programmeur** voegt het veld toe aan de ggv; onze taak wacht hierop |
| `nieuw te bouwen` | De gegevensverzameling of het object bestaat niet | **Programmeur** bouwt de ggv; onze taak wacht hierop |
| `te weinig info` | Niet vast te stellen uit ontwerp of omgeving | Uitzoeken in de omgeving of navragen bij de ontwerper |

Regels:

- **Verifieer in de omgeving, niet alleen in het ontwerp.**
- **Elke regel `nieuw te bouwen` of `veld ontbreekt` is een afhankelijkheid** en hoort als beslispunt terug.
- **Hergebruik gaat voor nieuwbouw.** Een kolom toevoegen aan een bestaande standaardweergave is vrijwel altijd beter dan een tweede weergave die bijna hetzelfde toont.

---

## Stap 4 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 5 — Buiten scope (altijd opnemen)

- Klantspecifieke eigen weergaven
- Technische performance van weergaven
- Het bouwen van de gegevensverzameling zelf als die nieuw is (programmeur)
- Boekings- en invoerlayouts (valt onder skill `boekingslayouts`)
- Autorisatie op weergaven (valt onder skill `autorisatie`)
- Rapporten (valt onder skill `rapporten`) en analyses (valt onder skill `analyses`)
- Veldzichtbaarheid per profiel (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 6 — Beslispunten (altijd opnemen, minimaal 1)

- Wordt een bestaande weergave uitgebreid of komt er een nieuwe standaardweergave?
- Welke velden moet de programmeur toevoegen voordat wij de kolom kunnen inrichten?
- Welke kolommen staan standaard aan en in welke volgorde?
- Welk filter of welke sortering is standaard actief, en welke records vallen daarmee af?
- Leveren we de weergave standaard uit?

---

## Stap 7 — Content (altijd apart opnemen)

- **"Wat zie je in deze weergave?"**
- **"Waar vind je de weergave?"** — menupad of object
- **"Welke regels zie je hier niet?"** — het standaardfilter
- **"Hoe pas je de weergave aan?"**

---

## Kwaliteitscriteria

- [ ] Per weergave is expliciet beantwoord of die gebouwd moet worden
- [ ] De gegevensverzameling is benoemd, of gemarkeerd als `te weinig info`
- [ ] Elk veld heeft een rol (kolom / filter / sortering)
- [ ] Per ggv en per veld staat of het al in Profit bestaat of door de programmeur gebouwd moet worden
- [ ] De standaardstand van kolommen, filter en sortering is benoemd
- [ ] Er staat bij welke records het standaardfilter uitsluit
- [ ] Elke afhankelijkheid richting de programmeur staat als beslispunt
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt
