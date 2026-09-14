---
name: portalpagina-insite
description: 'Breng de InSite-impact van een ontwerp in kaart op portalpaginas en de opmaak van standaardpaginas: welke InSite-paginas, paginaonderdelen of portals nieuw zijn, wijzigen of gecontroleerd moeten worden. Gebruik bij vragen als: welke InSite-paginas zijn nodig, portalpagina, standaardpagina controleren, InSite-opmaak.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Portalpagina / opmaak standaardpagina's (InSite)-analyse

> **Status: skelet.** De scansignalen en outputvelden hieronder zijn een startpunt en worden nog verder uitgewerkt. Gok nooit: gebruik `te weinig info` als je iets niet zeker kunt vaststellen.

## Doel

Volledig in kaart brengen welke **InSite-portalpagina's en standaardpagina's** een ontwerp raakt, inclusief de opmaak die gecontroleerd moet worden.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

| Term | Varianten |
|------|-----------|
| **InSite** | InSite, InSite-pagina, InSite-sjabloon |
| **Portal** | portal, portalpagina, portaaltoegang |
| **Standaardpagina** | standaardpagina, startpagina, opmaak |

### B) Impliciete signalen

| Signaal | Voorbeelden |
|---------|-------------|
| **Interne gebruiker voert iets uit** | "de medewerker dient in", "de manager keurt goed" |
| **Nieuw paginaonderdeel of tegel** | "op de startpagina komt een blok" |
| **Nieuwe processtap** | "de gebruiker doorloopt drie stappen" |
| **Wijziging in bestaande pagina-indeling** | "het veld verschuift naar tabblad X" |

---

## Stap 2 — Output samenstellen

| Veld | Inhoud |
|------|--------|
| **Pagina/onderdeel** | Naam van de pagina, het paginaonderdeel of de processtap |
| **Portal/sjabloon** | Bijbehorend portal of InSite-sjabloon |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `opmaak controleren` |
| **Opmaakwijziging** | Wat er visueel of qua indeling wijzigt, of `nader te bepalen` |
| **Doelgroep** | Welke gebruikersrol |
| **Status** | `komt voor in ontwerp` / `komt niet voor in ontwerp` / `te weinig info` (+ wat ontbreekt) |
| **Bron** | `[ontwerp]` of `[six-pager]` + Hoofdstuk/§ \| Pagina \| (anker: "…") |

---

## Stap 3 — Bronverwijzing (altijd toepassen)

> Hoofdstuk/§ … | Pagina … | (anker: "…")

---

## Stap 4 — Buiten scope (altijd opnemen)

- Huisstijl en centrale opmaakrichtlijnen
- Klantspecifieke portalinrichting
- Autorisatierollen voor InSite (valt onder skill `autorisatie`)
- OutSite-pagina's (valt onder skill `paginas-outsite`)

---

## Stap 5 — Beslispunten (altijd opnemen, minimaal 1)

Bijvoorbeeld:

- Komt er een nieuwe pagina of wordt een bestaande standaardpagina uitgebreid?
- Op welke portalpagina landt de gebruiker?
- Welke onderdelen tonen we standaard?

---

## Stap 6 — Content-sectie (altijd apart opnemen)

- **"Wat ziet de gebruiker op deze pagina?"**
- **"Waar vind je de pagina?"**
- **"Welke stappen doorloop je?"**

---

## Kwaliteitscriteria

- [ ] Elke pagina heeft portal/sjabloon en doelgroep
- [ ] Elk item heeft een bronverwijzing met herkomstlabel
- [ ] Buiten-scope-blok aanwezig
- [ ] Minimaal 1 beslispunt geformuleerd
- [ ] Content-sectie aanwezig
- [ ] `te weinig info` geeft aan wat ontbreekt

---

## Nog uit te werken

- Overzicht van bestaande InSite-sjablonen en standaardpagina's
- Menupaden voor InSite-paginabeheer
- Vaste controlepunten voor opmaak
