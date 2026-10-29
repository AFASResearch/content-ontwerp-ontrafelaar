---
name: autorisatie-en-functionaliteiten
description: 'Breng de autorisatie- en functionaliteit-impact van een ontwerp in kaart: Profit (autorisatiegroepen: menu-items, tabbladen, weergaven, acties) en InSite/OutSite (functionaliteiten, de rollen waaraan je ze koppelt en de pagina-onderdelen eronder). Gebruik bij vragen als: welke autorisaties zijn nodig, welke functionaliteit, aan welke rol koppelen, KPI autoriseren, ESS MSS splitsen, Profit menu-autorisatie.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Autorisatie- en functionaliteit-analyse

## Doel

Volledig in kaart brengen welke **autorisatie-impact** een ontwerp heeft, verdeeld over:

1. **Profit (autorisatiegroepen):** nieuwe of gewijzigde menu-items, tabbladen, weergaven en acties.
2. **InSite/OutSite (functionaliteiten):** welke functionaliteit nieuw is of wijzigt, welke **pagina-onderdelen** eronder hangen, en aan welke **rollen** we de functionaliteit koppelen.

---

## Het model voor InSite en OutSite

Autoriseren gebeurt op de **functionaliteit**, niet op de pagina. De keten is:

```
Functionaliteit  →  Onderdelen (pagina-onderdelen, bijv. KPI-secties)
       ↓
    Rollen (standaardrollen die wij meeleveren)
```

Drie regels die altijd gelden:

1. **Splits ESS en MSS.** Een functionaliteit krijgt vrijwel altijd een ESS- en een MSS-variant, zodat een klant één van beide kan uitzetten als hij die route niet wil gebruiken. Naamgeving: `ESS/<onderwerp>` en `MSS/<onderwerp> (InSite)`.
2. **OutSite is een derde variant.** Naamgeving: `MSS/<onderwerp> (OutSite)`, met eigen OutSite-rollen.
3. **KPI's en pagina-onderdelen autoriseer je als onderdeel.** Een KPI-sectie op de stamkaart krijgt geen eigen rol, maar hangt onder **Onderdelen** van de bijbehorende functionaliteit.

### Referentie: standaardrollen

Gebruik deze lijst om per functionaliteit een voorstel te doen. Noemt het ontwerp geen rollen, dan is dat een beslispunt — vul nooit zelf in zonder het te markeren.

| Kanaal | Rollen |
|---|---|
| InSite — medewerkerroute (ESS) | Medewerker (Profit), Functioneel applicatiebeheer (Profit), Sitebeheer (Profit) |
| InSite — leidinggevende- en HR-route (MSS) | Accountant (Profit), Functioneel applicatiebeheer (Profit), HR-adviseur (Profit), Management (Profit), Personeelsadministratie (Profit), Sitebeheer (Profit) |
| InSite — Flex en plaatsingen | Functioneel applicatiebeheer (Profit), Kandidaten beheren (Profit), Plaatsingen (Profit), Projectadministratie (Profit), Projecten applicatiebeheer (Profit), Projectleiding (Profit), Sitebeheer (Profit) |
| OutSite — Payroll Cloud | Beheerder accountancyportal, Medewerker accountancyportal, Personeelsadministrateur |

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Profit (autorisatiegroepen)

Markeer als autorisatie-impact als je ziet:

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw menupad** | HRM > … > … |
| **Nieuw tabblad** op eigenschappen | Tabblad Functiecategorie op de verkooprelatie |
| **Nieuwe weergave of overzicht** | Overzicht "Openstaande aanvragen" |
| **Nieuwe actie of knop** | Nieuw, Eigenschappen, Verwijderen, Omzetten |
| **Nieuw autorisatieproces** | "het tabblad krijgt een eigen autorisatieproces" |
| **Conditie of activering** | "alleen zichtbaar bij actieve Flex-activering" |
| **Overerving of conversie** | "bij conversie krijgen gebruikers met onderhoudsrechten het proces" |
| **Uitzondering** | "**niet autoriseerbaar**", "volgt de autorisatie van het scherm" |

### B) InSite/OutSite (functionaliteiten)

