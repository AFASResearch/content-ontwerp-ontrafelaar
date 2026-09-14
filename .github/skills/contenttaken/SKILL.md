---
name: contenttaken
description: 'Maak een overzichtelijke samenvatting van alle relevante contenttaken in een ontwerp. Controleer per geregistreerde skill of die voorkomt, wat er concreet nodig is bij het project en geef een copy-pasteklare output voor Word en OneNote.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Contenttaken

## Doel

Maak een overkoepelend inhoudelijk overzicht van alle contenttaken die in een functioneel ontwerp relevant zijn. De analyse werkt per registrerende skill en bepaalt per skill of die wel of niet voorkomt in het ontwerp.

De output is geschreven om direct te kunnen worden geplakt in Word of OneNote. Gebruik dus geen tabellen, geen complexe markdown-structuur en geen afkortingen die alleen in het systeem werken. Gebruik duidelijke, platte koppen en bullets.

---

## Gedrag van deze skill

1. Lees het ontwerp volledig en controleer per geregistreerde skill of die relevant is.
2. Geef voor elke skill een eigen samenvatting.
3. Als een skill voorkomt in het ontwerp, beschrijf je concreet welke content- of inrichtingstaken nodig zijn bij dit project.
4. Als een skill niet voorkomt, vermeld je dat expliciet en noteer je dat er voor deze skill geen contenttaken zijn vastgesteld.
5. Als de informatie ontbreekt, noteer je dat expliciet als `te weinig info` en noem je wat ontbreekt.
6. Gebruik altijd een bronverwijzing naar het ontwerp, bij voorkeur met hoofdstuk/§ | pagina | anker.
7. Houd de tekst kort, concreet en direct kopieerbaar.

---

## Geregistreerde skills die gecontroleerd worden

Controleer deze skills altijd in deze volgorde:

- analyses
- autorisatie
- berichtenjabloon
- boekingslayouts
- documentsjabloon
- icoontjes
- informatiebolletje
- paginas-outsite
- pocket
- portalpagina-insite
- profielen-en-veldcontexten
- rapporten
- schrijfwijzer
- signalen
- vertalingen
- weergaven
- workflow-condities

---

## Status die je gebruikt

Gebruik exact deze statuslabels:

- komt voor in ontwerp
- komt niet voor in ontwerp
- te weinig info

---

## Outputvorm voor Word en OneNote

Gebruik GEEN markdown-tabel. Gebruik deze strak geplakte structuur:

Skill: [naam van de skill]
Status: [komt voor in ontwerp / komt niet voor in ontwerp / te weinig info]
Samenvatting:
[1 tot 3 zinnen over wat er in het ontwerp relevant is of niet is]
Concrete contenttaken:
- [voornaamste taak 1]
- [voornaamste taak 2]
- [voornaamste taak 3]
Bronvermelding:
[hoofdstuk/§ | pagina | (anker: "...")]

Herhaal dit voor elke skill.

---

## Verwerking per skill

### 1. Als een skill voorkomt in het ontwerp

Schrijf een heldere en concrete samenvatting. Geef geen algemene uitleg, maar beschrijf wat het project precies moet doen.

Voorbeelden van concreet gedrag:

- benoem welke velden, pagina's, teksten, workflows, rapporten of rollen relevant zijn
- noem of iets nieuw is, aangepast moet worden of gecontroleerd moet worden
- benoem bij voorkeur de exacte content die nodig is, zoals:
  - tekst voor een informatiebolletje
  - naam van een rapport of documenttemplate
  - label of regel voor een berichtsjabloon
  - benodigde weergavekolommen of filters
  - velden die zichtbaar, verplicht of afgeschermd moeten worden
  - menu-item, knop of pagina die een icoon nodig heeft

Gebruik deze vaste formulering:

Samenvatting:
De skill [naam] komt voor in het ontwerp. Het project moet [korte, concrete beschrijving van de relevante inhoud].

Concrete contenttaken:
- [taak 1]
- [taak 2]
- [taak 3]

Bronvermelding:
[hoofdstuk/§ | pagina | (anker: "...")]

### 2. Als een skill niet voorkomt in het ontwerp

Gebruik deze formulering:

Samenvatting:
Deze skill komt niet voor in het ontwerp. Er is geen relevante content-, inrichting- of verificatietaak voor dit project vastgesteld.

Concrete contenttaken:
- Geen relevante taken vastgesteld

Bronvermelding:
[hoofdstuk/§ | pagina | (anker: "...")]

### 3. Als de informatie onvoldoende is

Gebruik deze formulering:

Samenvatting:
Deze skill is niet met zekerheid vast te stellen uit het ontwerp. De benodigde informatie ontbreekt op dit moment.

Concrete contenttaken:
- Verduidelijking nodig: [specifiek ontbrekende informatie]
- Controle nodig: [wat precies moet nog worden nagevraagd]

Bronvermelding:
[hoofdstuk/§ | pagina | (anker: "...")]

---

## Kwaliteitscriteria

- Er is voor elke geregistreerde skill een onderdeel.
- Elke skill heeft een status.
- Elke skill heeft een korte, concrete samenvatting.
- Bij een relevante skill staan concrete taken in bullets.
- Bij een niet-relevante skill staat expliciet dat er geen inhoudelijke taak is vastgesteld.
- Bij onzekerheid staat expliciet wat ontbreekt.
- Er staat een bronverwijzing bij elk item.
- De output is direct plaktbaar in Word en OneNote.

---

## Voorbeeldoutput

Skill: informatiebolletje
Status: komt voor in ontwerp
Samenvatting:
De skill informatiebolletje komt voor in het ontwerp. Het project moet veldtoelichtingen opzetten voor de relevante velden en de juiste inhoud per velduitwerking vastleggen.
Concrete contenttaken:
- Bepalen welke velden een informatiebolletje nodig hebben
- Tekst opstellen per informatiebolletje
- Controle of de tekst voldoet aan de bedrijfs- en gebruikersinstructies
Bronvermelding:
Hoofdstuk 3 | Pagina 12 | (anker: "Veldtoelichting bij invoervelden")

Skill: pocket
Status: komt niet voor in ontwerp
Samenvatting:
Deze skill komt niet voor in het ontwerp. Er is geen relevante Pocket-functionaliteit of mobiele contenttaak vastgesteld.
Concrete contenttaken:
- Geen relevante taken vastgesteld
Bronvermelding:
Hoofdstuk 5 | Pagina 18 | (anker: "Mobiele app impact")

---

## Belangrijk

Deze skill is een samenvatting en aggregatie-instrument. Het doel is niet om meer te verzinnen dan het ontwerp zegt, maar om per skill te bepalen of er wel of niet inhoudelijke contentwerkzaamheden zijn en zo concreet mogelijk te benoemen wat in het project gedaan moet worden.
