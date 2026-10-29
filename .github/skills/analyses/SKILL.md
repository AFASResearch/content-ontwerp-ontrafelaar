---
name: analyses
description: 'Breng de analyse-impact van een ontwerp in kaart: moet er een analyse gebouwd worden, welke gegevensverzameling en velden heeft die nodig, en wat bestaat al in Profit versus wat moet de programmeur nieuw toevoegen. Gebruik bij vragen als: welke analyses zijn nodig, gegevensverzameling toevoegen, dataset, analyse-impact, stuurinformatie, welke velden in de gegevensverzameling.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Analyses-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Moet er een analyse gebouwd worden?** (of moet een bestaande analyse worden aangepast)
2. **Welke gegevensverzameling en welke velden heeft die analyse nodig?**
3. **Wat bestaat al in Profit en wat moet de programmeur nieuw toevoegen?**

Vraag 3 bepaalt of dit een contenttaak is die wij zelf kunnen inrichten, of een afhankelijkheid richting de programmeur.

---

## Wat is een analyse?

Een analyse is stuurinformatie op basis van een **gegevensverzameling**. De gegevensverzameling levert de velden; de analyse bepaalt wat je toont, groepeert, filtert en optelt.

| # | Onderdeel | Toelichting |
|---|-----------|-------------|
| 1 | **Gegevensverzameling** | De bron. Levert alle velden die je in de analyse kunt gebruiken |
| 2 | **Velden** | Elk veld heeft een rol: groeperen, meetwaarde, filter of weergave |
| 3 | **De analyse zelf** | Naam, vindplaats (menupad), kanaal en doelgroep |

> **Geen gegevensverzameling = geen analyse.** Bepaal dus altijd eerst de bron, pas daarna de opmaak.

---

## Stap 1 — Scan het ontwerp: moet er een analyse komen?

### A) Harde trigger

Staat een van deze woorden letterlijk in het ontwerp, dan is er **altijd** een taak: bouwen en inchecken.

| Term | Varianten |
|------|-----------|
| **Analyse** | analyse, analyses, kubus |
| **Gegevensverzameling** | gegevensverzameling, ggv, dataset |
| **Stuurinformatie** | stuurinformatie, managementinformatie, KPI, dashboard |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Behoefte aan inzicht** | "de manager wil kunnen zien hoeveel…" |
| **Aantallen, totalen of verhoudingen** | "het gemiddelde loon per functiegroep" |
| **Filteren of groeperen** | "uitgesplitst per afdeling", "per periode" |
| **Nieuwe gegevens beschikbaar stellen** | "de gegevens worden beschikbaar voor analyse" |
| **Gegevensbron voor een ander onderdeel** | een signaal, rapport, weergave of berichtsjabloon dat een gegevensverzameling nodig heeft |

Bij alleen een impliciet signaal: markeer `te weinig info` en zet het door als vraag aan de ontwerper. Vul nooit zelf in dat er een analyse komt.

---

## Stap 2 — Output per analyse

Lever per analyse **twee blokken** op: eerst de kop, dan de gegevensverzameling met velden.

### Blok A — Analyse (kop)

