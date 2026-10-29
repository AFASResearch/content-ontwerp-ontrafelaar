# Wat de content-afdeling uit een ontwerp haalt

Dit document beschrijft per onderwerp wat wij na jouw ontwerp inrichten en meeleveren, en welke informatie we daarvoor uit het ontwerp moeten kunnen halen. Het is geen eisenlijst voor elk ontwerp: alleen de onderwerpen die jouw ontwerp raakt, zijn van toepassing.

Per onderwerp staat steeds hetzelfde:

| Kop | Betekenis |
|---|---|
| **Wij leveren** | Wat wij bouwen of inrichten en wat de klant krijgt |
| **Benoem in het ontwerp** | De gegevens die wij nodig hebben om dat te kunnen doen |
| **Vaak gemist** | Wat in de praktijk ontbreekt en ons een uitzoekvraag kost |

---

## Deel 1 · Schermen en velden

### Informatiebolletje

**Wij leveren:** de uitlegtekst achter het informatie-icoon bij een veld, in Profit, InSite en OutSite.

**Benoem in het ontwerp:** elk nieuw veld, elk verplaatst veld en elk veld waarvan de betekenis wijzigt. Heb je zelf al een tooltiptekst bedacht? Zet die erin — wij toetsen en herschrijven hem.

**Vaak gemist:** een ontwerp zet veldinfo buiten scope zonder te vermelden *welke* velden het raakt. Daardoor moeten wij de lijst alsnog zelf afleiden. Zet de velden erbij, ook als je ze buiten scope plaatst.

### Profielen en contexten

**Wij leveren:** aanmaakprofielen, beoordeelprofielen, afwijkende beoordeelprofielen per workflowtaak, en per profiel een context die bepaalt welke velden zichtbaar, wijzigbaar, verplicht of verborgen zijn.

**Benoem in het ontwerp:** per nieuw veld een rechtenmatrix: wat mag de instuurder, wat mag de beoordelaar, en wat geldt na afronding. Noem ook welke velden de klant niet mag verbergen.

**Vaak gemist:** drie dingen. Het **afwijkende beoordeelprofiel** per workflowtaak wordt niet benoemd. Een profielvariant met een **vast gevuld veld** wordt niet genoemd, of spreekt elders in het ontwerp zichzelf tegen. En een **alleen-lezen-context** ontbreekt in de matrix.

### Weergaven

**Wij leveren:** kolommen, filters en sorteringen in overzichten.

**Benoem in het ontwerp:** welke bestaande weergave een kolom erbij krijgt en of er een nieuwe weergave komt, en per kolom of het veld al in de gegevensverzameling zit of dat de programmeur het nog moet toevoegen. Noem ook expliciet als een weergave juist **niet** wordt uitgebreid.

**Vaak gemist:** drie dingen. Het nummer of de exacte naam van de weergave, waardoor wij niet weten welke variant we moeten aanpassen. Of het veld al in de gegevensverzameling zit: zit het er niet in, dan kunnen wij pas inrichten nadat de programmeur het heeft toegevoegd. En de standaardstand: welke kolommen staan aan, op welk veld sorteren we, en welk filter is standaard actief.

### Boekingslayouts

**Wij leveren:** de indeling en volgorde van invoervelden bij het boeken.

**Benoem in het ontwerp:** welke boekingssoort of welk dagboek het raakt, waar het nieuwe veld in de invoervolgorde komt, of het veld verplicht is, en of het alleen bij een bepaalde soort zichtbaar is.

**Vaak gemist:** het ontwerp beschrijft het veld wel, maar niet of het ook in de boekingsgang hoort. En of het veld al in het boekingsscherm bestaat: zo niet, dan moet de programmeur het eerst toevoegen voordat wij de layout kunnen inrichten.

### Icoontjes

**Wij leveren:** de aanvraag voor een icoon bij een menu-item, knop, tegel of processtap: de plek en de betekenis. Het icoon zelf maakt de afdeling **Media**, niet wij.

**Benoem in het ontwerp:** elk nieuw menu-item, tabblad, knop of tegel, en wat het icoon moet uitdrukken. Meestal is er geen nieuw icoon nodig; benoem het dus vooral als dat wél zo is.

**Vaak gemist:** nieuwe tabbladen en acties worden beschreven zonder dat duidelijk is of een bestaand icoon hergebruikt kan worden. Een nieuw icoon is bovendien een taak bij een andere afdeling: hoe later dat op tafel komt, hoe meer het de release in de weg zit.

