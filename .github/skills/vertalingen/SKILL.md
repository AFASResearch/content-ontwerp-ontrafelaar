---
name: vertalingen
description: 'Breng in kaart welke vertalingen nodig zijn voor de teksten van berichtsjablonen en signalen: onderwerp, berichtinhoud en signaaltekst in NL, ENG, DUI en FR, en lever de vertalingen uit met tags ongewijzigd. Gebruik bij vragen als: welke vertalingen zijn nodig, vertaal-impact, meertalig berichtsjabloon, vertaal dit berichtsjabloon, signaaltekst vertalen, taalregels, aanspreekvorm du of Sie.'
argument-hint: 'Geef het ontwerp mee, of plak de NL-brontekst (onderwerp + berichtinhoud) als platte tekst'
---

# Vertalingen-analyse

## Doel

Vaststellen welke **teksten vertaald** moeten worden, **in welke talen**, en de vertalingen **uitleveren** met alle tags ongewijzigd.

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

## Stap 1 — Input opvragen in het juiste formaat

Vraag de brontekst **als platte tekst** aan (of als HTML uit de editor).

> **Vraag geen `.emt`-bestand.** Een `.emt` is een gecomprimeerd binair Profit-exportbestand. Alleen de naam van het sjabloon is eruit te lezen; de tekst zelf niet. Laat de gebruiker het sjabloon in Profit openen en de inhoud van de editor kopiëren.

Vraag per berichtsjabloon om:

| Onderdeel | Toelichting |
|-----------|-------------|
| **Omschrijving** | Naam van het sjabloon, inclusief `(Profit)` |
| **Onderwerp (mail)** | Als losse regel |
| **Berichtinhoud** | Platte tekst, met de tags letterlijk op hun plek |
| **Tags** | Welke velden uit de gegevensverzameling erin staan |

Vraag per signaal om: de **signaaltekst** en de tekst van het eventuele **automatische e-mailbericht**.

**Tagnotatie:** tags staan in de aangeleverde tekst meestal tussen accolades, bijvoorbeeld `{Naam werkgever}`, `{Roepnaam}`, `{UPN}`. Soms staan ze zonder accolades (zo tonen ze in de editor). Vraag bij twijfel welke woorden tags zijn en welke gewone tekst. **Tags vertaal je nooit.**

---

## Stap 2 — Scan: waar haal je de teksten vandaan?

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

## Stap 3 — Controleer eerst de NL-brontekst (skill `schrijfwijzer`)

Je vertaalt nooit een zwakke brontekst. Loop de NL-tekst eerst langs de skill `schrijfwijzer`:

1. Staat de kernboodschap vroeg in de tekst (AKTO/piramide)?
2. Is de tekst B1, actief, klant- en servicegericht?
3. Is de tekst scanbaar: korte zinnen, 1 onderwerp per alinea, duidelijke kop?
4. Is er een heldere call-to-action als de lezer iets moet doen?

Regels bij deze controle:

- Stel **alleen** een verbeterde NL-tekst voor; pas de brontekst niet stilzwijgend aan. Leg de wijziging expliciet voor.
- Raakt de NL-tekst aangepast, vertaal dan de **goedgekeurde** versie, niet de oude.
- **De vertalingen nemen de toon van de NL-brontekst over**: zelfde register, zelfde mate van directheid, zelfde zinslengte. Een B1-NL-tekst levert een B1-vertaling op.
- Vertaal **betekenis en toon**, niet woord voor woord. Een letterlijke vertaling die stijf of formeel leest, voldoet niet.

---

## Stap 4 — Vertaalregels

### Tags

- Laat **tags uit de gegevensverzameling ongewijzigd** staan in élke taal, inclusief de accolades: `{Naam werkgever}`, `{Roepnaam}`, `{UPN}`.
- Pas de zin om de tag heen wél aan de doeltaal aan (lidwoord, naamval, woordvolgorde).
- Controleer na het vertalen dat elke taal **exact dezelfde tags** bevat als de NL-brontekst.

### Aanspreekvorm

Nederlands kent alleen *je* of *u*. Duits en Frans dwingen een keuze af:

| NL | ENG | DUI | FR |
|----|-----|-----|----|
| je (informeel) | you | du / dein | tu / ton |
| u (formeel) | you | Sie / Ihr | vous / votre |

