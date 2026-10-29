---
name: profielen-en-veldcontexten
description: 'Breng in kaart welke profielen en contexten een ontwerp raakt: aanmaakprofielen, beoordeelprofielen, afwijkende beoordeelprofielen per workflowtaak en de veldinstellingen per context (zichtbaar, wijzigbaar, verplicht, vast gevuld) in Profit, InSite, OutSite en Pocket. Gebruik bij vragen als: welke profielen zijn nodig, welke contexten, beoordeelprofiel, afwijkend beoordelingsprofiel, rechtenmatrix per context, veldzichtbaarheid, veldcontext aanpassen.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Profielen en contexten-analyse

## Doel

Vaststellen welke **profielen** we meeleveren, welke **contexten** daaronder hangen, en per context welke velden zichtbaar, wijzigbaar, verplicht, verborgen of vast gevuld zijn.

---

## Het model

Een ontwerp dat één profiel noemt, levert in de praktijk vier tot zes objecten op. Loop deze keten altijd volledig af:

```
Type dossieritem
   └─ Aanmaakprofiel                   →  context voor de instuurder
        └─ Gekoppeld beoordeelprofiel  →  context voor de beoordelaar
   └─ Afwijkend beoordeelprofiel       →  per workflowtaak te kiezen
```

Vier regels die altijd gelden:

1. **Elk aanmaakprofiel heeft een gekoppeld beoordeelprofiel.** Zonder dat onderscheid krijgen instuurder en beoordelaar dezelfde veldinstellingen, en kan een beoordelaar de vraag herschrijven of een instuurder het antwoord overschrijven.
2. **Een afwijkend beoordeelprofiel hoort bij een workflowtaak, niet bij een aanmaakprofiel.** Verschillende taken in dezelfde workflow kunnen verschillende velden nodig hebben. Noteer dus altijd: welke workflow, welke taak, welk profiel.
3. **Eén profiel per inhoudelijke variant.** Verschilt alleen de vulling van een veld — bijvoorbeeld een vast onderwerp — dan is dat toch een eigen profiel plus een eigen context.
4. **Contexten gelden over alle kanalen.** InSite ESS, InSite MSS, OutSite en Pocket gebruiken dezelfde context. Een afwijking per kanaal is een uitzondering die het ontwerp expliciet moet benoemen.

### Referentie: naamgevingspatroon

| Object | Patroon | Voorbeeld |
|---|---|---|
| Aanmaakprofiel | `Aanmaken <onderwerp>` | `Aanmaken vraag aan HR` |
| Aanmaakprofiel, variant | `Aanmaken <onderwerp> - <variant>` | `Aanmaken vraag aan HR - loontransparantie` |
| Beoordeelprofiel | `Beoordelen <onderwerp>` | `Beoordelen vraag aan HR` |
| Afwijkend beoordeelprofiel | `Beoordelen <onderwerp> - <handeling>` | `Beoordelen vraag aan HR - antwoord geven` |
| Context | `<onderwerp> – <handeling>` | `Vraag aan HR – antwoord geven` |

### Referentie: standaardcontexten bij een vraag-en-antwoordproces

| Context | Rol | Kern |
|---|---|---|
| `… – insturen` | instuurder | invoervelden wijzigbaar en verplicht; antwoordveld **verborgen** |
| `… – <variant> insturen` | instuurder | als hierboven, met één of meer velden **vast gevuld** |
| `… – antwoord geven` | beoordelaar | antwoordveld wijzigbaar; invoervelden zichtbaar maar read-only |
| `… – alleen lezen` | beide, na afronding | alles zichtbaar, niets wijzigbaar |

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Profiel** | profiel, aanmaakprofiel, beoordeelprofiel, afwijkend profiel, standaardprofiel |
| **Context** | context, profielcontext, veldcontext, veldinstellingen |
| **Rechtenmatrix** | rechten per profielcontext, zichtbaar/wijzigbaar/verplicht |
| **Vrije velden** | vrije velden, veldgroep Extra gegevens |
| **Starten in aanpassen** | starten in aanpassen, aanpassen-pagina |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld** | elk nieuw veld vraagt een keuze per context |
| **Terugloopstap in de workflow** | "HR kan om aanvulling vragen" → de instuurder heeft een eigen aanpassen-context nodig |
| **Twee rollen op hetzelfde scherm** | "HR beoordeelt de vraag" → aanmaak- én beoordeelcontext |
| **Veld dat na insturen vastligt** | "het onderwerp ligt na het insturen vast" |
| **Vast gevuld veld** | "het onderwerp wordt gevuld met …" → eigen profiel plus context |
| **Verplicht vanuit programmatuur** | "de klant kan dit veld niet verbergen" → uitzondering op de vrije veldinstellingen |
| **Voorwaardelijke zichtbaarheid in Profit** | "het veld is alleen zichtbaar bij actieve Flex-activering" |
| **Afgeschoven keuze** | "Content bepaalt of er extra profielen nodig zijn" → altijd een beslispunt |

