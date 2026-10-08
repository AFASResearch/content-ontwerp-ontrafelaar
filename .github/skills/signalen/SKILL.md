---
name: signalen
description: 'Breng de signaal-impact van een ontwerp in kaart en richt de signaaldefinitie in Profit in: gegevensverzameling met filter-, vergelijkings- en weergavevelden, signaaltype en verloop, naam, signaaltekst, gebruikerstoelichting, autorisatie, bestemming, workflow en e-mail. Gebruik bij vragen als: welke signalen zijn nodig, welk signaaltype kies ik, hoe schrijf ik de signaaltekst, welke velden heb ik nodig in de gegevensverzameling, maak de signaaldefinitie-paragraaf, signaal-impact, nieuw signaal, gewijzigd signaal, signalering in Profit.'
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

Let in het bijzonder op ontwerpen waarin een waarde op een **laag niveau** wordt overgenomen van een **hoger niveau** en daarna niet meer automatisch meeloopt. Dat levert vrijwel altijd een signaal op.

---

## Stap 2 - Per signaal de output invullen (Profit)

Lever per gevonden signaal een apart blok op met minimaal deze velden:

- **Vindplaats:** naam van het signaal (zie Stap 3 voor de naamconventie)
- **Nieuw/gewijzigd:** 1 zin met wat nieuw is of wijzigt
- **Gegevensverzameling:** nieuwe gegevensverzameling nodig ja/nee; noem ook de naam
- **Filtervelden:** welke velden de selectie bepalen, met de filterwaarde per veld
- **Vergelijkingsvelden:** welke twee velden tegen elkaar worden afgezet
- **Weergavevelden:** welke velden alleen dienen om de signaaltekst te vullen
- **Autorisatie:** autorisatie nodig ja/nee voor het signaal
- **Type signaal:** zie de beslisregel in Stap 4
- **Verloop:** wanneer het signaal verdwijnt
- **Vergelijkingswaarde:** `komt voor` / `komt niet voor` / `te weinig info` (met wat ontbreekt)
- **Signaaltekst:** de volledige tekst volgens de opzet in Stap 5
- **Gebruikerstoelichting:** de uitleg volgens de opzet in Stap 6
- **Bestemming:** wie het signaal moet ontvangen
- **Workflow:** moet het signaal een workflow starten ja/nee
- **Automatisch e-mailbericht:** moet het signaal automatisch een e-mailbericht versturen ja/nee
- **Benodigde talen:** in welke talen de signaaltekst nodig is (NL / ENG / DUI / FR), of `te weinig info`. Lever altijd de NL-brontekst; de vertalingen zelf worden uitgewerkt door de skill `vertalingen`, met de tags ongewijzigd
- **Bron (ontwerp):** hoofdstuk/§ + pagina + ankerzin/titel

Gebruik 1 item per signaal. Als een ontwerp meerdere signalen noemt, rapporteer ze los van elkaar.

### Velden hebben drie rollen

Splits de velden van de gegevensverzameling altijd in drie groepen. Zonder die driedeling vergeet je de tegenhanger van de vergelijking te koppelen en werkt het signaal niet.

| Rol | Waarvoor | Voorbeeld |
|-----|----------|-----------|
| **Filtervelden** | Bepalen welke records in de selectie vallen | `Synchroniseren = Ja`, `Afwijkend = Nee`, `Einddatum leeg of >= vandaag` |
| **Vergelijkingsvelden** | De eigenlijke trigger: twee waarden die ongelijk zijn | `Waarde laag niveau != Waarde hoog niveau` |
| **Weergavevelden** | Vullen alleen de signaaltekst | Naam, functie-omschrijving, werkgever, ingangsdatum |

Regels bij deze stap:

- **Toon omschrijvingen, geen codes.** Een codetabelcode zegt de ontvanger niets; neem het omschrijvingsveld op.
- **Sleutelvelden op niet-zichtbaar.** Volgnummers horen in de gegevensverzameling, niet in de tekst.
- **Veldcodes niet gokken.** Ken je de technische veldcode niet (bijvoorbeeld `U001`), zet dan `te weinig info` en zoek hem op in de omgeving.
- **Controleer of het vergelijkingsveld de actuele waarde ophaalt** en geen momentopname van het moment van aanmaken. Haalt het een momentopname op, dan vuurt het signaal nooit en merk je dat pas in productie.
- **Beschrijf welke records het filter uitsluit.** Filters op einddatum of scope bepalen wat de ontvanger níet ziet; dat hoort terug in de gebruikerstoelichting.

---

## Stap 3 - Naam van het signaal

Gebruik deze opbouw:

> `[module of koppeling]: [wat] [wie] wijkt af van [waarvan]`

Bijvoorbeeld: `Nedap ONS: weekkaartprofiel medewerker wijkt af van werkgever/functie`.

Regels:

