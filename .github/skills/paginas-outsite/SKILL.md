---
name: paginas-outsite
description: 'Breng de OutSite-impact van een ontwerp in kaart: wordt er functionaliteit uitgeleverd voor OutSite, welke OutSite-paginas zijn nieuw of wijzigen, en zijn er OutSite-profielen beschikbaar? Zoek altijd expliciet of het ontwerp OutSite-functionaliteit oplevert en controleer of er profielen zijn. Gebruik bij vragen als: welke OutSite-paginas zijn nodig, OutSite-impact, is er OutSite-functionaliteit, OutSite profielen, externe portal pagina.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Pagina's OutSite-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **OutSite-pagina's** een ontwerp raakt.

> **Eerste vraag, altijd:** wordt er in dit ontwerp **functionaliteit uitgeleverd voor OutSite**? Zoek daar actief naar; beantwoord die vraag expliciet vóór je aan de pagina-analyse begint.

> **Vaste controle:** ga altijd expliciet na of er **profielen beschikbaar zijn voor OutSite**. Rapporteer die uitkomst ook als het ontwerp er niets over zegt — dan met status `te weinig info`.

---

## Stap 1 — Wordt er functionaliteit uitgeleverd voor OutSite?

Dit is de kernvraag van deze skill. OutSite wordt in ontwerpen zelden als apart hoofdstuk benoemd, terwijl de functionaliteit er wel in zit. Zoek er dus gericht naar in plaats van af te wachten of het woord OutSite valt.

Loop deze drie vragen langs:

| # | Vraag | Waar je op let |
|---|-------|----------------|
| 1 | Staat OutSite **expliciet** in het ontwerp? | Het woord OutSite, een OutSite-pagina, portal of profiel |
| 2 | Is er een **externe gebruiker** die iets moet zien of doen? | Sollicitant, klant, leverancier, ouder, cursist, relatie — iedereen zonder Profit-licentie |
| 3 | Staat OutSite in de **afbakening**? | Zowel "in scope" als "buiten scope"; een expliciete uitsluiting is ook een antwoord |

Beantwoord de vraag met één van deze uitkomsten:

| Uitkomst | Wanneer | Vervolg |
|----------|---------|---------|
| **Ja, er komt OutSite-functionaliteit** | Het ontwerp beschrijft een pagina, proces of scherm voor een externe gebruiker | Beantwoord eerst stap 1b, ga daarna door met stap 2 |
| **Nee, geen OutSite** | Het ontwerp raakt alleen Profit, InSite of Pocket | Rapporteer `komt niet voor in ontwerp` en sluit af. Niet zwijgen: de uitkomst "nee" is ook een uitkomst |
| **Expliciet buiten scope** | Het ontwerp noemt OutSite en sluit het uit, of verwijst naar een later deelproject | Neem de uitsluiting over met bronverwijzing, en meld waar het wél wordt opgepakt |
| **Te weinig info** | Er is een externe gebruiker, maar het ontwerp zegt niet via welk kanaal | Zet `te weinig info` en stel de vraag aan de ontwerper: loopt dit via OutSite, Pocket of een ander kanaal? |

> **Let op de valkuil:** een proces dat in InSite is uitgewerkt, kan toch een OutSite-tegenhanger nodig hebben zodra er een externe partij in het proces zit. Benoem dat als aandachtspunt, ook als het ontwerp er niets over zegt.

---

## Stap 1b — Bij een JA: wát wordt er uitgeleverd en wie ziet het?

Is het antwoord op stap 1 **ja**, dan is de vraag nog niet af. "Er komt iets voor OutSite" is geen bruikbare uitkomst. Werk altijd deze twee vragen uit:

### 1. Wat wordt er uitgeleverd?

Benoem concreet wat de klant na de release in OutSite krijgt:

| Soort | Voorbeeld |
|-------|-----------|
| **Pagina** | Een nieuwe OutSite-pagina, of een wijziging op een bestaande |
| **Paginaonderdeel** | Een tegel, formulier, overzicht of tekstblok op een bestaande pagina |
| **Portal** | Een compleet nieuw portal, of een wijziging in een bestaand portal |
| **Proces of actie** | Wat de externe gebruiker kan indienen, aanvragen, uploaden of goedkeuren |
| **Profiel** | Het OutSite-profiel dat bepaalt welke velden zichtbaar en verplicht zijn |
| **Veld of gegeven** | Welke gegevens er nieuw zichtbaar worden |

Wordt het **standaard uitgeleverd** of moet de klant het zelf inrichten? Noteer dat erbij; dat bepaalt of er content nodig is voor de inrichting of alleen voor het gebruik.

### 2. Wie heeft hier recht op?

Bepaal **welke gebruiker dit te zien krijgt**. Dat is in OutSite bijna nooit "de gebruiker" in het algemeen: het is een specifieke externe doelgroep, en die bepaalt de toon, de terminologie en de afscherming.

