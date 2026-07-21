---
name: schrijfwijzer
description: 'Herschrijf en verbeter Nederlandse outputteksten volgens de AFAS-schrijfwijzer (AKTO/piramide, B1, klantgericht, servicegericht, actief en concreet). Gebruik bij vragen als: herschrijf deze tekst, maak dit klantgerichter, maak dit scanbaar, redigeer op B1-niveau, verbeter toon en call-to-action, geef schrijftips voor vervolgteksten.'
argument-hint: 'Plak de brontekst en noem doel, doelgroep, kanaal en gewenste actie'
---

# Schrijfwijzer

## Doel

Lever een verbeterde Nederlandse tekst op die:

1. Snel scanbaar is volgens AKTO/piramide-opbouw.
2. Klant- en servicegericht is op taalniveau B1.
3. Activerend, concreet en positief is.
4. Zo min mogelijk opvulling bevat.

Geef naast de herschreven tekst altijd korte, toepasbare schrijftips voor toekomstige teksten.

---

## Wanneer gebruiken

Gebruik deze skill bij alle schrijf- en redactieverzoeken, zoals:

- Herschrijven van e-mails, toelichtingen, meldingen, handleidingtekst of webcopy.
- Verbeteren van toon, duidelijkheid, structuur of klantgerichtheid.
- Omzetten van lange/ingewikkelde tekst naar scanbare B1-tekst.
- Aanscherpen van call-to-action, deadline en klantvoordeel.

Gebruik deze skill niet voor:

- Juridisch bindende herformuleringen waarbij exacte terminologie verplicht is.
- Vertalingen tussen talen (alleen Nederlandstalige kwaliteitsverbetering).

---

## Verplichte afstemming met andere skills

Als de input afkomstig is uit skill-output (zoals autorisatie- of informatiebolletje-analyses), dan gelden deze extra regels altijd:

1. Behoud de inhoudelijke structuur van de bron.
2. Laat vaste labels, statussen en veldnamen ongewijzigd.
3. Herschrijf voor helderheid, maar wijzig geen classificaties of besluiten.

Concreet:

- Koppen en blokvolgorde blijven gelijk, tenzij expliciet anders gevraagd.
- Tabellen blijven tabellen met dezelfde kolomnamen.
- Waarden zoals `komt voor`, `komt niet voor`, `te weinig info` blijven exact gelijk.
- Bronverwijzingen blijven in hetzelfde format (bijv. `Hoofdstuk/§ ... | Pagina ... | (anker: "...")`).
- Domeintermen zoals Profit, InSite, OutSite, autorisatiegroep, functionaliteit, informatiebolletje en veldinfo blijven behouden.
- Buiten scope, Beslispunten en Content-blokken blijven als aparte blokken bestaan als ze in de brontekst staan.

Doel bij skill-op-skill redactie:

- Wel verbeteren: leesbaarheid, zinslengte, actieve formulering, scanbaarheid.
- Niet veranderen: betekenis, scope-afbakening, statuswaarden, brondata, checklistuitkomst.

---

## Benodigde input

Vraag om ontbrekende context als die nodig is voor kwaliteit:

- Doel van de tekst.
- Doelgroep (klant/prospect/intern).
- Kanaal (e-mail, InSite, OutSite, documentatie, etc.).
- Gewenste actie van de lezer.
- Eventuele harde randvoorwaarden (max lengte, verplichte termen, deadlines).

Als context ontbreekt, maak redelijke aannames en noem ze kort.

---

## Werkwijze

### Stap 1 - Bepaal tekstdoel en hoofdboodschap

1. Vat in 1 zin samen wat de kernboodschap is.
2. Bepaal welke actie de lezer moet uitvoeren.
3. Schrap irrelevante of dubbele informatie.

### Stap 2 - Zet de structuur in AKTO/piramide

Bouw de tekst in maximaal vier delen op:

1. **Aansluiting**: aanleiding en opbrengst voor de lezer.
2. **Kern**: hoofdboodschap zo vroeg mogelijk.
3. **Toelichting**: alleen noodzakelijke extra uitleg.
4. **Onderbouwing**: relevante achtergrond als het echt helpt.

### Stap 3 - Verbeter stijl en taal

Pas deze regels toe:

- Schrijf op B1-niveau.
- Schrijf actief en direct.
- Vermijd vaktaal waar een gewone term kan.
- Gebruik moderne, positieve formuleringen.
- Vermijd de woorden `even`, `kunnen`, `zullen` en overmatig `worden` waar dat de zin zwakker maakt.
- Gebruik gebiedende wijs als je actie wilt uitlokken.

### Stap 4 - Maak de tekst scanbaar

- Gebruik duidelijke koppen boven kernalinea's.
- Houd 1 onderwerp per alinea.
- Gebruik opsommingstekens voor lijsten.
- Geef korte zinnen de voorkeur (richtlijn: gemiddeld circa 10 woorden).
- Wissel korte en langere zinnen af als dat natuurlijk leest.
- Cluster inhoud die logisch bij elkaar hoort.

### Stap 5 - Versterk inhoudelijke overtuigingskracht

Gebruik alleen als passend voor het doel:

- Sociale bewijskracht (bijv. klanttevredenheidsscore).
- Autoriteit (ervaring, innovatie, relevante klanten, expertise).
- Concreetheid (voorbeelden, schermpad, deadline, vervolgstap).

Verwerk waar mogelijk SUCCES-principes:

- Simple
- Unexpected
- Concrete
- Credible
- Empathie
- Story

### Stap 6 - Kwaliteitscontrole voor oplevering

Controleer:

- [ ] De kernboodschap staat vroeg in de tekst.
- [ ] De structuur volgt AKTO (of een beargumenteerde compacte variant).
- [ ] Er staat een duidelijke call-to-action met wat, wanneer en waarom.
- [ ] De tekst is scanbaar (koppen/alinea's/opsomming waar zinvol).
- [ ] Opvulling en doublures zijn verwijderd.
- [ ] Toon is klant- en servicegericht.
- [ ] Bij skill-output zijn structuur, labels, statuswaarden en bronnotatie intact gebleven.

---

## Beslispunten (branching)

Pas de output aan op basis van dit beslisschema:

1. **Moet de lezer iets doen?**
Ja: sluit af met expliciete actie, deadline en voordeel.
Nee: sluit af met heldere verwachting of vervolginformatie.

2. **Is de tekst lang of complex?**
Ja: gebruik volledige AKTO met tussenkoppen.
Nee: gebruik compacte AKTO met 1-2 korte alinea's en eventueel bullets.

3. **Is vakinhoud onvermijdelijk?**
Ja: leg jargon direct uit in eenvoudige woorden.
Nee: vervang jargon volledig door alledaagse taal.

4. **Is overtuiging nodig?**
Ja: voeg relevante bewijskracht/autoriteit toe.
Nee: houd de tekst feitelijk en kort.

---

## Outputformat

Lever altijd in deze volgorde:

1. **Herschreven tekst**
2. **Belangrijkste verbeteringen (kort)**: 3-7 concrete punten.
3. **Tips voor volgende teksten**: 3-5 direct toepasbare tips.
4. **Aannames** (alleen indien gebruikt).

---

## Speciale regels

- Behoud feitelijke inhoud; verander geen betekenis zonder dit te benoemen.
- Verzin geen cijfers, klantcases of claims.
- Als AFAS-boilerplate gevraagd wordt, gebruik exact de aangeleverde boilerplate.
- Als de bron te onduidelijk is, stel eerst 1-3 gerichte verduidelijkingsvragen.