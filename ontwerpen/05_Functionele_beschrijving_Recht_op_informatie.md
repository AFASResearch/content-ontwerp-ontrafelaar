# DP1 – Recht op informatie · Functionele beschrijving

> Functionele uitwerking van de brainstorm van 1 september 2026, aangevuld met de uitkomsten van de PM-terugkoppeling van 3 september 2026. Dit document voedt het latere FO `01_FO_Recht_op_informatie.md`.
>
> Onderdeel van het [Programma Loontransparantie](../00_Programma_Loontransparantie.md). Scope en afbakening van het deelproject staan in [00_Scope.md](00_Scope.md). Laatste bijwerking: 2026-09-10.
>
> Alle keuzes uit de brainstorm en de PM-terugkoppeling zijn besloten. Hoofdstuk 12 bevat de besluiten, de herzieningen en de punten die nog buiten dit document worden afgehandeld.
>
> Hoofdstuk 5 is op 8 september 2026 herzien naar een model met vier lagen, zodat DP2 – Rapportage er in een tweede fase op verder kan bouwen. De onderbouwing staat in dat hoofdstuk zelf, met onderzoek ON-08 en ON-09 als basis.
>
> Hoofdstuk 4, 7 en 8 zijn op 10 september 2026 herzien naar aanleiding van de feedback van de programmeur: het bijwerken van de lagen 2 en 3 verhuist naar een wachtrijtaak vanuit de dagovergang met een triggertabel, en de functie wordt per aangiftetijdvak bepaald in plaats van ultimo venster. De besluiten staan in blok M van hoofdstuk 12.
>
> Hoofdstuk 2, 3 en 9 zijn op 10 september 2026 aangevuld met de terminologie rond arbeidsverhouding en met §9.6 over landafhankelijkheid. Zie blok O van hoofdstuk 12.
>
> De term **loonkloof** is op 10 september 2026 vervangen door **loonverschil**, conform de ministeriële regeling van 10 juli 2026. Dat raakt de acht veldnamen, de KPI-titels en de schermteksten. Zie blok P van hoofdstuk 12.

---

## 1 Inleiding en afbakening

### 1.1 Aanleiding

De richtlijn loontransparantie geeft elke medewerker het recht om informatie op te vragen over het eigen loonniveau en over het gemiddelde loonniveau van collega's in dezelfde functiecategorie, uitgesplitst naar geslacht. Klanten moeten die informatie kunnen leveren zonder er handwerk voor te doen.

De gegevens die daarvoor nodig zijn, zitten al in Profit: in de loonaangifte. Maar ze staan verspreid, per aangiftetijdvak en per inkomstenverhouding. Elke presentatievorm zou die gegevens opnieuw moeten verzamelen, omrekenen en aggregeren. Dat is traag en het levert het risico op dat de KPI, een dashboard en een document verschillende uitkomsten tonen.

In dit ontwerp lossen we dat op met één voorbereide gegevensverzameling in vier lagen. We richten dit zo in dat de berekeningen één keer plaatsvinden, in een aparte wachtrijtaak buiten het salarisproces om, en dat elke presentatielaag daarna alleen nog leest.

### 1.2 Doel

Een gegevensmodel Recht op informatie neerzetten dat de actuele loontransparantiegegevens per arbeidsverhouding bevat, plus het proces dat het gevuld en actueel houdt. Op basis daarvan tonen we de medewerker KPI's met bijbehorende weergaven op de stamkaart.

### 1.3 Resultaat

Na oplevering geldt het volgende:

- De bestaande tabel Loonaangifte uren per medewerker is uitgebreid met de loonbedragen uit de loonaangifte, en vormt daarmee de brontabel per medewerker, dienstverband en aangiftetijdvak. Die tabel wordt direct bij het klaarzetten van de loonaangifte gevuld.
- Daarboven staat de tabel Loontransparantie per inkomstenverhouding met de waarden over de rapportageperiode, per functie waarin de medewerker binnen die periode heeft gewerkt, en de tabel Loontransparantie per functiecategorie met de vergelijkingscijfers voor mannen en vrouwen.
- Bovenaan staat de rapportageperiode: de vastlegging van de afbakening waarover is gerekend. Daardoor kan DP2 – Rapportage later dezelfde tabellen gebruiken voor een afgesloten kalenderjaar, zonder dat het model wordt opengebroken.
- Een triggertabel houdt bij welke werkgever en welk aangiftetijdvak zijn geraakt. Dat gebeurt bij het klaarzetten van de loonaangifte, maar ook bij een functiewijziging of een wijziging in de functiecategorie-inrichting.
- De wachtrijtaak **Bijwerken gegevens loontransparantie** stelt de twee tabellen erboven opnieuw samen. Die taak wordt vanuit de dagovergang Vernieuwen actuele gegevens gestart en staat los van het loonaangifteproces, zodat hij bij een fout gewoon opnieuw kan worden uitgevoerd.
- De medewerker ziet op de stamkaart onder Salaris een tabblad Loontransparantie met vier KPI's, een vergelijkingstabel en een overzicht van de functies in de eigen functiecategorie.
- De brontabel is direct bruikbaar als bron voor een Power BI-dashboard en voor latere documenten, zonder dat die opnieuw moeten rekenen.

### 1.4 Afbakening van dit document

In scope:

- Het gegevensmodel Recht op informatie: de vier lagen, hun sleutels, velden en betekenis, en per veld in welke fase het wordt gevuld.
- Het uitbreiden van de bestaande tabel Loonaangifte uren per medewerker met de zeven loonaangifterubrieken, inclusief het vullen ervan bij het klaarzetten van de loonaangifte en het eenmalig vullen over 2026 in de conversie naar Profit 9.
- De berekeningen die bij het vullen van die lagen plaatsvinden.
- De populatie: welke medewerkers en dienstverbanden wel en niet in de tabel komen.
- De periode waarover we rekenen en de manier waarop we het venster bepalen.
- Het vulproces: de triggertabel, de wachtrijtaak vanuit de dagovergang, herberekening, correcties en de eenmalige vulling in de conversie.
- De KPI en de weergaven op de stamkaart medewerker in InSite.
- De landtoets waarmee het tabblad alleen wordt getoond bij medewerkers onder Nederlandse wetgeving (§9.6).
- De gegevensverzamelingen waarmee de nieuwe tabellen worden ontsloten voor weergaven, documenten en het dashboard, plus de uitbreiding van de bestaande verzameling op de brontabel.
- Autorisatie, privacy en de groepsgrootte voor vergelijkingscijfers.

Buiten scope:

- De wettelijke rapportage over loonverschillen op organisatieniveau en de 5%-signalering. Die horen bij DP2 – Rapportage. DP2 rapporteert over een afgesloten kalenderjaar en gebruikt daarvoor dezelfde tabellen met een eigen rapportageperiode. Welke velden daarvoor in fase 2 worden toegevoegd staat in §5.7; het bouwen ervan valt buiten dit ontwerp.
- Uitzendkrachten en de gegevensuitwisseling tussen in- en uitlener. Die horen bij DP3.
- Het type dossieritem waarmee een medewerker een vraag stelt. Dat is ontworpen in DP4 – Vraag aan HR.
- Het rapport of document "Loontransparantie medewerker", de Pocket- en OutSite-route en de jaarlijkse notificatie. Deze raakvlakken benoemen we op hoofdlijn in hoofdstuk 11; de uitwerking volgt later.
- Het opnieuw ontwerpen van de functiecategorie-inrichting. Dat is de basis uit Profit 8 en die nemen we als gegeven.

### 1.5 Uitgangspunten

We richten dit ontwerp in op basis van zes uitgangspunten:

1. **Voorberekenen boven live rekenen.** We slaan de uitkomsten op die de KPI en het dashboard nodig hebben. Bij het uitlezen wordt niet gerekend.
2. **Verdichten mag nooit informatie weggooien die we nog nodig hebben.** Uit een gemiddelde kun je niet betrouwbaar een nieuw gemiddelde afleiden. We bewaren daarom de gegevens per aangiftetijdvak, zodat het dashboard de vragen achter een KPI kan beantwoorden en een andere doorsnede alsnog mogelijk is. Verdichting komt daar bovenop, niet in de plaats van.
3. **Uitlegbaar boven compact.** Support en consultancy krijgen detailvragen over elke KPI. Het model moet zo zijn opgezet dat elk getoond getal herleidbaar is tot de onderliggende perioden en rubrieken.
4. **Actueel én vastgelegd.** De medewerker ziet altijd de actuele stand. Daarnaast moet het model een afgesloten kalenderjaar kunnen bevriezen, omdat de wettelijke rapportage dat vraagt. Wat er niet komt is een peildatumweergave waarmee je willekeurig kunt terugkijken naar een oude stand.
5. **Het salarisproces mag er geen last van hebben.** Het klaarzetten van de loonaangifte vult alleen de brontabel en signaleert dat er iets is gewijzigd; het rekenwerk gebeurt daarbuiten, in een aparte taak.
6. **Eén definitie, één berekening, één tabel.** Rekenen we over een andere periode, dan verschilt alleen de sleutel; niet de formule en niet de tabel. Daarmee bouwt DP2 verder op hetzelfde model in plaats van naast een eigen model.

---

## 2 Begrippen

> **Let op bij de term arbeidsverhouding.** Het begrippenkader loontransparantie en de wettelijke bronnen gebruiken **arbeidsverhouding** als rekeneenheid. Dat is in Profit de **inkomstenverhouding**. Profit kent daarnaast het veld **aard arbeidsverhouding** uit de loonaangifte (§3.3), en dat is iets heel anders: dat zegt wélk soort dienstbetrekking het is, niet om welke eenheid het gaat. Waar in dit document arbeidsverhouding staat, wordt steeds de inkomstenverhouding bedoeld; het loonaangiftekenmerk noemen we voluit aard arbeidsverhouding.
>
> Om dezelfde reden hanteren we consequent **soort inkomstenverhouding**. Het begrippenkader noemt dat kenmerk *soort arbeidsverhouding*, maar het is precies het veld dat in Profit soort inkomstenverhouding heet (§3.2). We nemen de bronterm niet over, omdat die in Profit naar het verkeerde veld wijst.

| Begrip | Betekenis in dit ontwerp |
| --- | --- |
| Recht op informatie | Het recht van een medewerker om het eigen loonniveau en het gemiddelde loonniveau per functiecategorie, uitgesplitst naar geslacht, op te vragen. |
| Loonniveau | Het loon uitgedrukt in twee eenheden tegelijk: het bruto jaarloon én het bijbehorende bruto uurloon. |
| Loonverschil | Het verschil tussen het gemiddelde loonniveau van mannen en dat van vrouwen, uitgedrukt als percentage van het gemiddelde van de mannen. De ministeriële regeling hanteert deze term; het wetsvoorstel en het begrippenkader spreken van loonkloof. |
| Mediaan | Het bedrag waarbij de ene helft van een groep meer verdient en de andere helft minder. Naast het gemiddelde een tweede maat voor het midden, die ongevoelig is voor enkele uitschieters. |
| Wettelijk loonverschil | Het loonverschil berekend op het bruto jaarloon. Dit is de maat die de nota van toelichting voorschrijft. |
| Aanvullend loonverschil | Het loonverschil berekend op het bruto uurloon. Deze maat schrijft de wet niet voor; we berekenen hem omdat hij corrigeert voor deeltijd. |
| Jaaruren | De som van de verloonde uren over het venster. |
| Bruto jaarloon | De som van het brutoloon over het venster. |
| Bruto uurloon | Het bruto jaarloon gedeeld door de jaaruren. Hiermee vangen we het deeltijdeffect op; er is geen aparte deeltijdcorrectie op het jaarloon. |
| Jaarwaarde variabele componenten | De som van de looncomponenten bovenop het basisloon over het venster, zoals toeslagen en bonussen. |
| Uurwaarde variabele componenten | De jaarwaarde variabele componenten gedeeld door de jaaruren. |
| Loonaangifte | De periodieke aangifte loonheffingen. Bron voor het brutoloon en voor de verloonde uren. |
| Inkomstenverhouding (IKV) | De eenheid waarop de loonaangifte in Profit is opgebouwd. Een medewerker kan er meerdere hebben. Meerdere dienstverbanden kunnen onder hetzelfde inkomstenverhoudingnummer vallen; dat doet zich voor bij subdienstverbanden in het onderwijs. |
| Kapstokdienstverband | Het dienstverband waaronder één of meer subdienstverbanden hangen. De loonaangifte wordt op het kapstokdienstverband gedaan, inclusief de loongegevens van de subdienstverbanden eronder. |
| Subdienstverband | Een dienstverband dat onder een kapstokdienstverband hangt. Komt vooral voor in het onderwijs, waar een medewerker meerdere aanstellingen naast elkaar heeft binnen één inkomstenverhouding. |
| Hoofddienstverband | Het dienstverband dat als hoofddienstverband is aangemerkt. Een medewerker heeft er altijd precies één. |
| Functiecategorie | De groepering van functies waarbinnen we medewerkers met elkaar vergelijken. Ingericht door de klant, op basis van Profit 8. |
| Toegekende functie | De functie die gold op de laatste dag van een aangiftetijdvak. Het loon over dat hele tijdvak wordt aan die functie toegekend (§4.5). |
| Arbeidsverhouding | De rekeneenheid voor de gemiddelden, afkomstig uit het begrippenkader. In Profit is dat de **inkomstenverhouding**: één arbeidsverhouding is één inkomstenverhouding, niet één persoon. Een medewerker met twee inkomstenverhoudingen telt dus twee keer mee. Wisselt een arbeidsverhouding binnen de rapportageperiode van functie, dan levert dat per functie een eigen regel op die elk als volwaardige arbeidsverhouding meetelt (§6.3). Niet te verwarren met het loonaangiftekenmerk aard arbeidsverhouding. |
| Aard arbeidsverhouding | Het loonaangiftekenmerk dat aangeeft om wélk soort dienstbetrekking het gaat, zoals een arbeidsovereenkomst of een publiekrechtelijke aanstelling (§3.3). Een populatiefilter dus, en niet de rekeneenheid hierboven. |
| Vergelijkingsgroep | De arbeidsverhoudingen waarmee het loonniveau van de medewerker wordt vergeleken: alle arbeidsverhoudingen in dezelfde functiecategorie, uitgesplitst naar geslacht. |
| Geslacht | Het geslacht zoals vastgelegd in de administratie van de werkgever. Het begrippenkader kent vier waarden: man, vrouw, X en niet ingevuld. Alleen man en vrouw gaan de vergelijkingscijfers in (§3.8). |
| Rapportageperiode | De afbakening waarover een complete set cijfers is berekend. Het rapportagejaar bepaalt welke: **0** is het voortschrijdende venster voor het recht op informatie, een jaartal is een afgesloten kalenderjaar voor de wettelijke rapportage (§5.2). |
| Venster | De rapportageperiode van dit ontwerp: de laatste twaalf maanden of de laatste dertien tijdvakken, afhankelijk van de periodetabel van de werkgever (§4.3). |
| Periodetabel | De indeling die bepaalt hoe lang een aangiftetijdvak is. Profit kent er acht; dit ontwerp ondersteunt maand, vier weken en week. |
| Land van wetgeving | Het land onder wiens wetgeving een medewerker valt. Profit legt dat per medewerker vast in het veld `AfasKnCountryByLaw`. Bepaalt of het tabblad Loontransparantie wordt getoond (§9.6). |
| Klaargezette loonaangifte | Een aangiftetijdvak waarvoor de werkgever de loonaangifte heeft klaargezet. Dit is het moment waarop de brontabel wordt gevuld en waarop er een triggerregel wordt weggeschreven. |
| Triggertabel | De technische tabel waarin wordt bijgehouden welke combinatie van werkgever, periodetabel, jaar en periode is geraakt en dus moet worden bijgewerkt (§7.2). |
| Triggerregel | Één regel in die tabel. Wordt weggeschreven bij het klaarzetten of intrekken van een loonaangifte, bij een functiewijziging en bij een wijziging in de functiecategorie-inrichting. |
| Wachtrijtaak | De taak **Bijwerken gegevens loontransparantie**, die de lagen 2 en 3 opnieuw samenstelt. Wordt vanuit de dagovergang Vernieuwen actuele gegevens gestart en kan daarna los opnieuw worden uitgevoerd. |
| Dagovergang | De geplande taak Vernieuwen actuele gegevens, die de klant doorgaans elke nacht laat draaien. |
| Correctieperiode | Een periode waarmee achteraf een eerdere periode wordt gecorrigeerd, mogelijk over de jaargrens heen. |
| RSIN | Het Rechtspersonen en Samenwerkingsverbanden Informatienummer, toegekend door de Kamer van Koophandel. Het nummer waarop de wettelijke rapportage plaatsvindt. Meerdere werkgevers kunnen onder hetzelfde nummer vallen. |
| Rapportage-eenheid | De groep werkgevers waarbinnen wordt vergeleken. Het RSIN uit het veld Fiscaal nummer op de organisatie; is dat leeg, dan de werkgever zelf (§5.2). |
| Loonaangifte uren per medewerker | De bestaande tabel met de loonaangiftegegevens per medewerker, dienstverband en aangiftetijdvak, uitgebreid met de loonbedragen. De feitenlaag van het model; in dit document ook wel de brontabel. |
| Loontransparantie per inkomstenverhouding | De tabel met per rapportageperiode, inkomstenverhouding en functie één regel met de waarden over de tijdvakken die aan die functie zijn toegekend. In dit document kort: de regel per inkomstenverhouding. |
| Loontransparantie per functiecategorie | De tabel met de gemiddelden en de loonverschilpercentages per rapportageperiode en functiecategorie, met mannen en vrouwen naast elkaar op één regel. In dit document kort: de tabel per functiecategorie. |
| Totaal | Het aantal arbeidsverhoudingen in een functiecategorie samen, inclusief die met geslacht X of zonder ingevuld geslacht. Het totaal is dus niet de som van mannen en vrouwen. Van de gemiddelden en de medianen is er geen totaal (§5.5). |

---

## 3 Populatie

### 3.1 Wat we vastleggen

We nemen in de tabel de medewerkers op die onder de loontransparantieverplichting vallen. Dat is niet iedereen die in de verloning voorkomt. In de loonadministratie zitten ook personen die wel worden verloond, maar die geen medewerker in de zin van de richtlijn zijn.

We leggen per medewerker elke relevante arbeidsverhouding apart vast. Heeft een medewerker meerdere inkomstenverhoudingen, dan levert dat meerdere regels op. We voegen die regels niet samen. Dat is nodig omdat de loonaangifte in Profit per inkomstenverhouding wordt opgebouwd en omdat DP2 op dat niveau moet kunnen rapporteren.

De inkomstenverhouding is ook de rekeneenheid voor de gemiddelden. Het begrippenkader definieert de arbeidsverhouding als de inkomstenverhouding, dus een medewerker met twee inkomstenverhoudingen telt twee keer mee in het aantal arbeidsverhoudingen. Dat is bovendien inhoudelijk juist: functie en standplaats kunnen per arbeidsverhouding verschillen, en de vergelijking gaat over de functiecategorie waarin het loon is verdiend.

De brontabel legt de gegevens vast per dienstverband. Meerdere dienstverbanden kunnen onder hetzelfde inkomstenverhoudingnummer vallen; de taak telt die bij het samenstellen van de regel per inkomstenverhouding bij elkaar op (§5.4). Dat speelt vooral in het onderwijs, waar subdienstverbanden onder één kapstokdienstverband hangen. Hoofdstuk 6 werkt dit uit. Wat de medewerker vervolgens op de KPI ziet, is een presentatiekeuze; die staat in hoofdstuk 8.

**Het kapstokdienstverband is leidend voor de kenmerken.** De loonaangifte wordt op het kapstokdienstverband gedaan, inclusief de loongegevens van de subdienstverbanden eronder. Wij volgen dat: de functie, de functiecategorie en de overige kenmerken op de regel per inkomstenverhouding komen van het kapstokdienstverband, en de loonbedragen en uren van alle dienstverbanden onder dezelfde inkomstenverhouding worden opgeteld.

Dat is bewust. De subdienstverbanden vormen samen één arbeidsverhouding in de zin van het begrippenkader; ze apart meetellen zou de medewerker meerdere keren in dezelfde vergelijkingsgroep zetten en het gemiddelde omlaag trekken, omdat elk deel op zichzelf een klein loon heeft. De keerzijde is dat een medewerker met sterk verschillende aanstellingen onder één kapstok in de functiecategorie van de kapstok valt. Dat is de indeling die de werkgever zelf heeft gemaakt.

### 3.2 Het filter op soort inkomstenverhouding

We nemen niet iedereen op die in de verloning voorkomt. In de loonadministratie zitten ook personen die wel worden verloond, maar die geen eigen medewerker zijn in de zin van de richtlijn.

We filteren op de **soort inkomstenverhouding**. Dat kenmerk wordt ook in de loonaangifte gebruikt, ligt dus altijd vast en is per dienstverband eenduidig. Er komt geen handmatige aanvinkmogelijkheid voor de klant.

Voor eigen medewerkers tellen deze soorten mee:

| Soort | Omschrijving |
| --- | --- |
| 11 | Loon/salaris ambtenaren in de zin van de Ambtenarenwet |
| 13 | Loon/salaris directeuren NV/BV verzekerd voor de werknemersverzekeringen |
| 15 | Loon/salaris niet hiervoor genoemde medewerkers |
| 17 | Loon/salaris directeuren NV/BV niet verzekerd voor de werknemersverzekeringen |

Alle andere soorten vallen af. Daarmee blijven onder meer uitkeringen, pensioenen, wachtgeld en flexmedewerkers buiten de dataset.

Twee dingen zijn hierbij het opmerken waard:

- **Directeuren tellen wel mee**, zowel verzekerd (13) als niet verzekerd voor de werknemersverzekeringen (17). Een directeur-grootaandeelhouder valt daarmee binnen de populatie.
- **Dit filter geldt voor eigen medewerkers.** Voor uitzendkrachten geldt een eigen afbakening; die wordt in DP3 uitgewerkt.

Deze selectie sluit aan bij het begrippenkader loontransparantie, dat bij hetzelfde kenmerk dezelfde vier soorten inkomen noemt. Het kader spreekt daar van *soort arbeidsverhouding*; wij houden de Profit-term **soort inkomstenverhouding** aan (zie de opmerking bij hoofdstuk 2).

### 3.3 Het filter op aard arbeidsverhouding

De soort inkomstenverhouding alleen is niet genoeg. Soort 15 is breed en laat ook fictieve dienstbetrekkingen door, zoals musicus, deelvisser, thuiswerker en uitzendkracht. Die horen niet tot de eigen medewerkers in de zin van de richtlijn.

We filteren daarom ook op de **aard van de arbeidsverhouding**. Alleen arbeidsovereenkomsten naar burgerlijk recht tellen mee, aangevuld met de publiekrechtelijke aanstelling. Voor eigen medewerkers zijn dat deze codes:

| Aard | Omschrijving |
| --- | --- |
| 1 | Arbeidsovereenkomst, exclusief BBL |
| 18 | Publiekrechtelijke aanstelling |
| 21 | WSW beschut werk |
| 23 | WSW begeleid werk |
| 24 | Participatiewet beschut werk |
| 83 | Beroepspraktijkopleiding van de beroepsbegeleidende leerweg (BBL) |

Alle andere aarden vallen af. Daarmee verdwijnen onder meer musicus of artiest (6), stagiair (7), deelvisser (4), thuiswerker (8), uitzendkracht (11), payrolling (82) en de overige fictieve dienstbetrekkingen (81) uit de dataset.

De codes 11 (uitzendkracht), 22 (WSW detachering bij een reguliere werkgever) en 82 (payrolling) horen bij de uitzendketen. Die worden in DP3 opgepakt, bij de inlener in plaats van bij de uitlener.

Ook deze selectie volgt het begrippenkader loontransparantie.

### 3.4 Aanvullende selectiecriteria

Het begrippenkader stelt bij dezelfde selectie nog twee eisen: het loon moet groter dan nul zijn en het aantal verloonde uren moet groter dan nul zijn. We nemen die over. Een arbeidsverhouding zonder loon of zonder verloonde uren levert geen zinvol loonniveau op en zou de gemiddelden in de vergelijkingsgroep vertekenen.

We passen deze eisen toe op het venster als geheel, niet per tijdvak. Een medewerker die één tijdvak zonder uren had maar de rest van het jaar wel, telt dus gewoon mee.

### 3.5 Wanneer we het filter toepassen

De twee filters uit §3.2 en §3.3 werken op een ander niveau dan de twee eisen hierboven.

**Soort inkomstenverhouding en aard arbeidsverhouding toetsen we per tijdvak.** De brontabel legt beide vast per aangiftetijdvak, en een medewerker kan er binnen het venster van wisselen — bijvoorbeeld van een BBL-overeenkomst naar een gewone arbeidsovereenkomst. Alleen de tijdvakken waarin de arbeidsverhouding kwalificeert tellen mee in de bedragen en de uren.

Dat is nauwkeuriger dan één keer toetsen op de stand aan het einde van het venster. Zouden we dat doen, dan telt bij een wisseling loon mee uit tijdvakken waarin de medewerker niet onder de regeling viel, of valt loon weg uit tijdvakken waarin dat juist wel zo was.

**Loon en uren toetsen we over het venster als geheel**, zoals hierboven beschreven. Die twee eisen gaan over de vraag of er een zinvol loonniveau te berekenen valt, en dat is een eigenschap van het totaal.

Op de regel per inkomstenverhouding leggen we de soort en de aard vast zoals ze aan het einde van het venster golden (§5.4). Dat is een kenmerk voor herleidbaarheid en niet de waarde waarop is gefilterd. Wisselde iemand binnen het venster, dan kan de vastgelegde waarde dus afwijken van de waarde waarmee een deel van de tijdvakken is meegeteld.

### 3.6 Medewerkers die niet het hele jaar meetellen

Het venster van twaalf maanden loopt niet voor iedereen vol. Iemand kan halverwege in dienst zijn gekomen, uit dienst zijn gegaan of tussentijds van werkgever zijn gewisseld.

Voor het wisselen van werkgever is de oplossing al bepaald: werkgever zit in de sleutel, zodat gegevens van de ene werkgever niet worden overschreven door die van de andere.

We nemen een medewerker mee zolang er binnen het venster loon is verwerkt. Iemand die in de derde maand van het venster uit dienst ging, telt dus mee met het loon dat die persoon in het venster heeft gehad. Zo blijft de vergelijkingsgroep compleet en missen we geen collega's die een groot deel van het jaar wel meetelden.

Dit betekent dat het bruto jaarloon van zo'n medewerker lager uitvalt dan dat van iemand die het hele venster in dienst was. Dat werkt door in het wettelijke loonverschil, dat op het bruto jaarloon wordt berekend. Juist daarom berekenen we daarnaast het aanvullende loonverschil op het bruto uurloon; dat corrigeert vanzelf voor een korter dienstverband en voor deeltijd. Hoe we daarmee omgaan in de vergelijkingscijfers werken we uit in hoofdstuk 6.

### 3.7 Medewerkers zonder functiecategorie

De functiecategorie-inrichting is de verantwoordelijkheid van de klant. Er zullen medewerkers zijn met een functie die nog niet aan een categorie is gekoppeld.

