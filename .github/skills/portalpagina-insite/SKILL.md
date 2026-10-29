---
name: portalpagina-insite
description: 'Breng de InSite-opmaak-impact van een ontwerp in kaart: welke banners (afbeelding, titel, tekst), profielkeuzepaginas en medewerkerkeuzepaginas opgemaakt moeten worden, en welke pagina-onderdelen op een portalpagina komen. Gebruik bij vragen als: welke InSite-opmaak is nodig, banner, profielkeuzepagina, bannertekst, afbeelding bij profiel, pagina-onderdeel op de stamkaart.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# InSite-opmaak-analyse

## Doel

Vaststellen welke **InSite-opmaak** de content-afdeling moet maken: de banner op aanmaak-, profielkeuze- en medewerkerkeuzepagina's, en de plaatsing van pagina-onderdelen op portalpagina's.

## Wat valt hier wél onder

- **Banner** per sjabloon: afbeelding, titel en tekst.
- **Profielkeuzepagina** en **medewerkerkeuzepagina**: tekst per profiel.
- **Pagina-onderdelen** die op een portalpagina of standaard stamkaart landen: plaats en titel.

## Wat valt hier niet onder

Wij maken de standaardpagina's van InSite **niet meer zelf op**. Die komen uit de bouw. Staat er in het ontwerp een nieuw sjabloon, dan is de contenttaak uitsluitend de banner en de teksten erop — niet de veldindeling en niet de veldvolgorde.

Bestaat er voor een pagina **geen** standaardpagina (dat komt voor bij OutSite), dan moet die wél zelf opgemaakt en ingecheckt worden. Meld dat als apart item en verwijs naar `paginas-outsite`.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Sjabloon** | sjabloon, InSite-sjabloon, Aanmaken …, Beoordelen …, Aanpassen … |
| **Profielkeuze** | profielkeuze, profiel-medewerkerkeuze, medewerkerkeuze |
| **Banner** | banner, afbeelding, koptekst, toelichtende tekst |
| **Pagina-onderdeel** | pagina-onderdeel, tegel, KPI, sectie op de stamkaart |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Meerdere profielen op één sjabloon** | "de medewerker kiest bij het starten een profiel" → per profiel een eigen tekst |
| **Nieuwe sectie op een stamkaart** | "op de stamkaart komt een sectie X" |
| **ESS- en MSS-variant** | "de leidinggevende start namens de medewerker" → twee teksten, je-vorm tegenover de-medewerkervorm |
| **Toelichtende tekst zonder inhoud** | "invulling door team Content" → altijd een contenttaak |

> **Let op de vermenigvuldiging.** Eén sjabloon maal twee profielen maal ESS/MSS levert zes teksten op. Tel ze expliciet; het ontwerp doet dat zelden.

---

## Stap 2 — Output samenstellen

Eén rij per combinatie van **sjabloon × profiel**.

| Veld | Inhoud |
|------|--------|
| **Sjabloon** | Exacte sjabloonnaam, bijv. `Aanmaken vraag aan HR (ESS)` |
| **Profiel** | Het profiel waarvoor deze opmaak geldt, of `alle profielen` |
| **Kanaal** | InSite ESS / InSite MSS |
| **Afbeelding** | Bestandsnaam, of `te bepalen` |
| **Titel en tekst** | Concepttekst, geschreven volgens `schrijfwijzer` |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Regels voor de bannertekst

- Eén zin, imperatief, gericht op wat de gebruiker hier gaat doen.
- **ESS in de je-vorm**, **MSS over de medewerker**. Voorbeeld: `Stel je vraag aan HR.` tegenover `Stel een vraag aan HR voor je medewerker.`
- De profielkeuze- en medewerkerkeuzepagina beschrijven de **keuze**, niet het doel: `Kies de medewerker voor wie je een vraag aan HR wilt stellen.`
- Wijkt een profiel inhoudelijk af, dan krijgt dat profiel een eigen tekst én een eigen afbeelding.

### Pagina-onderdelen

Komt er een pagina-onderdeel bij, zoals een KPI-sectie, lever dan per onderdeel:

| Veld | Inhoud |
|------|--------|
| **Onderdeel** | Naam zoals die in de inrichting staat, bijv. `KPI's voor Loontransparantie (ESS)` |
| **Portalpagina** | Op welke pagina het landt en op welke plek |
| **Varianten** | ESS, MSS, en eventuele varianten per populatie, bijvoorbeeld per plaatsing |

De **autorisatie** van zo'n onderdeel valt onder `autorisatie-en-functionaliteiten`, niet hier.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- De veldindeling en veldvolgorde van standaardpagina's; die komen uit de bouw
- Huisstijl en centrale opmaakrichtlijnen
- Klantspecifieke portalinrichting
- Autorisatie op functionaliteit, rol of pagina-onderdeel (valt onder skill `autorisatie-en-functionaliteiten`)
- Veldzichtbaarheid per context (valt onder skill `profielen-en-veldcontexten`)
- OutSite-pagina's (valt onder skill `paginas-outsite`)
- Icoontjes bij knoppen en menu-items (valt onder skill `icoontjes`); bannerafbeeldingen vallen wél hier

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Welke afbeelding hoort bij welk profiel, en bestaat die al?
- Krijgt elk profiel een eigen tekst, of volstaat één tekst per sjabloon?
- Landt het pagina-onderdeel boven of onder de bestaande onderdelen?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat ziet de gebruiker op deze pagina?"**
- **"Waar vind je de pagina?"**
- **"Welk profiel kies je waarvoor?"**

---

## Kwaliteitscriteria

- [ ] Elke combinatie sjabloon × profiel heeft een eigen rij
- [ ] ESS- en MSS-teksten staan beide in de output en verschillen in aanspreekvorm
- [ ] Elke afbeelding is benoemd of expliciet `te bepalen`
- [ ] Pagina's zonder standaardpagina zijn apart gemeld
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Overzicht van beschikbare bannerafbeeldingen
- Menupaden voor InSite-paginabeheer
- Vaste controlepunten voor de opmaak