- Volg standaard de NL-brontekst: *je* → *du* / *tu*, *u* → *Sie* / *vous*.
- Benoem de gekozen aanspreekvorm **altijd** als beslispunt, zodat de opdrachtgever kan bijsturen.
- Houd de gekozen vorm **consistent** binnen één sjabloon, inclusief onderwerp en ondertekening.

### Terminologie

- Vertaal een vakterm overal in het sjabloon **hetzelfde**. Voorbeeld: inlognaam → *username* / *Benutzername* / *nom d'utilisateur*.
- Controleer of de gekozen term aansluit bij de term die Profit, InSite of OutSite al gebruikt. Wijkt die af, meld dat als beslispunt.

### Opmaak en leestekens

- Neem de opmaak van de brontekst over: vet, koppen, regelovergangen en alineastructuur blijven gelijk.
- Frans: spatie vóór `:`, `;`, `!` en `?` (`Ton nom d'utilisateur :`).
- Duits: zelfstandige naamwoorden met hoofdletter, `ß` waar dat hoort.
- Vertaal geen URL's, mailadressen of bestandsnamen.

---

## Stap 5 — Output samenstellen

Lever per te vertalen **tekstonderdeel** één blok op: eerst de kop, dan de vertalingen.

### Blok — Tekst (kop)

| Veld | Inhoud |
|------|--------|
| **Herkomst** | `berichtsjabloon` of `signaal` |
| **Naam** | Naam van het berichtsjabloon (incl. `(Profit)`) of van het signaal |
| **Tekstonderdeel** | Onderwerp (mail) / berichtinhoud / signaaltekst / e-mailbericht bij signaal |
| **Benodigde talen** | Welke van NL / ENG / DUI / FR, of `te weinig info` |
| **Gevraagde actie** | `nieuw vertalen` / `bestaande vertaling aanpassen` / `controleren` |
| **Tags ongewijzigd** | Opsomming van de tags die in elke taal gelijk blijven |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok — Vertaling: kies het juiste format

| Lengte tekst | Format |
|--------------|--------|
| **Kort** (onderwerp, signaaltekst, één regel) | Vertaaltabel: kolom **Taal** + kolom **Tekst** |
| **Lang** (volledige berichtinhoud) | Eén **apart tekstblok per taal** onder een kop `### ENG`, `### DUI`, `### FR`, zodat de tekst direct te kopiëren is naar de editor |

Gebruik nooit een tabelcel voor een tekst van meerdere alinea's: die is niet te kopiëren en de opmaak gaat verloren.

Vertaaltabel voor korte teksten:

| Taal | Tekst |
|------|-------|
| NL | … |
| ENG | … |
| DUI | … |
| FR | … |

Regels:

- **NL is altijd de brontekst** en wordt altijd ingevuld.
- Vul alleen de talen in die daadwerkelijk nodig zijn; markeer de rest als `niet nodig` of `te weinig info`.
- Is de brontekst nog niet vastgesteld: zet `nader te bepalen` en beschrijf wat de tekst moet overbrengen.
- Lever de vertaling **copy-pasteklaar** op: zonder toelichting door de tekst heen. Opmerkingen horen in de beslispunten.

---

## Stap 6 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item een bronverwijzing toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

Komt de brontekst rechtstreeks van de gebruiker (geplakt uit Profit) in plaats van uit een ontwerp? Gebruik dan `[aangeleverd sjabloon]` + de omschrijving van het sjabloon als bron.

---

## Stap 7 — Buiten scope (altijd opnemen)

- Vertalingen van veldlabels, menunamen, tabbladen en keuzewaarden
- Vertalingen van foutmeldingen en systeemmeldingen
- Vertalingen van InSite-/OutSite-paginateksten
- Vertalingen van helpteksten en informatiebolletjes
- Afbeeldingen, beeldmateriaal en footerteksten in het sjabloon
- Het technische proces van aanleveren en releasen van taalbestanden

---

## Stap 8 — Beslispunten (altijd opnemen, minimaal 1)

Neem in elk geval op:

- **Aanspreekvorm**: informeel (*du* / *tu*) of formeel (*Sie* / *vous*) in DUI en FR?
- **Terminologie**: welke term gebruiken we consistent voor een vakterm in elke taal, en sluit die aan bij Profit?
- **Review**: wie controleert de vertaling, en is er een native reviewer nodig?