> **Let op de afronding.** Zodra een workflow is afgehandeld, is standaard niets meer wijzigbaar. Dat hoef je niet apart in te richten, maar wél te melden zodat niemand er een extra context voor maakt.

---

## Stap 2 — Output samenstellen

Lever **twee blokken** op.

### Blok 1 — Profielen en contexten

Eén rij per profiel.

| Veld | Inhoud |
|------|--------|
| **Profiel** | Naam volgens het naamgevingspatroon |
| **Soort** | `aanmaken` / `beoordelen` / `afwijkend beoordelen` |
| **Gekoppeld aan** | Bij een aanmaakprofiel: het beoordeelprofiel. Bij een afwijkend profiel: de workflow **en** de taak |
| **Context** | De context die eronder hangt |
| **Kanalen** | InSite ESS / InSite MSS / OutSite / Pocket |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

### Blok 2 — Rechtenmatrix

Eén rij per veld, één kolom per context. Lever deze matrix **altijd**, ook als het ontwerp hem al bevat: toets hem dan en vul de ontbrekende contexten aan.

| Veld | insturen | variant insturen | antwoord geven | alleen lezen |
|---|---|---|---|---|
| *Veldnaam* | zichtbaar, wijzigbaar, verplicht | vast gevuld met "…" | zichtbaar, niet wijzigbaar | zichtbaar, niet wijzigbaar |

Toegestane waarden: `zichtbaar, wijzigbaar`, `zichtbaar, wijzigbaar, verplicht`, `zichtbaar, niet wijzigbaar`, `niet zichtbaar`, `vast gevuld met "…"`.

Noteer onder de matrix per uitzondering één regel:

- Velden die **verplicht zijn vanuit programmatuur** en die de klant dus niet kan verbergen.
- Velden die de klant **wél mag verbergen**, en welke veldinstellingen hij overhoudt: label, volgorde en hulptekst.
- De **veldgroep voor vrije velden**: wie hem mag vullen en wat er gebeurt als er geen vrije velden zijn.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische veldvalidaties en foutmeldingen
- Het datamodel van de mutatie- en profieltabel
- Functionaliteiten, rollen en pagina-onderdelen (valt onder skill `autorisatie-en-functionaliteiten`)
- Informatiebolletjes bij velden (valt onder skill `informatiebolletje`)
- De banner en de teksten op de profielkeuzepagina (valt onder skill `portalpagina-insite`)
- De workflowstappen zelf (valt onder skill `workflow-condities`); alleen de koppeling taak → afwijkend beoordeelprofiel hoort hier
- Weergaven (valt onder skill `weergaven`) en boekingslayouts (valt onder skill `boekingslayouts`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Hoeveel profielen leveren we mee, en krijgt elke variant een eigen aanmaak- én beoordeelprofiel?
- Welke workflowtaak krijgt welk **afwijkend** beoordeelprofiel?
- Is er een `alleen lezen`-context nodig, of volstaat het standaardgedrag na afronding?
- Welke velden mag de klant verbergen, en welke zijn verplicht vanuit programmatuur?
- Wijken de contexten per kanaal af, of gelden ze gelijk voor InSite, OutSite en Pocket?
- Welke waarde krijgt een vast gevuld veld, en is die lengte veilig?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welk profiel kies je waarvoor?"**
- **"Welke velden zie je in welke stap?"**
- **"Waar pas je dit aan?"** — menupad naar het profielbeheer
- **"Wat gebeurt er als een veld verborgen is?"**

---

## Kwaliteitscriteria

- [ ] Elk aanmaakprofiel heeft een benoemd gekoppeld beoordeelprofiel
- [ ] Elk afwijkend beoordeelprofiel noemt zowel de workflow als de taak
- [ ] Elk profiel heeft precies één context, met naam
- [ ] De rechtenmatrix is compleet: elk veld maal elke context, zonder lege cel
- [ ] Vast gevulde velden vermelden de letterlijke waarde
- [ ] Uitzonderingen op de vrije veldinstellingen staan apart benoemd
- [ ] De kanalen InSite ESS, InSite MSS, OutSite en Pocket zijn alle vier beoordeeld
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupaden voor profiel- en contextbeheer
- Overzicht van standaardprofielen per kanaal
- Verhouding tussen profiel, context en functionaliteit
