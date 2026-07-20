---
name: informatiebolletje
description: 'Breng de informatiebolletje-impact van een ontwerp in kaart: welke velden in Profit, InSite of OutSite een informatiebolletje (veldtoelichting) nodig hebben of moeten worden aangepast. Gebruik bij vragen als: welke informatiebolletjes zijn nodig, wat zijn de veldinfo-wijzigingen, maak de informatiebolletje-paragraaf, veldinfo content, veldtoelichting.'
argument-hint: 'Geef het ontwerp of het te analyseren hoofdstuk mee'
---

# Informatiebolletje-analyse

## Doel

Volledig in kaart brengen welke **informatiebolletjes** een ontwerp vereist — zowel expliciet benoemde als impliciet noodzakelijke veldinformatie — voor Profit, InSite en/of OutSite.

Een informatiebolletje is een toelichting die verschijnt wanneer een gebruiker op het icoontje bij een veld klikt. De inhoud wordt beheerd via: **Algemeen / Beheer / Management tool** > Functiegroep > Bestand > tabblad *Velden* > veld-eigenschappen > tabblad *Veld eigenschappen* > veld *Informatiebolletje*.

---

## Stap 1 — Scan het ontwerp: wat zoek je?

### A) Expliciete signalen

Markeer altijd als informatiebolletje-taak wanneer een van de volgende termen letterlijk voorkomt:

| Term | Varianten |
|------|-----------|
| **Informatiebolletje** | informatiebolletje, info-bolletje |
| **Veldinfo** | veldinfo, veld-info |
| **Veldinfo content** | veldinfo content, veldinformatie |

### B) Impliciete signalen

Markeer ook als informatiebolletje-taak wanneer uit de tekst blijkt dat een veld toelichting nodig heeft, ook al wordt de term "informatiebolletje" niet gebruikt. Herken dit aan:

| Signaal | Voorbeelden |
|---------|-------------|
| **Toelichting bij veld** | "het veld X behoeft uitleg", "een toelichting op veld X is gewenst" |
| **Gebruiksinstructie bij invoer** | "de gebruiker moet weten dat…", "uitleg over hoe het veld te gebruiken" |
| **Betekenis van waarden** | "de codes staan voor…", "dit veld bevat drie mogelijke waarden: …" |
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
| **Beoogde inhoud** | Samenvatting van de gevraagde of benodigde tekst, of `nader te bepalen` als het ontwerp dit niet specificeert |
| **Status** | `komt voor` / `te weinig info` (+ wat ontbreekt) |
| **Bron (ontwerp)** | Hoofdstuk/§ \| Pagina \| (anker: "ankerzin/titel") |

Gebruik één rij per veld. Als hetzelfde veld in meerdere kanalen een ander informatiebolletje nodig heeft, gebruik dan een aparte rij per kanaal.

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
- Tooltips of popups die via maatwerk/custom code worden getoond en niet via de Management tool worden gevuld