We nemen deze medewerkers gewoon op in de tabellen. Hun eigen loongegevens worden berekend en vastgelegd. Alleen de vergelijkingscijfers blijven leeg, want er is geen groep om mee te vergelijken. Op de stamkaart tonen de KPI's daardoor niets.

We signaleren dit niet aan de klant. Een functie zonder categorie valt eenvoudigweg nergens onder; het gevolg is zichtbaar doordat de medewerker geen loonverschilcijfers ziet. De klant bepaalt zelf of en wanneer hij de functiecategorie-inrichting compleet maakt. Doet hij dat, dan werkt het bij de eerstvolgende dagovergang door: een wijziging in de functiecategorie-inrichting laat alle werkgevers opnieuw doorrekenen (§7.2).

### 3.8 Medewerkers met geslacht X of zonder ingevuld geslacht

De vergelijkingscijfers zijn uitgesplitst naar man en vrouw. Het begrippenkader kent bij geslacht vier waarden — man, vrouw, X en niet ingevuld — maar rekent uitsluitend met de groep die als man is gekenmerkt en de groep die als vrouw is gekenmerkt. Medewerkers die zich als non-binair hebben laten registreren en medewerkers bij wie het geslacht niet is ingevuld vallen daarmee buiten beide groepen.

Dat is een bewuste keuze van de wetgever. De memorie van toelichting stelt dat de richtlijn is gericht op gelijk loon voor mannen en vrouwen en dat werkgevers niet hoeven te rapporteren over de loonverschillen van non-binaire personen. Het recht op informatie geldt voor hen wél: de toelichting schrijft dat een non-binaire medewerker om een vergelijking met **zowel de groep mannen als de groep vrouwen** binnen de categorie kan vragen.

Wij volgen dat zo:

- Deze medewerkers komen gewoon in de tabellen en zien hun eigen loongegevens: jaaruren, bruto jaarloon, bruto uurloon en de jaar- en uurwaarde variabele componenten.
- De kolommen Mannen en Vrouwen en de vier KPI-tegels zijn voor hen gewoon zichtbaar. Ze krijgen daarmee ongevraagd de vergelijking met beide groepen, precies wat de toelichting als recht beschrijft. Er is dus geen keuze te maken en niets extra's aan te vragen.
- Ze tellen niet mee in de gemiddelden per geslacht en niet in de loonverschilpercentages, omdat ze in geen van beide groepen vallen. Zo blijven die cijfers zuiver en sluiten ze aan op de wettelijke rapportage van DP2.
- Ze tellen wél mee in het totale aantal arbeidsverhoudingen van de functiecategorie (§5.5). Dat totaal is daardoor niet de som van mannen en vrouwen.

**We faciliteren geen keuze om als man of vrouw te worden meegeteld.** De toelichting laat toe dat iemand die zich als non-binair heeft geregistreerd zelf aangeeft in welke groep hij voor de rapportage wil meetellen, en verbiedt de werkgever om dat af te dwingen. Wij leggen die keuze niet vast: er komt geen extra veld en geen extra vraag aan de medewerker. Het geslacht in de administratie is leidend. AFAS heeft in de verdiepingssessie met het ministerie aangegeven deze constructie onwenselijk te vinden, omdat ze de medewerker dwingt zich alsnog als man of vrouw te positioneren en de werkgever extra administratie oplevert.

We tonen hierover geen aparte melding op de stamkaart. De medewerker ziet dezelfde tabel als iedereen, alleen zonder een groep waarin hij zichzelf terugvindt. Of daar tekst bij hoort is punt H3 in §12.

---

## 4 Periode en venster

### 4.1 Terugkijktermijn: twaalf maanden

We rekenen steeds over de laatste twaalf maanden. Dat is een voortschrijdend venster, geen kalenderjaar.

De wet legt voor het recht op informatie geen vaste referentieperiode vast. Voor de wettelijke rapportage in DP2 ligt het voorgaande kalenderjaar wél vast. Door hier voor twaalf voortschrijdende maanden te kiezen, krijgt de medewerker een actueel beeld in plaats van cijfers die tot anderhalf jaar oud kunnen zijn.

### 4.2 Eindpunt: het laatste klaargezette aangiftetijdvak

Het venster eindigt bij het laatste aangiftetijdvak waarvoor de werkgever de loonaangifte heeft klaargezet. Vanaf dat punt tellen we twaalf maanden terug.

Dat moment is bewust gekozen. De brontabel wordt op precies dat moment gevuld met de waarden die aan de Belastingdienst zijn gemeld. Zouden we het accorderen van de salarisverwerking als eindpunt nemen, dan zou het venster verder lopen dan de gegevens reiken.

We gebruiken bewust niet het tijdvak waarop een correctie betrekking heeft. Een correctie kan over de jaargrens gaan en raakt vaak maar een kleine groep medewerkers. Corrigeert een werkgever periode 12 van 2025 terwijl periode 3 van 2026 al is klaargezet, dan blijft periode 3 van 2026 het eindpunt. De correctie telt wel mee in de bedragen, maar verschuift het venster niet.

Het eindpunt geldt per werkgever. Werkgevers binnen dezelfde omgeving kunnen dus op verschillende perioden staan.

### 4.3 Het venster per periodetabel

De brontabel legt de gegevens per aangiftetijdvak vast, en de **periodetabel** van de werkgever bepaalt hoe lang zo'n tijdvak is. Profit kent acht periodetabellen. Wij ondersteunen er drie:

| Periodetabel | Venster | Aantal tijdvakken |
| --- | --- | --- |
| Maand | De laatste twaalf maanden | 12 |
| Vier weken | De laatste dertien perioden | 13, of 14 in een jaar met een restperiode |
| Week | De laatste tweeënvijftig weken | 13, of 14 in een jaar met een restperiode |

**Dertien perioden is geen aparte periodetabel.** Dat is het aantal tijdvakken dat de vierwekentabel per jaar oplevert. In eerdere versies van dit document stond het als vierde indeling; dat was onjuist.

**De vijf overige periodetabellen vallen buiten scope.** Jaar, halfjaar, kwartaal, twee weken en halve maand ondersteunen we niet. Voor werkgevers met zo'n tabel bouwen we geen venster op en blijven de tabellen leeg; de medewerker ziet de melding uit §8.6. Twaalf maanden zijn daar wel uit af te leiden, maar elke variant vraagt een eigen omrekenregel en eigen testgevallen, terwijl deze tabellen in de salarisadministratie zeldzaam zijn. Blijkt in de praktijk dat een van de vijf toch voorkomt, dan is dat een uitbreiding van deze tabel en niet van het model.

Bij weekverloning groeperen we de weken naar perioden van vier weken, terugtellend vanaf het laatste klaargezette tijdvak. Zo krijgt een weekverloner dezelfde periodestructuur als een vierwekenverloner en snijden we nooit een week doormidden. Groeperen naar kalendermaand zou dat wel doen, omdat weken over maandgrenzen heen lopen.

**De 53e week.** Een jaar telt niet altijd 52 weken. Profit vangt dat op met een restperiode aan het einde van de vierwekentabel; het veld Week53Processing op de periodetabel bepaalt hoe die wordt verwerkt. Valt zo'n restperiode binnen het venster, dan telt hij mee als extra tijdvak. Het venster beslaat dan veertien tijdvakken in plaats van dertien.

Dat is bewust. Zouden we altijd dertien tijdvakken terugtellen, dan mist een weekverloner in zo'n jaar precies één week loon terwijl de uren wel zijn verantwoord. Het bruto uurloon blijft dan kloppen, maar het bruto jaarloon — de wettelijke grondslag — valt te laag uit.

Elk venster beslaat daarmee ongeveer een jaar, waardoor de uitkomsten tussen werkgevers met verschillende periodetabellen vergelijkbaar blijven. De periodetabel leggen we op de regel vast, zodat altijd herleidbaar is hoe het venster is bepaald.

**Meerdere periodetabellen bij één werkgever.** Een werkgever kan maandbetaalden en weekbetaalden naast elkaar hebben. Het laatste klaargezette tijdvak wordt dan per periodetabel bepaald, en dus ook het venster. Twee medewerkers bij dezelfde werkgever kunnen daardoor een venster hebben dat op een andere datum eindigt. Wat dat betekent voor de rapportageperiode staat in §5.2.

### 4.4 De jaargrens

Een venster van twaalf maanden loopt bijna altijd over twee kalenderjaren. Voor de berekening maakt dat niets uit. De brontabel legt de bedragen per aangiftetijdvak vast, precies zoals ze aan de Belastingdienst zijn gemeld. De taak leest de tijdvakken van beide jaren en telt ze op.

Er is dus geen inrichting die over de jaargrens heen vergelijkbaar moet zijn. Dat zou anders liggen als we de bedragen uit lijstbegrippen zouden halen: die worden per kalenderjaar ingericht en een klant kan die inrichting tussen twee jaren wijzigen. Omdat we rechtstreeks de loonaangifterubrieken gebruiken, speelt dat niet.

### 4.5 De functie per aangiftetijdvak

De loonrekening in Profit is niet per functie opgebouwd, maar per inkomstenverhouding. De functie is bovendien geen onderdeel van de loonaangifte en staat dus niet in de brontabel. Voor dit ontwerp moeten we toch bepalen bij welke functie het loon hoort.

**We bepalen de functie per aangiftetijdvak, op de laatste dag van dat tijdvak.** Het loon over dat hele tijdvak wordt aan die functie toegekend. Wisselt iemand halverwege een tijdvak van functie, dan verdelen we het loon binnen dat tijdvak niet naar rato; het gaat volledig naar de functie waarin de medewerker het tijdvak afsloot.

Wisselt iemand binnen het venster van functie, dan worden de tijdvakken daarmee over twee of meer functies verdeeld. Laag 2 groepeert op die functie en schrijft per functie een eigen regel, met alleen de bedragen en uren van de tijdvakken die aan die functie zijn toegekend (§5.4). Het loon telt dus niet dubbel: het wordt verdeeld, niet gekopieerd.

**Dit herziet de eerdere keuze om de functie ultimo venster te bepalen.** Die keuze schoof het loon uit de oude functie mee naar de nieuwe functiecategorie. Bij een promotie of een overstap naar een heel ander vak vertekent dat precies de categorie waarover het loonverschil wordt berekend: het lagere loon uit de oude functie drukt het gemiddelde van de nieuwe categorie, terwijl de oude categorie een deelnemer mist die er wel degelijk loon heeft verdiend. Met de toekenning per tijdvak landt elk bedrag in de categorie waarin het is verdiend.

De prijs is dat een arbeidsverhouding binnen één venster in twee functiecategorieën kan vallen. Die regels tellen elk als volwaardige arbeidsverhouding mee in de vergelijkingscijfers (§6.3), met een bruto jaarloon over minder dan twaalf tijdvakken. Wat dat betekent voor de gemiddelden staat in §6.8; welke regel de medewerker op de stamkaart ziet, staat in §8.5.

De functiecategorie hoort bij de functie. We nemen daarvoor de koppeling zoals die op de laatste dag van de rapportageperiode geldt, zodat een herindeling van functiecategorieën meteen over de hele periode doorwerkt en niet leidt tot regels die deels in de oude en deels in de nieuwe indeling vallen.

De overige kenmerken die binnen het venster kunnen wijzigen — geslacht, soort inkomstenverhouding en aard arbeidsverhouding — blijven een momentopname op het einde van de rapportageperiode (§5.4).

---

## 5 Gegevensmodel: Recht op informatie

### 5.1 Opzet in vier lagen

Het model bestaat uit vier lagen. De onderste drie zijn elk een verdichting van de laag eronder; de bovenste laag legt vast **waarover** is gerekend.

| Laag | Wat erin staat | Niveau uit ON-09 | Waarvoor |
| --- | --- | --- | --- |
| 0. Rapportageperiode | Per rapportage-eenheid de afbakening waarover een complete set cijfers is berekend | N5 | Onderscheid tussen het venster en een afgesloten kalenderjaar, en de status daarvan |
| 1. Loonaangifte uren per medewerker | Per werkgever, medewerker, dienstverband en aangiftetijdvak de gemelde loonaangiftegegevens | N1 | Herleidbaarheid, dashboardanalyses en het opnieuw samenstellen van de lagen erboven |
| 2. Loontransparantie per inkomstenverhouding | Per rapportageperiode, inkomstenverhouding en functie de waarden over de tijdvakken die aan die functie zijn toegekend | N2 | De eigen waarden van de medewerker op de stamkaart |
| 3. Loontransparantie per functiecategorie | Per rapportageperiode en functiecategorie de gemiddelden, de aantallen en de loonverschilpercentages, met mannen en vrouwen naast elkaar | N3 en N4 | De vergelijkingscijfers en de KPI's op de stamkaart |

De kolom **Niveau uit ON-09** legt de koppeling met het onderzoek naar het begrippenkader. Op één punt wijken we daar bewust van af: ON-09 adviseert het groepsaggregaat (N3) te berekenen en niet op te slaan. Wij slaan het wél op, omdat de KPI anders bij elke pagina-opening over de hele functiecategorie moet optellen en omdat DP2 een bevroren stand nodig heeft. Dat volgt uitgangspunt 1: voorberekenen boven live rekenen. Het stamgegeven arbeidsjaareenheid uit fase 2 is niveau N0.

**Waarom er een vierde laag boven zit.** Het verschil tussen dit ontwerp en de wettelijke rapportage van DP2 is geen verschil in gegevens, maar in afbakening: hetzelfde bruto jaarloon van dezelfde arbeidsverhouding, één keer gemeten over een voortschrijdend venster en één keer over een kalenderjaar. Zetten we het venster vast in de tabelstructuur, dan past die tweede afbakening er niet naast en heeft DP2 een eigen model nodig. Door de rapportageperiode een gegeven te maken in plaats van een aanname, is één model genoeg.

In dit ontwerp — fase 1 — bestaat er per rapportage-eenheid precies één rapportageperiode, met rapportagejaar 0. In fase 2 komen daar rapportageperioden met een gevuld rapportagejaar bij. Dat vraagt geen nieuwe tabellen en geen sleutelwijziging, alleen extra regels en extra velden. Per veld is hieronder aangegeven in welke fase het wordt gevuld.

We slaan de brongegevens per aangiftetijdvak op en niet alleen het venstertotaal. De reden is dat verdichting informatie weggooit die we niet kunnen terughalen: uit een gemiddelde is geen nieuw gemiddelde af te leiden zonder rekenfouten, en een andere doorsnede is dan niet meer te maken. Het dashboard moet juist de vragen achter een KPI kunnen beantwoorden, zoals of een verschil samenhangt met dienstjaren, of het in bepaalde perioden piekt en wat er gebeurde na een functiewijziging. Dat kan alleen met gegevens per tijdvak. Omdat we daarvoor een bestaande tabel gebruiken, kost dat ons alleen de extra kolommen.

De tabel per functiecategorie ligt er bovenop voor performance en voor de uitlegbaarheid. De KPI leest daaruit één regel per functiecategorie en rekent zelf niets uit. Zonder die laag zou elke pagina-opening over de hele functiecategorie moeten optellen.

### 5.2 Laag 0: rapportageperiode

Een rapportageperiode beschrijft één afbakening waarover een complete set cijfers is berekend. De lagen 2 en 3 hangen eraan; laag 1 niet, want dat zijn feiten en geen perspectief.

**Sleutel**

| Onderdeel | Fase 1 | Fase 2 |
| --- | --- | --- |
| Soort rapportage-eenheid | RSIN als het veld Fiscaal nummer gevuld is, anders Werkgever | Idem |
| Rapportage-eenheid | Is het veld Fiscaal nummer gevuld, dan het RSIN uit dat veld; is het leeg, dan de werkgeverscode | Idem |
| Rapportagejaar | Altijd 0 | 0 voor het venster, een jaartal voor de rapportage |
| Volgnummer | Altijd 1 | Loopt op bij een correctie na vaststelling |

**Het rapportagejaar bepaalt de soort.** Er is géén apart sleutelonderdeel Soort rapportageperiode. Een rapportagejaar van **0** betekent het voortschrijdende venster van dit ontwerp; elk ander getal is een afgesloten kalenderjaar voor de wettelijke rapportage.

Soort en jaartal zouden anders één op één aan elkaar vastzitten — een kalenderjaar heeft altijd een jaartal, een venster nooit — en dan is het soort afleidbaar. Erger nog: met twee velden kan de combinatie ook fout staan, zoals soort Kalenderjaar zonder jaartal. Met één veld kan dat niet.

In de tekst blijven we spreken van **vensterregels** en **kalenderjaarregels**. Dat zijn leesbegrippen, afgeleid uit het rapportagejaar, en geen opgeslagen gegeven.

**De rapportage-eenheid: normaal het RSIN, anders de werkgever**

De wettelijke rapportage gaat per RSIN, en dat is ook het niveau waarop wij vergelijken (§6.3). Voor de rapportage is dat geen probleem: elke rechtspersoon en elk samenwerkingsverband krijgt bij inschrijving een RSIN, en de organisaties die er geen hebben — eenmanszaken — halen de grens van honderd werknemers niet.

Het **recht op informatie** kent die grens niet. Dat geldt voor elke medewerker, bij elke werkgever, ongeacht organisatiegrootte. We moeten dus ook een werkgever zonder RSIN kunnen bedienen, met hetzelfde model en dezelfde bronnen.

Daarom bestaat de sleutel uit twee delen: het **soort** rapportage-eenheid en de **waarde**.

| Situatie | Soort | Waarde |
| --- | --- | --- |
| Het veld Fiscaal nummer is gevuld | RSIN | Het RSIN uit dat veld |
| Het veld Fiscaal nummer is leeg | Werkgever | De werkgeverscode |

Het RSIN lezen we uit het veld **Fiscaal nummer** op de organisatie die bij de werkgever hoort. Profit kent dat veld al, met een eigen elfproefcontrole. Is het gevuld, dan is het soort RSIN en vallen alle werkgevers met datzelfde nummer in één groep. Is het leeg, dan is het soort Werkgever en vormt die werkgever zijn eigen groep.

**We dwingen het vullen van het Fiscaal nummer niet af.** Het veld is vandaag niet verplicht en dat laten we zo. Er komt geen validatie, geen conversie die het aanvult en geen signaal dat het ontbreekt. Klanten hoeven hun organisatiegegevens dus niet aan te passen om het recht op informatie te kunnen bieden.

Dat betekent dat een organisatie die in werkelijkheid wél een RSIN heeft, maar het niet in Profit heeft vastgelegd, behandeld wordt als een organisatie zonder RSIN: het RSIN blijft leeg en we groeperen op de werkgever, net als bij een eenmanszaak. De medewerker krijgt dan gewoon vergelijkingscijfers, alleen over een kleinere groep: de eigen werkgever in plaats van alle werkgevers van het concern. Wil een klant die bredere vergelijking, dan vult hij het Fiscaal nummer alsnog en werkt dat door bij de volgende run van de taak.

Voor de wettelijke rapportage in DP2 ligt dat anders: daar is het RSIN de sleutel van de aanlevering en zal het vullen wel een voorwaarde zijn. Dat vraagstuk hoort bij DP2 en niet hier.

**We laten het nummer niet leeg.** Zouden we dat wel doen, dan zouden alle werkgevers zonder ingevuld Fiscaal nummer in één en dezelfde vergelijkingsgroep terechtkomen. De lonen van niet-verwante organisaties zouden dan in hetzelfde gemiddelde worden getrokken, en dat levert cijfers op die niets betekenen en bovendien loongegevens van de ene klantadministratie zichtbaar maken in de andere.

**We leiden het nummer ook niet af uit het loonheffingsnummer.** Dat lijkt aantrekkelijk, want de eerste negen posities daarvan zijn het fiscale nummer en bij een eenmanszaak is dat altijd gevuld. Maar bij een eenmanszaak zijn die negen posities het **burgerservicenummer** van de ondernemer, en een BSN en een RSIN zijn niet van elkaar te onderscheiden: beide zijn negencijferige nummers met dezelfde elfproef. Wie altijd het loonheffingsnummer gebruikt, slaat dus ongemerkt BSN's op in een veld dat RSIN heet. Dat willen we niet, om drie redenen:

- Een BSN mag alleen worden verwerkt waar dat wettelijk is voorgeschreven. De loonaangifte is zo'n grondslag; een groeperingssleutel in een loontransparantietabel is dat niet.
- Het veld staat in laag 0 en laag 3, en die zijn ontsloten via weergaven, gegevensverzamelingen en Power BI (§9.2). Een BSN in een veld dat RSIN heet wordt daar door niemand als BSN herkend en dus nergens afgeschermd.
- In fase 2 is dit veld de sleutel van de aanlevering aan het monitoringsorgaan. De memorie van toelichting merkt het BSN expliciet aan als identificerend nummer dat niet openbaar wordt gemaakt, ook niet van iemand met een eenmanszaak.

Het soort rapportage-eenheid maakt bovendien zichtbaar waaróp is gegroepeerd. Staan er twee kleine werkgevers naast elkaar die niet in één groep zitten, dan is aan het soort te zien waarom.

**Subheffingsnummers.** Een RSIN kan meerdere loonheffingsnummers hebben, die alleen in het subnummer achter de L verschillen. Die horen bij dezelfde rapportage-eenheid; het begrippenkader schrijft voor dat subheffingsnummers met het hoofdheffingsnummer worden samengevoegd. Omdat wij op het Fiscaal nummer van de organisatie groeperen en niet op het loonheffingsnummer, gebeurt dat vanzelf — mits dat veld is gevuld.

**Velden**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Begindatum | Datum | 1 | Vanaf wanneer is gerekend. Bij een venster indicatief: het eindpunt verschilt per werkgever én per periodetabel, dus één datum kan niet voor alle regels kloppen. De exacte grenzen staan op de regel per inkomstenverhouding. |
| Einddatum | Datum | 1 | Tot en met wanneer is gerekend. Om dezelfde reden indicatief. We nemen de **laatste** einddatum die binnen de eenheid voorkomt, zodat zichtbaar is tot hoe ver de gegevens reiken. |
| Aantal arbeidsverhoudingen totaal | Getal | 1 | Alle regels per inkomstenverhouding in deze rapportageperiode, ook die zonder functiecategorie. Groter dan of gelijk aan de som van de totalen op laag 3 (§6.7). |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze rapportageperiode voor het laatst heeft samengesteld. |
| Status rapportageperiode | Code | 2 | In bewerking, vastgesteld, ingediend of gecorrigeerd. |
| Aantal medewerkers in fte | Getal | 2 | De som van de jaaruren gedeeld door de arbeidsjaareenheid (§6.7). Bepaalt of en hoe vaak de werkgever rapportageplichtig is. |

Wie een kalenderjaar heeft vastgesteld en wanneer, leggen we niet in eigen velden vast. Daarvoor gebruiken we de standaard loggingvelden.

Deze laag levert drie dingen op die het model anders niet heeft: een vensterstand en een jaarstand die naast elkaar bestaan, historie doordat elk rapportagejaar een eigen rapportageperiode is, en versiebeheer op de plek waar het hoort. Ook het opschonen wordt er eenvoudiger van: een rapportageperiode verwijderen is de hele set verwijderen.

### 5.3 Laag 1: Loonaangifte uren per medewerker

Hiervoor gebruiken we de **bestaande tabel Loonaangifte uren per medewerker** (`AfasHrTaxHoursPerEmployee`). Die legt per medewerker, dienstverband en aangiftetijdvak vast wat er in de loonaangifte is gemeld, en bestaat sinds de invoering van de WAB. Granulariteit, vastlegmoment en bronvastheid passen bij wat dit ontwerp nodig heeft, dus we bouwen geen eigen tabel.

**Sleutel** — ongewijzigd: werkgever, periodetabel, jaar, periode, medewerker en volgnummer dienstverband.

De rapportageperiode zit **niet** in deze sleutel. Deze laag bevat feiten uit de loonaangifte, geen perspectief. Zowel de vensterstand als een latere jaarstand leest dezelfde regels.

Het **dienstverband** is het fijnste niveau in de sleutel; het inkomstenverhoudingnummer staat als kenmerk op de regel, in het bestaande veld Inkomstenverhoudingnummer. Per dienstverband en tijdvak is er precies één regel, en op die regel is het inkomstenverhoudingnummer eenduidig.

Andersom kunnen meerdere dienstverbanden wél onder hetzelfde inkomstenverhoudingnummer vallen. Dat doet zich voor bij subdienstverbanden, vooral in het onderwijs: de loonaangifte wordt gedaan op het kapstokdienstverband, inclusief de loongegevens van de subdienstverbanden eronder. Laag 2 groepeert daarom op inkomstenverhouding en telt de dienstverbanden daarbinnen op (§5.4). Voor de kenmerken — en dus voor de functie — volgt laag 2 het kapstokdienstverband (§3.1). Het dienstverbandnummer blijft beschikbaar om aanvullende gegevens mee op te halen.

De **functie staat niet in deze laag**. De functie is geen onderdeel van de loonaangifte, dus we leggen hem hier niet vast. De taak bepaalt hem bij het samenstellen van laag 2 uit de dienstverband- en functiehistorie, per aangiftetijdvak (§4.5).

**Velden die er al in staan**

| Veld | Kolom | Gebruik in dit ontwerp |
| --- | --- | --- |
| Werkgever | `AfasHrEmployerId` | Selectie |
| Loonheffingsnummer | `AfasHrTaxNumber` | Selectie. De rapportage-eenheid bepalen we niet hieruit maar uit het veld Fiscaal nummer op de organisatie (§5.2) |
| Periodetabel | `AfasHrPeriodTableId` | Bepaalt het venster |
| Jaar | `AfasHrYear` | Bepaalt het venster |
| Periode | `AfasHrPeriodSeqNo` | Bepaalt het venster |
| Medewerker | `AfasKnEmployeeId` | Sleutel |
| Volgnummer dienstverband | `AfasHrEmploymentSeqNo` | Sleutel |
| Inkomstenverhoudingnummer | `AfasHrUserEmploymentSeqNo` | De rekeneenheid voor laag 2 en 3 |
| Soort inkomstenverhouding | `AfasHrSrtIV` | Populatiefilter (§3.2) |
| Aard arbeidsverhouding | `AfasHrCdAard` | Populatiefilter (§3.3) |
| Verwerkte uren | `AfasHrAantVerlU` | De verloonde uren; de noemer van het uurloon |
| Contracturen per week | `AfasHrAantCtrcturenPWk` | Duiding en controle |
| Contracturen per aangiftetijdvak | `AfasHrContractHoursPerPeriod` | Duiding en controle |
| Kalenderdagen | `AfasHrCalenderDays` | Duiding bij een tijdvak dat niet volledig is gevuld |
| Onbepaalde tijd | | Niet gebruikt in dit ontwerp; blijft staan voor de WAB |
| Schriftelijke arbeidsovereenkomst | | Niet gebruikt in dit ontwerp; blijft staan voor de WAB |
| Oproepovereenkomst | | Niet gebruikt in dit ontwerp; blijft staan voor de WAB |

