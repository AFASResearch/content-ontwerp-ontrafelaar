---
name: signalen
description: 'Breng de signaal-impact van een ontwerp in kaart: welke nieuwe of gewijzigde signalen nodig zijn en hoe de signaaldefinitie in Profit moet worden ingericht (gegevensverzameling, autorisatie, type, bestemming, workflow en e-mail). Gebruik bij vragen als: welke signalen zijn nodig, maak de signaaldefinitie-paragraaf, signaal-impact, nieuw signaal, gewijzigd signaal, signalering in Profit.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Signalen-analyse (Signaaldefinitie)

## Doel

Volledig in kaart brengen welke **signaal-impact** een ontwerp veroorzaakt voor **Signaaldefinitie** in Profit.

Het gaat specifiek om nieuwe of gewijzigde signalen die functioneel nodig zijn door nieuwe/gewijzigde functionaliteit.

---

## Stap 1 - Scan het ontwerp: wat zoek je?

Markeer als signaal-impact wanneer je een aanwijzing ziet voor een **nieuw signaal** in Profit, bijvoorbeeld in de richting:

- **Algemeen > ... > ...**

Herken signalen zowel expliciet (het woord "signaal" staat genoemd) als impliciet (een proces vraagt om automatische signalering).

---

## Stap 2 - Per signaal de output invullen (Profit)

Lever per gevonden signaal een apart blok of een aparte tabelrij op met minimaal deze velden:

- **Gegevensverzameling:** nieuwe gegevensverzameling nodig ja/nee; noem ook de naam van de gegevensverzameling
- **Autorisatie:** autorisatie nodig ja/nee voor het signaal
- **Vindplaats:** naam van het signaal
- **Nieuw/gewijzigd:** 1 zin met wat nieuw is of wijzigt
- **Type signaal:** op datum, op gegevens of repeterend
- **Vergelijkingswaarde:** komt voor / komt niet voor / te weinig info (met wat ontbreekt)
- **Signaaltekst:** voorbeeld van een signaaltekst
- **Bestemming:** wie het signaal moet ontvangen
- **Workflow:** moet het signaal een workflow starten ja/nee
- **Automatisch e-mailbericht:** moet het signaal automatisch een e-mailbericht versturen ja/nee
- **Benodigde talen:** in welke talen de signaaltekst nodig is (NL / ENG / DUI / FR), of `te weinig info`. Lever altijd de NL-brontekst; de vertalingen zelf worden uitgewerkt door de skill `vertalingen`
- **Bron (ontwerp):** hoofdstuk/§ + pagina + ankerzin/titel

Gebruik 1 item per signaal. Als een ontwerp meerdere signalen noemt, rapporteer ze los van elkaar.

---

## Stap 3 - Bronverwijzing-regel (altijd toepassen)

Voeg bij **elk** signaal altijd **Bron (ontwerp)** toe in dit format:

> Hoofdstuk/§ ... | Pagina ... | (anker: "...")

Als hoofdstuk/pagina niet betrouwbaar beschikbaar is (bijvoorbeeld niet in de tekstlaag):

- vermeld dat expliciet;
- gebruik dan sectietitel of tekstfragment als anker.

---

## Stap 4 - Beslispunten (altijd opnemen)

Neem minimaal 1 beslispunt op. Gebruik bijvoorbeeld:

- Moet een signaal worden toegevoegd?
- Is autorisatie nodig voor het signaal?
- Wat is de bestemming van het signaal?

---

## Stap 5 - Buiten scope (altijd opnemen)

Benoem onderstaande onderwerpen expliciet als buiten scope:

- Technische IAM/SSO/IdP/AD-inrichting
- Licenties/abonnementen
- Backend/database-autorisaties die niet als menu/tab/rol zichtbaar zijn
- Teksten van e-mails/berichten, tenzij het ontwerp expliciet een sjabloon of rol wijzigt

---

## Stap 6 - Content (altijd apart opnemen)

Neem aan het eind altijd een aparte sectie **Content** op met minimaal deze vragen:

- Welk signaal moet je toevoegen? (naam)
- Is een nieuwe gegevensverzameling nodig? (ja/nee)
- Is autorisatie nodig? (ja/nee)
- Wat is het type signaal? (op datum, op gegevens of repeterend)

---

## Aanbevolen outputsjabloon

Gebruik bij voorkeur deze structuur:

### Signaal 1 - [Naam]

- Gegevensverzameling: ...
- Autorisatie: ...
- Vindplaats: ...
- Nieuw/gewijzigd: ...
- Type signaal: ...
- Vergelijkingswaarde: ...
- Signaaltekst: ...
- Bestemming: ...
- Workflow: ...
- Automatisch e-mailbericht: ...
- Benodigde talen: ...
- Bron (ontwerp): Hoofdstuk/§ ... | Pagina ... | (anker: "...")

### Beslispunten

- ...

### Buiten scope

- ...

### Content

- Welk signaal moet je toevoegen? (naam)
- Is een nieuwe gegevensverzameling nodig? (ja/nee)
- Is autorisatie nodig? (ja/nee)
- Wat is het type signaal? (op datum, op gegevens of repeterend)