---

## Deel 2 · Toegang

### Autorisatie

**Wij leveren:** in Profit de autorisatieprocessen op menu-items, tabbladen, weergaven en acties. In InSite en OutSite de **functionaliteiten**, de **rollen** waaraan we ze koppelen, en de **onderdelen** die eronder hangen, zoals KPI-secties op een stamkaart.

**Benoem in het ontwerp:** per nieuw scherm of pagina-onderdeel vier dingen — de naam van de functionaliteit, welke onderdelen eronder vallen, aan welke rollen we koppelen, en of er een ESS-, MSS- en OutSite-variant komt.

**Vaak gemist:** dit is het onderwerp waar het meest ontbreekt.

- De **functionaliteitsnamen** staan er niet in, terwijl wij ze moeten aanmaken.
- De **ESS/MSS-splitsing** wordt niet gemaakt. Eén beschreven route levert bij ons bijna altijd twee of drie functionaliteiten op, zodat een klant één route kan uitzetten.
- KPI's en pagina-onderdelen worden beschreven als scherminhoud, niet als iets dat we onder een functionaliteit moeten hangen.
- De rolkeuze wordt doorgeschoven met "team Content bepaalt", zonder kader. Bij Loontransparantie ging dat om ongeveer 25 koppelingen.

---

## Deel 3 · Processen

### Workflow en condities

**Wij leveren:** de workflows, de processtappen, de condities en per taak het profiel waarmee die taak wordt afgehandeld.

**Benoem in het ontwerp:** per stap wie de taak krijgt, welke actie hij heeft, welke conditie de route bepaalt, en welk profiel de stap gebruikt. Noem ook of er in een stap een rapport wordt gegenereerd.

**Vaak gemist:** het **aantal workflows**. Een ontwerp gaat uit van één workflow voor twee profielen, terwijl de stappen in de praktijk uiteenlopen en er twee workflows nodig zijn. En de koppeling van een taak aan een **afwijkend beoordelingsprofiel** staat er niet in.

### Signalen

**Wij leveren:** de signaaldefinitie: gegevensverzameling, filters, signaaltype, signaaltekst, gebruikerstoelichting, bestemming en autorisatie.

**Benoem in het ontwerp:** waarop het signaal afgaat, wie het ontvangt en welke velden erin moeten staan.

**Vaak gemist:** de signaaltekst zelf, en de velden die de gegevensverzameling moet bevatten om die tekst te kunnen vullen.

### Pocket

**Wij leveren:** de vaststelling wat er in Pocket beschikbaar komt, de autorisatie daarop (op rollen of gebruikers) en de uitleg erover. De app zelf bouwen wij **niet**.

**Benoem in het ontwerp:** of Pocket geraakt wordt, en zo ja welke functionaliteit de gebruiker in de app krijgt, wie die mag gebruiken en of er een pushmelding bij hoort. Benoem het ook als Pocket **niet** geraakt wordt.

**Vaak gemist:** Pocket wordt stilzwijgend overgeslagen, terwijl hetzelfde proces in InSite wel is uitgewerkt. En als Pocket wél wordt genoemd, ontbreekt op welke rollen of gebruikers de functionaliteit geautoriseerd moet worden.

---

## Deel 4 · Teksten naar de klant

### Opmaak InSite

**Wij leveren:** de banner met afbeelding, titel en tekst op aanmaak-, profielkeuze- en medewerkerkeuzepagina's. De standaardpagina's zelf maken wij **niet** meer op; die komen uit de bouw.

**Benoem in het ontwerp:** welke sjablonen er komen, welke profielen daarop uitkomen, en voor welke doelgroep elke variant bedoeld is.

**Vaak gemist:** de **aantallen**. Eén sjabloon maal twee profielen maal ESS en MSS is zes teksten en twee afbeeldingen. Een zin als "toelichtende tekst, invulling door Content" maakt niet zichtbaar hoeveel teksten dat zijn, waar ze staan en wie ze leest.

### Pagina's OutSite

**Wij leveren:** de OutSite-pagina's, en bij sjablonen waarvoor **geen standaardpagina** bestaat ook de opmaak zelf, die wij maken en inchecken.