Het veld Verwerkte uren draagt dat label, maar wordt gevuld met de loonaangifterubriek aantal verloonde uren. Dat is precies de noemer die we nodig hebben. De aard en de soort worden bepaald op de eerste inkomstenperiode binnen het tijdvak; bij een wijziging halverwege legt de tabel dus de situatie aan het begin van het tijdvak vast.

**Velden die we toevoegen**

De tabel bevat nu alleen uren en contractkenmerken. Voor het loonniveau voegen we de zeven ontbrekende bedragen uit §6.2 toe.

De waarden komen **niet uit lijstbegrippen**, maar uit de vastgelegde loonaangiftegegevens per medewerker in de tabel **`AfasHrTaxEmployee`**. Die tabel wordt bij het opbouwen van het aangiftebericht gevuld met exact de bedragen die aan de Belastingdienst worden gemeld. De rubrieknummers hieronder benoemen alleen wélk gegeven het is; het overnemen zelf gaat kolom voor kolom.

| Toe te voegen veld | Rubriek | Bronkolom in `AfasHrTaxEmployee` | Veld-ID |
| --- | --- | --- | --- |
| Loon LB/PH normaal tarief | 1287 | `AfasHrBasisTaxNT` | `BaTN` |
| Loon LB/PH bijzonder tarief | 1287, deel bijzonder tarief | `AfasHrBasisTaxBT` | `BaTB` |
| Vakantiebijslag | 1317 | `AfasHrHollidayPay` | `Holl` |
| Opgebouwd recht vakantiebijslag | 1318 | `AfasHrHollidayPayRight` | `HlRi` |
| Waarde niet in geld uitgekeerd loon | 1321 | `AfasHrPayNotInMoney` | `HlPN` |
| Opname arbeidsvoorwaardenbedrag | 5068 | `AfasHrOpnAvwb` | `OpAv` |
| Opbouw arbeidsvoorwaardenbedrag | 5069 | `AfasHrOpbAvwb` | `ObAv` |

Het loon LB/PH uit de formules in §6.1 is de som van het normale en het bijzondere tarief. Door beide apart vast te leggen hebben we zowel dat totaal als het deel bijzonder tarief, zonder een bedrag twee keer op te slaan. De correctie kunstenaar en sporter (1670) is in deze bedragen al verwerkt en heeft dus geen eigen kolom.

Het aantal verloonde uren staat er al in en hoeft niet te worden toegevoegd. Het bestaande veld Verwerkte uren (`AfasHrAantVerlU`) wordt gevuld uit `AfasHrPaydHours` (veld-ID `PyHr`) van diezelfde brontabel, en dat is precies de noemer die we voor het uurloon nodig hebben.

Alle zeven bedragen zijn op het moment van klaarzetten al beschikbaar; er is geen extra berekening en geen extra bron nodig. De uitbreiding volgt hetzelfde pad als de velden die er nu al in worden gezet, en gebeurt dus **direct bij het klaarzetten van de loonaangifte**. Bij bestaande klanten worden deze zeven velden over 2026 eenmalig gevuld in de conversie naar Profit 9 (§7.7).

**Wat we bewust niet toevoegen**

- **Geen berekende bedragen.** Het brutoloon en de waarde variabele componenten leggen we hier niet vast. De brontabel bevat uitsluitend wat aan de Belastingdienst is gemeld; het rekenwerk gebeurt in laag 2. Wijzigt een definitie, dan hoeft de historie niet te worden herschreven.
- **Geen indelingskenmerken.** Functie, functiecategorie en geslacht horen bij de regel per inkomstenverhouding. De functie leiden we per tijdvak af bij het samenstellen van laag 2 (§4.5); geslacht en de overige kenmerken bepalen we ultimo rapportageperiode.
- **Geen correctie-indicatie, berichtreferentie of vastlegtijdstip.** Wat dat betekent voor correcties en voor het dashboard staat in §7.5.

Fase 2 vraagt op deze laag geen enkele uitbreiding. De populatie is af te leiden uit de aard van de arbeidsverhouding.

### 5.4 Laag 2: Loontransparantie per inkomstenverhouding

Deze tabel bevat per rapportageperiode, per inkomstenverhouding en per functie één regel met de stand over die periode. De taak stelt die samen uit de tijdvakken in de brontabel.

**Sleutel:** rapportageperiode, werkgever, medewerker, inkomstenverhouding en functie.

Hier vindt de vertaling van dienstverband naar inkomstenverhouding plaats. De brontabel levert regels per dienstverband; de taak groepeert die op het inkomstenverhoudingnummer en telt de bedragen en de uren van de onderliggende dienstverbanden op. Vallen twee dienstverbanden onder hetzelfde nummer — subdienstverbanden onder één kapstok — dan levert dat dus één regel op, met de kenmerken van het kapstokdienstverband. Dat is inhoudelijk juist: de inkomstenverhouding is de arbeidsverhouding uit het begrippenkader en daarmee de rekeneenheid voor de gemiddelden.

**De functie zit wél in de sleutel.** De taak kent elk aangiftetijdvak toe aan de functie die op de laatste dag van dat tijdvak gold (§4.5) en groepeert daarop. Wisselde de arbeidsverhouding binnen de rapportageperiode van functie, dan levert dat dus meerdere regels op: per functie één, met alleen de tijdvakken die aan die functie zijn toegekend.

Het loon telt daarbij niet dubbel. Elk tijdvak wordt aan precies één functie toegekend, dus de regels verdelen de rapportageperiode; ze overlappen niet. De som van de regels van één inkomstenverhouding is nog steeds het totaal over die periode.

Is de medewerker in een tijdvak niet aan een functie gekoppeld, dan blijft de functie op die regel leeg. Die regel bestaat dus wel, maar valt in geen enkele functiecategorie (§3.7).

Ten opzichte van een model zonder rapportageperiode zijn er twee sleutelonderdelen bij gekomen: de rapportageperiode en de functie. Daarmee kan dezelfde arbeidsverhouding één of meer vensterregels hebben en later ook kalenderjaarregels.

**Kenmerken**

We leggen deze kenmerken vast als momentopname op het einde van de rapportageperiode, behalve de functie: die hoort bij de sleutel en geldt voor de tijdvakken op deze regel. Daarmee blijft de regel zelfstandig leesbaar en hoeft de KPI niet te koppelen aan andere tabellen. De keerzijde is dat een wijziging in de stamgegevens pas doorwerkt na de volgende run van de taak.

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Functie | Verwijzing | 1 | Sleutelonderdeel. De functie waaraan de tijdvakken op deze regel zijn toegekend (§4.5). Leeg als er in die tijdvakken geen functie was gekoppeld. |
| Functiecategorie | Verwijzing | 1 | De categorie waarin die functie valt op de laatste dag van de rapportageperiode. Leeg als de functie niet gekoppeld is. |
| Geslacht | Code | 1 | Nodig voor de uitsplitsing in de vergelijkingscijfers. |
| Soort inkomstenverhouding | Code | 1 | Ultimo-waarde. Legt vast waarom een regel meetelt (11, 13, 15 of 17). |
| Aard arbeidsverhouding | Code | 1 | Ultimo-waarde. Legt vast waarom een regel meetelt (1, 18, 21, 23, 24 of 83). |
| Periodetabel | Verwijzing | 1 | Maand, vier weken of week (§4.3). Legt vast hoe de rapportageperiode is bepaald. |
| Populatie | Code | 2 | Eigen medewerker of uitzendkracht, afgeleid uit de aard van de arbeidsverhouding. |

Gegevens die altijd actueel moeten zijn, leggen we hier bewust **niet** vast. Of dit het hoofddienstverband is, en de datum in en uit dienst, halen we bij het opbouwen van de KPI op uit de stamgegevens. Zouden we ze opslaan, dan zouden we ze ook moeten bijwerken zodra ze wijzigen, en dat is niet wat deze taak doet. Uit welke dienstverbanden een regel is opgebouwd, is af te leiden uit de brontabel.

Het RSIN staat niet op deze regel: dat zit in de sleutel van de rapportageperiode.

**Berekende waarden**

Deze waarden gelden over de tijdvakken binnen de rapportageperiode die aan de functie op deze regel zijn toegekend. Wisselde de arbeidsverhouding niet van functie, dan is dat de volledige rapportageperiode. De taak berekent per tijdvak eerst het brutoloon en de waarde variabele componenten uit de rubrieken in de brontabel, en telt die daarna op (§6.1).

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Jaaruren | Aantal | 1 | De verloonde uren over de toegekende tijdvakken. |
| Bruto jaarloon | Bedrag | 1 | Het brutoloon over de toegekende tijdvakken. |
| Bruto uurloon | Bedrag | 1 | Bruto jaarloon gedeeld door jaaruren. |
| Jaarwaarde variabele componenten | Bedrag | 1 | Het deel van het loon dat bovenop het basisloon komt. |
| Uurwaarde variabele componenten | Bedrag | 1 | De jaarwaarde gedeeld door de jaaruren. |
| Aantal toegekende tijdvakken | Getal | 1 | Hoeveel aangiftetijdvakken aan deze functie zijn toegekend. Maakt zichtbaar over hoeveel van de rapportageperiode deze regel gaat. |
| Begindatum | Datum | 1 | De eerste dag van het eerste toegekende tijdvak. Legt vast vanaf wanneer is gerekend, zodat dat bij de informatie kan worden vermeld. |
| Einddatum | Datum | 1 | De laatste dag van het laatste toegekende tijdvak. |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze regel voor het laatst heeft samengesteld. |

Het aantal toegekende tijdvakken leggen we wél vast, anders dan de tellingen die eerder zijn geschrapt. Welke tijdvakken aan welke functie zijn toegekend, is namelijk niet uit de brontabel te lezen: de functie staat daar niet in (§5.3). Zonder dit veld is niet te zien of een regel over drie of over twaalf tijdvakken gaat, en dat is precies wat een lager bruto jaarloon verklaart. De begin- en einddatum volstaan daar niet voor, omdat een medewerker binnen één venster van functie kan wisselen en later kan terugkeren.

De kwartielverdeling, de arbeidsjaarfractie en de vastlegging of iemand variabele componenten heeft ontvangen, horen bij de wettelijke rapportage. Die werken we in DP2 uit; ze zijn af te leiden uit de velden hierboven.

Welke rubrieken precies het basisloon en de variabele componenten vormen, werken we uit in hoofdstuk 6.

### 5.5 Laag 3: Loontransparantie per functiecategorie

Deze tabel bevat de uitkomsten die de KPI en de vergelijkingstabel tonen. De taak stelt hem samen uit de regels per inkomstenverhouding.

**Sleutel:** rapportage-eenheid, rapportageperiode, populatie en functiecategorie.

| Sleutelonderdeel | Fase 1 | Fase 2 |
| --- | --- | --- |
| Soort rapportage-eenheid | RSIN als het veld Fiscaal nummer gevuld is, anders Werkgever (§5.2) | Idem |
| Rapportage-eenheid | Is het veld Fiscaal nummer gevuld, dan het RSIN uit dat veld; is het leeg, dan de werkgeverscode | Idem |
| Rapportageperiode | Rapportagejaar 0 | Ook een gevuld rapportagejaar |
| Populatie | Altijd eigen medewerker | Ook uitzendkracht (DP3) |
| Functiecategorie | Altijd gevuld | Ook leeg, voor de organisatiebrede kengetallen |

**Geslacht zit niet in de sleutel.** Eén functiecategorie levert precies één regel op, met de cijfers voor mannen en vrouwen naast elkaar in aparte velden.

De rapportage-eenheid zit ook in de sleutel van de rapportageperiode, maar we nemen hem hier expliciet op. De verdichting gaat nadrukkelijk per functiecategorie **binnen** een rapportage-eenheid, en zo'n eenheid kan uit meerdere werkgevers bestaan. Door hem op de regel zelf te zetten is de tabel zelfstandig leesbaar en hoeft een weergave of dashboard niet eerst naar laag 0 te koppelen.

Werkgever staat er bewust **niet** als apart veld op. Eén regel gaat over alle werkgevers binnen die eenheid samen, dus er is geen werkgever die erbij hoort. Zouden we hem toch opnemen, dan valt de vergelijkingsgroep uiteen in een groep per werkgever en klopt het gemiddelde niet meer (§6.3). Bij soort Werkgever is de eenheid toevallig één werkgever, maar dat is dan de waarde van de sleutel en geen extra veld.

Het sleutelonderdeel populatie dragen we in fase 1 met een vaste waarde mee. Achteraf een sleutel uitbreiden is duurder dan hem nu meenemen. Voor de kwartielverdeling geldt dat niet: die hoort bij de wettelijke rapportage en wordt in DP2 uitgewerkt, inclusief de sleuteluitbreiding die daarvoor nodig is.

**Velden per geslacht en de aantallen**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Aantal arbeidsverhoudingen mannen | Getal | 1 | Het aantal regels per inkomstenverhouding met geslacht man, niet het aantal personen (§6.3). |
| Aantal arbeidsverhoudingen vrouwen | Getal | 1 | Idem, met geslacht vrouw. |
| Aantal arbeidsverhoudingen totaal | Getal | 1 | De omvang van de hele functiecategorie, inclusief geslacht X en niet ingevuld. |
| Gemiddelde jaaruren mannen | Aantal | 1 | Het gemiddelde van de individuele waarden (§6.3). |
| Gemiddelde jaaruren vrouwen | Aantal | 1 | Idem. |
| Gemiddeld bruto jaarloon mannen | Bedrag | 1 | Idem. |
| Gemiddeld bruto jaarloon vrouwen | Bedrag | 1 | Idem. |
| Gemiddeld bruto uurloon mannen | Bedrag | 1 | Idem. |
| Gemiddeld bruto uurloon vrouwen | Bedrag | 1 | Idem. |
| Gemiddelde jaarwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Gemiddelde jaarwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |
| Gemiddelde uurwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Gemiddelde uurwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |
| Mediaan bruto jaarloon mannen | Bedrag | 1 | Niet af te leiden uit gemiddelden; wordt berekend uit de regels per inkomstenverhouding (§6.6). |
| Mediaan bruto jaarloon vrouwen | Bedrag | 1 | Idem. |
| Mediaan bruto uurloon mannen | Bedrag | 1 | Idem. |
| Mediaan bruto uurloon vrouwen | Bedrag | 1 | Idem. |
| Mediane jaarwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Mediane jaarwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |
| Mediane uurwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Mediane uurwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |

Dat zijn eenentwintig velden, alle in fase 1.

**De medianen per functiecategorie gaan verder dan het begrippenkader.** Dat kent de mediaan uitsluitend op organisatieniveau: de C- en D-reeks gelden voor de hele populatie eigen werknemers. Binnen een arbeidscategorie kent het alleen gemiddelden, de G-reeks (§6.9). Een mediaan per functiecategorie komt dus nooit in de wettelijke rapportage terecht.

We leggen hem toch vast, om drie redenen. Het is een bruikbaar gegeven voor het dashboard: staat het gemiddelde ver van de mediaan, dan is de verdeling binnen die functiecategorie scheef en trekt bijvoorbeeld één hoog salaris het gemiddelde omhoog. Dat is precies de vraag achter een opvallend loonverschilpercentage. Verder is een mediaan niet achteraf uit een gemiddelde te reconstrueren, dus wie hem later wil hebben mist de tussenliggende perioden voorgoed. En de kosten zijn beperkt: de taak heeft de regels per inkomstenverhouding op dat moment toch al in handen, en het gaat om sorteren binnen één functiecategorie.

**De organisatiebrede medianen die DP2 wél moet aanleveren komen in fase 2.** Die vullen dezelfde velden op een regel met een **lege functiecategorie** (§5.7). De rekenwijze is identiek; alleen de selectie is breder. Er komt dus geen apart veld en geen aparte tabel voor.

**Er is geen mediaan van de jaaruren.** Het begrippenkader kent die niet. Het kent medianen op precies de vier maatstaven waarop ook het loonverschil wordt berekend. Van de gemiddelden zijn er daarom vijf en van de medianen vier.

**Alleen het aantal krijgt ook een totaal.** Van de gemiddelden en de medianen komt er géén totaalvariant.

De reden is dat we die nergens gebruiken. De vergelijkingstabel toont Jij, Mannen en Vrouwen (§8.3), de vier KPI's rekenen mannen tegen vrouwen af (§6.5), en ook de wettelijke rapportage in DP2 zet die twee groepen tegen elkaar. Een categoriebreed gemiddelde beantwoordt geen enkele vraag die we stellen. Blijkt later, bijvoorbeeld in het dashboard, dat het toch nodig is, dan is dat een veld erbij op dezelfde regel: geen sleutel- of tabelwijziging.

De reden dat het **aantal** wél een totaal krijgt, is dubbel. Het zegt hoe groot de categorie is, en het verschil met de som van mannen en vrouwen laat zien hoeveel arbeidsverhoudingen geslacht X of geen ingevuld geslacht hebben (§3.8). Hoeveel dat er zijn leggen we dus niet apart vast. Voor DP2 is dit totaal bovendien de noemer bij het aandeel ontvangers van variabele componenten en bij de kwartielverdeling.

**Het totaal is niet de som van mannen en vrouwen.** Arbeidsverhoudingen met geslacht X of zonder ingevuld geslacht tellen wel mee in het totale aantal, maar in geen van beide geslachtsgroepen. Het aantal arbeidsverhoudingen totaal is dus groter dan of gelijk aan de som van de twee.

**Velden die één keer voorkomen**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Loonverschil jaarloon | Percentage | 1 | Op gemiddeld bruto jaarloon; de wettelijke maat voor het recht op informatie. |
| Loonverschil uurloon | Percentage | 1 | Op gemiddeld bruto uurloon. |
| Loonverschil componenten jaarwaarde | Percentage | 1 | Op de gemiddelde jaarwaarde variabele componenten. |
| Loonverschil componenten uurwaarde | Percentage | 1 | Op de gemiddelde uurwaarde variabele componenten. |
| Mediane loonverschil jaarloon | Percentage | 1 | Op mediaan bruto jaarloon. |
| Mediane loonverschil uurloon | Percentage | 1 | Op mediaan bruto uurloon. |
| Mediane loonverschil componenten jaarwaarde | Percentage | 1 | Op de mediane jaarwaarde variabele componenten. |
| Mediane loonverschil componenten uurwaarde | Percentage | 1 | Op de mediane uurwaarde variabele componenten. |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze regel voor het laatst heeft samengesteld. |

Daarmee is het setje compleet. Het begrippenkader kent acht genderloonverschillen op organisatieniveau: vier op gemiddelden en vier op medianen. Binnen een arbeidscategorie kent het er vier, alle op gemiddelden. Wij leggen alle acht per functiecategorie vast, waarmee de vier mediane percentages een eigen uitbreiding zijn (§6.9). Alleen de eerste, Loonverschil jaarloon, komt op de stamkaart; de andere zeven zijn er voor het dashboard en voor DP2.

De 5%-signalering, de kwartielgrenzen, de onderbouwing bij een overschrijding en de status van de beoordeling horen bij de wettelijke rapportage. Die velden nemen we hier niet op; DP2 werkt ze uit.

**Waarom één regel en geen regel per geslacht.** De eerdere opzet had geslacht in de sleutel en dus drie regels per functiecategorie: mannen, vrouwen en een totaalregel. Dat leverde één tabel op met twee soorten regels die elk andere velden vulden — de gemiddelden alleen op de geslachtsregels, de loonverschilpercentages alleen op de totaalregel. Wie zo'n tabel leest, moet altijd eerst weten welk soort regel hij voor zich heeft. Dat is lastig uit te leggen aan een consultant en foutgevoelig in een weergave of dashboardquery.

Met één regel per functiecategorie verdwijnt dat onderscheid. Daar komt bij:

- **De KPI leest één regel.** De vier tegels en de vergelijkingstabel worden uit dezelfde regel gevuld, in plaats van uit drie regels die eerst bij elkaar gezocht moeten worden.
- **Een ontbrekende groep is een leeg veld, geen ontbrekende regel.** Zijn er geen mannen in de categorie, dan blijven de mannenvelden leeg. In de oude opzet ontbrak de regel en moest elke lezer daarop voorbereid zijn. Dat maakt de afhandeling uit §8.6 eenvoudiger.
- **De verhouding is direct zichtbaar.** Het aantal mannen, het aantal vrouwen en het totale aantal staan naast elkaar op één regel en zijn dus meteen tegen elkaar te controleren.
- **Het sluit aan bij wat de rapportage vraagt.** De wettelijke rapportage vraagt steeds het aandeel of het gemiddelde van mannen náást dat van vrouwen. Ook de kwartielverdeling in DP2 vraagt per kwartiel het aandeel mannen en vrouwen; met deze opzet is dat één regel per kwartiel in plaats van twee.

De prijs is dat de tabel breed wordt en dat een derde geslachtscategorie een tabelwijziging zou vragen in plaats van een extra regel. Dat laatste risico is klein: de richtlijn schrijft de uitsplitsing naar mannen en vrouwen voor, en medewerkers met geslacht X of zonder ingevuld geslacht tellen volgens §3.8 alleen in het totale aantal mee.

**Herzien: we leggen de loonverschilpercentages wél vast.** Eerder was het argument dat een percentage aan twee regels tegelijk hangt en dus nergens thuishoort. Met één regel per functiecategorie is dat bezwaar helemaal weg: het percentage hoort bij precies deze regel. Vastleggen is bovendien consistent met uitgangspunt 1, de KPI leest en rekent niet. En het is noodzakelijk voor fase 2, want een vastgestelde rapportage moet het percentage bevatten dat destijds is verstrekt, ook als een definitie later wijzigt.

De mediaan blijft buiten de vergelijkingstabel op de stamkaart (§6.4). We berekenen en bewaren hem wel vanaf fase 1, voor het dashboard en voor DP2. De rekenwijze staat in §6.6.

### 5.6 Bewaartermijn

De brontabel wordt **niet opgeschoond**. Regels blijven staan zolang het tijdvak niet wordt ingetrokken. Dat is de bestaande werking van de tabel Loonaangifte uren per medewerker en die laten we ongewijzigd.

Dat is ruimer dan het venster nodig heeft — voor het recht op informatie zouden twaalf of dertien tijdvakken volstaan — maar het levert twee voordelen op. Er is altijd een compleet afgesloten kalenderjaar aanwezig op het moment dat DP2 dat jaar wil vaststellen, en een correctie die na de jaargrens binnenkomt kan nog worden verwerkt. Bovendien zou opschonen betekenen dat we een opruimroutine bouwen op een tabel die er nu geen heeft, met gevolgen voor het bestaande WAB-gebruik.

De twee tabellen erboven bewaren voor de **vensterregels** geen historie. Bij elke run stelt de taak ze opnieuw samen en overschrijft de vorige waarde. Dat past bij het doel: de medewerker wil weten hoe het er nu voor staat, niet hoe het er een jaar geleden voor stond.

In fase 2 komen daar kalenderjaarregels bij. Die blijven staan zolang de bijbehorende rapportageperiode bestaat, en dat is het rapportagejaar plus vier voorgaande jaren. Dat volgt uit de verplichting om ook over de vier voorgaande jaren informatie te kunnen verstrekken.

**Let op:** de mediaan en de kwartielverdeling worden berekend uit de **regels per inkomstenverhouding**, niet uit de brontabel. De meerjarige bewaring die de rapportage nodig heeft, geldt dus voor de twee tabellen boven de brontabel. De brontabel dient voor herleidbaarheid, correctieverwerking en het dashboard.

### 5.7 Wat fase 2 toevoegt

DP2 – Rapportage moet rapporteren over een **afgesloten kalenderjaar**. Dit ontwerp werkt met een voortschrijdend venster dat eindigt bij het laatste klaargezette aangiftetijdvak. Die twee vallen niet samen, maar het zijn wel dezelfde gegevens over een andere afbakening. DP2 krijgt daarom geen eigen structuur, maar een tweede rapportageperiode op dezelfde vier lagen.

Wat fase 2 toevoegt, is daarmee overzichtelijk:

| Wijziging | Aard |
| --- | --- |
| Rapportageperioden met een gevuld rapportagejaar | Extra regels op laag 0 |
| Status rapportageperiode | Extra veld op laag 0 |
| Aantal medewerkers in fte | Extra veld op laag 0 |
| Kalenderjaarregels per arbeidsverhouding | Extra regels op laag 2 |
| Regels met lege functiecategorie: de organisatiebrede A-, B-, C- en D-reeks | Extra regels op laag 3 |
| Kwartielverdeling, 5%-signalering, kwartielgrenzen, onderbouwing en aandeel ontvangers | Uit te werken in DP2, inclusief het kwartiel als extra sleutelonderdeel op laag 3 |
| Arbeidsjaareenheid: het aantal uren per fte per werkgever per jaar | Nieuw stamgegeven |
| Gegevensverzamelingen met een filter op een gevuld rapportagejaar | Varianten naast de bestaande (§5.9) |
| Bewaartermijn van de kalenderjaarregels | Parameterwijziging |

Er komt in fase 2 dus **geen nieuwe tabel** bij, op het stamgegeven arbeidsjaareenheid na. De sleutel van laag 0 en laag 2 wijzigt niet; laag 3 krijgt het kwartiel erbij zodra DP2 de kwartielverdeling uitwerkt. Op laag 1 verandert helemaal niets: de brontabel bevat dan al alle rubrieken die de rapportage nodig heeft. Dat is het punt van de rapportageperiode.

Wat DP2 daarnaast hergebruikt zijn de definities, de rubrieken en de rekenwijze uit hoofdstuk 6. Die moeten identiek zijn, anders leggen de KPI en de wettelijke rapportage verschillende uitkomsten naast elkaar. Voor de vulling betekent dat één rekenroutine met het periodebereik als parameter: het venster in fase 1, het kalenderjaar in fase 2.

Voor DP2 blijft één punt open. Het moment waarop een kalenderjaar definitief wordt ligt nog niet vast; het voorstel is na afloop van de correctietermijn op de loonaangifte, met een handmatige vaststelling door de werkgever.

De medianen en de mediane loonverschilpercentages waren eerder aan fase 2 toegewezen. Die vullen we nu al in fase 1 (§5.5), zodat het dashboard er meteen over beschikt. Dat betreft wél de medianen **per functiecategorie**; de organisatiebrede varianten die de rapportage vraagt komen in fase 2, op regels met een lege functiecategorie (§6.9).

De arbeidscategorie uit het begrippenkader is géén apart begrip: het is dezelfde groepering als de functiecategorie. In Profit hanteren we consequent de term functiecategorie. Er komt dus geen extra veld en geen extra sleutelonderdeel voor.

### 5.8 Opschonen

Een arbeidsverhouding kan uit de selectie vallen: de medewerker is uit dienst en het venster is voorbij zijn laatste loon geschoven, of de soort inkomstenverhouding is gewijzigd naar een soort die niet meetelt. Ook kan een functieregel vervallen doordat het venster is opgeschoven en er geen tijdvakken meer aan die functie zijn toegekend.

De taak verwijdert dan de betreffende regel per inkomstenverhouding. We laten geen regels staan met bevroren cijfers, want die zouden op de stamkaart een actueel beeld suggereren dat niet meer klopt. De medewerker ziet dan de melding uit §8.6 in plaats van verouderde bedragen.

Raakt een functiecategorie leeg, dan verwijdert de taak ook de bijbehorende regels uit de tabel per functiecategorie.

