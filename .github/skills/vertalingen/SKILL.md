---
name: vertalingen
description: 'Breng in kaart welke vertalingen nodig zijn voor de teksten van berichtsjablonen en signalen: onderwerp, berichtinhoud en signaaltekst in NL, ENG, DUI en FR. Gebruik bij vragen als: welke vertalingen zijn nodig, vertaal-impact, meertalig berichtsjabloon, signaaltekst vertalen, taalregels.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Vertalingen-analyse

## Doel

Vaststellen welke **teksten vertaald** moeten worden en in welke talen.

> **Scope (voorlopig beperkt):** deze skill geldt **alleen** voor de teksten van:
>
> 1. **Berichtsjablonen** — het veld *Onderwerp (mail)* en de inhoud van de berichtsjabloon-editor.
> 2. **Signalen** — de signaaltekst en een eventueel automatisch e-mailbericht.
>
> Teksten van andere onderdelen (veldlabels, menunamen, meldingen, InSite-pagina's) vallen **buiten scope** zolang deze beperking geldt.

---

## Talen

| Code | Taal |
|------|------|
| **NL** | Nederlands |
| **ENG** | Engels |
| **DUI** | Duits |
| **FR** | Frans |

---

## Stap 1 — Scan: waar haal je de teksten vandaan?

Deze skill werkt op de uitkomsten van twee andere skills:

| Bron-skill | Wat je overneemt |
|------------|------------------|
| `berichtsjabloon` | Per berichtsjabloon: de omschrijving, het onderwerp en de berichtinhoud |
| `signalen` | Per signaal: de signaaltekst en de tekst van het automatische e-mailbericht |

Let daarnaast in het ontwerp op expliciete aanwijzingen:

| Term | Varianten |
|------|-----------|
| **Vertaling** | vertaling, vertalen, taal, taalregel, meertalig |
| **Anderstalige ontvanger** | "buitenlandse vestiging", "in de eigen taal van de ontvanger" |

Zegt het ontwerp niets over talen? Gebruik dan `te weinig info` en zet het door als vraag aan de ontwerper. **Niet zelf invullen.**

---

## Stap 2 — Output samenstellen

Lever per te vertalen tekst één blok op.

### Blok — Tekst

| Veld | Inhoud |
|------|--------|
| **Herkomst** | `berichtsjabloon` of `signaal` |
| **Naam** | Naam van het berichtsjabloon (incl. `(Profit)`) of van het signaal |
| **Tekstonderdeel** | Onderwerp (mail) / berichtinhoud / signaaltekst / e-mailbericht bij signaal |
| **Benodigde talen** | Welke van NL / ENG / DUI / FR, of `te weinig info` |
| **Gevraagde actie** | `nieuw vertalen` / `bestaande vertaling aanpassen` / `controleren` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok — Vertaaltabel

| Taal | Tekst |
|------|-------|
| NL | … |
| ENG | … |
| DUI | … |
| FR | … |

Regels:

- **NL is altijd de brontekst** en wordt altijd ingevuld.
- Vul alleen de talen in die daadwerkelijk nodig zijn; markeer de rest als `niet nodig` of `te weinig info`.
- Laat **tags uit de gegevensverzameling ongewijzigd** staan in elke taal (bijv. `Roepnaam`, `Vacature`).
- Is de brontekst nog niet vastgesteld: zet `nader te bepalen` en beschrijf wat de tekst moet overbrengen.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item een bronverwijzing toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Vertalingen van veldlabels, menunamen, tabbladen en keuzewaarden
- Vertalingen van foutmeldingen en systeemmeldingen
- Vertalingen van InSite-/OutSite-paginateksten
- Vertalingen van helpteksten en informatiebolletjes
- Het technische proces van aanleveren en releasen van taalbestanden

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- In welke talen leveren we deze tekst uit?
- Wie levert de vertaling aan en wie controleert die?
- Gebruiken we een bestaande vertaling opnieuw of schrijven we een nieuwe tekst?
- Welke term gebruiken we consistent voor een nieuw begrip in elke taal?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke teksten moeten vertaald worden?"**
- **"In welke talen is dit beschikbaar?"**
- **"Welke term gebruiken we waarvoor?"** — consistente terminologie

---

## Kwaliteitscriteria

- [ ] Elke tekst is herleidbaar naar een berichtsjabloon of signaal
- [ ] NL is altijd ingevuld
- [ ] Per tekst is expliciet beantwoord welke talen nodig zijn
- [ ] Tags staan ongewijzigd in elke taal
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Waar vertalingen worden beheerd en aangeleverd
- Of NL altijd verplicht is en de overige talen optioneel
- Terminologielijst voor consistente vertalingen
- Wanneer de scope wordt verbreed naar andere onderdelen dan berichtsjablonen en signalen