**Benoem in het ontwerp:** of er OutSite-functionaliteit komt, welke externe doelgroep die ziet, en of er een standaardpagina beschikbaar is.

**Vaak gemist:** het verschil tussen "bestaat al" en "maken wij". Een sjabloonlijst zonder die vermelding kost ons een hele taak, in beide richtingen.

### Berichtsjabloon

**Wij leveren:** de e-mailberichten: onderwerp, tekst en de tags die uit de gegevensverzameling komen.

**Benoem in het ontwerp:** welk bericht wanneer wordt verstuurd, aan wie, en welke gegevens erin moeten staan.

**Vaak gemist:** de velden die als tag nodig zijn, en daarmee of de gegevensverzameling die velden al bevat.

### Documentsjabloon

**Wij leveren:** brieven en correspondentiesjablonen: de tekst en de tags die uit de gegevensverzameling komen.

**Benoem in het ontwerp:** welk document, voor wie, met welke gegevens, en hoe het bij de ontvanger komt — als download, als afdruk of als **bijlage bij een mail**. Gaat het als bijlage mee, dan hoort er ook een berichtsjabloon bij: op het tabblad E-mail leggen wij de titel, de bijlage en de inhoud van het bericht vast.

**Vaak gemist:** drie dingen. Het onderscheid tussen een document en een rapport, dat bepaalt of er een type document nodig is. Het onderscheid tussen een document en een mail, waardoor de helft van de taak blijft liggen. En of de velden die als tag nodig zijn al in de gegevensverzameling zitten.

### Vertalingen

**Wij leveren:** de vertalingen van berichtsjablonen en signaalteksten naar Engels, Duits en Frans.

**Benoem in het ontwerp:** of de functionaliteit meertalig wordt uitgeleverd.

**Vaak gemist:** de vertaalvraag komt pas achteraf op tafel. Elke tekst die wij meeleveren — banner, profielkeuze, meldingstekst, rapport — heeft er een.

---

## Deel 5 · Output en analyse

### Rapporten

**Wij leveren:** twee soorten. Een **afdrukrapport** dat de gebruiker uit een menu start, en een **rapport in de workflow** dat een behandelaar in een stap genereert en dat als bijlage bij het dossieritem komt.

**Benoem in het ontwerp:** welk soort het is, welke gegevensverzameling eronder ligt, welke velden erop staan en voor wie het bedoeld is.

**Vaak gemist:** de **naam**. De rapportkeuze in de workflow wordt niet gefilterd op de workflow waarin de behandelaar zit, dus hij kiest uit de volledige lijst. De naam moet op zichzelf herkenbaar zijn. Daarnaast ontbreekt vaak welke velden daadwerkelijk op het rapport komen.

### Analyses en gegevensverzamelingen

**Wij leveren:** de gegevensverzamelingen waarmee weergaven, rapporten en dashboards worden gevoed, en de analyses die daarop draaien.

**Benoem in het ontwerp:** welke verzameling nieuw is of wordt uitgebreid, met welke velden en welke filters, welke afnemer hem gebruikt, en waarvoor elk veld dient: groeperen, optellen, filteren of alleen tonen.

**Vaak gemist:** of een bestaande verzameling wordt uitgebreid of dat er een nieuwe bijkomt, en welke filters standaard meegaan. Daarnaast ontbreekt welke velden de programmeur nog moet toevoegen; juist die regels bepalen wanneer wij kunnen beginnen.

---

## Checklist per nieuw object

Loop dit af voor elk nieuw scherm, veld, pagina, proces of rapport. Vijf vragen, elk één zin.

| Vraag | Voorbeeld van een bruikbaar antwoord |
|---|---|
| **Wat** komt erbij? | Functionaliteit `ESS/Loontransparantie raadplegen` |
| **Waar** zit het? | InSite, stamkaart medewerker, onderaan de groep Salaris |
| **Wie** ziet het? | Rol Medewerker (Profit); MSS-variant voor HR-adviseur en Management |
| **Hoe** krijgen we het werkend? | Pagina-onderdeel `KPI's voor Loontransparantie (ESS)` koppelen als onderdeel van die functionaliteit |
| **Bestaat het al?** | De gegevensverzameling bestaat; het veld Peildatum moet de programmeur nog toevoegen |

Kun je er één niet beantwoorden? Zet hem dan als open punt in het ontwerp. Een open punt met eigenaar is voor ons bruikbaarder dan een aanname.
