---
name: pocket
description: 'Bepaal of een ontwerp Pocket benoemt en wat dat voor ons betekent: welke functionaliteit in de AFAS Pocket-app beschikbaar komt en of die geautoriseerd moet worden op rollen of gebruikers. Pocket zelf ontwikkelen wij niet. Gebruik bij vragen als: heeft dit impact op Pocket, Pocket-app, mobiele app, Pocket-functionaliteit, Pocket autoriseren.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Pocket-analyse

## Doel

Deze skill beantwoordt drie vragen:

1. **Wordt Pocket benoemd in het ontwerp?**
2. **Zo ja: welke functionaliteit komt er in Pocket?**
3. **Moet die functionaliteit geautoriseerd worden op rollen of gebruikers?**

> **Wij ontwikkelen Pocket niet.** Er is dus nooit een bouwtaak voor ons in de app zelf. Onze taak beperkt zich tot: vaststellen wat er in Pocket beschikbaar komt, de autorisatie daarop, en de uitleg erover.

---

## Stap 1 — Wordt Pocket benoemd?

Begin bij `komt niet voor in ontwerp`. Wijk daar alleen van af als het ontwerp Pocket aantoonbaar noemt.

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
| **Rollen of gebruikers** | Aan welke rollen of gebruikers we koppelen; uitwerking via skill `autorisatie` |
| **Benodigde inrichting** | Wat aan moet staan voordat het in Pocket werkt |
| **Pushmelding** | ja / nee / `te weinig info` |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

Regels:

- **"Beschikbaar in Pocket" beantwoord je altijd expliciet.** Laat dit veld nooit leeg.
- **Autorisatie is de kerntaak.** Komt er functionaliteit in Pocket, bepaal dan altijd of die op rollen of gebruikers geautoriseerd moet worden, en zet de uitwerking door naar de skill `autorisatie`.
- **Noemt het ontwerp geen rollen**, dan is dat een beslispunt. Vul nooit zelf rollen in zonder dat te markeren.
- **Geen bouwtaak voor ons.** Schrijf nooit op dat wij een Pocket-scherm maken of wijzigen.
- **Komt de functionaliteit in InSite én Pocket?** Benoem beide routes; ze kunnen verschillende rollen hebben.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Is hoofdstuk of pagina niet betrouwbaar beschikbaar, vermeld dat expliciet en gebruik sectietitel of tekstfragment als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

- Het ontwikkelen van de Pocket-app en de schermen daarin
- App-store releases en technische app-versies
- Apparaatbeheer en MDM
- De uitwerking van de autorisatie zelf (valt onder skill `autorisatie`)
- Profielen en veldcontexten (valt onder skill `profielen-en-veldcontexten`)
- De InSite-pagina's achter hetzelfde proces (valt onder skill `portalpagina-insite`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

- Komt de functionaliteit ook naar Pocket, of alleen naar InSite?
- Moet de Pocket-functionaliteit geautoriseerd worden, en zo ja op welke rollen of gebruikers?
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