De brontabel raken we hierbij niet aan. Die wordt beheerd door het loonaangifteproces: een tijdvak verdwijnt alleen als de aangifte wordt ingetrokken.

Dit opschonen raakt alleen de **vensterregels**. Kalenderjaarregels worden nooit opgeschoond op grond van de actuele situatie: die zijn een vastlegging van hoe het toen was. Ze verdwijnen alleen als de hele rapportageperiode buiten de bewaartermijn valt.

### 5.9 Gegevensverzamelingen

De tabellen zijn alleen bruikbaar als ze ook ontsloten worden. Voor de twee nieuwe tabellen leveren we daarom gegevensverzamelingen mee — drie in totaal, want laag 2 krijgt er twee — en voor de brontabel breiden we de bestaande verzameling uit. Die verzamelingen vormen tegelijk de **enige** route naar deze gegevens: eigen weergaven rechtstreeks op de tabellen sluiten we af (§9.2).

De rapportageperiode (laag 0) krijgt geen eigen gegevensverzameling. Die laag bevat geen cijfers, alleen de afbakening. De kenmerken ervan — rapportage-eenheid, rapportagejaar, begindatum, einddatum en datum laatste berekening — nemen we mee in de twee verzamelingen erboven, zodat altijd zichtbaar is waarover en wanneer is gerekend.

**Loonaangifte uren per medewerker — bestaande verzameling, uit te breiden**

Voor laag 1 komt er géén nieuwe gegevensverzameling. Die tabel is al ontsloten; we vullen die verzameling aan met de zeven toegevoegde bedragen uit §5.3, zodat het dashboard de loonniveaus per aangiftetijdvak kan lezen.

Dat vraagt wel om aandacht bij de autorisatie. De bestaande ontsluiting is gemaakt voor uren en contractkenmerken; met de loonbedragen erbij komt er individuele beloningsinformatie in te staan die er nu niet in zit. De ontsluiting moet daarom worden herzien voordat de uitbreiding wordt uitgeleverd, inclusief de view in de querywizard en de InSite-datamodeldefinitie. Dat is punt G2 in §12.

**Loontransparantie per inkomstenverhouding (actuele functie)**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per inkomstenverhouding (§5.4) |
| Standaardfilter | Rapportagejaar 0 en de **actuele functie** van de medewerker |
| Filterautorisatie | Medewerkerautorisatie bij het lezen |
| Velden | Alle kenmerken en berekende waarden uit §5.4, aangevuld met de kenmerken van de rapportageperiode |
| Sortering | Medewerker, inkomstenverhouding |
| Gebruik | De weergave Mijn loonniveau vergeleken (§8.3), het document Loontransparantie medewerker en de gegevensverzameling van DP4 – Vraag aan HR |

Het standaardfilter op rapportagejaar 0 is nodig omdat in fase 2 kalenderjaarregels in dezelfde tabel komen. Zonder filter zou een medewerker zijn eigen loon meerdere keren zien, één keer per rapportageperiode. DP2 levert een eigen variant met een filter op een gevuld rapportagejaar.

**Het filter op de actuele functie** zorgt ervoor dat elke presentatievorm hetzelfde toont. Laag 2 bevat per functie een regel (§5.4), dus zonder filter zou een medewerker die van functie is gewisseld zijn loon over twee regels verdeeld zien. Vraagt hij zijn gegevens op — via de KPI of via een document in de workflow — dan gelden de cijfers van de functie die op dat moment geldig is. We nemen daarvoor de **actuele** functie en niet de functie op de laatste dag van het venster: het venster eindigt bij het laatste klaargezette aangiftetijdvak en loopt dus achter op vandaag.

Dat betekent ook dat een recente functiewijziging tot een lege uitkomst kan leiden. Is er nog geen loonaangifte klaargezet waarin de nieuwe functie valt, dan bestaat er nog geen regel voor die functie. Wat de medewerker dan ziet, staat in §8.5 en §8.6.

**Loontransparantie per inkomstenverhouding (alle functies)**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per inkomstenverhouding (§5.4) |
| Standaardfilter | Rapportagejaar 0 |
| Filterautorisatie | Medewerkerautorisatie bij het lezen |
| Velden | Gelijk aan de verzameling hierboven |
| Sortering | Medewerker, inkomstenverhouding, functie |
| Gebruik | Het Power BI-dashboard |

Deze tweede verzameling laat het filter op de functie weg en toont dus alle functieregels binnen het venster. Het dashboard heeft die nodig: juist de vergelijking tussen de regel vóór en ná een functiewijziging laat zien wat er met het loonniveau is gebeurd. Met alleen de actuele functieregel is die vraag niet te beantwoorden.

De twee verzamelingen verschillen **uitsluitend** in dat ene filter. Basistabel, velden en autorisatie zijn identiek, dus er is geen tweede definitie te onderhouden en er kunnen geen twee waarheden ontstaan. De medewerkerautorisatie geldt ook hier: wie een dashboard bouwt ziet alleen de medewerkers waarvoor hij geautoriseerd is (§9.2).

Wie deze verzameling gebruikt moet er rekening mee houden dat één medewerker meerdere regels kan hebben. Optellen over de regels van één inkomstenverhouding geeft het totaal over het venster; middelen erover geeft een getal dat nergens op slaat, omdat de regels een verschillend aantal tijdvakken beslaan. Het veld Aantal toegekende tijdvakken (§5.4) maakt dat zichtbaar.

**Loontransparantie per functiecategorie**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per functiecategorie (§5.5) |
| Standaardfilter | Rapportagejaar 0 |
| Filterautorisatie | Niet van toepassing; de regel gaat over een groep en niet over een medewerker |
| Velden | Alle velden uit §5.5, aangevuld met de kenmerken van de rapportageperiode |
| Sortering | Rapportage-eenheid, functiecategorie |
| Gebruik | De vier KPI-tegels (§8.2), de kolommen Mannen en Vrouwen in de vergelijkingstabel (§8.3) en het dashboard |

Medewerkerautorisatie kan hier niet: er staat geen medewerker op de regel. De afscherming loopt dus volledig via de autorisatie op de gegevensverzameling zelf. Dat is bewust, want een gemiddelde in een kleine categorie is herleidbaar tot een individuele collega (§9.3).

**Geen variant zonder autorisatie.** Voor het dashboard zou een verzameling zonder medewerkerautorisatie handiger zijn, maar dan is de afweging uit §9.2 te omzeilen. Een HR-medewerker die over de hele organisatie mag rapporteren, is voor al die medewerkers geautoriseerd en ziet met de gewone verzameling dus alles wat hij nodig heeft. Wie dat niet is, hoort die gegevens ook in een dashboard niet te zien.

---

## 6 Berekeningen

### 6.1 De waarden van de medewerker zelf

De rubrieken staan **per aangiftetijdvak** in de brontabel. De taak berekent daaruit per tijdvak het brutoloon en de waarde variabele componenten, kent elk tijdvak toe aan een functie (§4.5), en telt daarna per functie op tot de waarden op de regel per inkomstenverhouding:

| Waarde | Formule |
| --- | --- |
| Jaaruren | Som van AantVerlU (3515) |
| Bruto jaarloon | Som van (LnLbPh (1287 + 1670) − VakBsl (1317) − OpnAvwb (5068) + OpgRchtVakBsl (1318) + OpbAvwb (5069)) − [Jaarwaarde variabele componenten] |
| Bruto uurloon | [Bruto jaarloon] / [Jaaruren] |
| Jaarwaarde variabele componenten | Som van (WrdLn (1321) + LnTabBB, alleen bijzonder tarief (1287 + 1670) − VakBsl (1317) − OpnAvwb (5068)) |
| Uurwaarde variabele componenten | [Jaarwaarde variabele componenten] / [Jaaruren] |

De optellingen gebeuren op de bedragen per tijdvak, niet op de uurwaarden. Het bruto uurloon over het venster is dus het opgetelde jaarloon gedeeld door de opgetelde uren, en nadrukkelijk niet het gemiddelde van twaalf periode-uurlonen. Dat laatste zou een tijdvak met weinig uren even zwaar laten wegen als een volle periode.

De volgorde van optellen is daarbij: eerst binnen één tijdvak alle dienstverbanden die onder dezelfde inkomstenverhouding vallen — de kapstok met zijn subdienstverbanden — en daarna alleen de tijdvakken die aan dezelfde functie zijn toegekend. Zo staat op elke regel per inkomstenverhouding het volledige loon van die arbeidsverhouding over de tijdvakken waarin de medewerker die functie had.

Deze opbouw volgt het begrippenkader loontransparantie. Daarin is het brutoloon gedefinieerd als het loon verminderd met de waarde variabele componenten, met als toelichting dat dit in de Europese richtlijn het loonniveau of basisloon heet. Het bruto jaarloon is dus het basisloon; de variabele componenten staan er los naast en zijn er niet in begrepen. Het begrippenkader spreekt voluit van "aanvullende of variabele componenten"; in dit ontwerp korten we dat af tot **variabele componenten**, zodat de veldnamen en de schermteksten werkbaar blijven.

De rekenvolgorde wijkt af van de leesvolgorde hierboven. De taak bepaalt eerst de uren, dan de waarde variabele componenten, en pas daarna het brutoloon, omdat die waarde daarvan wordt afgetrokken. De twee uurwaarden volgen als laatste, en die berekenen we alleen op de regel per inkomstenverhouding, niet per tijdvak.

De vakantiebijslag en het arbeidsvoorwaardenbedrag tellen mee op het moment van opbouw, niet van uitbetaling. Het uitbetaalde bedrag gaat eruit en het opgebouwde recht gaat erin. Daardoor is het bruto jaarloon onafhankelijk van de vraag of het vakantiegeld in geld, in uren of anders is vergoed, en krijgt een medewerker in de maand van uitbetaling geen piek.

Het aantal jaaruren kan op de regel per inkomstenverhouding niet nul zijn: verloonde uren groter dan nul is een selectiecriterium (§3.4). Per afzonderlijk tijdvak kan het wél nul zijn, bijvoorbeeld bij onbetaald verlof. Dat is geen probleem, omdat we de uurwaarden alleen over het venster berekenen en niet per tijdvak.

Een correctie kan het bruto jaarloon over het venster negatief maken. Een negatief loonniveau is niet uitlegbaar, dus we behandelen dat als nul. Die ondergrens passen we toe op het venstertotaal in de regel per inkomstenverhouding, niet op het losse tijdvak in de brontabel; daar mag een gecorrigeerd bedrag gewoon negatief zijn.

**Voor de variabele componenten wijken we hiermee bewust af van het begrippenkader.** Het kader bepaalt in §3.6.4 dat de waarde variabele componenten niet negatief kan zijn, en dat is daar de waarde **per tijdvak**; de jaarwaarde is vervolgens de som van die al afgekapte bedragen. Wij kappen pas af op het venstertotaal. Dat maakt verschil:

| Aanpak | Tijdvak A: −100 | Tijdvak B: +300 | Jaarwaarde |
| --- | --- | --- | --- |
| Afkappen per tijdvak, dan optellen | 0 | 300 | 300 |
| Optellen, dan afkappen (dit ontwerp) | −100 | 300 | 200 |

We kiezen voor de tweede rij. Een correctie hoort een eerder tijdvak te kunnen terugdraaien; kappen we per tijdvak af, dan blijft een teruggedraaid bedrag in de jaarwaarde hangen en telt loon mee dat de medewerker niet heeft gehad. Bovendien is de ondergrens zo van toepassing op precies het getal dat we tonen. DP2 moet dezelfde keuze aanhouden, anders wijken de KPI en de wettelijke rapportage van elkaar af.

We rekenen binnen een berekening onafgerond door en ronden af op het moment van wegschrijven, op **twee decimalen**. Dat geldt voor elke laag: de bedragen op de regel per inkomstenverhouding, de gemiddelden en de medianen op de regel per functiecategorie, en de percentages. Wat we opslaan is dus hetzelfde getal als wat we tonen.

Dat betekent dat een gemiddelde wordt berekend uit al afgeronde bedragen. Het alternatief — meer decimalen bewaren dan we tonen — levert een nauwkeuriger gemiddelde op, maar maakt het onmogelijk om een getoond getal na te rekenen: de som van de zichtbare bedragen komt dan niet uit op het zichtbare gemiddelde. Uitlegbaarheid weegt hier zwaarder dan de laatste decimaal (uitgangspunt 3).

We passen geen deeltijdcorrectie toe op het bruto jaarloon. Het bruto uurloon vangt het deeltijdeffect vanzelf op. Daarom drukken we het loonniveau altijd in beide eenheden uit: het bruto jaarloon laat zien wat iemand feitelijk verdient en is de wettelijke maat, het bruto uurloon maakt de vergelijking eerlijk.

### 6.2 De gebruikte rubrieken

Alle waarden komen uit bestaande gegevens van de loonaangifte. Er worden geen nieuwe looncomponenten ingericht en er zijn geen lijstbegrippen voor nodig. De bedragen worden bij het klaarzetten van de loonaangifte vanuit `AfasHrTaxEmployee` in de brontabel vastgelegd; de technische kolomnamen staan in §5.3.

| Rubriek | Rubrieknummer | Omschrijving |
| --- | --- | --- |
| AantVerlU | 3515 | Aantal verloonde uren, afgerond |
| LnLbPh | 1287 + 1670 | Loon LB/PH, samen met de correctie kunstenaar en sporter |
| LnTabBB | 1287 + 1670 | Loon belast volgens tabel bijzondere beloningen; alleen het deel met bijzonder tarief. In de brontabel heet dit veld Loon LB/PH bijzonder tarief (§5.3) |
| VakBsl | 1317 | Vakantiebijslag |
| OpgRchtVakBsl | 1318 | Opgebouwd recht vakantiebijslag |
| WrdLn | 1321 | Waarde niet in geld uitgekeerd loon |
| OpnAvwb | 5068 | Opname arbeidsvoorwaardenbedrag |
| OpbAvwb | 5069 | Opbouw arbeidsvoorwaardenbedrag |

**LnLbPh en LnTabBB staan niet voor niets op dezelfde nummers.** Ze komen uit dezelfde rubrieken 1287 en 1670. LnTabBB is daarbinnen geen apart bedrag maar een **deelverzameling**: het deel dat tegen bijzonder tarief is belast. Het onderscheid ontstaat door een extra filter op het tarief, niet door een andere bron. Daarom leggen we in de brontabel beide delen apart vast (§5.3): het normale tarief en het bijzondere tarief. Samen vormen ze LnLbPh, en het tweede deel alleen is LnTabBB. Zo slaan we geen bedrag dubbel op en is de splitsing toch beschikbaar.

Twee regels uit het begrippenkader horen bij de jaarwaarde variabele componenten en zijn in de formule zelf niet zichtbaar:

- De waarde kan **niet negatief** zijn. Komt de berekening onder nul uit, dan houden we nul aan.
- De opname van het arbeidsvoorwaardenbedrag trekken we **alleen af als die in de loonaangifte als loon bijzondere beloning is verantwoord**. Is dat niet zo, dan blijft de aftrek achterwege.

Vakantiebijslag en arbeidsvoorwaardenbedrag, inclusief een dertiende maand, horen bij het bruto jaarloon en niet bij de variabele componenten. Daarom worden ze in de formule voor de jaarwaarde weer in mindering gebracht.

### 6.3 De vergelijkingsgroep

De medewerker wordt vergeleken met alle arbeidsverhoudingen in dezelfde functiecategorie, uitgesplitst naar geslacht. Alleen regels per inkomstenverhouding die aan het populatiefilter uit hoofdstuk 3 voldoen tellen mee. Medewerkers met geslacht X en medewerkers zonder ingevuld geslacht tellen niet mee in de gemiddelden per geslacht, wel in het totale aantal arbeidsverhoudingen (§3.8).

De groep loopt over alle werkgevers binnen dezelfde **rapportage-eenheid**: alle werkgevers met hetzelfde RSIN, of — als het veld Fiscaal nummer op de organisatie leeg is — die ene werkgever alleen (§5.2). Het RSIN is het niveau waarop de wettelijke rapportage plaatsvindt, dus zo sluiten het recht op informatie en de latere rapportage op elkaar aan. Het voorkomt ook dat een concern met veel kleine werkgevers per werkgever te kleine groepen overhoudt om nog iets te kunnen tonen.

Werkgevers zonder ingevuld Fiscaal nummer worden nooit met elkaar vergeleken. Elk van hen vormt een eigen rapportage-eenheid, dus hun lonen komen niet in één gemiddelde terecht.

**We tellen per arbeidsverhouding, niet per persoon.** Het begrippenkader legt de arbeidsverhouding vast op het niveau van de inkomstenverhouding. Een medewerker met twee inkomstenverhoudingen levert dus twee regels op en telt twee keer mee in de vergelijkingsgroep. Vallen die twee in verschillende functiecategorieën, dan telt de medewerker in beide groepen mee, elk met het loon dat in die arbeidsverhouding is verdiend. Dat is geen dubbeltelling die we moeten wegwerken: het loon uit de ene arbeidsverhouding hoort inhoudelijk niet bij de functiecategorie van de andere.

**Elke functieregel telt als volwaardige arbeidsverhouding.** Wisselde een arbeidsverhouding binnen het venster van functie, dan levert dat meerdere regels op (§5.4). Elk van die regels telt in zijn eigen functiecategorie mee als één arbeidsverhouding, met het loon over de tijdvakken die aan die functie zijn toegekend. Ook hier is er geen dubbeltelling van bedragen: elk tijdvak zit in precies één regel.

Het gevolg is wél dat zo'n medewerker in twee functiecategorieën als deelnemer meetelt, met in beide een bruto jaarloon over minder dan twaalf tijdvakken. Dat drukt het gemiddelde jaarloon van die categorieën. We corrigeren daar niet voor, om dezelfde reden als bij medewerkers die niet het hele venster in dienst waren: de wet schrijft het jaarloon als grondslag voor, en het loonverschil op uurloon staat ernaast om het effect te kunnen duiden (§6.8).

**Het gemiddelde is het gemiddelde van de individuele waarden.** We tellen de waarden van de arbeidsverhoudingen bij elkaar op en delen door het aantal arbeidsverhoudingen (§6.7):

> gemiddeld bruto uurloon van de mannen = som van de bruto uurlonen van de mannen / aantal mannelijke arbeidsverhoudingen

Dat volgt het begrippenkader. De andere mogelijkheid was het totale loon delen door de totale uren, maar dan weegt een voltijder zwaarder dan een deeltijder in hetzelfde gemiddelde. Het recht op informatie gaat over de vraag hoe individuele lonen zich tot elkaar verhouden, dus iedere arbeidsverhouding weegt even zwaar. DP2 moet dezelfde rekenwijze aanhouden.

### 6.4 De vergelijkingscijfers

De vergelijkingstabel toont per regel drie kolommen: **Jij**, **Mannen** en **Vrouwen**. De kolommen Mannen en Vrouwen bevatten het gemiddelde van die groep binnen de functiecategorie, gelezen uit de tabel per functiecategorie. Mannen staan eerst omdat zij de referentiegroep zijn in alle loonverschilpercentages (§8.3).

De vijf regels zijn, in deze volgorde: jaaruren, bruto jaarloon, bruto uurloon, jaarwaarde variabele componenten en uurwaarde variabele componenten.

**De kolom Individueel verschil vervalt.** De mockup bevatte een percentage dat de eigen waarde afzette tegen het gemiddelde. Dat laten we los. Het juridische kader stuurt op het verschil tussen mannen en vrouwen binnen de functiecategorie en op een drempel van vijf procent op categorieniveau, niet op de afwijking van één individu. Een individueel percentage nodigt uit tot een conclusie die het niet kan dragen: iemand die vijftien procent onder het gemiddelde zit, kan gewoon minder ervaring of minder dienstjaren hebben. De medewerker kan het verschil bovendien zelf aflezen uit de kolommen ernaast, en het loonverschilpercentage staat al als KPI boven de tabel.

**De kolom Mediaan vervalt eveneens.** De mockup toonde één mediaan van de hele functiecategorie, mannen en vrouwen samen. Die past niet bij de rapportagedefinitie, waarin de mediaan van de mannen wordt afgezet tegen die van de vrouwen. Het alternatief was twee kolommen toevoegen, mediaan mannen en mediaan vrouwen, voor alle vijf de regels. Dat zou de tabel op zeven kolommen brengen voor een gegeven dat naast de gemiddelden weinig toevoegt voor de individuele medewerker. Het mediane loonverschil hoort thuis in de wettelijke rapportage van DP2 en in het dashboard, niet op de stamkaart. Het datamodel heeft er wel velden voor (§5.5); die worden vanaf fase 1 gevuld, zodat het dashboard erover beschikt.

### 6.5 De loonverschilpercentages

Het loonverschil zet het gemiddelde van de mannen af tegen dat van de vrouwen:

> loonverschil = (gemiddelde mannen − gemiddelde vrouwen) / gemiddelde mannen

De mannen vormen de referentiegroep, wat aansluit bij de manier waarop het loonverschil wettelijk wordt uitgedrukt.

We berekenen deze formule op **vier grondslagen**:

| Percentage | Grondslag | Status |
| --- | --- | --- |
| Loonverschil jaarloon | Gemiddeld bruto jaarloon | Wettelijk voorgeschreven |
| Loonverschil uurloon | Gemiddeld bruto uurloon | Aanvullend |
| Loonverschil componenten jaarwaarde | Gemiddelde jaarwaarde variabele componenten | Aanvullend |
| Loonverschil componenten uurwaarde | Gemiddelde uurwaarde variabele componenten | Aanvullend |

Deze vier namen gebruiken we overal: als veldnaam in §5.5, als grondslag hier en als titel van de KPI-tegels in §8.2.

De taak berekent deze vier percentages en legt ze vast op de regel per functiecategorie (§5.5). De KPI leest ze en rekent zelf niets meer uit.

**Het bruto jaarloon is de wettelijke grondslag.** De nota van toelichting schrijft voor het recht op informatie voor dat wordt uitgegaan van het gemiddeld bruto jaarloon van mannen tegenover dat van vrouwen, uitgedrukt als percentage van het gemiddelde loonniveau van de mannelijke werknemers. Dat volgen we, ook al is het uurloon inhoudelijk zuiverder. Wat de wet voorschrijft, moet Profit tonen.

**Het bruto uurloon berekenen we ernaast.** Het jaarloon meet voor een deel een urenverschil in plaats van een loonverschil: vrouwen werken vaker in deeltijd, en wie halverwege in dienst kwam heeft een lager jaarloon. Het uurloon corrigeert daarvoor. Klanten zullen die vraag stellen zodra ze het wettelijke percentage zien, en dan moet het antwoord er zijn. Het percentage staat daarom naast het wettelijke, niet in plaats daarvan.

**De variabele componenten krijgen een eigen percentage.** De wettelijke rapportage onderscheidt het basisloon van de variabele componenten. Een organisatie kan een klein verschil in basisloon hebben en een groot verschil in bonussen en toeslagen. Zonder apart percentage verdwijnt dat in het totaal.

**Een percentage vraagt twee groepen.** Ontbreekt een van beide — geen mannen of geen vrouwen in de functiecategorie — dan blijft het percentage leeg. Hetzelfde geldt als het gemiddelde van de mannen nul is; delen door nul levert geen uitlegbaar getal op.

We tonen in die gevallen nadrukkelijk **geen 100%**. Rekenkundig zou je dat kunnen verdedigen als de vrouwengroep leeg is: het hele mannengemiddelde is dan het verschil. Maar voor de medewerker leest 100% als een maximaal loonverschil, terwijl er in werkelijkheid niets te vergelijken valt. Het gemiddelde van de groep die er wél is, tonen we gewoon in de vergelijkingstabel (§8.6).

**We slaan het percentage op als getal met twee decimalen.** Een loonverschil van 5,23% leggen we vast als 5,23 en niet als 0,0523. Het begrippenkader rekent de formule ook maal honderd procent. Zo staat er in de tabel hetzelfde getal als op het scherm en in de rapportage, en is er geen plek waar een factor honderd kan worden vergeten.

De mockup toont één percentage op het bruto jaarloon. Bij de uitwerking van het scherm gaan we uit van vier percentages.

### 6.6 De medianen

De mediaan is het bedrag waarbij de ene helft van de groep meer verdient en de andere helft minder. We berekenen hem per functiecategorie, per geslacht, uit de regels per inkomstenverhouding die aan het populatiefilter uit hoofdstuk 3 voldoen. Dezelfde vergelijkingsgroep dus als bij de gemiddelden (§6.3).

Het algoritme volgt het begrippenkader:

> Sorteer de waarden van laag naar hoog. Is het aantal oneven, neem dan de middelste waarde. Is het aantal even, neem dan het gemiddelde van de twee middelste waarden.

Twee dingen zijn hierbij van belang. De waarden hoeven **niet uniek** te zijn: verdienen drie mannen exact hetzelfde, dan staan die drie bedragen ook alle drie in de rij. En we sorteren de **individuele waarden per arbeidsverhouding**, niet per persoon — net als bij de gemiddelden telt een medewerker met twee arbeidsverhoudingen dus twee keer mee.

We berekenen de mediaan op vier maatstaven: bruto jaarloon, bruto uurloon, jaarwaarde variabele componenten en uurwaarde variabele componenten. Voor de jaaruren doen we het niet; het begrippenkader kent die mediaan niet.

Is een geslachtsgroep leeg, dan blijft de mediaan leeg. We vullen geen nul, want nul zou betekenen dat er iemand is die niets verdient.

**Het mediane loonverschil** werkt net als het gewone loonverschil, maar dan op medianen in plaats van gemiddelden:

> mediane loonverschil = (mediaan mannen − mediaan vrouwen) / mediaan mannen

Ook deze vier percentages slaan we op als getal met twee decimalen. Is de mediaan van de mannen leeg of nul, dan blijft het percentage leeg.

Het verschil tussen het gemiddelde en het mediane loonverschil is zelf een signaal. Wijken ze sterk af, dan is de loonverdeling scheef: enkele hoge of lage salarissen trekken het gemiddelde weg van het midden. Juist daarom vraagt de wettelijke rapportage om beide.

Die rapportage vraagt ze wel **organisatiebreed** en niet per functiecategorie (§6.9). De mediaan die wij per functiecategorie berekenen is een eigen uitbreiding, bedoeld voor het dashboard; de rekenwijze hierboven is dezelfde die DP2 in fase 2 op de hele populatie toepast.

### 6.7 De tellingen

Bij elke groep hoort een aantal. Dat is niet alleen een kengetal, het is ook de noemer van de gemiddelden uit §6.3.

**Op de regel per functiecategorie (laag 3)** tellen we drie aantallen:

| Aantal | Wat we tellen |
| --- | --- |
| Aantal arbeidsverhoudingen mannen | De regels per inkomstenverhouding in deze functiecategorie met geslacht man |
| Aantal arbeidsverhoudingen vrouwen | Idem, met geslacht vrouw |
| Aantal arbeidsverhoudingen totaal | Alle regels in deze functiecategorie, ongeacht het geslacht |

Het totaal bevat dus ook de arbeidsverhoudingen met geslacht X en die zonder ingevuld geslacht. Die tellen wel mee in het totaal, maar in geen van beide geslachtsgroepen (§3.8). Daarom geldt:

> aantal totaal ≥ aantal mannen + aantal vrouwen

Hoeveel arbeidsverhoudingen dat verschil vormen, leggen we niet apart vast; dat is het verschil tussen het totaal en de som van de twee.

**We tellen regels, niet medewerkers.** Een medewerker die binnen het venster van functie wisselde heeft meerdere regels en telt dus in meerdere functiecategorieën mee (§6.3). Hetzelfde geldt voor een medewerker met twee inkomstenverhoudingen. Het aantal arbeidsverhoudingen is daarmee geen telling van personen, en de som over alle functiecategorieën kan hoger uitkomen dan het aantal medewerkers in de organisatie.

**Op de rapportageperiode (laag 0)** staat één aantal: het aantal arbeidsverhoudingen totaal. Dat is de telling van **alle** regels per inkomstenverhouding in deze rapportageperiode.

Dat getal is groter dan of gelijk aan de som van de totalen op laag 3. Medewerkers zonder functiecategorie krijgen namelijk wel een regel per inkomstenverhouding, maar komen in geen enkele functiecategorie terecht (§3.7). Wie de twee lagen naast elkaar legt en een verschil ziet, kijkt dus naar het aantal arbeidsverhoudingen waarvan de functie nog niet aan een categorie is gekoppeld. Dat is bruikbare stuurinformatie voor het dashboard.

**Het aantal medewerkers in fte** is een ander begrip en telt geen regels maar uren:

> aantal medewerkers in fte = som van de jaaruren / arbeidsjaareenheid

De arbeidsjaareenheid is het aantal uren dat een voltijdmedewerker in een jaar werkt, door de werkgever zelf bepaald. Dat stamgegeven bestaat nog niet in Profit en komt er in fase 2 bij; daarom is dit veld pas dan te vullen. Het begrippenkader noemt dit begrip *aantal werknemers*; wij houden de Profit-term aan, omdat "aantal werknemers" hier verwarrend is — het gaat om een fte-getal en niet om een telling van personen.

Dit getal bepaalt of en hoe vaak een werkgever rapportageplichtig is. Voor het recht op informatie speelt het geen rol.

### 6.8 Onvolledige vensters in de vergelijking

We nemen medewerkers mee zolang er loon in het venster valt. Wie halverwege in of uit dienst ging, heeft daardoor een lager bruto jaarloon en minder jaaruren dan een collega die het hele venster meedraaide. Hetzelfde geldt voor wie binnen het venster van functie wisselde: die heeft per functiecategorie een regel over een deel van het venster (§4.5).

We corrigeren daar niet voor en we tellen niemand apart. Iedereen in de functiecategorie telt mee in alle vergelijkingscijfers. Een aparte telling voor de jaarbedragen zou de groep verkleinen en het geheel moeilijker uitlegbaar maken.

Dit betekent dat de jaaruren, het bruto jaarloon en de jaarwaarde in de vergelijking een gemengd beeld geven: ze bevatten zowel volledige als gedeeltelijke arbeidsverhoudingen. Dat raakt het wettelijke loonverschil, dat juist op het jaarloon wordt berekend. We accepteren dat, omdat de wet die grondslag voorschrijft en omdat het effect over een hele functiecategorie doorgaans klein is. Het loonverschil uurloon staat ernaast om het te kunnen duiden: wijken de twee percentages sterk af, dan zit het verschil in de arbeidsomvang en niet in de beloning.

Welke tijdvakken daadwerkelijk loon bevatten is uit de brontabel te lezen, en het aantal toegekende tijdvakken staat op de regel per inkomstenverhouding (§5.4). Het dashboard kan deze groep daarmee apart bekijken.

### 6.9 Herkomst van de formules

Het begrippenkader nummert zijn formules. Onderstaande tabel legt vast welk nummer bij welk veld uit dit ontwerp hoort, zodat een uitkomst tot de bron te herleiden is en DP2 dezelfde formule aanhoudt.

Daarbij is één onderscheid bepalend. Het begrippenkader kent twee niveaus: **organisatiebreed** over alle eigen werknemers (de A-, B-, C- en D-reeks) en **binnen een arbeidscategorie** (de G-reeks). Onze tabel per functiecategorie zit op het tweede niveau, dus daar horen de G-nummers bij.

| Veld in dit ontwerp | Formule in het begrippenkader |
| --- | --- |
| Loonverschil jaarloon | G.M11 |
| Loonverschil uurloon | G.M21 |
| Loonverschil componenten jaarwaarde | G.M31 |
| Loonverschil componenten uurwaarde | G.M41 |
| Mediane loonverschil jaarloon | Geen; eigen uitbreiding |
| Mediane loonverschil uurloon | Geen; eigen uitbreiding |
| Mediane loonverschil componenten jaarwaarde | Geen; eigen uitbreiding |
| Mediane loonverschil componenten uurwaarde | Geen; eigen uitbreiding |

**De vier mediane percentages hebben geen nummer.** Het begrippenkader kent de mediaan alleen organisatiebreed — C11, C21, D11 en D21 — en niet binnen een arbeidscategorie. Een mediaan per functiecategorie is dus een bewuste uitbreiding van ons model, die nooit in de wettelijke rapportage terechtkomt. Waarom we hem toch vastleggen staat in §5.5.

**De A-, B-, C- en D-reeks komen in fase 2.** Dat zijn dezelfde acht percentages, maar dan over de hele populatie. Ze vullen dezelfde velden op een regel met een **lege functiecategorie** (§5.7). De formule is identiek; alleen de selectie is breder.

De E-reeks (aandeel ontvangers van variabele componenten) en de F-reeks (F.111n tot en met F.141n, het aandeel mannen en vrouwen per kwartiel op jaar- en uurbasis) vallen buiten dit ontwerp en worden in DP2 uitgewerkt.

---

## 7 Vulproces

### 7.1 Wanneer de gegevens worden bijgewerkt

Het bijwerken gebeurt in twee snelheden.

**Laag 1 wordt direct bijgewerkt.** Zet de werkgever de loonaangifte over een tijdvak **klaar**, dan schrijft het loonaangifteproces meteen de brontabel weg, inclusief de zeven toegevoegde bedragen (§5.3). Dat is de bestaande werking en daar veranderen we niets aan. De feiten staan er dus op het moment dat ze aan de Belastingdienst worden gemeld.

We sluiten daarmee bewust aan bij het bestaande vulmoment van de brontabel en niet bij het accorderen van de salarisverwerking. Bij het accorderen staan de loonaangifterubrieken nog niet vast; het klaarzetten is de laatste stap waarin ze worden bepaald en weggeschreven.

**De lagen 0, 2 en 3 werken we bij met een aparte wachtrijtaak.** Die taak heet **Bijwerken gegevens loontransparantie** en wordt gestart vanuit de dagovergang **Vernieuwen actuele gegevens**. Hij draait dus doorgaans elke nacht.

Dat is een bewuste keuze om de berekening los te trekken van het loonaangifteproces:

- **Het salarisproces heeft er geen last van.** Het klaarzetten wordt er niet trager of kwetsbaarder van, en een fout in de berekening kan het klaarzetten niet raken.
- **De taak is opnieuw uit te voeren.** Gaat er iets mis, dan kan hij los worden gestart. Er hoeft niet eerst een loonaangifte te worden klaargezet om een herstelrun uit te lokken.
- **Niet alleen de loonaangifte is van invloed.** Een functiewijziging verandert de functie waaraan tijdvakken worden toegekend (§4.5) en daarmee de indeling in functiecategorieën; een wijziging in de functiecategorie-inrichting verandert de vergelijkingsgroep zelf. Die wijzigingen komen niet via het loonaangifteproces binnen. Met een dagelijkse taak werken ze vanzelf door, en meestal eerder dan bij de eerstvolgende loonaangifte.

De prijs is actualiteit: de cijfers op de stamkaart lopen maximaal één dagovergang achter op de brongegevens. Voor het recht op informatie is dat ruim voldoende, want de wettelijke reactietermijn is twee maanden (§7.7).

Het venster blijft eindigen bij het laatste **klaargezette** aangiftetijdvak (§4.2). De taak bepaalt dat bij elke run opnieuw en verschuift het venster dus niet zelf.

### 7.2 De triggertabel

De taak moet weten voor welke werkgevers er iets is veranderd. Zou hij elke nacht alle werkgevers volledig doorrekenen, dan doet hij bij verreweg de meeste runs werk dat niets oplevert.

Daarom houden we dat bij in een technische **triggertabel**. Die is niet zichtbaar voor de klant en wordt niet ontsloten via weergaven of gegevensverzamelingen. Hij hoort ook niet bij het gegevensmodel uit hoofdstuk 5: er staan geen loongegevens in, alleen werkvoorraad.

**Sleutel:** werkgever, periodetabel, jaar en periode.

Eén regel zegt: voor deze werkgever is dit aangiftetijdvak geraakt en moet worden meegenomen. Meer hoeft er niet in te staan. Wát er precies is gewijzigd doet niet ter zake, omdat de taak de betrokken werkgever toch volledig opnieuw doorrekent (§7.3). Dat houdt de tabel klein en maakt hem ongevoelig voor de vraag welk proces de regel heeft weggeschreven.

**We slaan het op periodeniveau op.** Vanuit de loonaangifte is de periode direct voorhanden. Vanuit een functiewijziging moet hij worden opgezocht, maar dat is goed te doen omdat de periodetabel van het dienstverband bekend is. Bij de realisatie bepaalt de programmeur hoe dat precies wordt ingevuld.

Het alternatief — alleen de werkgever vastleggen — zou dat opzoekwerk besparen, maar dan valt de venstertoets uit §7.3 weg en rekent elke wijziging de werkgever volledig door, ook een correctie op een tijdvak van jaren geleden.

**Wanneer er een triggerregel wordt weggeschreven**

| Gebeurtenis | Welke regels |
| --- | --- |
| Klaarzetten van de loonaangifte | Het klaargezette tijdvak |
| Intrekken van een loonaangifte | Het ingetrokken tijdvak |
| Functiewijziging op het dienstverband: nieuw, gewijzigd of verwijderd | Alle aangiftetijdvakken die de begin- en einddatum van de functie raken |
| Wijziging in de functiecategorie-inrichting | Voor **alle** werkgevers het laatste klaargezette tijdvak, per periodetabel |

**Bij een functiewijziging leiden we de tijdvakken af uit de begin- en einddatum van de functie.** Elk aangiftetijdvak waarin die periode valt levert een triggerregel op. Raakt de wijziging meerdere tijdvakken — een functiewijziging met terugwerkende kracht bijvoorbeeld — dan komen die er allemaal in. Bij het bijwerken bepaalt de taak vervolgens welke van die tijdvakken binnen het venster vallen en dus relevant zijn (§7.3).

**Een contractwijziging schrijft géén triggerregel.** Nieuw, eigenschappen wijzigen, verwijderen, contractverlenging en indienstmelding vallen er dus buiten. Twee redenen: een contractwijziging is niet per se een functiewijziging, en als hij de loongegevens raakt, leidt hij zelf al tot een correctie op de loonaangifte — en die schrijft wél een triggerregel weg. Alleen de functie is een gegeven dat de indeling in functiecategorieën verandert zonder dat er iets in de loonaangifte gebeurt, en daarom is dat het enige stamgegeven waarop we triggeren.

**Een wijziging in de functiecategorie-inrichting raakt iedereen.** Koppelt de klant een functie aan een andere categorie, voegt hij een categorie toe of haalt hij er een weg, dan verandert de vergelijkingsgroep van elke medewerker met zo'n functie — en daarmee de gemiddelden van beide betrokken categorieën. Die wijziging hangt niet aan een werkgever en niet aan een tijdvak, dus is er geen kleinere afbakening te maken dan alle werkgevers.

We schrijven daarvoor per werkgever en periodetabel één regel weg, op het **laatste klaargezette tijdvak**. Dat tijdvak valt per definitie binnen het venster, dus de venstertoets uit §7.3 laat de regel altijd door. Meer regels zijn niet nodig: één triggerregel is genoeg om een werkgever volledig te laten doorrekenen. Werkgevers die nog nooit een aangifte hebben klaargezet krijgen geen regel; daar valt ook niets te berekenen.

**Wijzigingen buiten het venster leiden niet tot bijwerken.** Dat filteren we niet bij het wegschrijven maar bij het uitvoeren van de taak (§7.3). Het venster kan tussen die twee momenten namelijk verschuiven, en de schrijvende processen hoeven er geen weet van te hebben hoe het wordt bepaald.

**Opschonen.** Een triggerregel wordt verwijderd zodra de taak hem heeft verwerkt, ook als die verwerking uitmondt in "niets te doen, want dit tijdvak valt buiten het venster". Loopt de taak vast, dan blijven de regels staan en worden ze bij de volgende run alsnog meegenomen. Dat is precies waarvoor de tabel bestaat: hij maakt het bijwerken herstelbaar zonder dat iemand hoeft te achterhalen wat er is gemist.

### 7.3 Wat de taak doet

De taak Bijwerken gegevens loontransparantie werkt de lagen 0, 2 en 3 bij. Laag 1 raakt hij niet aan; die wordt gevuld door het loonaangifteproces (§7.1).

1. leest de triggertabel en bepaalt de werkgevers waarvoor een regel openstaat;
2. bepaalt per werkgever en periodetabel het laatste klaargezette aangiftetijdvak en daarmee het venster;
3. toetst per triggerregel of het tijdvak binnen dat venster valt; regels die er volledig buiten vallen leiden niet tot een bijwerking en worden alleen opgeruimd;
4. werkt voor de overblijvende werkgevers de rapportageperiode met rapportagejaar 0 bij;
5. selecteert de arbeidsverhoudingen die aan het populatiefilter voldoen;
6. leest per arbeidsverhouding de tijdvakken binnen het venster uit de brontabel, zo nodig over twee kalenderjaren, telt daarbij de dienstverbanden onder dezelfde inkomstenverhouding per tijdvak op, en kent elk tijdvak toe aan de functie die op de laatste dag ervan gold (§4.5);
7. berekent per tijdvak het brutoloon en de waarde variabele componenten, telt die per functie op, bepaalt de kenmerken en schrijft per functie de regel per inkomstenverhouding;
8. stelt de tabel per functiecategorie opnieuw samen voor de geraakte rapportage-eenheden, inclusief de acht loonverschilpercentages;
9. verwijdert de regels die niet meer aan de selectie voldoen en ruimt de verwerkte triggerregels op.

Stap 3 is de reden dat de triggertabel de periode bevat en niet alleen de werkgever. Een correctie op een tijdvak van twee jaar geleden verandert niets aan wat de medewerker ziet en hoeft dus geen volledige doorrekening van die werkgever uit te lokken.

De brontabel schrijft de taak niet. Die wordt gevuld door het loonaangifteproces; de taak leest hem alleen. Daarmee is stap 5 en verder puur leeswerk op bronvaste gegevens.

De rekenroutine in stap 7 krijgt het periodebereik als parameter mee. In fase 1 is dat het venster. Datzelfde mechanisme vult in fase 2 een rapportageperiode met een gevuld rapportagejaar, zonder tweede rekenimplementatie en dus zonder tweede waarheid.

De taak stelt de gegevens bij elke run volledig opnieuw samen voor de werkgevers die aan de beurt zijn. Er wordt niet bijgewerkt op basis van een vorige stand. Dat maakt het proces voorspelbaar: elke run geeft hetzelfde resultaat bij dezelfde brongegevens. Het maakt het ook uitlegbaar, want elk getal op het scherm is terug te volgen naar de perioden en rubrieken eronder.

**De taak is ook los te starten.** Hij draait normaal vanuit de dagovergang, maar kan daarnaast handmatig worden uitgevoerd, bijvoorbeeld na een fout of nadat een klant zijn functiecategorieën heeft ingericht en de cijfers niet tot de volgende nacht wil afwachten. Omdat de taak alles opnieuw samenstelt, is een extra run nooit schadelijk.

De taak leest bestaande tabellen en schrijft uitsluitend naar de drie eigen tabellen en de triggertabel. Ze wijzigt geen loongegevens.

### 7.4 Omvang van een run

Stap 4 tot en met 7 raken alleen de werkgevers waarvoor een triggerregel binnen het venster openstond. Het venster wordt toch al per werkgever en periodetabel bepaald, en werkgevers zonder wijziging leveren dezelfde uitkomst als de vorige run.

De zwaarste run is die na een wijziging in de functiecategorie-inrichting: dan staan er triggerregels voor alle werkgevers open en rekent de taak de hele omgeving door (§7.2). Dat komt weinig voor — een klant herziet zijn functiecategorieën niet dagelijks — en het is de enige manier om de vergelijkingscijfers op de nieuwe indeling te krijgen. Bij een reguliere run gaat het om de werkgevers die die dag daadwerkelijk iets hebben gewijzigd.

Stap 8 is breder. De tabel per functiecategorie gaat per **rapportage-eenheid**, en meerdere werkgevers kunnen tot dezelfde eenheid horen. Verandert er iets bij één werkgever, dan verandert het gemiddelde van de hele groep. De taak stelt die regels daarom opnieuw samen op basis van de regels per inkomstenverhouding van **alle werkgevers binnen die eenheid**, ook al zijn die zelf niet opnieuw doorgerekend. Dat is een goedkope bewerking: het is een optelling over regels per inkomstenverhouding, niet over tijdvakken.

Beperken we die stap wel tot één werkgever, dan zouden de vergelijkingscijfers de bijdrage van de andere werkgevers verliezen. Daarom is dit de enige stap die buiten de eigen werkgever kijkt. Heeft de werkgever geen RSIN, dan is de eenheid die ene werkgever en valt stap 8 samen met de rest van de run.

In de rest van dit hoofdstuk staat **RSIN** kortweg voor de rapportage-eenheid uit §5.2.

**Gelijktijdige runs binnen één RSIN.** Met één taak vanuit de dagovergang is dit grotendeels opgelost: de taak verwerkt de rapportage-eenheden één voor één, dus twee werkgevers binnen hetzelfde concern kunnen elkaars verdichting niet meer overschrijven. In de eerdere opzet — één wachtrijtaak per klaargezette aangifte — kon dat wel, en dat herstelde zich niet vanzelf.

De eis blijft toch staan dat er per RSIN nooit meer dan één run tegelijk loopt, omdat de taak ook handmatig kan worden gestart en dat kan samenvallen met de dagovergang:

- Start een taak terwijl er al een run bezig is die hetzelfde RSIN raakt, dan **wacht** die tot de lopende klaar is. Ze wordt niet afgebroken en niet overgeslagen.
- Staan er meerdere runs te wachten, dan is één keer doorrekenen genoeg. De taak stelt alles volledig opnieuw samen (§7.3), dus de laatste wachtende run levert hetzelfde resultaat als alle wachtende runs achter elkaar.
- Het wachten geldt voor de **hele** run, niet alleen voor stap 8. De stappen ervoor schrijven de regels per inkomstenverhouding waar de verdichting op steunt.
- Runs voor **verschillende** RSIN's mogen wel gelijktijdig lopen. Die raken elkaars regels niet.

Hoe dat wachten wordt gerealiseerd — een lock op RSIN-niveau of een wachtrij met één actieve taak — hoort bij het technisch ontwerp (§12, punt E1). Het wachten is voor de gebruiker onzichtbaar: de taak loopt buiten het loonaangifteproces om.

### 7.5 Correcties

Bij een correctie op een eerder tijdvak werkt het loonaangifteproces de bestaande regel in de brontabel bij. De regel wordt overschreven met de gecorrigeerde stand; er komt geen tweede regel bij. De brontabel bevat daarmee altijd de **laatste ingediende stand** per tijdvak, precies zoals die bij de Belastingdienst bekend is. Het klaarzetten van de correctie schrijft ook een triggerregel weg voor het gecorrigeerde tijdvak.

De taak stelt de twee tabellen erboven bij de eerstvolgende run opnieuw samen, dus de bedragen worden vanzelf goed. Dat geldt ook voor een **jaaroverschrijdende** correctie: die volgt dezelfde route en hoeft niet apart te worden afgehandeld. Dat is eenvoudiger dan de eerdere opzet, waarin een correctie binnen het jaar een eigen run startte en een jaaroverschrijdende correctie moest meeliften op het eerstvolgende reguliere tijdvak.

Dit heeft twee gevolgen die we accepteren:

- **Er is geen correctiehistorie.** Wat er eerder is verstrekt, is niet meer op te vragen. Dat is functioneel gewenst — de medewerker hoort de juiste bedragen te zien — maar het betekent ook dat het dashboard een piek in een tijdvak niet als correctie kan herkennen.
- **Het venster begrenst wat meetelt.** Valt het gecorrigeerde tijdvak buiten het venster, dan is de regel in de brontabel wel bijgewerkt, maar telt hij niet mee in de regel per inkomstenverhouding. De taak ruimt de triggerregel dan alleen op (§7.3, stap 3). Dat is de consequentie van een venster van één jaar en het geldt voor elke correctie die verder terugreikt.

De correctie verschuift het venster niet. Het eindpunt blijft het laatste klaargezette reguliere tijdvak. Zo voorkomen we dat een correctie op bijvoorbeeld periode 12 van 2025 het venster terugzet terwijl de werkgever al op periode 3 van 2026 zit. Een correctietijdvak raakt bovendien vaak maar een kleine groep medewerkers en is dus geen geschikt ijkpunt.

### 7.6 Intrekken van een loonaangifte

Een werkgever kan een ingediende loonaangifte intrekken. Het loonaangifteproces verwijdert dan de bijbehorende regels uit de brontabel; die werking bestaat al.

Dat maakt een eerder eindpunt ongeldig. De intrekking schrijft daarom net als het klaarzetten een triggerregel weg. Bij de eerstvolgende run bepaalt de taak opnieuw wat het laatste klaargezette tijdvak is en schuift het venster een tijdvak terug. De medewerker ziet daardoor tijdelijk oudere cijfers, tot er opnieuw een aangifte is klaargezet.

Dat is bewust: het venster volgt altijd het laatste klaargezette tijdvak. Cijfers laten staan van een tijdvak dat is ingetrokken, zou betekenen dat we loongegevens tonen die niet meer zijn aangegeven.

### 7.7 Nieuwe klanten en de conversie naar Profit 9

Bij een nieuwe implementatie zijn de tabellen leeg. Er is dan nog geen aangifte klaargezet, dus er valt niets te berekenen. De tabellen raken gevuld zodra de eerste relevante aangifte is klaargezet en de taak daarna heeft gedraaid.

Dat is acceptabel. De werkgever moet een informatieverzoek beantwoorden binnen een redelijke termijn en uiterlijk binnen **twee maanden** na de datum van het verzoek. Dat staat in artikel 10b, derde lid van het wetsvoorstel en volgt artikel 7, vierde lid van de richtlijn. Een werkgever zet zijn eerste loonaangifte doorgaans binnen enkele weken klaar, dus ruim binnen die termijn.

Bij bestaande klanten bestaat de brontabel al en bevat hij historie, maar **zonder de loonbedragen**. Die vullen we eenmalig aan **in de conversie naar Profit 9**, over het jaar **2026**, op basis van de loonaangiftegegevens die in de omgeving aanwezig zijn.

We doen dat in de conversie en niet bij de eerstvolgende loonaangifte. Dat scheelt een controle die bij elke aangifte over 2026 opnieuw zou moeten draaien, het maakt het klaarzetten niet zwaarder, en de gegevens staan er in één keer voor alle werkgevers tegelijk. Bovendien is de uitkomst daarmee onafhankelijk van de vraag wanneer een klant zijn eerste aangifte na de release klaarzet.

Voor tijdvakken van andere jaren vult de conversie niets. Het venster reikt hooguit twaalf maanden of dertien tijdvakken terug, dus 2026 is genoeg om het venster in de loop van 2027 volledig te laten vollopen. Zolang dat niet zo is, rekent de taak met de tijdvakken die er wél zijn.

Eén beperking blijft staan: de loonaangiftegegevens verdwijnen zodra een salarisverwerking of aangifte wordt verwijderd. Voor die tijdvakken kan de conversie niets vullen en blijven de bedragen leeg. Die tijdvakken tellen dan niet mee in het venster.

De conversie schrijft geen triggerregels. Na de conversie stelt de taak bij de eerstvolgende dagovergang de lagen 2 en 3 hoe dan ook voor alle werkgevers samen, omdat die tabellen dan nog niet bestaan.

### 7.8 Als de taak niet slaagt

De bestaande gegevens blijven staan tot de nieuwe generatie compleet is. Een mislukte run mag er nooit toe leiden dat de medewerker een lege of half gevulde KPI ziet.

Daarvoor werkt de taak **transactioneel per rapportage-eenheid**. Binnen één transactie stelt ze achtereenvolgens opnieuw samen:

1. de regels per inkomstenverhouding van de werkgevers die aan de beurt zijn;
2. de regels per functiecategorie van de hele rapportage-eenheid;
3. de rapportageperiode, met de datum van de laatste berekening als laatste schrijfactie.

Slaagt een van die stappen niet, dan rolt de hele transactie terug en blijft de vorige generatie ongewijzigd staan. Er is dus geen tussenstand waarin laag 2 al is bijgewerkt en laag 3 nog niet, of waarin een deel van de functiecategorieën nieuw is en een deel oud.

**De triggerregels blijven bij een fout staan.** Ze worden pas opgeruimd als de transactie voor die rapportage-eenheid is geslaagd. Daardoor pakt de volgende run precies op waar het misging, zonder dat iemand hoeft te achterhalen welke werkgevers zijn overgeslagen. Loopt een rapportage-eenheid vast, dan gaat de taak wel door met de overige eenheden; één probleemgeval mag de rest niet blokkeren.

De datum van de laatste berekening schrijven we bewust als laatste. Die datum is daarmee het bewijs dat de hele set compleet is: staat er een oude datum, dan is de laatste run niet geslaagd, en dat is zichtbaar in de weergaven en bij de informatie die aan de medewerker wordt verstrekt.

De taak schrijft alleen naar de drie eigen tabellen en de triggertabel. De brontabel wordt gevuld door het loonaangifteproces en valt buiten deze transactie, zodat een mislukte berekening nooit de aangiftegegevens raakt.

De verwerking is idempotent. De taak stelt alles volledig opnieuw samen en werkt niet bij op basis van een vorige stand, dus een mislukte run kan zonder voorbereiding opnieuw worden gestart en levert bij dezelfde brongegevens hetzelfde resultaat. Er is geen herstelroutine nodig die een halve stand repareert.

De omvang van de transactie is de betrokken werkgevers voor laag 2 en één RSIN voor laag 3. Bij een concern met veel werkgevers kan dat een lange transactie opleveren. Dat raakt het loonaangifteproces niet, omdat de taak daarbuiten loopt, maar het is wel de reden om de verdichting per RSIN te serialiseren (§7.4).

Op de regel staat de datum van de laatste berekening en de einddatum van de rapportageperiode. Daarmee is altijd zichtbaar hoe actueel de gegevens zijn, ook als een run is mislukt.

## 8 Presentatie: KPI en weergaven op de stamkaart

### 8.1 Waar de medewerker het vindt

Op de stamkaart medewerker in InSite komt onder **Salaris** een nieuw tabblad **Loontransparantie**. Daar staan vier KPI-tegels, met daaronder twee weergaven.

De medewerker ziet het eigen loonniveau en de vergelijkingscijfers van de eigen functiecategorie. Alle getoonde waarden komen uit één regel per inkomstenverhouding en één regel per functiecategorie; er wordt bij het openen van de pagina niets herberekend. Ook de vier loonverschilpercentages zijn voorberekend (§5.5). Welke regel per inkomstenverhouding dat is als er meerdere zijn, staat in §8.5.

De cijfers zijn zo actueel als de laatste geslaagde run van de taak Bijwerken gegevens loontransparantie (§7.1). Die draait doorgaans elke nacht, dus een wijziging van vandaag is morgen zichtbaar.

### 8.2 De vier KPI-tegels

De tegels staan in deze volgorde:

| Nr. | Titel | Grondslag |
| --- | --- | --- |
| 1 | Loonverschil jaarloon | Gemiddeld bruto jaarloon |
| 2 | Loonverschil componenten jaarwaarde | Gemiddelde jaarwaarde variabele componenten |
| 3 | Loonverschil uurloon | Gemiddeld bruto uurloon |
| 4 | Loonverschil componenten uurwaarde | Gemiddelde uurwaarde variabele componenten |

Tegel 1 staat bovenaan omdat dat de wettelijk voorgeschreven maat is. Daarna volgt de opsplitsing naar de jaarwaarde van de variabele componenten, en pas daarna dezelfde twee op uurwaarde. Zo staan de jaarcijfers bij elkaar en de uurcijfers bij elkaar, en hoeft de medewerker niet tussen twee grondslagen heen en weer te lezen.

Elke tegel is als volgt opgebouwd:

| Kenmerk | Invulling |
| --- | --- |
| Type | Value |
| Subtitel | Laatste 12 maanden |
| Waarde | Het bijbehorende loonverschilpercentage, gelezen van de regel per functiecategorie (§5.5, §6.5) |
| Waardetype | Percentage |
| Toelichting onder de waarde | Vrouwen verdienen gemiddeld minder dan mannen |
| Info-icoon | Uitleg over de grondslag, de berekening en de gebruikte periode |

Is de uitkomst negatief, dan verdienen vrouwen in deze categorie gemiddeld meer. De toelichtende tekst past zich daarop aan. Is er geen gemiddelde voor de mannen, dan blijft de tegel leeg met de melding uit §8.6.

De subtitel is **Laatste 12 maanden**. De mockup toont daar een jaartal, maar dat klopt niet bij een voortschrijdend venster dat over twee kalenderjaren loopt. Bij dertien perioden gaat het feitelijk om dertien perioden; voor de medewerker is dat in alle gevallen ongeveer een jaar. De precieze begin- en einddatum staan in de uitleg achter het info-icoon.

Het info-icoon van tegel 1 vermeldt dat dit de wettelijk voorgeschreven maat is. Dat van tegel 3 legt uit dat het uurloon corrigeert voor deeltijd en voor een dienstverband dat niet het hele jaar liep, en dat het percentage daarom kan afwijken van tegel 1.

### 8.3 Weergave Mijn loonniveau vergeleken

Onder de tegels staat een tabel met vijf regels en drie kolommen.

Regels:

1. Jaaruren
2. Bruto jaarloon
3. Bruto uurloon
4. Jaarwaarde variabele componenten
5. Uurwaarde variabele componenten

Kolommen:

| Kolom | Inhoud |
| --- | --- |
| Jij | De eigen waarde van de medewerker, uit de regel per inkomstenverhouding |
| Mannen | Het gemiddelde van de mannen in de functiecategorie, uit de tabel per functiecategorie |
| Vrouwen | Het gemiddelde van de vrouwen in de functiecategorie, uit de tabel per functiecategorie |

**Mannen staan vóór vrouwen.** Dat is geen willekeurige volgorde: de mannen zijn de referentiegroep. Alle loonverschilpercentages delen door het gemiddelde van de mannen (§6.5), dus dat getal is de noemer. Wie de tabel van links naar rechts leest, ziet eerst waar hij zelf staat, dan de referentie en dan de groep die daartegen wordt afgezet — dezelfde volgorde als in de formule.

Er is geen kolom Mediaan en geen kolom Individueel verschil. De onderbouwing staat in §6.4.

Elke regel heeft een info-icoon met uitleg over wat de waarde betekent en hoe die is opgebouwd.

Er komt geen grafiek bij de KPI's. De vier tegels tonen de percentages en deze tabel toont de onderliggende gemiddelden per geslacht; een staafgrafiek zou dezelfde twee getallen een derde keer laten zien. Verdiepende beelden, zoals de verdeling binnen een categorie of het verloop over de perioden, horen in het dashboard.

### 8.4 Weergave Functies in jouw functiecategorie

Onder de vergelijkingstabel staat een weergave met de functies die tot dezelfde functiecategorie behoren als de medewerker. Zo ziet de medewerker met welke functies zijn loon wordt vergeleken.

| Kenmerk | Invulling |
| --- | --- |
| Titel | Functies in jouw functiecategorie |
| Bron | De functiecategorie-inrichting van de klant |
| Kolom | Omschrijving |
| Sortering | Alfabetisch op omschrijving |
| Aantal regels | Alle functies; bij een lange lijst scrollt de weergave |

We lezen de lijst uit de **functiecategorie-inrichting**, niet uit de regels per inkomstenverhouding. De medewerker ziet daarmee de volledige categorie zoals de werkgever die heeft bedoeld, ook functies waarop op dit moment niemand werkt. Zou de lijst uit die regels komen, dan zou zichtbaar worden hoe klein de vergelijkingsgroep feitelijk is, en dat maakt de cijfers herleidbaarder.

De eigen functie van de medewerker krijgt geen aparte markering en staat niet bovenaan. De lijst is puur alfabetisch.

De weergave toont alleen functieomschrijvingen. Er staan geen aantallen, namen of bedragen per functie in, omdat dat tot herleidbare gegevens zou leiden.

Is de functie van de medewerker niet aan een categorie gekoppeld, dan is er geen lijst en blijft de weergave leeg. Dat past bij §3.7: er is dan ook geen vergelijking.

### 8.5 Meerdere regels per medewerker

Een medewerker kan meerdere regels per inkomstenverhouding hebben, om twee redenen: hij heeft meerdere inkomstenverhoudingen, of hij is binnen het venster van functie gewisseld (§5.4). Op de stamkaart tonen we altijd één regel.

**Welke regel dat is**, bepalen we in twee stappen:

1. de inkomstenverhouding van het **hoofddienstverband**;
2. daarbinnen de regel van de **actuele functie**: de functie die geldt op het moment van opvragen.

We kijken bewust naar de actuele functie en niet naar de functie op de laatste dag van het venster. Het venster eindigt bij het laatste klaargezette aangiftetijdvak en loopt dus achter op vandaag. Vraagt de medewerker zijn gegevens op, dan hoort hij te worden vergeleken met de collega's in de functie die hij op dat moment heeft. Het filter zit op de gegevensverzameling (§5.9), zodat de KPI, het document en de route van DP4 alle drie hetzelfde tonen.

Wisselde de medewerker binnen het venster van functie, dan ziet hij dus de cijfers van zijn huidige functie, over de tijdvakken waarin hij die functie had. Het aantal toegekende tijdvakken staat op de regel (§5.4), zodat te verklaren is waarom het bruto jaarloon lager uitvalt dan een vol jaar.

**Bij een recente functiewijziging is er mogelijk nog geen regel.** Is er nog geen loonaangifte klaargezet waarin de nieuwe functie valt, dan heeft de taak voor die functie nog niets kunnen berekenen. De medewerker ziet dan geen eigen waarden in de kolom Jij.

De **vergelijkingscijfers zijn er wel**. De vier KPI-tegels en de kolommen Mannen en Vrouwen lezen de tabel per functiecategorie (§5.5) en hebben de eigen regel niet nodig; welke categorie dat is, leiden we af uit de actuele functie. De medewerker ziet dus meteen waar zijn nieuwe functiecategorie staat, ook al ontbreekt zijn eigen loon nog. Dat vult zich vanzelf zodra de eerstvolgende loonaangifte is klaargezet en de taak daarna heeft gedraaid.

Welk dienstverband het hoofddienstverband is, staat niet op de regel zelf. De KPI haalt dat bij het opbouwen op uit de stamgegevens (§5.4), zodat een wijziging meteen doorwerkt en niet pas na de volgende run van de taak.

Een KPI toont één waarde. Een keuzelijst waarmee de medewerker wisselt tussen arbeidsverhoudingen of eerdere functies past niet bij dit type tegel en zou het scherm onnodig ingewikkeld maken. Voor het overgrote deel van de medewerkers is er bovendien maar één regel.

Heeft een medewerker meer dan één inkomstenverhouding, dan maken we dat zichtbaar en verwijzen we naar de uitgebreide route: een gegenereerd document of een vraag via het type dossieritem uit DP4.

### 8.6 Als er geen gegevens zijn

De medewerker kan om verschillende redenen geen volledige informatie zien. We maken in alle gevallen duidelijk waarom, zodat het scherm niet zomaar leeg is:

| Situatie | Wat de medewerker ziet |
| --- | --- |
| Er is nog geen loonaangifte klaargezet, of de taak heeft nog niet gedraaid | Een melding dat de gegevens beschikbaar komen zodra de eerste loonaangifte is verwerkt |
| De arbeidsverhouding valt buiten de regeling | Een neutrale melding dat de loongegevens niet onder de regeling vallen. Geldt bij een soort inkomstenverhouding of aard arbeidsverhouding die niet meetelt, bij een periodetabel die we niet ondersteunen (§4.3), en als er over het venster geen loon of geen verloonde uren zijn (§3.4) |
| De functie is niet aan een functiecategorie gekoppeld | Geen KPI's en geen vergelijkingscijfers; wel de eigen waarden, met de melding dat vergelijken niet mogelijk is |
| De medewerker is recent van functie gewisseld en er is nog geen loonaangifte over die functie klaargezet | Geen eigen waarden in de kolom Jij; de vier KPI's en de kolommen Mannen en Vrouwen van de nieuwe functiecategorie zijn er wél, met de melding dat de eigen gegevens nog volgen |
| Er zijn geen mannen in de functiecategorie | Geen KPI's; wel de eigen waarden en de kolom Vrouwen, met de melding dat er niets te vergelijken valt |
| Er zijn geen vrouwen in de functiecategorie | Geen KPI's; wel de eigen waarden en de kolom Mannen, met dezelfde melding |

**Een lege geslachtsgroep werkt beide kanten op.** Ontbreekt een van de twee groepen, dan blijven alle acht percentages leeg — ook als er wel een gemiddelde voor de andere groep is. Een percentage vraagt immers twee groepen. De gevulde kolom tonen we wél: die informatie is er en heeft waarde, ook zonder vergelijking. We tonen nooit 100% als de ene groep ontbreekt; dat zou lezen als een maximaal loonverschil terwijl er in werkelijkheid niets te vergelijken valt.

**Ontbrekende eigen gegevens blokkeren de vergelijking niet.** Bij een recente functiewijziging is er nog geen regel per inkomstenverhouding voor de nieuwe functie, maar de tabel per functiecategorie is er wel. De KPI's en de kolommen Mannen en Vrouwen lezen alleen die tabel, dus die vullen we gewoon (§8.5). Alleen de kolom Jij blijft leeg. Zouden we het hele blok verbergen, dan zag de medewerker niets terwijl de informatie waar hij recht op heeft — het loonverschil in zijn functiecategorie — beschikbaar is.

**Er is geen melding voor nul verloonde uren.** Die situatie stond hier eerder wel, maar kan niet optreden: verloonde uren groter dan nul is een selectiecriterium (§3.4), dus wie geen uren heeft komt niet in de tabellen en valt onder de tweede situatie hierboven.

### 8.7 Teksten

De onderstaande teksten zijn een voorstel. Team Content scherpt ze aan.

**Meldingen** [voorstel]

| Situatie | Tekst |
| --- | --- |
| Nog geen loonaangifte klaargezet | Je ziet hier je loongegevens zodra je werkgever de eerste loonaangifte heeft verwerkt. |
| Arbeidsverhouding valt buiten de regeling | Voor dit dienstverband kunnen we geen loonvergelijking maken. Heb je hier vragen over? Stel ze aan HR. |
| Functie niet gekoppeld aan een functiecategorie | We kunnen je loon nog niet vergelijken. Je functie hoort nog niet bij een functiecategorie. Vraag je werkgever hiernaar. |
| Geen mannen in de functiecategorie | We kunnen geen loonverschil berekenen. In jouw functiecategorie werken op dit moment geen mannen. |
| Geen vrouwen in de functiecategorie | We kunnen geen loonverschil berekenen. In jouw functiecategorie werken op dit moment geen vrouwen. |
| Meer dan één dienstverband | Je hebt meer dan één dienstverband. Hier zie je de gegevens van je hoofddienstverband. Wil je alle dienstverbanden zien? Stel dan een vraag aan HR. |
| Binnen het jaar van functie gewisseld | Je bent dit jaar van functie gewisseld. Hier zie je de gegevens van je huidige functie, over de periode waarin je die functie had. |
| Recent van functie gewisseld, eigen gegevens nog niet berekend | Je bent onlangs van functie gewisseld. Je eigen loongegevens over deze functie zie je zodra je werkgever de eerstvolgende loonaangifte heeft verwerkt. De vergelijking met je nieuwe functiecategorie staat er al wel. |

De melding bij "valt buiten de regeling" is bewust neutraal gehouden. De onderliggende reden — een soort inkomstenverhouding die niet meetelt, of een niet-ondersteunde periodetabel — zegt de medewerker niets en zou tot vragen leiden die hij zelf niet kan oplossen. De verwijzing naar HR is er om die vraag op de juiste plek te laten landen.

**Uitleg achter de info-iconen** [voorstel]
| Onderdeel | Tekst |
| --- | --- |
| Loonverschil jaarloon | Dit percentage laat zien hoeveel vrouwen in jouw functiecategorie gemiddeld minder verdienen dan mannen. We rekenen met het bruto jaarloon over de laatste 12 maanden, van [begindatum] tot en met [einddatum]. Dit is de manier waarop de wet het loonverschil voorschrijft. |
| Loonverschil componenten jaarwaarde | Dit percentage gaat alleen over het loon bovenop het basisloon, zoals toeslagen en bonussen. Zo zie je of het verschil in je basisloon zit of in wat daar bovenop komt. |
| Loonverschil uurloon | Dit percentage rekent met het bruto uurloon in plaats van het jaarloon. Werken mannen en vrouwen in jouw categorie verschillend veel uren, dan geeft dit percentage een eerlijker beeld. Wijkt het sterk af van het percentage hierboven, dan zit het verschil vooral in het aantal uren. |
| Loonverschil componenten uurwaarde | Dit percentage gaat over het loon bovenop je basisloon, omgerekend per verloond uur. |
| Jaaruren | Het aantal uren dat in de afgelopen 12 maanden voor je is verloond. |
| Bruto jaarloon | Je brutoloon over de afgelopen 12 maanden. Werkte je niet het hele jaar of in deeltijd, dan is dit bedrag lager. |
| Bruto uurloon | Je brutoloon over de afgelopen 12 maanden, gedeeld door het aantal verloonde uren. Hiermee kun je je loon eerlijk vergelijken, ook als je in deeltijd werkt. |
| Jaarwaarde variabele componenten | Het deel van je loon bovenop je basisloon, zoals toeslagen en bonussen, over de afgelopen 12 maanden. |
| Uurwaarde variabele componenten | Het deel van je loon bovenop je basisloon, zoals toeslagen en bonussen, per verloond uur. |
| Functies in jouw functiecategorie | Dit zijn de functies waarmee je loon wordt vergeleken. Je werkgever bepaalt welke functies bij elkaar horen. |

---

## 9 Autorisatie, privacy en groepsgrootte

### 9.1 Wie wat ziet

De gegevens op de stamkaart gaan over het loon van de medewerker zelf en over gemiddelden van collega's. Dat is gevoelige informatie.

We stellen het tabblad beschikbaar aan de medewerker zelf, aan HR en aan de manager. HR moet informatieverzoeken kunnen beantwoorden en de manager moet het gesprek over beloning kunnen voeren met de eigen medewerkers.

Het tabblad Loontransparantie is **autoriseerbaar**. De klant bepaalt zelf per rol of het zichtbaar is. Wil een klant het niet voor managers openstellen, dan kan dat.

### 9.2 Afscherming van de tabellen zelf

De brontabel en de regels per inkomstenverhouding bevatten loongegevens van alle medewerkers. Zonder afscherming zouden die via een eigen weergave of gegevensverzameling te benaderen zijn, en dan is de afweging over herleidbaarheid uit §9.3 te omzeilen.

Dit vraagt bijzondere aandacht, omdat we een **bestaande** tabel uitbreiden. De tabel Loonaangifte uren per medewerker is nu al ontsloten via een view in de querywizard en via een InSite-datamodeldefinitie. Met de loonbedragen erbij komt daar individuele beloningsinformatie in te staan die er nu niet in zit. De bestaande ontsluiting moet daarom worden herzien voordat de uitbreiding wordt uitgeleverd; dat is punt G2 in §12.

We ontsluiten de gegevens verder uitsluitend via de meegeleverde weergaven en gegevensverzamelingen (§5.9). Op die gegevensverzamelingen passen we **medewerkerautorisatie** toe bij het lezen: een gebruiker ziet alleen de gegevens van de medewerkers waarvoor hij geautoriseerd is.

De tabel per functiecategorie bevat geen individuele gegevens, alleen gemiddelden per groep. Die valt onder dezelfde afscherming, omdat een gemiddelde in een kleine groep alsnog herleidbaar is (§9.3).

### 9.3 Groepsgrootte

We hanteren **geen ondergrens** voor de vergelijkingscijfers. Zodra er een functiecategorie is, tonen we de gemiddelden, ook als een geslachtsgroep uit één persoon bestaat.

De afweging tussen privacy en het recht op gelijk loon is al door de wetgever gemaakt. De toelichting bij het wetsvoorstel stelt dat het recht op gelijk loon de doorslag geeft en dat de verwerking van persoonsgegevens noodzakelijk is om aan de wettelijke verplichting te voldoen. Wij maken die afweging dus niet opnieuw en zetten er ook geen eigen drempel overheen. Een ondergrens van bijvoorbeeld vijf medewerkers zou het recht in kleine en scheef verdeelde organisaties structureel uithollen, precies daar waar een loonverschil het hardst aankomt.

Dit betekent dat de gegevens in kleine categorieën herleidbaar zijn tot een individuele collega. Bij één vrouw in de categorie is het gemiddelde van de vrouwen simpelweg haar salaris, en dat is dan zichtbaar voor iedereen in die categorie.

Dat is een bewust aanvaard risico. Wat we er wel tegenover zetten: de gegevens worden alleen voor dit doel gebruikt en zijn afgeschermd zoals beschreven in §9.2. De klant kan bovendien zelf sturen via de indeling van zijn functiecategorieën.

### 9.4 Wat we niet tonen

We tonen geen namen, geen aantallen per geslacht, geen bedragen per functie en geen hoogste of laagste waarde binnen de groep. De medewerker ziet alleen gemiddelden, nooit de onderliggende individuele waarden van collega's.

### 9.5 Uitlevering

We leveren de functionaliteit generiek uit onder de bestaande HR-conditie. Er komt geen aparte activering. Het gaat om een wettelijke verplichting die voor alle klanten geldt, dus iedere klant krijgt het meteen.

De klant houdt grip via de autorisatie op het tabblad en via de eigen inrichting van de functiecategorieën.

### 9.6 Landafhankelijkheid

De berekening is opgebouwd uit de rubrieken van de **Nederlandse loonaangifte** (§6.2). Daarmee werkt dit ontwerp alleen voor medewerkers die onder Nederlandse wetgeving vallen. In België doet AFAS de loonaangifte niet — de salarisgegevens lopen daar via sociaalsecretariaten — dus daar is er geen bron waarmee het venster gevuld kan worden. Een variant op de loonberekening in plaats van de loonaangifte lost dat niet op, want ook dan blijven de begrippen Nederlands.

**De gegevens filteren zichzelf al.** De brontabel wordt uitsluitend gevuld bij het klaarzetten van de Nederlandse loonaangifte (§7.1). Een medewerker die daar niet in voorkomt, krijgt dus ook geen regel per inkomstenverhouding en telt niet mee in de vergelijkingscijfers. De taak heeft daarom geen eigen landfilter nodig en het gegevensmodel evenmin: er zit **geen landafhankelijk sleutelonderdeel of veld** in. Komt er later een Belgische bron, dan vult die dezelfde vier lagen zonder dat het model wordt opengebroken.

**Wat wél nodig is, is een toets bij het tonen.** Zonder die toets ziet een Belgische medewerker een tabblad met de melding "je ziet hier je loongegevens zodra je werkgever de eerste loonaangifte heeft verwerkt" (§8.6). Die melding is voor hem onjuist en wekt een verwachting die nooit wordt ingelost.

We toetsen daarvoor het **land van wetgeving van de medewerker**:

| Onderwerp | Invulling |
| --- | --- |
| Gegeven | `AfasKnCountryByLaw` op `AfasKnBasicContact`, te bereiken via `AfasKnEmployee.AfasKnBasicContactId` |
| Waarden | ISO-landcodes van twee posities; in de praktijk `NL` en `BE` |
| Leeg | Behandelen als `NL`, conform de bestaande conventie in HR (`ISNULL(AfasKnCountryByLaw, 'NL')`) |
| Gedrag | Is de waarde niet `NL`, dan tonen we het tabblad Loontransparantie niet |
| Bestaande functie | `GetEmployeesCountryByLaw(employeeId)` in `AfasHrGeneralLib`, beschikbaar vanuit webforms |

Dit is een bestaand patroon en niet iets nieuws. HR gebruikt dit veld op tientallen plekken om Nederlandse en Belgische functionaliteit te scheiden, en er is een KPI die precies dit doet: **Saldi geboorteverlof** leest het land van wetgeving van de medewerker, toont de Nederlandse variant bij `NL`, de Belgische bij `BE`, en toont niets bij een ander land.

**Waarom niet het land van wetgeving op de administratie** (`CoLa`, businesscomponent `KnUnp`). Dat veld bestaat en HR gebruikt het ook, maar het geldt voor de hele administratie. Eén administratie kan werkgevers en medewerkers uit meerdere landen bevatten, en dan valt de toets de verkeerde kant op: óf een Belgische medewerker krijgt het tabblad alsnog, óf een Nederlandse medewerker in een als Belgisch ingerichte administratie krijgt het ten onrechte niet. Het medewerkerveld is fijnmazig genoeg en het enige dat de vraag beantwoordt die wij stellen.

Open blijft de vraag of België functioneel binnen de scope van dit deelproject valt, en zo ja welke bron daar in de plaats treedt van de loonaangifte (hoofdstuk 12, punt O1).

---

## 10 Randvoorwaarden en performance

- **Het salarisproces gaat voor.** Het klaarzetten van de loonaangifte vult laag 1 en schrijft een triggerregel weg; meer doet het niet. Het rekenwerk gebeurt in een aparte wachtrijtaak buiten het loonaangifteproces. Duurt een run lang, dan mag dat het klaarzetten niet raken.
- **De gegevens zijn maximaal één dagovergang oud.** De taak draait vanuit Vernieuwen actuele gegevens (§7.1). Laag 1 is direct actueel, de lagen 2 en 3 lopen daar hooguit één nacht op achter.
- **De taak moet herstartbaar zijn.** Bij een fout blijven de triggerregels staan en kan de taak los opnieuw worden uitgevoerd (§7.8). Er mag geen handmatige reparatie nodig zijn om een gemiste werkgever alsnog mee te nemen.
- **De triggertabel blijft klein.** Regels worden opgeruimd zodra ze zijn verwerkt (§7.2). Groeit hij toch, dan is dat een signaal dat de taak niet slaagt.
- **Bij het uitlezen wordt niet gerekend.** De KPI en de weergaven lezen kant-en-klare waarden uit twee regels: die per inkomstenverhouding en die per functiecategorie. Ook de vier loonverschilpercentages zijn voorberekend.
- **De brontabel groeit met de tijd.** We schonen hem niet op, zoals dat nu ook al niet gebeurt. Het aantal regels neemt per jaar toe met het aantal dienstverbanden maal twaalf of dertien. De uitbreiding voegt daar zeven bedragen per regel aan toe.
- **De verdichting kijkt breder dan één werkgever.** De tabel per functiecategorie gaat per rapportage-eenheid. Een run raakt daardoor ook regels van werkgevers die zelf niet zijn doorgerekend (§7.4).
- **Een wijziging in de functiecategorie-inrichting rekent de hele omgeving door.** Dat is de zwaarste run (§7.2). Hij past binnen het tijdvenster van de dagovergang en komt weinig voor, maar het is wel het geval waarmee bij het bouwen rekening moet worden gehouden.
- **De berekening staat op één plek.** De taak rekent, de presentatielagen lezen. Het dashboard mag de berekeningen uit hoofdstuk 6 niet opnieuw implementeren in eigen queries; dan ontstaan er twee waarheden die apart onderhouden moeten worden.
- **Elk getal moet uitlegbaar zijn.** Support en consultancy krijgen vragen als "wat zit er in deze KPI" en "hoe komt dit percentage tot stand". De keten van rubriek naar periode naar venster naar gemiddelde moet daarom navolgbaar zijn zonder in de code te kijken.
- **De klant richt de functiecategorieën in.** Zonder die koppeling zijn er geen vergelijkingscijfers. Profit vult die koppeling niet automatisch aan.
- **Het veld Fiscaal nummer op de organisatie bepaalt de breedte van de vergelijking.** Is het gevuld, dan vergelijken we over alle werkgevers met dat RSIN; is het leeg, dan vormt elke werkgever een eigen groep en vallen concerns uiteen in kleinere groepen (§5.2). We dwingen het vullen niet af, vullen het niet zelf aan en signaleren het ontbreken niet.
- **De gegevens zijn zo actueel als het laatste klaargezette aangiftetijdvak, en zo vers als de laatste geslaagde run.** Op de regel per inkomstenverhouding staan de einddatum en de datum van de laatste berekening, zodat dat bij de informatie kan worden vermeld.

---

## 11 Raakvlakken