- **Noem altijd wie afwijkt én waarvan.** Zonder beide helften moet de ontvanger de tekst openen om te snappen waar het over gaat.
- **Gebruik een gedeeld voorvoegsel** als meerdere signalen bij dezelfde functionaliteit horen. Ze staan dan bij elkaar in de signalenlijst.
- **Gebruik geen woord dat ook een veldnaam is**, tenzij het signaal precies over dat veld gaat. Een titel met "Afwijkend weekkaartprofiel" is fout als het signaal juist afgaat terwijl dat veld op Nee staat.
- **Vermijd vage woorden als "standaard".** Noem het object dat de ontvanger in Profit ziet, zoals `werkgever/functie`.

---

## Stap 4 - Kies het signaaltype

Profit kent vier typen. Gebruik deze beslisregel:

| Type | Kies dit als | Let op |
|------|--------------|--------|
| **Gegevens, standaard verloop (S)** | De trigger is een gegevensvergelijking én de regel valt na correctie vanzelf uit de gegevensverzameling | Standaardkeuze bij afwijkingssignalen |
| **Gegevens, afwijkend verloop (A)** | Het signaal moet blijven staan nadat de regel uit de selectie verdwijnt, of moet verlopen op een ándere voorwaarde dan de trigger | Vereist een apart verloopfilter; alleen gebruiken als dat echt nodig is |
| **Op datum (D)** | Een peildatum zet het signaal aan, los van gegevensverschillen | Een datum die alleen in het filter zit is géén reden voor dit type |
| **Op repetering (R)** | Het signaal moet met een vaste frequentie terugkeren | Niet gebruiken voor afwijkingen: die wil je zien zodra ze ontstaan |

Noteer altijd expliciet **wanneer het signaal verloopt**, ook als dat automatisch gaat.

---

## Stap 5 - Schrijf de signaaltekst

Een signaaltekst kun je **niet opmaken**: geen vet, geen koppen, geen opsommingstekens. Waarden uit codetabellen zijn vaak gewone woorden en verdwijnen daardoor in een lopende zin.

Gebruik daarom deze vaste opzet:

```
[Eén zin die zegt wat er aan de hand is.]

Label 1: {tag}
Label 2: {tag}
Label 3: {tag}
Waarde laag niveau: {tag}
Waarde hoog niveau: {tag}

[Wat de ontvanger moet doen, met beide geldige uitkomsten.]
```

Regels:

- **Zet de twee vergeleken waarden onder elkaar**, als laatste twee labelregels. Het verschil springt er dan uit.
- **Labels op aparte regels**, waarden erachter. Geen lopende zin met ingebedde tags.
- **Lukken regeleinden niet?** Zet de waarden dan tussen aanhalingstekens in de lopende zin. Test dat met een lange codetabelwaarde voordat je ervoor kiest.
- **Tags vertaal of wijzig je nooit**, ook niet als de tagnaam een typefout bevat. De tag moet overeenkomen met het veld in de gegevensverzameling. Signaleer de typefout apart.
- **Noem geen datum in de actie die in het verleden ligt.** Een ingangsdatum is context, geen instructie.
- Pas de skill `schrijfwijzer` toe: B1, actief, tweede persoon, korte zinnen.

### Call-to-action: altijd twee uitkomsten

Bij een afwijkingssignaal zijn er meestal twee correcte uitkomsten. Benoem ze allebei, anders gaan ontvangers onterecht corrigeren:

1. De afwijking is onbedoeld → corrigeer de waarde.
2. De afwijking is bewust → leg vast dát het bewust is.

**Controleer of de voorgestelde actie uitvoerbaar is.** Is het veld op dat niveau alleen-lezen, dan is "pas het veld aan" een onmogelijke instructie. Verifieer dit in de omgeving en niet alleen in het ontwerp: een ontwerp kan een veld read-only noemen terwijl het in de praktijk wijzigbaar is. Wijkt de omgeving af van het ontwerp, meld dat als beslispunt.

---

## Stap 6 - Schrijf de gebruikerstoelichting

Lever naast de signaaltekst altijd een toelichting voor wie het signaal inhoudelijk wil snappen. Houd deze vaste opbouw aan, elk onderdeel in één of twee zinnen:

1. **Wat laat dit signaal zien?** De afwijking in één zin.
2. **Hoe ontstaat dit?** De oorzaak, meestal een wijziging die niet doorwerkt.
3. **Welke records zie je hier?** Wat de filters in- en uitsluiten. Overslaan mag niet als een filter records wegfiltert.
4. **Waarom is dit belangrijk?** Het gevolg als je niets doet.
5. **Wat doe je ermee?** Beide uitkomsten uit Stap 5, plus wanneer het signaal verdwijnt.

Houd de toelichting onder de 120 woorden. Is hij langer, schrap dan de opsomming van triggervoorwaarden: die leidt af van de actie.

---

## Stap 7 - Toets: kan de ontvanger het signaal wegkrijgen?

Loop deze toets **altijd** langs voordat je een signaal voorstelt.

Bestaat er een manier om vast te leggen dat een afwijking bewust is (bijvoorbeeld een afwijken-toggle)? Zo niet, dan levert elke legitieme uitzondering een **permanent signaal** op dat de ontvanger nooit kan wegkrijgen zonder de uitzondering ongedaan te maken.