Aanvullend, waar van toepassing:

- In welke talen leveren we deze tekst uit?
- Gebruiken we een bestaande vertaling opnieuw of schrijven we een nieuwe tekst?
- Blijven afbeelding, footer en links in alle talen gelijk?

---

## Stap 9 — Content-sectie (altijd apart opnemen)

- **"Welke teksten moeten vertaald worden?"**
- **"In welke talen is dit beschikbaar?"**
- **"Welke term gebruiken we waarvoor?"** — consistente terminologie

---

## Voorbeeld — Medewerkerbericht UPN (Profit)

Verkorte uitwerking die het opleverformat laat zien.

### Blok — Tekst 1: Onderwerp (mail)

| Veld | Inhoud |
|------|--------|
| **Herkomst** | `berichtsjabloon` |
| **Naam** | Medewerkerbericht UPN (Profit) |
| **Tekstonderdeel** | Onderwerp (mail) |
| **Benodigde talen** | NL (bron) + ENG, DUI, FR |
| **Gevraagde actie** | nieuw vertalen |
| **Tags ongewijzigd** | {Naam werkgever} |
| **Status** | komt voor in ontwerp |
| **Bron** | `[aangeleverd sjabloon]` Medewerkerbericht UPN (Profit) |

| Taal | Tekst |
|------|-------|
| NL | Welkom bij {Naam werkgever} - je inlognaam staat voor je klaar |
| ENG | Welcome to {Naam werkgever} - your username is ready for you |
| DUI | Willkommen bei {Naam werkgever} - dein Benutzername steht für dich bereit |
| FR | Bienvenue chez {Naam werkgever} - ton nom d'utilisateur est prêt |

### Blok — Tekst 2: Berichtinhoud

Lange tekst, dus **per taal een apart blok**. Tags ongewijzigd: `{Naam werkgever}`, `{Roepnaam}`, `{UPN}`.

> **DUI**
>
> **Willkommen bei {Naam werkgever}, schön, dass du da bist!**
>
> **Hallo {Roepnaam},**
>
> Heute ist dein erster Arbeitstag bei {Naam werkgever}. Herzlich willkommen! …
>
> **Dein Benutzername:**
> **{UPN}**

### Beslispunten bij dit voorbeeld

1. Aanspreekvorm DUI en FR: informeel (*du* / *tu*) aangehouden, passend bij het NL *je*. Formeel gewenst? Dan alle blokken aanpassen.
2. Term "inlognaam" vertaald als *username* / *Benutzername* / *nom d'utilisateur*. Check consistentie met Profit en InSite.
3. Nog geen native review op ENG, DUI en FR.
4. Afbeelding en footer vallen buiten scope: blijven die in alle talen gelijk?

---

## Kwaliteitscriteria

- [ ] De brontekst is als platte tekst of HTML aangeleverd (geen `.emt`)
- [ ] Elke tekst is herleidbaar naar een berichtsjabloon of signaal
- [ ] De NL-brontekst is getoetst aan de skill `schrijfwijzer`
- [ ] NL is altijd ingevuld
- [ ] Per tekst is expliciet beantwoord welke talen nodig zijn
- [ ] Tags staan ongewijzigd in elke taal, en elke taal bevat dezelfde tags als NL
- [ ] De aanspreekvorm is per taal bewust gekozen en consistent toegepast
- [ ] Vaktermen zijn binnen het sjabloon consistent vertaald
- [ ] Lange teksten staan per taal in een apart, copy-pasteklaar blok
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd, inclusief aanspreekvorm en review
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Waar vertalingen worden beheerd en aangeleverd
- Of NL altijd verplicht is en de overige talen optioneel
- Terminologielijst voor consistente vertalingen (inclusief vaste vertaling van begrippen als inlognaam, medewerker, dienstverband)
- Vaste keuze voor de aanspreekvorm in DUI en FR, zodat dit geen beslispunt per sjabloon meer is
- Standaardvertalingen voor terugkerende bouwstenen (aanhef, ondertekening, links)
- Wanneer de scope wordt verbreed naar andere onderdelen dan berichtsjablonen en signalen