| Onderwerp | Raakvlak |
| --- | --- |
| DP2 – Rapportage | Gebruikt dezelfde vier lagen met een rapportageperiode waarvan het rapportagejaar is gevuld. Fase 2 voegt alleen regels en velden toe; er komt geen nieuwe tabel bij, op het stamgegeven arbeidsjaareenheid na (§5.7). De sleutel van laag 0 en laag 2 wijzigt niet; laag 3 krijgt het kwartiel erbij zodra DP2 de kwartielverdeling uitwerkt. **DP2 moet dezelfde functietoekenning per aangiftetijdvak aanhouden** (§4.5), anders wijken de vergelijkingscijfers en de wettelijke rapportage van elkaar af en telt een medewerker die van functie wisselde in beide een andere categorie mee. DP2 hergebruikt ook de definities, de rubrieken en de rekenwijze uit hoofdstuk 6; die moeten identiek zijn, anders leggen de KPI en de wettelijke rapportage verschillende uitkomsten naast elkaar. De kwartielverdeling en de 5%-signalering worden in DP2 uitgewerkt. De medianen en de mediane loonverschilpercentages zitten al in het model, maar worden in fase 1 alleen **per functiecategorie** gevuld; het begrippenkader kent de mediaan uitsluitend organisatiebreed (§6.9). DP2 hoeft er dus geen velden voor toe te voegen, maar moet ze wél zelf vullen op de regels met een lege functiecategorie. **Geslacht X en niet ingevuld vragen in DP2 om extra aandacht:** deze arbeidsverhoudingen blijven buiten de berekening van het loonverschil (§3.8), maar tellen volgens de memorie van toelichting en de ministeriële regeling wél mee bij het aantal werknemers dat de rapportageplicht bepaalt, én in de noemer van het aandeel ontvangers van variabele componenten en van de kwartielverdeling. Teller en noemer lopen daar dus niet over dezelfde populatie. **De rapportage-eenheid wordt in DP2 op dezelfde manier bepaald** als hier (§5.2); in de praktijk zal dat altijd een RSIN zijn, want zonder RSIN is er geen rapportageplicht en een organisatie die er echt geen heeft is een eenmanszaak die de grens van honderd werknemers niet haalt. Waar wij het vullen van het veld Fiscaal nummer voor het recht op informatie niet afdwingen (§5.2), zal DP2 dat wél als voorwaarde moeten stellen: zonder dat nummer kan de rapportage niet worden aangeleverd. Hoe dat wordt afgedwongen — validatie, signaal of blokkade bij het vaststellen — hoort bij DP2. |
| DP3 – Uitzendkrachten | Uitzendkrachten vallen buiten de populatie van dit ontwerp. De gescheiden rapportage en de uitwisseling tussen in- en uitlener worden daar uitgewerkt. |
| DP4 – Vraag aan HR | Het profiel **Recht op informatie** van het type dossieritem Vraag aan HR is de route voor medewerkers die meer willen weten of meerdere arbeidsverhoudingen hebben. DP4 heeft daarvoor een gegevensverzameling gereserveerd; die vullen we vanuit de gegevensverzameling Loontransparantie per inkomstenverhouding (§5.9). |
| Power BI | De brontabel is opgezet als directe bron voor een dashboard. Daarvoor breiden we de bestaande gegevensverzameling Loonaangifte uren per medewerker uit met de zeven bedragen (§5.9); daarnaast leest het dashboard **Loontransparantie per inkomstenverhouding (alle functies)** en de verzameling op de tabel per functiecategorie. Het dashboard beantwoordt de vragen die de KPI's oproepen: waar zit het verschil, hangt het samen met dienstjaren, piekt het in bepaalde perioden, wat gebeurde er na een functiewijziging. Het dashboard leest en rekent niet opnieuw wat de taak al heeft berekend. |
| Document Loontransparantie medewerker | Het gegenereerde document toont alle arbeidsverhoudingen naast elkaar — elk op de **actuele functie**, net als de KPI —, waar de stamkaart alleen die van het hoofddienstverband toont (§8.5). Het leest de gegevensverzameling Loontransparantie per inkomstenverhouding (§5.9). De uitwerking volgt later. |
| Pocket en OutSite | De praatplaat voorziet in een route via Pocket voor medewerkers en via OutSite voor accountants en inleners. Beide gebruiken dezelfde gegevens. De uitwerking valt buiten deze beschrijving. |
| Jaarlijkse notificatie | De verplichting om medewerkers jaarlijks op hun recht te wijzen, automatiseren we niet in Profit. De klant vult dit zelf in, bijvoorbeeld met een bericht op het intranet. |

## 12 Openstaande keuzes

| Nr. | Onderwerp | Status |
| --- | --- | --- |
| D3b | Herleidbaarheid nu er geen ondergrens is (§9.3) | Besloten op 9 september 2026 · er komt geen ondergrens. Punt afgesloten. |
| E1 | Serialiseren van de verdichting per RSIN (§7.4) | Open · beperkt na blok M. Met één taak vanuit de dagovergang worden de rapportage-eenheden na elkaar verwerkt, dus twee werkgevers binnen één concern kunnen elkaars verdichting niet meer overschrijven. De resterende eis — nooit meer dan één run tegelijk per RSIN als een handmatige start samenvalt met de dagovergang — hoort bij het technisch ontwerp. |
| F1 | Vulmoment van de brontabel (§7.1) | Besloten op 8 september 2026 · het klaarzetten van de loonaangifte wordt de trigger, zie blok G. Blijft staan voor laag 1; voor de lagen erboven herzien in blok M |
| F2 | Arbeidscategorie versus functiecategorie (§5.7) | Besloten op 9 september 2026 · het is hetzelfde begrip. Profit hanteert de term functiecategorie; er komt geen apart veld en geen apart sleutelonderdeel. |
| G1 | Eerste vulling bij bestaande klanten (§7.7) | Herzien op 10 september 2026 · het aanvullen gebeurt niet bij het klaarzetten van een aangifte over 2026, maar eenmalig in de conversie naar Profit 9. Zie blok M, punt M6. |
| G2 | Bestaande ontsluiting van de brontabel (§9.2) | Open · bespreekpunt voor PM. De tabel is nu al benaderbaar via een view in de querywizard en via een InSite-datamodeldefinitie. Met de loonbedragen erbij moet die ontsluiting worden herzien vóór uitlevering. |
| H1 | Afwijkende term variabele componenten (§6.1) | Besloten op 9 september 2026 · we hanteren variabele componenten. Het begrippenkader spreekt van "aanvullende of variabele componenten"; die volledige term is als veldnaam en als kolomkop onwerkbaar. |
| H2 | Mediane loonkloofpercentages (§5.5, hoofdstuk 11) | Besloten op 9 september 2026 · de vier mediane percentages zijn alsnog in het model opgenomen en worden vanaf fase 1 gevuld, zie blok K. DP2 hoeft ze niet opnieuw te beleggen. · **aangescherpt op 10 september 2026, zie blok M punt M22: fase 1 vult ze alleen per functiecategorie, de organisatiebrede varianten die de rapportage vraagt komen in fase 2** |
| H3 | Toelichting bij geslacht X of niet ingevuld (§3.8, §8.7) | Open · we tonen deze medewerkers dezelfde tabel als iedereen, zonder aparte melding. De vraag is of er een korte uitleg bij hoort dat de vergelijking bewust met beide groepen wordt getoond, of dat tekst hier juist ongewenste aandacht op de registratie vestigt. Voorleggen aan PM en team Content. |
| L10 | Inkomstenverhoudingnummer op de brontabel (§5.3, §5.4) | Afgehandeld op 10 september 2026 · geverifieerd in de Profit-repository. De tabel heeft naast het volgnummer dienstverband ook het veld **Inkomstenverhoudingnummer**. Laag 2 kan daar dus rechtstreeks op groeperen; een join naar de dienstverbandgegevens is niet nodig. Zie blok M, punt M15. |
| L11 | Aanname over inkomstenverhouding en dienstverband (§2, §5.3) | Afgehandeld op 10 september 2026 · de aanname **klopt in één richting**: een nieuwe inkomstenverhouding levert altijd ook een nieuw (sub)dienstverband op, dus de sleutel van laag 1 blijft ongewijzigd. Wat niet klopt is de omkering: meerdere dienstverbanden kunnen onder hetzelfde inkomstenverhoudingnummer vallen, als subdienstverbanden onder één kapstok. Zie blok M, punten M7 en M16, en blok O, punt O3. |
| N1 | Triggerregel bij wijziging van de functiecategorie-inrichting (§7.2) | Besloten op 10 september 2026 · een wijziging in de functiecategorie-inrichting schrijft een triggerregel weg voor **alle** werkgevers, op het laatste klaargezette tijdvak per periodetabel. Die wijziging hangt niet aan een werkgever of een tijdvak, dus een kleinere afbakening is er niet. Punt afgesloten. |
| N2 | Prestatie van de dagelijkse run (§7.3, §7.4) | Besloten op 10 september 2026 · de run past binnen het tijdvenster van de dagovergang. Er komt geen begrenzing op het aantal rapportage-eenheden per run. Punt afgesloten. |
| N3 | Eerdere functieregels voor het dashboard (§5.9) | Besloten op 10 september 2026 · laag 2 krijgt **twee** gegevensverzamelingen. **Loontransparantie per inkomstenverhouding (actuele functie)** voor de KPI, het document en DP4, met een filter op rapportagejaar 0 én de actuele functie. **Loontransparantie per inkomstenverhouding (alle functies)** voor het dashboard, met alleen het filter op rapportagejaar 0. Ze verschillen uitsluitend in dat ene filter. Punt afgesloten. |
| L12 | Meertaligheid van de schermteksten (§8.7) | Open · de conceptteksten zijn alleen in het Nederlands opgesteld. Of het reguliere vertaalproces volstaat of er iets bijzonders speelt bij deze gevoelige teksten, hoort bij team Content. |
| L13 | Acceptatiecriteria | Open · dit document bevat geen toetsbare criteria waarmee is vast te stellen dat de bouw klaar is. Die horen in het FO zelf; te beleggen bij het opstellen daarvan. |
| J2 | Eenmanszaak met meerdere subheffingsnummers (§5.2) | Open · aanvaard gevolg van besluit J1. Zonder RSIN groeperen we op werkgever, dus staan meerdere subheffingsnummers van dezelfde eenmanszaak in aparte vergelijkingsgroepen als ze in Profit als aparte werkgevers zijn ingericht. Dichttimmeren zou een surrogaatsleutel per fiscaal nummer vragen; dat weegt niet op tegen de complexiteit voor deze zeldzame en per definitie kleine groep. |
| O1 | Landafhankelijkheid van de bron (§1.1, §1.4, §9.6) | Open · beperkt na blok O. Alle bedragen komen uit de rubrieken van de Nederlandse loonaangifte (blok I, punt I2), dus dit ontwerp werkt alleen voor Nederland. De **oplossingsrichting staat vast**: het tabblad wordt alleen getoond bij medewerkers met land van wetgeving `NL` en het datamodel blijft landonafhankelijk (§9.6, blok O punt O4). Wat openblijft is de vraag voor PM of België functioneel binnen de scope van dit deelproject valt, en zo ja welke bron daar in de plaats treedt van de loonaangifte. |

Alle punten die als PM1 tot en met PM8 bij PM voorlagen, zijn op 3 september 2026 besloten. De uitkomsten staan hieronder in blok E.

Afgehandeld in blok A:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| A2 | Populatiefilter op soort inkomstenverhouding (§3.2) | Voor eigen medewerkers 11, 13, 15 en 17 |
| A5 | Populatiefilter op aard arbeidsverhouding (§3.3) | Voor eigen medewerkers 1, 18, 21, 23, 24 en 83 |
| A6 | Aanvullende selectiecriteria (§3.4) | Loon groter dan nul en verloonde uren groter dan nul, getoetst over het venster |
| A3 | Medewerkers uit dienst binnen het venster (§3.6) | Meenemen zolang er loon in het venster valt |
| A4 | Medewerkers zonder functiecategorie (§3.7) | Wel in de tabel, zonder vergelijkingscijfers; de KPI's tonen niets en we signaleren het niet aan de klant |
| A7 | Medewerkers met geslacht X of zonder ingevuld geslacht (§3.8) | Wel in de tabel, tellen niet mee in de gemiddelden per geslacht; ze zien wel beide groepen. We faciliteren geen keuze om als man of vrouw te worden meegeteld |

Afgehandeld in blok B:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| B1 | Terugkijktermijn en eindpunt (§4.1, §4.2) | Voortschrijdend venster van twaalf maanden, eindigend bij het laatste klaargezette aangiftetijdvak · eindpunt herzien op 8 september 2026, zie blok G |
| B4 | Functie in de sleutel (§5.4) | Nee, functie is een kenmerk van de regel per inkomstenverhouding · **herzien op 10 september 2026, zie blok M** |
| B6 | Kenmerken vastleggen (§5.4) | Als momentopname op het einde van de rapportageperiode |
| B9 | Opschonen (§5.8) | Regels die niet meer aan de selectie voldoen worden verwijderd |

Herzien op 3 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| B2 | Venster bij weekverloning (§4.3) | Tweeënvijftig weken terugtellen, geen hergroepering | Weken groeperen naar dertien perioden van vier weken |
| B5 | Vastlegniveau (§5.1) | Alleen een standregel per dienstverband; geen periodegegevens | Brontabel per dienstverband per periode, met daarboven een standregel en een verdichte tabel |
| B7 | Bewaartermijn (§5.6) | Geen historie | Twaalf of dertien perioden in de brontabel; standregel en verdichte tabel zonder historie · opnieuw herzien op 8 september 2026, zie blok F |
| C4 | Grondslag loonkloofpercentage (§6.5) | Bruto uurloon in plaats van bruto jaarloon | Bruto jaarloon als wettelijke maat, bruto uurloon aanvullend ernaast |
| C3 | Kolom Individueel verschil (§6.4) | Afrekenen tegen het gemiddelde van het eigen geslacht | Kolom vervalt |
| C13 | Mediaan bij een even aantal (§6.4) | Gemiddelde van de twee middelste waarden | Vervalt; de mediaan verdwijnt uit de vergelijkingstabel en verhuist naar DP2 |

Afgehandeld in blok C:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| C1 | Opbouw van de begrippen uit de loonaangifte (§6.1, §6.2) | Vastgelegd conform het begrippenkader loontransparantie; het bruto jaarloon is het basisloon |
| C2 | Reikwijdte van de vergelijkingsgroep (§6.3) | Alle werkgevers met hetzelfde RSIN · **aangevuld op 9 september 2026 met de fallback voor werkgevers zonder RSIN, zie J1** |
| C5 | Onvolledige vensters (§6.8) | Iedereen meetellen, geen correctie; de loonkloof uurloon duidt het effect |
| C6 | Omvang van een run (§7.4) | Alleen de werkgever die zojuist de aangifte klaarzette, behalve de verdichting: die gaat over alle werkgevers met hetzelfde RSIN |
| C7 | Correcties (§7.5) | Correctie binnen het jaar start een eigen run; jaaroverschrijdende correctie loopt mee in de eerstvolgende reguliere run · **herzien op 10 september 2026, zie blok M** |
| C8 | Wettelijke reactietermijn (§7.7) | Twee maanden na de datum van het verzoek (artikel 10b, derde lid) |
| C9 | Signalering bij functies zonder categorie (§3.7) | Geen signalering; het gevolg is zichtbaar doordat de KPI's niets tonen |
| C12 | Afronding en negatieve bedragen (§6.1) | Intern onafgerond doorrekenen, tonen op twee decimalen; negatief bruto jaarloon wordt nul op de regel per inkomstenverhouding |
| C14 | Soort taak en moment (§7.1) | Wachtrijtaak vanuit het accorderen, met een afhankelijkheid van de accordeertaak · **herzien op 8 september 2026, zie blok G** |
| C15 | Deblokkeren van een geaccordeerde periode (§7.6) | Taak draait opnieuw; het venster schuift terug · **herzien op 8 september 2026, zie blok G** |

Afgehandeld in blok D:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| D1 | Periodeaanduiding in de KPI (§8.2) | Subtitel: Laatste 12 maanden |
| D2 | Meerdere arbeidsverhoudingen (§8.5) | Alleen de regel van het hoofddienstverband op de stamkaart, met verwijzing naar document of Vraag aan HR |
| D3 | Groepsgrootte (§9.3) | Geen ondergrens; we tonen altijd de gemiddelden, ook bij één persoon per geslacht |
| D4 | Zichtbaarheid (§9.1) | Medewerker, HR en manager; het tabblad is autoriseerbaar |
| D8 | Afscherming van de tabellen (§9.2) | Alleen via de meegeleverde weergaven en gegevensverzamelingen, met medewerkerautorisatie bij het lezen |
| D5 | Teksten (§8.7) | Conceptteksten opgenomen, gemarkeerd als voorstel voor team Content |
| D6 | Uitlevering (§9.5) | Generiek onder de HR-conditie, geen aparte activering |
| D7 | Weergave Functies in jouw functiecategorie (§8.4) | Uit de functiecategorie-inrichting, alleen de omschrijving, alfabetisch, alle functies zonder markering van de eigen functie |

Afgehandeld in blok E, de PM-terugkoppeling van 3 september 2026:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| E2 (PM1) | Grondslag van het loonkloofpercentage (§6.5) | Bruto jaarloon is de wettelijke maat, conform de nota van toelichting. Het bruto uurloon berekenen we ernaast omdat het corrigeert voor deeltijd. |
| E3 (PM2) | Apart percentage voor de variabele componenten (§6.5) | Ja, op jaarwaarde en op uurwaarde. Vier percentages in totaal. |
| E4 (PM3) | Mediaan in de vergelijkingstabel (§6.4) | Vervalt. Eén mediaan van de hele categorie past niet bij de rapportagedefinitie; twee kolommen wegen niet op tegen de extra breedte. De mediaan hoort bij DP2 en het dashboard. |
| E5 (PM4) | Waar we rekenen (§5.1) | Brontabel per dienstverband per periode, met een standregel en een verdichte tabel erboven. Verdichten mag geen informatie weggooien die het dashboard nodig heeft. |
| E6 (PM4) | Periode-eenheid en bewaartermijn (§4.3, §5.6) | Twaalf maanden of dertien perioden van vier weken · **bewaartermijn herzien op 8 september 2026, zie blok F** |
| E7 (PM5) | Ondergrens voor de vergelijkingscijfers (§9.3) | Geen ondergrens. De wetgever heeft de afweging tussen privacy en het recht op gelijk loon al gemaakt en laat het recht op gelijk loon voorgaan. |
| E8 (PM6) | Aansluiting op DP2 (§5.7) | DP2 krijgt een eigen structuur voor het afgesloten kalenderjaar · **herzien op 8 september 2026, zie blok F** |
| E9 (PM7) | Kolom Individueel verschil (§6.4) | Vervalt. Het juridische kader stuurt op het verschil binnen de categorie, niet op de afwijking van één individu. |
| E10 (PM8) | Rekeneenheid en rekenwijze (§6.3) | Rekenen per arbeidsverhouding · **verduidelijkt op 8 september 2026: dat is de inkomstenverhouding, zie blok G**. Het gemiddelde is het gemiddelde van de individuele waarden, conform het begrippenkader. |
| E11 | KPI's op de stamkaart (§8.2, §8.3) | Alle vier de percentages, in de volgorde jaarloon, componenten jaarwaarde, uurloon, componenten uurwaarde. Geen grafiek; de gemiddelden staan in de vergelijkingstabel. |
| E12 | Functie per periode (§4.5) | Blijft op ultimo venster, ook nu de brontabel per tijdvak vastlegt. Anders kan een arbeidsverhouding in twee functiecategorieën vallen. · **herzien op 10 september 2026, zie blok M** |

Herzien in blok F, de datamodelherziening van 8 september 2026:

Aanleiding was de vraag om het datamodel in één keer met de juiste gelaagdheid neer te zetten, zodat fase 1 alleen de velden voor het recht op informatie vult en fase 2 dezelfde tabellen uitbreidt voor de rapportage. De onderbouwing en de volledige veldindeling staan in hoofdstuk 5, met onderzoek ON-08 en ON-09 als basis. Het losse werkdocument waarin deze herziening is voorbereid is op 10 september opgeruimd; de inhoud staat nu volledig in dit document.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| F3 | Aantal lagen (§5.1) | Drie lagen: brontabel, standregel en verdichte tabel | Vier lagen; er komt een peilperiode boven, die de afbakening, de status en de definitieversie vastlegt |
| F4 | Sleutel van de standregel en de verdichte tabel (§5.4, §5.5) | Eén stand per dienstverband, respectievelijk per rapportagenummer en functiecategorie | De peilperiode zit in de sleutel, zodat een venster en een kalenderjaar naast elkaar bestaan |
| F5 | Aard arbeidsverhouding en soort inkomstenverhouding (§5.3) | Alleen op de standregel, als momentopname | Ook per periode in de brontabel; het zijn per tijdvak vastgelegde loonaangiftegegevens die binnen een jaar kunnen wijzigen |
| F6 | Loonkloofpercentages (§5.5, §6.5) | Niet vastleggen; de KPI rekent ze uit twee regels | Vastleggen op de totaalregel. De KPI leest en rekent niet, en een vastgestelde rapportage bevat het percentage dat destijds is verstrekt · de totaalregel is met I7 vervangen door de regel per functiecategorie |
| F7 | Mediaan (§5.5) | Valt buiten het model | Blijft buiten de stamkaart, maar het model heeft er velden voor · **herzien met K1: die worden vanaf fase 1 gevuld** |
| F8 | Bewaartermijn brontabel (§5.6) | Twaalf of dertien perioden | Het lopende en het voorgaande kalenderjaar, als parameter · **opnieuw herzien op 8 september 2026, zie blok G** |
| F9 | Historie (§5.6) | Geen historie, alles wordt overschreven | Vensterregels worden overschreven, kalenderjaarregels niet. Een vastgestelde rapportage mag niet stil wijzigen |
| F10 | Aansluiting op DP2 (§5.7) | DP2 heeft een eigen structuur nodig | DP2 gebruikt dezelfde tabellen met een andere peilperiode. Fase 2 voegt alleen regels en velden toe |
| F11 | Sleutel op inkomstenverhouding (§5.3) | Niet nader bepaald | Expliciet het nummer van de inkomstenverhouding uit de loonaangifte · **herzien op 8 september 2026, zie blok G** |
| F12 | Sleutelonderdelen populatie en kwartiel (§5.5) | Niet aanwezig | Vanaf fase 1 leeg meegedragen. Achteraf een sleutel uitbreiden is duurder dan hem nu meenemen |

Herzien in blok G, de keuze voor de bestaande brontabel op 8 september 2026:

Laag 1 wordt niet langer een eigen tabel, maar de bestaande tabel Loonaangifte uren per medewerker, uitgebreid met de loonbedragen. Dat raakt hoofdstuk 4, 5, 7 en 9.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| G3 | Brontabel (§5.3) | Een eigen tabel per werkgever, medewerker, inkomstenverhouding en periode | De bestaande tabel Loonaangifte uren per medewerker, met zeven rubrieken erbij |
| G4 | Sleutel van de brontabel (§5.3) | Expliciet op inkomstenverhouding; herziet F11 | Ongewijzigd op dienstverband. Een nieuwe inkomstenverhouding levert altijd ook een nieuw dienstverband op, dus het inkomstenverhoudingnummer is per regel eenduidig |
| G5 | Rekeneenheid (§3.1, §6.3) | Eén arbeidsverhouding is één dienstverband | Eén arbeidsverhouding is één inkomstenverhouding. Laag 2 groepeert de dienstverbanden daaronder |
| G6 | Berekende bedragen in laag 1 (§5.3) | Brutoloon en waarde AVC per periode vastleggen | Alleen de ruwe rubrieken. Het rekenwerk gebeurt in laag 2, zodat een definitiewijziging geen herschrijven van historie vraagt |
| G7 | Extra velden in laag 1 (§5.3) | Correctie-indicatie, berichtreferentie en vastlegtijdstip | Vervallen. Alleen de zeven bedragen worden toegevoegd |
| G8 | Trigger en eindpunt (§4.2, §7.1) | Accorderen van de salarisperiode; herziet C14 en F1 | Klaarzetten van de loonaangifte. Dat is het bestaande vulmoment van de brontabel |
| G9 | Deblokkeren (§7.6) | Deblokkeren van een geaccordeerde periode; herziet C15 | Intrekken van een loonaangifte. Het loonaangifteproces verwijdert de regels al · **herzien op 10 september 2026, zie blok M** |
| G10 | Bewaartermijn laag 1 (§5.6) | Lopend en voorgaand kalenderjaar; herziet F8 | Geen opschoning. De bestaande tabel kent er geen en die werking laten we ongemoeid |
| G11 | Eerste vulling (§7.7) | De eerste run vult meteen het hele venster | Herzien op 9 september 2026: het klaarzetten van een aangifte over 2026 vult de ontbrekende rubrieken van dat jaar alsnog aan. Zie blok I · **opnieuw herzien op 10 september 2026, zie blok M** |

Herzien in blok H, de naamgevingsronde van 8 september 2026:

Alle velden, sleutelonderdelen en tabellen zijn een voor een op naamgeving nagelopen. Naast het hernoemen zijn velden geschrapt die live te joinen of af te leiden zijn, en velden die bij de wettelijke rapportage horen. Het leidende principe: wat live te joinen of af te leiden is, slaan we niet op.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| H3 | Term voor de afbakening (hele document) | Peilperiode | Rapportageperiode. "Peil" suggereert een moment, terwijl het een bereik is |
| H4 | Nummer waarop wordt vergeleken (hele document) | Rapportagenummer, RSIN of beide door elkaar | Overal RSIN |
| H5 | Term voor het loon bovenop het basisloon (hele document) | Aanvullende of variabele componenten | Variabele componenten · zie openstaand punt H1 |
| H6 | Naam van laag 2 (§5.4) | Standregel Recht op informatie | Loontransparantie per inkomstenverhouding, kort: de regel per inkomstenverhouding |
| H7 | Naam van laag 3 (§5.5) | Verdichte tabel Vergelijkingscijfers | Loontransparantie per functiecategorie, kort: de tabel per functiecategorie |
| H8 | Namen van de vier loonkloofpercentages (§5.5, §6.5, §8.2) | Drie verschillende namensets naast elkaar in het datamodel, de berekening en de KPI | Eén set: Loonkloof jaarloon, Loonkloof uurloon, Loonkloof componenten jaarwaarde, Loonkloof componenten uurwaarde · **herzien op 10 september 2026, zie blok P: loonkloof is loonverschil geworden** |
| H9 | Definitieversie op laag 0 (§5.2); herziet F3 | Vastleggen welke versie van de begrippen is gebruikt | Vervalt |
| H10 | Vaststelling op laag 0 (§5.2) | Eigen velden voor vastgesteld op en door, indieningsdatum en aanleiding | Vervallen; de standaard loggingvelden volstaan |
| H11 | Hoofddienstverband en datum in en uit dienst op laag 2 (§5.4, §8.5) | Als momentopname vastgelegd | Vervallen; live joinen. Opslaan zou betekenen dat ze bij elke wijziging moeten worden bijgewerkt |
| H12 | Tellingen op laag 2 (§5.4) | Aantal dienstverbanden, aantal perioden en aantal perioden met loon | Vervallen; af te leiden uit de periodetabel en de brontabel |
| H13 | Fase 2-velden op laag 2 en 3 (§5.4, §5.5); herziet F12 | Kwartielen, arbeidsjaarfractie, componenten ontvangen, kwartielgrenzen, onderbouwing, status beoordeling en drempel overschreden | Vervallen uit dit ontwerp; DP2 werkt ze uit, inclusief het kwartiel als sleutelonderdeel op laag 3 |
| H14 | Mediane loonkloofpercentages (§5.5); herziet F7 | Velden op de totaalregel | Vervallen; de medianen voor mannen en vrouwen blijven staan, DP2 berekent de percentages daaruit · **herzien met K1: de vier mediane percentages zijn alsnog opgenomen** |
| H15 | Term voor de eigen medewerker (hoofdstuk 3, §5.4, §5.5) | Werknemer | Medewerker. Uitzondering: wettelijke termen zoals werknemersverzekeringen en letterlijke citaten uit het wetsvoorstel |