Is dat het geval, kies dan uit:

| Optie | Wat je doet | Nadeel |
|-------|-------------|--------|
| Afwijken-toggle toevoegen | Nieuw veld dat de bewuste afwijking vastlegt | Ontwerpwijziging; leg voor aan de ontwerper |
| Afwijkend verloop (A) | Ontvanger sluit het signaal handmatig af | Komt terug tenzij het verloopfilter dat afvangt |
| Signaal schrappen | Dit verschil niet signaleren | Je mist onbedoelde afwijkingen |

Leg de uitkomst vast als beslispunt. Signaleer ook expliciet als twee signalen in hetzelfde ontwerp hierin verschillen.

---

## Stap 8 - Bronverwijzing-regel (altijd toepassen)

Voeg bij **elk** signaal altijd **Bron (ontwerp)** toe in dit format:

> Hoofdstuk/§ ... | Pagina ... | (anker: "...")

Als hoofdstuk/pagina niet betrouwbaar beschikbaar is (bijvoorbeeld niet in de tekstlaag):

- vermeld dat expliciet;
- gebruik dan sectietitel of tekstfragment als anker.

---

## Stap 9 - Beslispunten (altijd opnemen)

Neem minimaal 1 beslispunt op. Neem in elk geval op wat je in de stappen hierboven niet hard kon maken:

- Hoe heet het signaal in de Signaaldefinitie?
- Klopt het gekozen signaaltype, zeker bij datum- of scopefilters?
- Kan de ontvanger een bewuste afwijking vastleggen? (uitkomst van Stap 7)
- Is autorisatie nodig voor het signaal?
- Wat is de bestemming: alleen Profit of ook per e-mail?
- Eén gedeelde gegevensverzameling voor meerdere signalen, of één per signaal?
- Geldt er een conditie, bijvoorbeeld dat het signaal alleen actief is na activering van een koppeling?
- Wijkt de omgeving af van het ontwerp (read-only, veldnamen, extra velden)?

---

## Stap 10 - Buiten scope (altijd opnemen)

Benoem onderstaande onderwerpen expliciet als buiten scope:

- Technische IAM/SSO/IdP/AD-inrichting
- Licenties/abonnementen
- Backend/database-autorisaties die niet als menu/tab/rol zichtbaar zijn
- Teksten van e-mails/berichten, tenzij het ontwerp expliciet een sjabloon of rol wijzigt
- De vertalingen zelf; die lopen via de skill `vertalingen`

---

## Stap 11 - Content (altijd apart opnemen)

Neem aan het eind altijd een aparte sectie **Content** op met minimaal deze vragen:

- Welk signaal moet je toevoegen? (naam)
- Is een nieuwe gegevensverzameling nodig? (ja/nee)
- Is autorisatie nodig? (ja/nee)
- Wat is het type signaal en wanneer verloopt het?
- Kan de ontvanger het signaal wegkrijgen? (ja/nee + hoe)

---

## Aanbevolen outputsjabloon

### Signaal 1 - [Naam volgens Stap 3]

- Nieuw/gewijzigd: ...
- Gegevensverzameling: ...
- Filtervelden: ...
- Vergelijkingsvelden: ...
- Weergavevelden: ...
- Autorisatie: ...
- Type signaal: ...
- Verloop: ...
- Vergelijkingswaarde: ...
- Bestemming: ...
- Workflow: ...
- Automatisch e-mailbericht: ...
- Benodigde talen: ...
- Bron (ontwerp): Hoofdstuk/§ ... | Pagina ... | (anker: "...")

**Signaaltekst**

> [tekst volgens Stap 5]

**Gebruikerstoelichting**

> [tekst volgens Stap 6]

### Beslispunten

- ...

### Buiten scope

- ...

### Content

- Welk signaal moet je toevoegen? (naam)
- Is een nieuwe gegevensverzameling nodig? (ja/nee)
- Is autorisatie nodig? (ja/nee)
- Wat is het type signaal en wanneer verloopt het?
- Kan de ontvanger het signaal wegkrijgen? (ja/nee + hoe)

---

## Kwaliteitscriteria

- [ ] Elk signaal heeft filtervelden, vergelijkingsvelden en weergavevelden apart benoemd
- [ ] Het vergelijkingsveld haalt aantoonbaar de actuele waarde op
- [ ] De naam noemt wie afwijkt én waarvan, en botst niet met een veldnaam
- [ ] Het signaaltype is onderbouwd en het verloopmoment staat erbij
- [ ] De signaaltekst gebruikt labels op aparte regels en toont beide waarden onder elkaar
- [ ] De call-to-action noemt beide geldige uitkomsten en is uitvoerbaar op dat niveau
- [ ] De gebruikerstoelichting benoemt welke records het filter uitsluit
- [ ] De toets uit Stap 7 is uitgevoerd en vastgelegd
- [ ] Tags staan ongewijzigd en zijn doorgezet naar de skill `vertalingen`
- [ ] `te weinig info` geeft aan wat ontbreekt