| Veld | Inhoud |
|------|--------|
| **Naam** | Naam van de analyse |
| **Gevraagde actie** | `nieuw bouwen + inchecken` / `aanpassen` / `controleren` |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad, of `te weinig info` als je het niet kunt verifiëren |
| **Doelgroep** | Voor wie de analyse bedoeld is |
| **Gebruikt door** | Welk rapport, signaal, weergave of berichtsjabloon op dezelfde bron steunt |
| **Standaard uitleveren** | ja / nee / `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok B — Gegevensverzameling en velden

| Veld | Inhoud |
|------|--------|
| **Gegevensverzameling** | Naam van de ggv, of `te weinig info` |
| **Nieuwe ggv nodig** | ja / nee / `te weinig info` |
| **Velden** | Per veld: rol, waarvoor je het gebruikt en of het al bestaat (zie tabel hieronder) |
| **Ontbrekende velden** | Velden die de analyse nodig heeft maar die (nog) niet in de ggv zitten |

Werk de velden altijd zo uit:

| Veld | Rol | Waarvoor | Bestaat in Profit |
|------|-----|----------|-------------------|
| … | `groeperen` / `meetwaarde` / `filter` / `weergave` | Wat het veld in de analyse doet | Zie Stap 3 |

Regels bij dit blok:

- **Elk veld krijgt een rol.** Zonder rol weet de bouwer niet of het veld in de rijen, de kolommen, het filter of alleen in beeld hoort.
- **Toon omschrijvingen, geen codes.** Een codetabelcode zegt de gebruiker niets; neem het omschrijvingsveld op.
- **Gok veldcodes en ggv-namen nooit.** Ken je de exacte naam niet, zet `te weinig info` en zoek hem op in de omgeving.
- **Controleer of het veld de actuele waarde ophaalt** en geen momentopname.

---

## Stap 3 — Bestaat het al in Profit, of moet de programmeur het bouwen?

Dit is de kern van deze skill. Beantwoord dit **per gegevensverzameling en per veld**:

| Uitkomst | Wat het betekent | Wie pakt het op |
|----------|------------------|-----------------|
| `bestaat in Profit` | De ggv of het veld is er al en is bruikbaar | **Wij** — contenttaak, direct in te richten |
| `ggv bestaat, veld ontbreekt` | De bron is er, het benodigde veld niet | **Programmeur** voegt het veld toe aan de ggv; onze taak wacht hierop |
| `nieuw te bouwen` | De gegevensverzameling bestaat niet | **Programmeur** bouwt de ggv; onze taak wacht hierop |
| `te weinig info` | Niet vast te stellen uit ontwerp of omgeving | Uitzoeken in de omgeving of navragen bij de ontwerper |

Regels:

- **Verifieer in de omgeving, niet alleen in het ontwerp.** Een ontwerp noemt vaak een veld dat in Profit anders heet of al bestaat.
- **Elke regel `nieuw te bouwen` of `veld ontbreekt` is een afhankelijkheid.** Benoem die expliciet als beslispunt, zodat duidelijk is dat wij pas kunnen inrichten nadat de programmeur heeft geleverd.
- **Hergebruik gaat voor nieuwbouw.** Volstaat een bestaande ggv met een extra veld, stel dat voor in plaats van een nieuwe ggv.

---

## Stap 4 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item een bronverwijzing toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 5 — Buiten scope (altijd opnemen)

- Technische performance en query-optimalisatie
- Klantspecifieke eigen analyses
- Het bouwen van de gegevensverzameling zelf als die nieuw is (programmeur)
- Rapporten en rapportlayouts (valt onder skill `rapporten`)
- Weergaven (valt onder skill `weergaven`) en boekingslayouts (valt onder skill `boekingslayouts`)
- Autorisatie op de analyse (valt onder skill `autorisatie-en-functionaliteiten`)

---

## Stap 6 — Beslispunten (altijd opnemen, minimaal 1)

Neem in elk geval op wat je in de stappen hierboven niet hard kon maken:

- Komt er een nieuwe gegevensverzameling, of volstaat een bestaande met extra velden?
- Welke velden moet de programmeur toevoegen voordat wij kunnen inrichten?
- Welke velden gebruiken we om te groeperen en welke als meetwaarde?
- Leveren we de analyse standaard uit, of is het een voorbeeld voor de klant?
- Steunen meerdere onderdelen (signaal, rapport, weergave) op dezelfde ggv?

---

## Stap 7 — Content (altijd apart opnemen)

- **"Welke analyse gebruik je waarvoor?"**
- **"Waar vind je de analyse?"** — menupad
- **"Welke gegevens zitten erin?"** — bron en belangrijkste velden
- **"Wat moet ingericht zijn voordat je de analyse kunt gebruiken?"**

---

## Kwaliteitscriteria

- [ ] Per analyse is expliciet beantwoord of die gebouwd moet worden
- [ ] De gegevensverzameling is benoemd, of gemarkeerd als `te weinig info`
- [ ] Elk veld heeft een rol (groeperen / meetwaarde / filter / weergave)
- [ ] Per ggv en per veld staat of het al in Profit bestaat of door de programmeur gebouwd moet worden
- [ ] Elke afhankelijkheid richting de programmeur staat als beslispunt
- [ ] Veldcodes en ggv-namen zijn geverifieerd, niet gegokt
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt
