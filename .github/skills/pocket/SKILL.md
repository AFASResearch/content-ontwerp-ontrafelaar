---
name: pocket
description: 'Bepaal of een ontwerp daadwerkelijke Pocket-functionaliteit introduceert of wijzigt en of die geautoriseerd moet worden op rollen of gebruikersgroepen. Een simpele vermelding van Pocket is niet genoeg; alleen een echte wijziging van de app-functionaliteit telt mee. Pocket zelf ontwikkelen wij niet. Gebruik bij vragen als: heeft dit impact op Pocket, Pocket-app, mobiele app, Pocket-functionaliteit, Pocket autoriseren.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Pocket-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Wijzigt het ontwerp de Pocket-functionaliteit echt?**
2. **Zo ja: welke functionaliteit komt er in Pocket?**
3. **Moet die functionaliteit geautoriseerd worden op rollen of gebruikersgroepen?**

> **Alleen echte Pocket-functionaliteitswijzigingen tellen mee.** Een korte vermelding van Pocket, of een verwijzing zonder feitelijke app-impact, is geen contenttaak. Wij ontwikkelen Pocket niet. Onze taak beperkt zich tot: vaststellen of er nieuwe of gewijzigde functionaliteit in de app ontstaat, hoe die geautoriseerd wordt, en welke inrichting daarvoor nodig is.

---

## Stap 1 — Wijzigt de Pocket-functionaliteit?

Begin bij `komt niet voor in ontwerp`. Wijk daar alleen van af als het ontwerp aantoonbaar maakt dat Pocket een nieuwe of gewijzigde functionaliteit krijgt.

Een vermelding van Pocket zonder feitelijke app-impact is geen werkitem. Als het ontwerp alleen zegt dat Pocket iets kan zien of dat het een raakvlak is, maar niet dat de app-functionaliteit verandert of uitgebreid wordt, blijft de uitkomst `komt niet voor in ontwerp`.

### A) Harde trigger

| Term | Varianten |
|------|-----------|
| **Pocket** | Pocket, AFAS Pocket, app |
| **Mobiel** | mobiel, mobiele app, smartphone, telefoon |
| **Pushmelding** | pushmelding, notificatie op de telefoon |

### B) Impliciete signalen

Deze signalen zijn **geen bewijs** dat Pocket in scope is, maar wel een reden om het na te vragen:

| Signaal | Voorbeelden |
|---------|-------------|
| **Proces dat onderweg wordt uitgevoerd** | verlof aanvragen, declaratie indienen, uren boeken |
| **Goedkeuring door leidinggevende** | workflowtaken die vaak mobiel worden afgehandeld |
| **Foto of bijlage vanaf de telefoon** | "de gebruiker maakt een foto van de bon" |

Bij alleen een impliciet signaal: `te weinig info` + vraag aan de ontwerper of de functionaliteit ook naar Pocket komt. Stel nooit zelf vast dat iets in Pocket beschikbaar is.

---

## Stap 2 — Output per Pocket-onderdeel

| Veld | Inhoud |
|------|--------|
| **Onderdeel** | De functionaliteit, het scherm of het proces in Pocket |
| **Benoemd in ontwerp** | ja (expliciet) / nee / alleen impliciet |
| **Beschikbaar in Pocket** | ja / nee / `te weinig info` |
| **Wat kan de gebruiker doen** | Welke handeling de app ondersteunt, in één zin |
| **Autorisatie nodig** | ja / nee / `te weinig info` |
| **Rollen of gebruikers** | Aan welke rollen of gebruikers we koppelen; uitwerking via skill `autorisatie-en-functionaliteiten` |
| **Benodigde inrichting** | Wat aan moet staan voordat het in Pocket werkt |
| **Pushmelding** | ja / nee / `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Regels:

- **"Beschikbaar in Pocket" beantwoord je altijd expliciet.** Laat dit veld nooit leeg.
- **Autorisatie is de kerntaak.** Komt er functionaliteit in Pocket, bepaal dan altijd of die op rollen of gebruikersgroepen geautoriseerd moet worden, en zet de uitwerking door naar de skill `autorisatie-en-functionaliteiten`.
- **Noemt het ontwerp geen rollen of gebruikersgroepen**, dan is dat een beslispunt. Vul nooit zelf rollen in zonder dat te markeren.
- **Geen bouwtaak voor ons.** Schrijf nooit op dat wij een Pocket-scherm maken of wijzigen.
- **Komt de functionaliteit in InSite én Pocket?** Benoem beide routes; ze kunnen verschillende rollen hebben.
- **Alleen echte functionaliteitswijzigingen tellen.** Een vermelding van Pocket zonder wijziging van de app-functionaliteit is geen Ja.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Het ontwikkelen van de Pocket-app en de schermen daarin
- App-store releases en technische app-versies
- Apparaatbeheer en MDM
- De uitwerking van de autorisatie zelf (valt onder skill `autorisatie-en-functionaliteiten`)
- Profielen en veldcontexten (valt onder skill `profielen-en-veldcontexten`)
- De InSite-pagina's achter hetzelfde proces (valt onder skill `portalpagina-insite`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

- Verandert de app-functionaliteit echt, of is Pocket alleen ter mentionatie genoemd?
- Komt de functionaliteit ook naar Pocket, of alleen naar InSite?
- Moet de Pocket-functionaliteit geautoriseerd worden, en zo ja op welke rollen of gebruikersgroepen?
- Is een pushmelding gewenst?
- Welke inrichting moet de klant doen voordat het in Pocket werkt?

---

## Stap 6 — Content (altijd apart opnemen)

- **"Wat kun je in Pocket doen?"**
- **"Waar vind je het in de app?"**
- **"Wie mag dit?"** — de rollen
- **"Wat moet ingericht zijn?"**

---

## Kwaliteitscriteria

- [ ] Er staat expliciet of Pocket in het ontwerp benoemd wordt
- [ ] Voor elk onderdeel is "beschikbaar in Pocket" expliciet beantwoord
- [ ] Voor elk onderdeel is beantwoord of autorisatie nodig is, en op welke rollen of gebruikers
- [ ] Ontbrekende rollen staan als beslispunt, niet zelf ingevuld
- [ ] Er staat geen bouwtaak voor ons in de app zelf
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt
