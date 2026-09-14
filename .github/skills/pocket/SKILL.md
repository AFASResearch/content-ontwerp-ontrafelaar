---
name: pocket
description: 'Breng de Pocket-impact van een ontwerp in kaart: welke functionaliteit, schermen of processen in de AFAS Pocket-app nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: heeft dit impact op Pocket, Pocket-app, mobiele app, Pocket-functionaliteit.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Pocket-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **Pocket-functionaliteit** een ontwerp raakt en wat daarvoor ingericht of beschreven moet worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Pocket** | Pocket, AFAS Pocket, app |
| **Mobiel** | mobiel, mobiele app, smartphone |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Proces dat onderweg wordt uitgevoerd** | verlof aanvragen, declaratie indienen, uren boeken |
| **Pushmelding** | "de gebruiker krijgt een melding op zijn telefoon" |
| **Goedkeuring door leidinggevende** | workflowtaken die vaak mobiel worden afgehandeld |
| **Foto of bijlage vanaf telefoon** | "de gebruiker maakt een foto van de bon" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Onderdeel** | Scherm, proces of functie in Pocket |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Beschikbaar in Pocket** | ja / nee / `te weinig info` |
| **Benodigde inrichting** | Wat aan moet staan om het in Pocket te gebruiken |
| **Doelgroep** | Welke gebruikersrol |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- App-store releases en technische app-versies
- Apparaatbeheer en MDM
- Autorisatie (valt onder skill `autorisatie`)
- Profielen en veldcontexten (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Komt de functionaliteit ook naar Pocket, of alleen naar InSite?
- Welke velden tonen we wel/niet op een klein scherm?
- Is een pushmelding gewenst?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat kun je in Pocket doen?"**
- **"Waar vind je het in de app?"**
- **"Wat moet ingericht zijn?"**

---

## Kwaliteitscriteria

- [ ] Voor elk onderdeel is "beschikbaar in Pocket" expliciet beantwoord
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Welke processen Pocket ondersteunt
- Waar Pocket-functionaliteit wordt ingericht
- Relatie tussen Pocket-profielen en InSite-profielen
