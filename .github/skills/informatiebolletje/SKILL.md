---
name: informatiebolletje
description: 'Breng de informatiebolletje-impact van een ontwerp in kaart: welke velden in Profit, InSite of OutSite een informatiebolletje (veldtoelichting) nodig hebben of moeten worden aangepast. Gebruik bij vragen als: welke informatiebolletjes zijn nodig, wat zijn de veldinfo-wijzigingen, maak de informatiebolletje-paragraaf, veldinfo content, veldtoelichting.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Informatiebolletje-analyse

## Doel

Volledig in kaart brengen welke **informatiebolletjes** een ontwerp vereist — zowel expliciet benoemde als impliciet noodzakelijke veldinformatie — voor Profit, InSite en/of OutSite.

Een informatiebolletje is een toelichting die verschijnt wanneer een gebruiker op het icoontje bij een veld klikt.

---

## Waar vul je het informatiebolletje?

1. Open de omgeving en zet de **consultancy-modus** aan.
2. Ga naar **Consultancy / Anta Taal / Veldinfo content (informatiebolletje)**.
3. Zoek het veld en open de regel. Er zijn twee weergaven: één met de velden waarvan het bolletje gevuld is en één met **Alle velden**. Zie je het veld niet? Kijk dan bij `Alle velden`.
4. Vul de tekst bij de eigenschappen en sla op. De wijziging is nog niet direct zichtbaar in de weergave; open de regel opnieuw om hem te zien.
5. Push op de normale manier. Onder SQL2XML staat het veld onder `Veldinfo content`.

### Vaste regels

- **Content is eigenaar van de Nederlandse tekst.** Elke wijziging in de Nederlandse tekst loopt via de content-afdeling.
- **Een veld kan op meerdere plekken worden gebruikt.** Controleer altijd via de weergave `Alle velden` waar het veld nog meer voorkomt. Is het veld gedeeld, houd de tekst dan generiek of laat het bolletje ongemoeid en zet de uitleg in de help.
- **Elke wijziging maakt een nieuw ResId.** Ook bij het aanpassen van een bestaand bolletje. De tekst staat één à twee dagen later in de Vertaaltool en gaat automatisch mee in het reguliere vertaalproces. Je hoeft hiervoor geen aparte vertaaltaak op te voeren.
- **Maximale lengte is niet gedocumenteerd.** Hanteer korte zinnen en een compacte tekst. Noem bij twijfel expliciet dat de limiet onbekend is.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

Markeer altijd als informatiebolletje-taak wanneer een van de volgende termen letterlijk voorkomt:

| Term | Varianten |
|------|-----------|
| **Informatiebolletje** | informatiebolletje, info-bolletje |
| **Veldhelp** | veldhelp, veld-help |
| **Veldinfo** | veldinfo, veld-info |
| **Veldinfo content** | veldinfo content, veldinformatie |
| **Tooltip** | tooltip |

### B) Impliciete signalen

Markeer ook als informatiebolletje-taak wanneer uit de tekst blijkt dat een veld toelichting nodig heeft, ook al wordt de term "informatiebolletje" niet gebruikt. Herken dit aan:

| Signaal | Voorbeelden |
|---------|-------------|
| **Nieuw veld** | "krijgt een nieuw veld X", "op scherm Y komt veld X" |
| **Verplaatst veld** | "de instelling verhuist van A naar B" |
| **Gewijzigde betekenis** | "het veld wordt voortaan gevuld met…" |
| **Toelichting bij veld** | "het veld X behoeft uitleg", "een toelichting op veld X is gewenst" |
| **Gebruiksinstructie bij invoer** | "de gebruiker moet weten dat…", "uitleg over hoe het veld te gebruiken" |
| **Betekenis van waarden** | "de codes staan voor…", "dit veld bevat drie mogelijke waarden: …" |
| **Voorwaardelijke zichtbaarheid** | "het veld is zichtbaar afhankelijk van…" |
| **Complexe invoereis** | "het formaat is…", "de waarde mag alleen…" |
| **Verwijzing naar externe context** | "zie ook…", "conform CAO…" — als dit bij een veld staat |

---

## Stap 2 — Output samenstellen

Lever voor elk gevonden item een rij op in onderstaande tabel.

| Veld | Inhoud |
|------|--------|
| **Veldnaam** | Naam van het veld zoals in het ontwerp of de applicatie |
| **Bestand/scherm** | Functiegroep / bestand / scherm / sjabloon waar het veld staat |
| **Kanaal** | Profit / InSite / OutSite / meerdere |
| **Type signaal** | `expliciet` (term staat erin) of `impliciet` (veld heeft aantoonbaar toelichting nodig) |
| **Gevraagde actie** | `nieuw` / `aanpassen` / `verwijderen` |
| **Gedeeld veld?** | `nee` / `ja, tekst generiek houden` / `onbekend, controleren via weergave Alle velden` |
| **Beoogde inhoud** | Concrete concepttekst, of `nader te bepalen` als het ontwerp dit niet specificeert |
| **Vertaalgevolg** | `ja, nieuw ResId` bij elke nieuwe of gewijzigde Nederlandse tekst |
| **Status** | `komt voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

Gebruik één rij per veld. Als hetzelfde veld in meerdere kanalen een ander informatiebolletje nodig heeft, gebruik dan een aparte rij per kanaal.

Sluit de tabel altijd af met de sectie **Waar vul je het informatiebolletje?**, zodat de lezer het pad en de vaste regels bij de hand heeft.

---

## Stap 3 — Bronverwijzing (altijd toepassen)

Voeg bij **elk** item **Bron (ontwerp)** toe:

> Hoofdstuk/§ … | Pagina … | (anker: "…")

Als hoofdstuk/pagina **niet betrouwbaar beschikbaar** is:
- Vermeld dat expliciet.
- Gebruik **sectietitel of tekstfragment** als anker.

---

## Stap 4 — Buiten scope (altijd opnemen)

Sluit de volgende onderwerpen expliciet uit en benoem ze als "buiten scope":

- Helptext of documentatie buiten velden (bijv. procesbeschrijvingen, handleidingen)
- Verplichte veldvalidaties of foutmeldingen (die worden elders beheerd)
- Vrije tekstvelden op InSite-pagina's die geen veldkoppeling hebben
- Tooltips of popups die via maatwerk/custom code worden getoond en niet via `Veldinfo content` worden gevuld
- De vertaling naar ENG, DUI en FR — die loopt automatisch via de Vertaaltool en valt niet onder de skill `vertalingen`
