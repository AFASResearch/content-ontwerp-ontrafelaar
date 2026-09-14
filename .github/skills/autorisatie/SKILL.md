---
name: autorisatie
description: 'Breng de autorisatie-impact van een ontwerp in kaart: Profit (autorisatiegroepen: menu-items, tabbladen, weergaven, acties) én InSite/OutSite (autorisatierollen: paginas, portals, paginaonderdelen, functionaliteit). Gebruik bij vragen als: welke autorisaties zijn nodig, wat zijn de autorisatiewijzigingen, maak de autorisatieparagraaf, InSite/OutSite rollen, Profit menu-autorisatie.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Autorisatie-analyse

## Doel

Volledig in kaart brengen welke **autorisatie-impact** een ontwerp heeft, verdeeld over:

1. **Profit (autorisatiegroepen):** nieuwe/gewijzigde menu-items, tabbladen, weergaven, acties.
2. **InSite/OutSite (autorisatierollen):** nieuwe/gewijzigde pagina's/portals/overzichten/paginaonderdelen, gekoppeld aan functionaliteit.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Profit (autorisatiegroepen)

Markeer als autorisatie-impact als je ziet:

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw menupad** | HRM > … > … |
| **Nieuw tabblad** op eigenschappen | Tab "Verlof" op medewerkerkaart |
| **Nieuwe weergave/overzicht** | Overzicht "Openstaande aanvragen" |
| **Nieuwe actie/knop** | Nieuw, Verwijderen, Omzetten, Matchen |
| **Conditie/feature** | "alleen zichtbaar als … aan staat" |
| **Overerving/conversie** | "rechten van Algemeen gelden ook voor tab X" |
| **Uitzondering** | "**niet autoriseerbaar**" |

### B) InSite/OutSite (autorisatierollen)

Markeer als rol-impact als je ziet:

| Signaal | Voorbeelden |
|---------|-------------|
| **InSite/OutSite sjabloon** | "InSite sjabloon Mijn verlof" |
| Nieuwe **pagina**, **paginaonderdeel**, **overzicht**, **processtap** | |
| Nieuwe **portal** / "portaltoegang" / "type portal" | |
| Koppeling aan **functionaliteit** | "koppeling aan functionaliteit X is nodig" |

---

## Stap 2 — Output samenstellen

Lever altijd **twee losse blokken** op: eerst Profit, dan InSite/OutSite.

### Output 1 — Profit

Voor elk gevonden item:

| Veld | Inhoud |
|------|--------|
| **Item** | Menu-item / tabblad / weergave / actie |
| **Vindplaats** | Exact menupad óf object + tabblad |
| **Nieuw/gewijzigd** | 1 zin |
| **Conditie** | Ja/nee — alleen vermelden als het ontwerp dit noemt |
| **Autorisatie-hint uit ontwerp** | Overerving / conversie / niet autoriseerbaar — alleen als genoemd |
| **Status** | `komt voor` / `komt niet voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

### Output 2 — InSite/OutSite

Voor elk gevonden item:

| Veld | Inhoud |
|------|--------|
| **Kanaal** | InSite of OutSite |
| **Pagina/onderdeel** | Sjabloonnaam + pagina(onderdeel)/overzicht |
| **Functionaliteit** | Genoemd? ja → welke / nee → "ontbreekt" |
| **Nieuw/gewijzigd** | 1 zin |
| **Conditie/zichtbaarheid** | Ja/nee — alleen als het ontwerp dit noemt |
| **Status** | `komt voor` / `komt niet voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item **Bron (ontwerp)** toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Als hoofdstuk/pagina **niet betrouwbaar beschikbaar** is (bijv. niet in de tekstlaag):
- Vermeld dat expliciet.
- Gebruik **sectietitel of tekstfragment** als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

Sluit expliciet de volgende onderwerpen uit en benoem ze als "buiten scope":

- Technische IAM/SSO/IdP/AD-inrichting
- Licenties/abonnementen
- Backend/database-autorisaties die niet als menu/tab/rol zichtbaar zijn
- Teksten van e-mails/berichten, tenzij het ontwerp expliciet een **sjabloon/rol** wijzigt

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Formuleer altijd minimaal één beslispunt, bijvoorbeeld:

- **Wie krijgt standaard toegang** tot nieuwe Profit-menu's/tabbladen en/of InSite/OutSite-functionaliteit als het ontwerp dit niet benoemt?
- Moet toegang **beperkt** worden (privacy/AI/gevoelige data)?
- Als functionaliteit ontbreekt bij InSite/OutSite: **aan welke functionaliteit koppelen we de autorisatierol?**

---

## Stap 6 — Content-sectie (altijd apart opnemen)

Sluit af met een blok "Content" dat beantwoordt:

- **"Waar vind ik het?"** — menupad of pagina
- **"Welke rechten heb je nodig?"** — autorisatiegroep of rol
- **"Wat zie je als je geen rechten hebt?"** — alleen invullen als het ontwerp dit beschrijft

---

## Kwaliteitscriteria

Controleer voor je de output levert:

- [ ] Elk Profit-item heeft een vindplaats (menupad of object + tab)
- [ ] Elk InSite/OutSite-item heeft kanaal + sjabloonnaam + functionaliteitstatus
- [ ] Elk item heeft een **Bron (ontwerp)**-verwijzing
- [ ] Buiten-scope-blok is aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] Status `te weinig info` geeft aan wat er ontbreekt