Markeer als functionaliteit-impact als je ziet:

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw sjabloon of pagina** | "Aanmaken vraag aan HR (ESS)" |
| **Nieuwe functionaliteit** | "de functionaliteit ESS/… wordt gebruikt voor…" |
| **Nieuw pagina-onderdeel of KPI** | "op de stamkaart komt een sectie met vijf KPI-tegels" |
| **Rolafhankelijke route** | "de leidinggevende start namens de medewerker" → ESS- én MSS-variant |
| **Payroll Cloud of OutSite** | "ook beschikbaar in OutSite" → eigen functionaliteit en eigen rollen |
| **Afgeschoven keuze** | "welke rollen worden meegeleverd, is aan team Content" → altijd een beslispunt |

---

## Stap 2 — Output samenstellen

Lever altijd **twee losse blokken** op: eerst Profit, dan InSite/OutSite.

### Output 1 — Profit

Voor elk gevonden item:

| Veld | Inhoud |
|------|--------|
| **Item** | Menu-item / tabblad / weergave / actie |
| **Vindplaats** | Exact menupad óf object + tabblad |
| **Autorisatieproces** | Eigen proces, of erft van het scherm |
| **Nieuw/gewijzigd** | 1 zin |
| **Conditie** | Alleen vermelden als het ontwerp dit noemt |
| **Conversie** | Wat een bestaande klant automatisch krijgt — alleen als genoemd |
| **Status** | `komt voor` / `komt niet voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

### Output 2 — InSite/OutSite

Eén blok per **functionaliteit**:

| Veld | Inhoud |
|------|--------|
| **Functionaliteit** | Exacte naam, bijv. `ESS/Loontransparantie raadplegen` |
| **Kanaal** | InSite ESS / InSite MSS / OutSite |
| **Nieuw/gewijzigd** | 1 zin |
| **Onderdelen** | De pagina-onderdelen die eronder hangen, bijv. `KPI's voor Loontransparantie (ESS)`. Leeg = geen |
| **Rollen** | De rollen waaraan we koppelen, uit de referentietabel. Noemt het ontwerp ze niet: voorstel + beslispunt |
| **Status** | `komt voor` / `komt niet voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

> **Controle op volledigheid.** Levert het ontwerp een ESS-route, dan hoort er vrijwel altijd een MSS-variant bij, en bij Payroll Cloud een OutSite-variant. Ontbreekt er één, meld dat als `te weinig info` in plaats van hem stilzwijgend weg te laten.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item **Bron (ontwerp)** toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Als hoofdstuk/pagina **niet betrouwbaar beschikbaar** is (bijv. niet in de tekstlaag):
- Vermeld dat expliciet.
- Gebruik **sectietitel of tekstfragment** als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

Sluit expliciet de volgende onderwerpen uit en benoem ze als "buiten scope":

- Technische IAM/SSO/IdP/AD-inrichting
- Licenties en abonnementen
- Backend- en database-autorisaties die niet als menu, tabblad of functionaliteit zichtbaar zijn
- Veldzichtbaarheid per profielcontext (valt onder skill `profielen-en-veldcontexten`)
- De opmaak van pagina's en banners (valt onder skill `portalpagina-insite`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Formuleer altijd minimaal één beslispunt, bijvoorbeeld:

- Aan **welke rollen** koppelen we elke functionaliteit, als het ontwerp dat openlaat?
- Komt er een **aparte ESS- en MSS-functionaliteit**, of volstaat er één?
- Moet toegang **beperkt** worden vanwege privacy of gevoelige loongegevens?
- Krijgt een nieuw pagina-onderdeel een eigen functionaliteit, of hangt het onder een bestaande?
- Krijgen bestaande klanten het nieuwe proces via **conversie**, of moeten ze het zelf toekennen?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

Sluit af met een blok "Content" dat beantwoordt:

- **"Waar vind ik het?"** — menupad of pagina
- **"Welke rechten heb je nodig?"** — autorisatiegroep, of functionaliteit plus rol
- **"Wat zie je als je geen rechten hebt?"** — alleen invullen als het ontwerp dit beschrijft

---

## Kwaliteitscriteria

Controleer voor je de output levert:

- [ ] Elk Profit-item heeft een vindplaats en een autorisatieproces
- [ ] Elke functionaliteit heeft kanaal, onderdelen en rollen
- [ ] ESS-, MSS- en OutSite-varianten zijn alle drie beoordeeld
- [ ] Elk pagina-onderdeel hangt onder een benoemde functionaliteit
- [ ] Elk item heeft een **Bron (ontwerp)**-verwijzing
- [ ] Buiten-scope-blok is aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] Status `te weinig info` geeft aan wat er ontbreekt
