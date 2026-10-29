---
name: rapporten
description: 'Breng de rapport-impact van een ontwerp in kaart: welke rapportlayouts, standaardrapporten en rapporten-in-de-workflow in Profit, InSite of OutSite nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: welke rapporten zijn nodig, rapportlayout aanpassen, standaardrapport, rapport in de workflow genereren, afdrukken, rapportage-impact.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Rapporten-analyse

## Doel

Volledig in kaart brengen welke **rapporten en rapportlayouts** een ontwerp raakt en wat daarvoor ingericht of aangevuld moet worden.

---

## Twee soorten rapporten

| Soort | Waar de gebruiker hem start | Let op |
|---|---|---|
| **Afdrukrapport** | Vanuit een menu-item of weergave in Profit | Vindplaats en doelgroep zijn leidend |
| **Rapport in de workflow** | De behandelaar kiest het in een workflowstap; het resultaat komt als bijlage bij het dossieritem | Het rapport legt **zelf** vast welke gegevensverzamelingen het gebruikt — het type dossieritem hoeft ze niet beschikbaar te stellen |

> **De rapportkeuze in de workflow wordt niet gefilterd.** De behandelaar kiest uit de volledige lijst rapporten, ongeacht in welke workflow hij zit. De naam moet daarom op zichzelf herkenbaar zijn. Noteer de voorgestelde naam altijd expliciet in de output.

> **Rapport of document?** Een rapport wordt alleen getoond en bewaard. Moet het stuk bewerkt of ondertekend worden, dan is het een document en valt het onder `documentsjabloon`. Noemt het ontwerp dat onderscheid niet, dan is dat een beslispunt.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **Rapport** | rapport, rapportage, standaardrapport |
| **Rapportlayout** | rapportlayout, layout, afdruklayout |
| **Rapport in workflow** | workflow-editor, rapport genereren, als bijlage toevoegen |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Afdrukken of uitvoeren** | "de gebruiker drukt het overzicht af" |
| **Nieuwe velden in rapportage** | "veld X moet ook in het rapport" |
| **Controle- of verantwoordingsbehoefte** | "de accountant moet kunnen aantonen…" |
| **Periodieke output** | "maandelijks wordt een overzicht opgeleverd" |
| **Uitgebreidere route dan het scherm** | "de stamkaart toont alleen het hoofddienstverband; het rapport toont alles" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Rapportnaam** | De exacte naam zoals die in de keuzelijst komt te staan |
| **Soort** | `afdrukrapport` / `rapport in de workflow` |
| **Kanaal** | Profit / InSite / OutSite |
| **Vindplaats** | Menupad, of de workflow en de stap waarin hij wordt gekozen |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `controleren` |
| **Velden/gegevens** | Welke gegevens erop staan, of `nader te bepalen` |
| **Gegevensbron** | Gegevensverzameling waarop het rapport rust, of `nader te bepalen` |
| **Resultaat** | Wat er met de uitvoer gebeurt: afdruk, pdf, bijlage bij het dossieritem |
| **Doelgroep** | Voor wie het rapport bedoeld is |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Technische performance en query-optimalisatie
- Klantspecifieke maatwerkrapportages
- Analyses en gegevensverzamelingen (valt onder skill `analyses`)
- Documenten en brieven (valt onder skill `documentsjabloon`)
- Weergaven (valt onder skill `weergaven`) en boekingslayouts (valt onder skill `boekingslayouts`)
- De workflowstap waarin het rapport wordt gegenereerd (valt onder skill `workflow-condities`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Wordt een bestaand rapport uitgebreid of komt er een nieuw rapport?
- Is het een rapport of een document, en moet het stuk bewerkt kunnen worden?
- Welke naam krijgt het rapport, zodat het in de ongefilterde keuzelijst herkenbaar is?
- Welke velden uit de gegevensverzameling staan daadwerkelijk op het rapport?
- Voor welke doelgroep leveren we het rapport standaard uit?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Welk rapport gebruik je waarvoor?"**
- **"Waar vind ik het?"** — menupad of workflowstap
- **"Welke gegevens staan erin?"**

---

## Kwaliteitscriteria

- [ ] Per rapport is het soort bepaald: afdrukrapport of rapport in de workflow
- [ ] Bij een rapport in de workflow is de naam expliciet voorgesteld
- [ ] Elk rapport heeft kanaal, vindplaats en doelgroep
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Menupad voor rapportbeheer in Profit
- Onderscheid tussen rapport, rapportlayout en afdrukvorm
- Welke rapporten standaard worden uitgeleverd