| Doelgroep | Typisch proces |
|-----------|----------------|
| **Sollicitant** | Vacature bekijken, solliciteren, status volgen |
| **Medewerker (buiten InSite om)** | Eigen gegevens inzien zonder InSite-licentie |
| **Klant of relatie** | Order, factuur of dossier inzien |
| **Leverancier** | Factuur of opdracht indienen |
| **Cursist of deelnemer** | Inschrijven, cursusgegevens inzien |
| **Ouder, lid of vrijwilliger** | Gegevens doorgeven of inzien |
| **Anoniem bezoeker** | Een publiek formulier zonder inloggen |

Beantwoord per pagina of onderdeel:

| Vraag | Waarom het uitmaakt |
|-------|---------------------|
| **Wie ziet dit?** | Bepaalt de aanspreekvorm en het woordgebruik in de teksten |
| **Moet die inloggen?** | Anoniem of ingelogd verandert wat er getoond mag worden |
| **Welke rol of profiel hoort erbij?** | Bepaalt de afscherming; de rol zelf valt onder skill `autorisatie` |
| **Wat mag deze gebruiker níét zien?** | Externe gebruikers zien standaard minder dan interne |

> Zegt het ontwerp niet wie de doelgroep is? Dan is dat `te weinig info` en een vraag aan de ontwerper. **Vul nooit zelf een doelgroep in**: of de sollicitant of de medewerker dit ziet, verandert de hele uitwerking.

---

## Stap 2 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **OutSite** | OutSite, OutSite-pagina, OutSite-portal |
| **Profiel** | OutSite-profiel, profiel |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Externe gebruiker** | "de sollicitant", "de klant", "de leverancier" |
| **Publiek toegankelijk proces** | "zonder inloggen", "via de website" |
| **Aanmelding of aanvraag van buitenaf** | "extern indienen van een aanvraag" |

---

## Stap 3 — Output samenstellen

Begin de output **altijd** met de uitkomst van stap 1:

| Veld | Inhoud |
|------|--------|
| **Wordt er OutSite-functionaliteit uitgeleverd?** | `ja` / `nee` / `expliciet buiten scope` / `te weinig info` (+ wat ontbreekt) |
| **Wat wordt er uitgeleverd?** | Concreet: pagina, paginaonderdeel, portal, proces, profiel of veld (stap 1b) |
| **Standaard of zelf inrichten?** | `standaard uitgeleverd` / `klant richt zelf in` / `te weinig info` |
| **Wie ziet dit?** | De externe doelgroep: sollicitant, medewerker, klant, leverancier, cursist, anoniem bezoeker … of `te weinig info` |
| **Inloggen nodig?** | ja / nee / `te weinig info` |
| **Onderbouwing** | Waarop je die conclusie baseert |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Is het antwoord `nee` of `expliciet buiten scope`, dan ben je klaar; de tabel hieronder vul je dan niet in. Is het `ja` of `te weinig info`, werk dan per pagina uit:

| Veld | Inhoud |
|------|--------|
| **Pagina/onderdeel** | Naam van de OutSite-pagina of het paginaonderdeel |
| **Portal/sjabloon** | Bijbehorend portal of sjabloon |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Profiel aanwezig** | ja (welk profiel) / nee / `te weinig info` |
| **Doelgroep** | Welke externe gebruiker dit ziet, per pagina |
| **Wat mag deze gebruiker niét zien** | Gegevens die bewust afgeschermd blijven, of `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 4 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 5 — Buiten scope (altijd opnemen)

- Technische hosting, domeinen en certificaten
- Autorisatierollen voor OutSite (valt onder skill `autorisatie`)
- InSite-portalpagina's (valt onder skill `portalpagina-insite`)
- Profielen en veldcontexten in algemene zin (valt onder skill `profielen-en-veldcontexten`)

---

## Stap 6 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Levert dit ontwerp OutSite-functionaliteit op, of loopt het externe deel via een ander kanaal?
- Welke externe doelgroep krijgt dit te zien: de sollicitant, de medewerker, de klant of nog iemand anders?
- Moet de gebruiker inloggen, of is de pagina anoniem toegankelijk?
- Is er al een OutSite-profiel, of moet er een nieuw profiel komen?
- Wordt de pagina standaard uitgeleverd of alleen op aanvraag?
- Welke gegevens mogen extern zichtbaar zijn, en welke juist niet?

---

## Stap 7 — Content-sectie (altijd apart opnemen)

- **"Wat ziet de externe gebruiker?"**
- **"Voor wie is deze pagina bedoeld?"**
- **"Waar vind je de pagina?"**
- **"Welk profiel is nodig?"**

---

## Kwaliteitscriteria

- [ ] De vraag "wordt er functionaliteit uitgeleverd voor OutSite?" is expliciet beantwoord, ook als het antwoord `nee` is
- [ ] Bij een `ja` is concreet benoemd **wát** er wordt uitgeleverd
- [ ] Bij een `ja` is benoemd **wie** het te zien krijgt, met de doelgroep bij naam
- [ ] Er staat nergens "de gebruiker" waar een specifieke doelgroep bedoeld wordt
- [ ] Voor elke pagina is de profielcheck expliciet beantwoord
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Overzicht van bestaande OutSite-portals en -profielen
- Menupaden voor OutSite-beheer
- Regels voor wat extern zichtbaar mag zijn