Besloten in blok I, op 9 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| I1 | Terugwerkend vullen van de rubrieken (§7.7); herziet G11 | Het venster loopt in ongeveer een jaar vol | Bij het klaarzetten van een aangifte over 2026 worden ontbrekende rubrieken van dat jaar alsnog gevuld uit de nominatieve loonaangiftegegevens. Alleen voor 2026 · **herzien op 10 september 2026, zie blok M** |
| I2 | Bron van de bedragen (§1.1, §4.4, §6.2, hoofdstuk 10) | Loonaangifte én lijstbegrippen | Uitsluitend de loonaangifterubrieken uit de brontabel. Daarmee vervalt het jaargrensprobleem en de randvoorwaarde dat de klant zijn lijstbegrippen consistent inricht |
| I3 | Vullen van de zeven rubrieken (§1.4) | Niet expliciet belegd | Onderdeel van dit project; geen afhankelijkheid van een ander team |
| I4 | RSIN op laag 3 (§5.5) | Alleen indirect, via de rapportageperiode | Expliciet in de sleutel. Werkgever komt er niet op: één regel gaat over alle werkgevers met dat RSIN · **herzien met J1: het sleutelonderdeel is de rapportage-eenheid** |
| I5 | Gedrag bij een mislukte run (§7.8) | Bestaande gegevens blijven staan, zonder verdere uitwerking | Uitgewerkt: één transactie per rapportage-eenheid, laag 2 vóór laag 3 vóór de rapportageperiode, de datum van de laatste berekening als laatste schrijfactie, en idempotent opnieuw te draaien |
| I6 | Arbeidscategorie (§5.7); sluit F2 | Mogelijk een apart begrip naast de functiecategorie | Hetzelfde begrip. Profit hanteert functiecategorie |
| I7 | Vorm van laag 3 (§5.5); herziet I4 gedeeltelijk | Geslacht in de sleutel: drie regels per functiecategorie, met de gemiddelden op de geslachtsregels en de loonkloofpercentages op een totaalregel | Geslacht uit de sleutel: één regel per functiecategorie, met elk veld per geslacht. Heft het onderscheid tussen twee soorten regels met verschillende velden op · **aangescherpt met J6: alleen mannen en vrouwen, geen totaalvariant** |

Herzien in blok J, de rapportage-eenheid, op 9 september 2026:

Aanleiding was de vraag wat er gebeurt als een werkgever geen RSIN heeft. Voor de rapportage speelt dat niet: elke rechtspersoon krijgt bij inschrijving een RSIN en organisaties zonder RSIN — eenmanszaken — halen de grens van honderd werknemers niet. Het recht op informatie kent die grens echter niet en moet voor elke werkgever werken, op hetzelfde model en dezelfde bronnen.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| J1 | Groeperingssleutel van laag 0 en laag 3 (§5.2, §5.5, §6.3); herziet C2 en I4 | Het RSIN als enige sleutel | De rapportage-eenheid als sleutel, bestaande uit soort plus waarde. Is het veld Fiscaal nummer op de organisatie gevuld, dan is dat RSIN de eenheid; is het leeg, dan vormt de werkgever zijn eigen eenheid. Zo belanden werkgevers zonder ingevuld Fiscaal nummer nooit in één gemiddelde |
| J3 | Herkomst van het nummer (§5.2, §5.3) | Herleiden uit werkgever en loonheffingsnummer | Lezen uit het veld **Fiscaal nummer** op de organisatie. Niet afleiden uit het loonheffingsnummer: bij een eenmanszaak zijn de eerste negen posities het BSN van de ondernemer, en een BSN is niet van een RSIN te onderscheiden. Dat zou ongemerkt BSN's opslaan in een veld dat RSIN heet, in tabellen die via weergaven, gegevensverzamelingen en Power BI zijn ontsloten |
| J5 | Verplichten van het Fiscaal nummer (§5.2, hoofdstuk 10) | Niet belegd | We dwingen het niet af. Geen validatie, geen conversie en geen signaal. Heeft een organisatie in werkelijkheid wel een RSIN maar staat het veld leeg, dan blijft het RSIN leeg en groeperen we op de werkgever, net als bij een eenmanszaak. De klant kan het alsnog vullen; dat werkt door bij de volgende run. Voor DP2 is het vullen wél een voorwaarde, maar dat hoort daar |
| J4 | Subheffingsnummers (§5.2) | Niet belegd | Vallen vanzelf samen, omdat we op het RSIN van de werkgever groeperen en niet op het loonheffingsnummer. Dat volgt het begrippenkader, dat samenvoegen met het hoofdheffingsnummer voorschrijft |
| J6 | Totaalvariant op laag 3 (§5.5); scherpt I7 aan | Elk veld drie keer: mannen, vrouwen en totaal | Alleen mannen en vrouwen. Van de gemiddelden en de medianen komt er geen totaalvariant, omdat die nergens wordt gebruikt: de vergelijkingstabel, de KPI's en de wettelijke rapportage zetten steeds mannen tegen vrouwen af. Alleen **Aantal arbeidsverhoudingen totaal** blijft, als omvang van de categorie en als noemer voor DP2 · de veldentelling is met K1 gewijzigd |
| J7 | Ontsluiting van de tabellen (§5.9) | Alleen op hoofdlijn benoemd in §9.2 | Twee nieuwe gegevensverzamelingen, één per nieuwe tabel, met een standaardfilter op rapportagejaar 0. Voor de brontabel komt er geen nieuwe verzameling: de bestaande verzameling Loonaangifte uren per medewerker wordt uitgebreid met de zeven bedragen. Medewerkerautorisatie op laag 1 en 2; laag 3 heeft geen medewerker op de regel en wordt afgeschermd via de autorisatie op de verzameling zelf. Er komt geen variant zonder autorisatie voor het dashboard · **herzien op 10 september 2026: laag 2 krijgt twee verzamelingen, zie blok M punt M21** |
| J8 | Soort rapportageperiode (§5.2); herziet F3 | Apart sleutelonderdeel naast het rapportagejaar | Vervalt. Het rapportagejaar bepaalt de soort: 0 is het voortschrijdende venster, een jaartal is een afgesloten kalenderjaar. Soort en jaar zaten één op één aan elkaar vast, dus het soort was afleidbaar — en een ongeldige combinatie is nu onmogelijk. Venster en kalenderjaar blijven als leesbegrip bestaan |
| J9 | Rapportage-eenheid in fase 2 (§5.2, §5.5); scherpt J1 aan | In fase 2 altijd een RSIN | De bepaling is in beide fasen gelijk: is het veld Fiscaal nummer gevuld, dan het RSIN uit dat veld, en is het leeg, dan de werkgeverscode. Dat een rapportageplichtige werkgever in de praktijk altijd een RSIN heeft, verandert de definitie niet |

Besloten in blok K, de controle op de berekende velden, op 9 september 2026:

Aanleiding was een controle of voor elk berekend veld in het datamodel ook de berekening is beschreven, en of die klopt met het begrippenkader v0.86E. De vijf waarden per arbeidsverhouding, de tien gemiddelden en de vier loonkloofpercentages bleken correct en volledig gedekt. De punten hieronder waren dat niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| K1 | Medianen en mediane loonkloofpercentages (§5.5, §6.6); herziet F7 en H14 | Acht medianen als fase 2-veld, zonder beschreven berekening; de vier mediane percentages belegd bij DP2 | Alle twaalf velden in het model en vanaf **fase 1** gevuld. Het recht op informatie toont ze niet, maar ze zijn niet uit een gemiddelde te reconstrueren en het dashboard heeft ze meteen nodig. Daarmee is het setje compleet: acht genderloonkloven, vier op gemiddelden en vier op medianen · **aangescherpt met M22: het begrippenkader kent de mediaan alleen organisatiebreed, dus de mediaan per functiecategorie is een eigen uitbreiding** |
| K2 | Rekenwijze van de mediaan (§6.6) | Nergens beschreven | Uitgeschreven conform het begrippenkader: sorteren van laag naar hoog, de middelste bij een oneven aantal, het gemiddelde van de twee middelste bij een even aantal. Waarden hoeven niet uniek te zijn en we sorteren per arbeidsverhouding, niet per persoon |
| K3 | Rekenwijze van de tellingen (§6.7) | Alleen als veldtoelichting, zonder telregel | Eigen paragraaf. Het aantal is tegelijk de noemer van de gemiddelden. Het totaal op laag 3 bevat ook geslacht X en niet ingevuld, dus is groter dan of gelijk aan de som van mannen en vrouwen. Het totaal op laag 0 bevat daarnaast de arbeidsverhoudingen zonder functiecategorie en is dus groter dan of gelijk aan de som van de laag 3-totalen |
| K4 | Aantal medewerkers in fte (§6.7) | Formule alleen in de veldtoelichting | Opgenomen in hoofdstuk 6. Klopt met het begrippenkader, dat het begrip *aantal werknemers* noemt; wij houden de Profit-term aan omdat het een fte-getal is en geen telling van personen |
| K5 | Eenheid van de percentages (§6.5, §6.6) | Niet vastgelegd | Opslaan als getal met twee decimalen: 5,23 voor 5,23%. Het begrippenkader rekent de formule ook maal honderd procent |
| K6 | Ondergrens op de variabele componenten (§6.1) | Beschreven als conform het begrippenkader | Bewuste **afwijking**, nu als zodanig benoemd. Het kader kapt af per tijdvak (§3.6.4); wij kappen af op het venstertotaal. Reden: een correctie moet een eerder tijdvak kunnen terugdraaien, en de ondergrens hoort op het getal dat we tonen. DP2 volgt dezelfde keuze |
| K7 | Rubrieknummers van LnLbPh en LnTabBB (§6.2) | Beide 1287 + 1670, zonder uitleg — las als een fout | Toegelicht: LnTabBB is geen apart bedrag maar een deelverzameling van dezelfde rubrieken, afgebakend door een extra filter op bijzonder tarief. De brontabel legt het normale en het bijzondere deel apart vast, zodat niets dubbel wordt opgeslagen |
| K8 | Kolomvolgorde in de vergelijkingstabel (§8.3, §6.4) | Jij, Vrouwen, Mannen | Jij, **Mannen**, Vrouwen. De mannen zijn de referentiegroep en staan in alle acht loonkloofpercentages in de noemer; de tabel leest daarmee in dezelfde volgorde als de formule. Het datamodel hanteerde die volgorde al. De twee schermteksten die met "Vrouwen verdienen gemiddeld minder" beginnen blijven ongewijzigd: die gaan over de richting van de uitkomst, niet over een opsomming |

Besloten in blok L, de scherpstelronde, op 9 september 2026:

Aanleiding was een doorlichting op onduidelijkheden, aannames en gaten. Vier bevindingen zijn geverifieerd in de Profit-repository; de rest volgde uit interne tegenstrijdigheden.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| L1 | Periodetabellen (§4.3, §5.4) | Maand, vier weken, dertien perioden of week | Profit kent er acht; dertien perioden is er géén van, maar het aantal tijdvakken dat de vierwekentabel oplevert. We ondersteunen **maand, vier weken en week**. Jaar, halfjaar, kwartaal, twee weken en halve maand vallen buiten scope: elke variant vraagt een eigen omrekenregel terwijl ze zeldzaam zijn |
| L2 | De 53e week (§4.3) | Genegeerd; altijd dertien tijdvakken | Profit kent een restperiode met het veld Week53Processing. Valt die binnen het venster, dan telt hij mee als veertiende tijdvak. Anders mist een weekverloner in zo'n jaar één week loon in de wettelijke grondslag |
| L3 | Meerdere periodetabellen bij één werkgever (§4.3, §5.2) | Aangenomen dat het eindpunt per werkgever geldt | Komt voor: maandbetaalden naast weekbetaalden. Het eindpunt wordt per werkgever **en periodetabel** bepaald. De begin- en einddatum op laag 0 zijn daarom indicatief; de exacte grenzen staan per arbeidsverhouding |
| L4 | Peilmoment van het populatiefilter (§3.5) | Niet belegd; §5.3 en §5.4 noemden verschillende peilmomenten | Soort inkomstenverhouding en aard arbeidsverhouding toetsen we **per tijdvak**; alleen kwalificerende tijdvakken tellen mee. Loon en uren toetsen we over het venster als geheel. De ultimo-waarde op de regel is een kenmerk, niet de filterwaarde |
| L5 | Nul verloonde uren (§6.1, §8.6, §8.7) | Zowel selectiecriterium als schermmelding | De melding vervalt. Uren groter dan nul blijft selectiecriterium, dus het geval kan zich op de regel niet voordoen. Per tijdvak mag het aantal wel nul zijn |
| L6 | Lege geslachtsgroep (§6.5, §8.6) | Alleen het geval zonder mannen was belegd | Symmetrisch: ontbreekt een van beide groepen, dan blijven alle acht percentages leeg en tonen we de gevulde kolom wél. Nooit 100%, want dat leest als een maximale loonkloof terwijl er niets te vergelijken valt |
| L7 | Buiten de populatie vallen (§8.6, §8.7) | Geen schermsituatie | Eigen situatie met een neutrale melding, die ook de niet-ondersteunde periodetabellen en het ontbreken van loon of uren afdekt. De onderliggende reden noemen we niet: die zegt de medewerker niets en is voor hem niet op te lossen |
| L8 | Precisie van de bedragen (§6.1) | Intern onafgerond, afronden bij tonen | Afronden op **twee decimalen bij het wegschrijven**, in elke laag. Wat we opslaan is wat we tonen. Een gemiddelde wordt dus uit afgeronde bedragen berekend; dat kost de laatste decimaal maar maakt elk getoond getal narekenbaar |
| L9 | Hoofdstukkop en telwoord (§1.5, hoofdstuk 4) | Hoofdstuk 4 had geen kop; §1.5 kondigde vier uitgangspunten aan bij zes | Kop "Periode en venster" toegevoegd; telwoord gecorrigeerd |

Herzien in blok M, de feedback van de programmeur, op 10 september 2026:

Aanleiding was een technische toets op het vulproces en op de sleutelkeuzes van laag 1 en 2. Vier bevindingen zijn geverifieerd in de Profit-repository. Het raakt hoofdstuk 3, 4, 5, 6, 7, 8 en 10.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| M1 | Trigger voor de lagen 2 en 3 (§7.1); herziet G8 gedeeltelijk | Een wachtrijtaak per klaargezette loonaangifte, afhankelijk van het klaarzetten | De wachtrijtaak **Bijwerken gegevens loontransparantie**, gestart vanuit de dagovergang Vernieuwen actuele gegevens. Los uit te voeren en dus herstartbaar, en hij vangt ook functiewijzigingen op die niet via de loonaangifte binnenkomen |
| M2 | Vulmoment van laag 1 (§5.3, §7.1) | Impliciet onderdeel van dezelfde keten | Blijft **direct** bij het klaarzetten van de loonaangifte. Alleen de lagen erboven verhuizen naar de dagovergang |
| M3 | Triggertabel (§7.2) | Niet aanwezig | Nieuwe technische tabel met werkgever, periodetabel, jaar en periode. Houdt bij wat is geraakt, wordt opgeruimd na verwerking en maakt een mislukte run herstelbaar zonder handwerk |
| M4 | Venstertoets bij het uitvoeren (§7.3) | Elke gebeurtenis leidde tot een volledige run | De taak toetst per triggerregel of het tijdvak binnen het venster valt. Wijzigingen daarbuiten leiden niet tot bijwerken en worden alleen opgeruimd |
| M5 | Naam van de taak (§7.1) | Alleen "de wachtrijtaak" | **Bijwerken gegevens loontransparantie**, volgens het bestaande patroon werkwoord + object (Klaarzetten loonaangifte, Bijwerken werkbegroting, Herberekenen verlof) |
| M6 | Eerste vulling van de zeven velden (§7.7); herziet G11 en I1 | Bij het klaarzetten van een aangifte over 2026 de eerdere tijdvakken van dat jaar aanvullen | Eenmalig in de **conversie naar Profit 9**, over 2026, op basis van de aanwezige loonaangiftegegevens. Scheelt een controle bij elke aangifte over 2026 en zet de gegevens in één keer voor alle werkgevers klaar |
| M7 | Meerdere dienstverbanden per inkomstenverhouding (§3.1, §5.3, §5.4, §6.1) | Alleen benoemd als mogelijkheid | Uitgewerkt: het gaat om subdienstverbanden onder één kapstokdienstverband, vooral in het onderwijs. De loonaangifte staat op de kapstok, inclusief de loongegevens van de subdienstverbanden. Laag 2 neemt de kenmerken en de functie van de kapstok en telt de loongegevens van alle dienstverbanden binnen de inkomstenverhouding op |
| M8 | Functie in laag 2 (§4.5, §5.4, §6.3); herziet B4 en E12 | Functie ultimo venster, niet in de sleutel; één regel per inkomstenverhouding | Functie **per aangiftetijdvak**, bepaald op de laatste dag van dat tijdvak, en wél in de sleutel. Wisselt een arbeidsverhouding van functie, dan komt er per functie een regel met alleen de toegekende tijdvakken. Het loon telt niet dubbel maar wordt verdeeld: elk tijdvak zit in precies één regel |
| M9 | Meetellen van functieregels (§6.3, §6.7) | Niet van toepassing | Elke functieregel telt als volwaardige arbeidsverhouding in zijn eigen functiecategorie. Het aantal arbeidsverhoudingen is daarmee een telling van regels en niet van personen. Het gevolg — een lager bruto jaarloon in beide categorieën — accepteren we, net als bij medewerkers die niet het hele venster in dienst waren (§6.8) |
| M10 | Regel op de stamkaart (§8.5) | Alleen de regel van het hoofddienstverband | De inkomstenverhouding van het hoofddienstverband, en daarbinnen de regel van de functie op de laatste dag van het venster · **aangescherpt met M19** |
| M11 | Aantal toegekende tijdvakken (§5.4); herziet H12 gedeeltelijk | Tellingen op laag 2 geschrapt omdat ze afleidbaar waren | Het aantal toegekende tijdvakken komt terug als veld. Welke tijdvakken aan welke functie zijn toegekend is niet uit de brontabel te lezen, want de functie staat daar niet in |
| M12 | Correcties (§7.5); herziet C7 | Correctie binnen het jaar startte een eigen run, een jaaroverschrijdende correctie liep mee met het eerstvolgende reguliere tijdvak | Beide leveren een triggerregel op en lopen mee in de eerstvolgende dagovergang. Er is geen apart geval meer |
| M13 | Intrekken van een loonaangifte (§7.6); herziet G9 | Maakt een wachtrijtaak aan | Schrijft een triggerregel weg; de taak schuift het venster bij de eerstvolgende run terug |
| M14 | Serialiseren per RSIN (§7.4); beperkt E1 | Noodzakelijk omdat elke klaargezette aangifte een eigen taak startte | Grotendeels opgelost: één taak per dagovergang verwerkt de rapportage-eenheden na elkaar. De eis blijft alleen staan voor het geval een handmatige start samenvalt met de dagovergang |
| M15 | Inkomstenverhoudingnummer op de brontabel (§5.3); sluit L10 | Onbevestigd | Bevestigd in de repository: de tabel heeft naast het volgnummer dienstverband ook het veld Inkomstenverhoudingnummer. Laag 2 kan daar rechtstreeks op groeperen |
| M16 | Aanname over inkomstenverhouding en dienstverband (§2, §5.3); sluit L11 | Een nieuwe inkomstenverhouding levert altijd ook een nieuw dienstverband op | Blijft staan, mits als **(sub)dienstverband** gelezen · **aangescherpt op 10 september 2026, zie blok O, punt O3**. De omkering geldt niet: meerdere dienstverbanden kunnen onder één inkomstenverhoudingnummer vallen, zie M7. De sleutel van laag 1 blijft ongewijzigd, omdat er per dienstverband en tijdvak precies één regel is |

| M17 | Reikwijdte van de triggers (§7.2); scherpt M3 aan | Ook contractwijzigingen: nieuw, eigenschappen wijzigen, verwijderen, contractverlenging en indienstmelding | Alleen **functiewijzigingen**. Een contractwijziging is niet per se een functiewijziging, en raakt hij de loongegevens, dan leidt hij zelf al tot een correctie op de loonaangifte — die schrijft de triggerregel dan weg. De perioden leiden we af uit de begin- en einddatum van de functie; de taak bepaalt daarna welke daarvan binnen het venster vallen |
| M18 | Vastlegniveau van de triggertabel (§7.2) | Niet onderbouwd | Per **periode**, niet alleen per werkgever. Vanuit de loonaangifte is de periode voorhanden; bij een functiewijziging moet hij worden opgezocht, wat goed te doen is omdat de periodetabel bekend is. Zonder periode vervalt de venstertoets en rekent elke wijziging de werkgever volledig door. De technische invulling bepaalt de programmeur bij de realisatie |
| M19 | Welke functieregel wordt getoond (§5.9, §8.5); scherpt M10 aan | De functie op de laatste dag van het venster | De **actuele** functie op het moment van opvragen. Het venster eindigt bij het laatste klaargezette tijdvak en loopt dus achter op vandaag. De gegevensverzameling op laag 2 filtert erop, zodat de KPI, het document en de route van DP4 hetzelfde tonen |
| M20 | Nog geen gegevens over de nieuwe functie (§8.5, §8.6) | Niet belegd | Is er nog geen loonaangifte klaargezet waarin de nieuwe functie valt, dan blijft de kolom Jij leeg. De vier KPI-tegels en de kolommen Mannen en Vrouwen tonen wél de cijfers van de nieuwe functiecategorie: die komen uit laag 3, hebben de eigen regel niet nodig, en de categorie is af te leiden uit de actuele functie |
| M21 | Aantal gegevensverzamelingen op laag 2 (§5.9); herziet J7 | Één verzameling per nieuwe tabel | **Twee** verzamelingen op laag 2: *(actuele functie)* voor de KPI, het document en DP4, en *(alle functies)* voor het dashboard. Ze verschillen alleen in het filter op de functie; basistabel, velden en medewerkerautorisatie zijn identiek, dus er is geen tweede definitie te onderhouden |
| M22 | Niveau van de mediaan (§5.5, §6.6, §6.9); scherpt K1 aan | De acht percentages per functiecategorie waren gemapt aan A11, A21, B11, B21 en C11, C21, D11, D21 | Gecorrigeerd. Het begrippenkader kent die acht **organisatiebreed**; binnen een arbeidscategorie kent het er vier, alle op gemiddelden: G.M11, G.M21, G.M31 en G.M41. Onze tabel per functiecategorie hoort dus bij de G-reeks. De vier **mediane** percentages per functiecategorie zijn daarmee een eigen uitbreiding zonder nummer. Ze blijven staan: ze komen nooit in de wettelijke rapportage, maar maken een scheve loonverdeling binnen een categorie zichtbaar en zijn niet achteraf uit een gemiddelde te reconstrueren. De organisatiebrede A-, B-, C- en D-reeks komt in fase 2 op dezelfde velden, op regels met een lege functiecategorie |

Besloten in blok O, de terminologie- en landronde, op 10 september 2026:

Aanleiding was de constatering dat de bronterm *arbeidsverhouding* in Profit naar een ander gegeven wijst dan bedoeld, en de vraag of het ontwerp buiten Nederland bruikbaar is.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| O2 | Term voor het populatiekenmerk (§2, §3.2) | De bronterm *soort arbeidsverhouding* werd naast de Profit-term gebruikt | Alleen **soort inkomstenverhouding**. Hoofdstuk 2 legt vast dat de bronterm *arbeidsverhouding* de inkomstenverhouding is en dat *aard arbeidsverhouding* een ander gegeven is. De bronterm overnemen zou in Profit naar het verkeerde veld wijzen |
| O3 | Aanname over inkomstenverhouding en dienstverband (§5.3); scherpt M16 aan | Onjuist als algemene regel | **Klopt in één richting**: een nieuwe inkomstenverhouding levert altijd ook een nieuw (sub)dienstverband op, dus de sleutel van laag 1 blijft ongewijzigd. Alleen de omkering geldt niet — meerdere dienstverbanden kunnen onder één inkomstenverhoudingnummer vallen |
| O4 | Landafhankelijkheid (§1.4, §9.6); beperkt O1 | Niet belegd; het ontwerp ging impliciet uit van Nederland | Het tabblad Loontransparantie wordt alleen getoond bij **land van wetgeving `NL` van de medewerker** (`AfasKnCountryByLaw`, leeg = NL). Het **datamodel blijft landonafhankelijk**: de brontabel wordt alleen door de Nederlandse loonaangifte gevuld, dus de gegevens filteren zichzelf al en de taak heeft geen landfilter nodig. Het veld `CoLa` op de administratie is bewust **niet** gebruikt: dat geldt voor de hele administratie en is te grof · voorlopig, in afwachting van de PM-keuze over België |

Besloten in blok P, de terminologiewijziging loonverschil, op 10 september 2026:

Aanleiding was de constatering dat de ministeriële regeling van 10 juli 2026 — de nieuwste en meest concrete bron, die ook de rapportageformats voorschrijft — consequent spreekt van **loonverschillen man/vrouw**, waar het begrippenkader v0.86E *genderloonkloof* hanteert.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| P1 | Term voor het percentage (hele document); herziet H8 | Loonkloof | **Loonverschil**, conform de ministeriële regeling. Het wetsvoorstel definieert in artikel 1 nog wél *loonkloof*; hoofdstuk 2 vermeldt beide, zodat de aansluiting op de wettekst zichtbaar blijft |
| P2 | Namen van de acht velden (§5.5, §6.5, §6.6, §6.9, §8.2) | Loonkloof jaarloon, Loonkloof uurloon, Loonkloof componenten jaarwaarde, Loonkloof componenten uurwaarde, plus de vier mediane varianten | Loonverschil jaarloon, Loonverschil uurloon, Loonverschil componenten jaarwaarde, Loonverschil componenten uurwaarde, plus Mediane loonverschil jaarloon, uurloon, componenten jaarwaarde en componenten uurwaarde |
| P3 | Samenstellingen in de lopende tekst en de schermteksten | loonkloofpercentage, loonkloofcijfers, wettelijke loonkloofrapportage, genderloonkloven | loonverschilpercentage, loonverschilcijfers, wettelijke rapportage over loonverschillen, genderloonverschillen. De meldingen in §8.7 spreken van "geen loonverschil berekenen" |
| P4 | Citaten en formulenummers (§6.9) | Niet belegd | Blijven ongewijzigd. Het begrippenkader v0.86E noemt zijn formules GENDERLOONKLOOF; de codes G.M11 tot en met D21 en de verwijzingen daarnaar veranderen niet |
| P5 | Besluitenlog (hoofdstuk 12) | Niet belegd | De blokken A tot en met O blijven met de oude term staan. Een log legt vast wat er destijds is besloten; dat is dezelfde lijn als bij *peilperiode*, dat in blok F blijft staan en met blok H punt H3 is hernoemd |
