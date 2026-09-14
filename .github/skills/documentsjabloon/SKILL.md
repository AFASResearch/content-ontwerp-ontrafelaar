---
name: documentsjabloon
description: 'Breng de documentsjabloon-impact van een ontwerp in kaart: welke brieven, documenten en correspondentiesjablonen in Profit, InSite of OutSite nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: welke documentsjablonen zijn nodig, briefsjabloon, correspondentie, document genereren, pdf uit Profit.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Documentsjabloon-analyse

> **Status: skelet.** De inhoud wordt nog samen uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **documentsjablonen** een ontwerp raakt: brieven, documenten en correspondentie die nieuw gebouwd, aangepast of gecontroleerd moeten worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Documentsjabloon** | documentsjabloon, briefsjabloon, Word-sjabloon |
| **Correspondentie** | correspondentie, brief, uitnodiging, bevestiging |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Document als uitkomst** | "er wordt een contract gegenereerd", "de gebruiker downloadt een pdf" |
| **Formele vastlegging** | "de afspraak wordt schriftelijk bevestigd" |
| **Nieuwe gegevens in een document** | "het document bevat voortaan ook veld X" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Sjabloonnaam** | Naam van het documentsjabloon |
| **Kanaal** | Profit / InSite / OutSite |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Aanleiding** | Welke gebeurtenis of processtap het document oplevert |
| **Ontvanger** | Wie het document ontvangt |
| **Gegevens/velden** | Welke gegevens in het document komen, of `nader te bepalen` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Huisstijl, beeldmateriaal en centrale opmaakrichtlijnen
- E-mailberichten (valt onder skill `berichtsjabloon`)
- Rapportlayouts (valt onder skill `rapporten`)
- Klantspecifieke documentsjablonen

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Komt er een nieuw documentsjabloon of passen we een bestaand sjabloon aan?
- Welke gegevens komen in het document?
- Wie is de ontvanger als het ontwerp dit niet benoemt?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welke tekst en gegevens komen in het document?"**
- **"Waar richt je het sjabloon in?"** — menupad
- **"Wanneer ontvangt de gebruiker dit document?"**

---

## Kwaliteitscriteria

- [ ] Elk sjabloon heeft kanaal, aanleiding en ontvanger
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Opbouw van een documentsjabloon en welke onderdelen het bevat
- Menupad voor documentsjabloonbeheer in Profit
- Hoe gegevens uit Profit in het document terechtkomen
- Of en hoe vertaling van documentteksten wordt geregeld
