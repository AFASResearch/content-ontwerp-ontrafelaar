# DP1 – Recht op informatie · Functionele beschrijving

> Functionele uitwerking van de brainstorm van 1 september 2026, aangevuld met de uitkomsten van de PM-terugkoppeling van 3 september 2026. Dit document voedt het latere FO `01_FO_Recht_op_informatie.md`.
>
> Onderdeel van het [Programma Loontransparantie](../00_Programma_Loontransparantie.md). Scope en afbakening van het deelproject staan in [00_Scope.md](00_Scope.md). Laatste bijwerking: 2026-10-19.
>
> Alle keuzes uit de brainstorm en de PM-terugkoppeling zijn besloten. Hoofdstuk 12 bevat de besluiten, de herzieningen en de punten die nog buiten dit document worden afgehandeld.
>
> **Het overleg met PM van 15 september 2026 raakt dit document ingrijpend.** Laag 1 is niet langer de bestaande tabel Loonaangifte uren per medewerker, maar bestaat uit drie eigen brontabellen die via lijstbegrippen worden gevuld uit de **geaccordeerde salarisverwerking** in plaats van uit de klaargezette loonaangifte. Dat raakt hoofdstuk 1, 2, 4, 5, 6, 7, 9, 10 en 11. Zie blok R in hoofdstuk 12.
>
> Uit datzelfde overleg volgt dat het **bruto jaarloon niet de wettelijk voorgeschreven maat** blijkt te zijn. Daarom krijgt het bruto uurloon de voorkeur en tonen we nog twee KPI-tegels in plaats van vier. Verder is de scope afgebakend op Nederland, komt de sectie op drie standaard stamkaarten en vervalt de conversie. Zie blok S.
>
> **De sectie krijgt op 17 september 2026 vier KPI-tegels.** Naast de twee loonverschilpercentages op uurbasis komen er twee grafieken bij: **Gemiddeld bruto jaarloon** als horizontale staaf met Jij, Mannen en Vrouwen, en **Aantal inkomstenverhoudingen** als taartdiagram met het aantal mannen en vrouwen. De titels van de eerste twee tegels verliezen de toevoeging *functiecategorie*. Dat raakt hoofdstuk 8 en §9.4, want we tonen daarmee wél aantallen per geslacht. Zie blok V.
>
> **De brongegevens staan per loontijdvak en niet per aangiftetijdvak.** Dat volgt op 17 september 2026 uit blok R: de brontabellen worden uit de geaccordeerde salarisverwerking gevuld, dus het tijdvak volgt de salarisverwerking. Daardoor ondersteunen we **alle acht periodetabellen** in plaats van drie, en moet de taak het venster van een jaar per periodetabel bepalen — 12 tijdvakken bij maand, 13 bij vier weken, 52 of 53 bij week. Verder zijn de lijstbegrippen gesplitst: bestaande voor medewerkers, nieuw te maken voor uitzendkrachten. Dat raakt hoofdstuk 1 tot en met 7 en hoofdstuk 10. Zie blok W.
>
> **De brontabellen worden niet via gegevensverzamelingen ontsloten.** Op 22 september 2026 vervalt de gegevensverzameling op laag 1. Deze gegevens stellen we niet binnen Profit beschikbaar; het Power BI-dashboard leest de tabellen rechtstreeks uit. Laag 2 en laag 3 houden hun gegevensverzamelingen. Dat raakt §1.4, §5.9, §9.2 en hoofdstuk 11. Zie blok Y.
>
> **Het voortgangsoverleg van 22 september 2026 levert vier wijzigingen op.** **Formatieverdeling telt niet mee**: we kijken altijd naar de functie van het dienstverband (§4.5). Het **hoofddienstverband** is de scope voor Profit 9 en de tabbladen per dienstverband zijn een uitbreiding (§8.5). Tegel 4 heet weer **Samenstelling functiecategorie** (§8.2). En het document Loontransparantie medewerker wordt een **rapport** uit de workflow-editor (§5.9, hoofdstuk 11). Daarnaast komen Pocket en Jonas als raakvlak in hoofdstuk 11 en is de uitleveringsvraag als openstaand punt opgenomen. Zie blok X.
>
> **De verkooprelatie op laag 3 is niet fase-afhankelijk.** Op 22 september 2026 is gecorrigeerd dat §5.4 en §5.5 de fase-as en de populatie-as door elkaar haalden. De verkooprelatie is gevuld bij populatie Ter beschikking gestelde arbeidskrachten én soort Recht op informatie — dus juist in fase 1. Zie blok Z.
>
> **De uitzendkrachten aan uitlenerzijde komen erbij.** Op 22 september 2026 is besloten dat dit deelproject de brontabel voor uitzendkrachten zelf vult en daarmee ook laag 2 en laag 3 met populatie *Ter beschikking gestelde arbeidskrachten*. Dat hoorde bij DP3, maar het dient het recht op informatie en dus dit ontwerp. Het populatiefilter is vastgelegd — aard 11, 22 en 82, *sinds blok AN bepaalt de aard niet meer de populatie* — en een plaatsingmutatie krijgt geen eigen triggerregel. Verder komt er een deelproject **DP5 – Functiecategorie en flex** bij. Dat raakt §1.4, §3.2, §3.3, §5.3, §5.4, §5.5, §7.2, §7.4, hoofdstuk 10 en hoofdstuk 11. Zie blok AA.
>
> **Twee punten uit de conflictronde van 23 september 2026.** Het nalopen van blok AA leverde vijf tegenstrijdigheden op; drie waren redactioneel. De twee inhoudelijke: de cijfers voor uitzendkrachten zijn pas bruikbaar **ná DP5** en dat wordt aanvaard, en de **rapportage** hoort in haar geheel bij DP2 in plaats van verdeeld over DP2 en DP3. Dat raakt hoofdstuk 10 en hoofdstuk 11. Zie blok AB.
>
> **Hoofdstuk 8 is op 23 september 2026 volledig herzien.** De vergelijkingstabel vervalt; de sectie bestaat uit **vijf KPI-tegels** en twee weergaven. Alles staat op **uurbasis** rond één nieuw kerngetal, het **totaal uurloon**. Er is geen juridische basis om het bruto jaarloon bij het recht op informatie te tonen, dus dat verdwijnt van het scherm. Het percentage over de variabele componenten vervalt als tegel; er komt een **individueel loonverschil** voor in de plaats. Twee technische beperkingen bepalen de indeling: wisselen tussen dienstverbanden kan niet, en boven de KPI's kan geen titel of tekst staan, dus de functiecategorie komt als pagina-onderdeel er&oacute;nder. Dat raakt hoofdstuk 1, 2, 3, 5, 6, 7 en 8. Zie blok AC.
>
> **Op 24 september 2026 is de sectie nagelopen.** De eerste twee tegels krijgen een sprekender titel, het tabblad komt onderaan in de groep Salaris, en de actieknop start de profielkeuze in plaats van direct het profiel Recht op informatie. Inhoudelijk weegt de **grondslag van het individueel loonverschil** het zwaarst: die wordt afgezet tegen het gemiddelde van de héle functiecategorie in plaats van tegen het eigen geslacht, omdat de richtlijn juist over gelijke beloning *ongeacht* geslacht gaat. Dat raakt hoofdstuk 2, 3, 5, 6, 7, 8 en 9. Zie blok AD.
>
> **Pocket komt op 24 september 2026 in scope.** Wat tot dan een raakvlak was, is nu een op te leveren onderdeel: een **dataconnector** met vier modi waarmee de app per medewerker en dienstverband de KPI-gegevens en de functielijst ophaalt, en de pagina's *tonen* en *aanpassen* voor het type dossieritem **Vraag aan HR** — een technisch type waarvan Pocket de extra velden niet vanzelf toont. De schermen en de flow blijven bij team Pocket. Twee dingen springen eruit: de connector krijgt als eerste Pocket-connector een **dienstverband-parameter**, met de toets dat dat dienstverband bij de ingelogde medewerker hoort, en daardoor toont **Pocket méér dan de stamkaart** bij meerdere dienstverbanden. Dat raakt §1.3, §1.4, §8.8, §9.1 en hoofdstuk 11. Zie blok AD, punten AD8 en AD9.
>
> **Er komen op 28 september 2026 negen verklarende bedragen bij.** De brainstorm over het dashboard levert een set nieuwe lijstbegrippen op — langdurige ziekte, onbetaald verlof, ouderverlof, kopen en verkopen van uren, inhouding i.v.m. uitruil, incidentele uitkering, bijtelling vervoermiddel en een vrije rubriek — die op de twee eigen brontabellen en op laag 2 worden vastgelegd. Ze verklaren een deel van een loonverschil, zodat niet elk verschil tot een informatieverzoek leidt. Twee dingen wijken af van de bestaande loonbegrippen: het is **één set voor beide populaties**, per dienstverband (*sinds blok AN: per inkomstenverhouding*) én per plaatsing, en AFAS onderhoudt ze maar ze **staan open** voor eigen intellingen van de klant. Juist daarom blijven ze buiten elke formule en elk gemiddelde. Dat raakt §5.3, §5.4, §5.9, §6.1 en §6.2. Zie blok AE.
>
> **De lijstbegrippen voor uitzendkrachten zijn er.** Op 29 september 2026 heeft het cao-team de set opgeleverd: **zeven** begrippen met Profit Id **6.782 tot en met 6.788**, beschikbaar per plaatsing en — net als bij medewerkers — door AFAS meegeleverd en dichtgezet (*sinds blok AL staat die set juist open voor eigen intellingen*). Daarmee vervalt de laatste blokkerende afhankelijkheid van dit deelproject en gaat punt W1 dicht. Twee dingen liggen er nu expliciet in vast: medewerkers en uitzendkrachten houden **elk een eigen set**, zodat de looninrichting van beide populaties gescheiden blijft, en de set telt er **zeven en geen acht**, omdat WrdLn niet naar een plaatsing te herleiden is. Het datamodel, de formules en het vulproces wijzigen niet. Dat raakt §1.4, hoofdstuk 2, §5.3, §6.1 en §6.2. Zie blok AF.
>
> **De sleutel van laag 2 krijgt er op 1 oktober 2026 de functiecategorie bij.** Binnen Flex kan op de plaatsing een **afwijkende functiecategorie** worden vastgelegd. Heeft een uitzendkracht bij één inlener twee plaatsingen in dezelfde functie maar in verschillende functiecategorieën, dan horen daar **twee regels per inkomstenverhouding** bij: die regels vallen in twee vergelijkingsgroepen en mogen dus niet op één regel samenvallen. De unieke sleutel van laag 2 telt daarmee zes velden in plaats van vijf. Dat raakt §4.5, §5.1, §5.3, §5.4, §5.9 en §7.3. Zie blok AG.
>
> **Het RSIN komt op 1 oktober 2026 uit het loonheffingsnummer.** Het veld Fiscaal nummer op de organisatie valt af als groeperingssleutel: Profit bewaakt dat veld met een **integriteitsregel** die hetzelfde nummer bij maar één organisatie toelaat, en die regel kunnen we niet wijzigen. Juist een concern met één RSIN onder meerdere organisaties — het geval dat we willen samenvoegen — kan het veld dus niet overal vullen. We leiden het RSIN daarom af uit de **eerste negen posities van het loonheffingsnummer**, bepaald per **werkgever én periodetabel**. Daarmee wordt het RSIN de sleutel van laag 0 en blijft het veld **Werkgever leeg**: per RSIN kunnen meerdere werkgevers voorkomen die één rapportage-eenheid moeten blijven. Het veld blijft wel behouden, voor het geval het later van waarde blijkt. Twee gevolgen zijn aanvaard: bij een **eenmanszaak** staat er een BSN in het veld RSIN, en een wijzigend loonheffingsnummer laat een lege rapportageperiode achter. Dat raakt hoofdstuk 2, §5.2, §5.3, §5.5, §5.9, §6.3, §7.3, §7.4 en hoofdstuk 10 en 11. Zie blok AH.
>
> **Het vulproces krijgt op 6 oktober 2026 twee triggers uit Flex erbij.** DP5 legt de functiecategorie van een uitzendkracht op twee plekken vast, en beide schrijven voortaan een triggerregel weg: de **functiecategorie op de functie van de klantovereenkomst** — voor elke werkgever met een plaatsing op die functie — en de **afwijkende functiecategorie op de plaatsing**, bij vullen, wijzigen én leegmaken. Daarmee is besluit AA5 herzien; voor de overige plaatsingmutaties blijft het gelden. Op de **functie van de plaatsing** triggeren we niet: die is niet wijzigbaar. Daarnaast is de reikwijdte van het bijwerken verbreed. Omdat functie en functiecategorie óók op laag 1 staan, herbouwt een trigger op **stamgegevens** voortaan de bronregels van het **hele venster** in plaats van één tijdvak; een trigger op **salarisgegevens** blijft bij dat ene tijdvak. Om die twee te kunnen onderscheiden krijgt de triggertabel het kenmerk **Soort trigger**. Dat raakt §1.3, hoofdstuk 2, §5.3, §7.1 tot en met §7.4, §8.1 en hoofdstuk 10. Zie blok AI.
>
> **De loonbegrippen voor uitzendkrachten zijn op 7 oktober 2026 uitgeschreven.** Dat de definities per populatie verschillen stond er al, maar nergens wáárin. Nu is bevestigd dat lijstbegrip 6.783 **alleen de looncomponenten onder het reguliere tarief** bevat en dus géén LnLbPh is. Daarmee werkt de gedeelde formule voor het bruto jaarloon niet voor deze populatie: die trekt de variabele componenten af van een totaalbedrag dat er niet is. Uitzendkrachten krijgen een **eigen formule** — som van ([Brutoloon] + OpgRchtVakBsl + OpbAvwb) — en de twee loonvelden in de brontabellen voor uitzendkrachten en extern heten voortaan **Brutoloon** en **Brutoloon bijzonder tarief**, zonder de toevoeging LB/PH. Let op: het veld *Brutoloon* is **niet** het bruto jaarloon van laag 2; de twee reserveringen komen er nog bij. Dat raakt §5.3, §6.1 en §6.2. **De oude formule is al gebouwd**; het herstel staat als urgent punt AJ-a in hoofdstuk 12. Zie blok AJ.
>
> **Ook bij medewerkers klopte het loonbegrip niet.** Op 7 oktober 2026 is in de Profit-repository geverifieerd dat **LnLbPh het totale loon LB/PH is, inclusief het deel onder bijzonder tarief**, en dat LnTabBB daarvan een deelverzameling is: hetzelfde lijstbegrip, één keer zonder en één keer met een filter op het tarief. Een begrip dat alleen het normale tarief oplevert bestaat niet. Het veld *Loon LB/PH normaal tarief* heet daarom voortaan **Loon LB/PH** en bevat het totaal, met *Loon LB/PH bijzonder tarief* als deelverzameling ernaast. De twee mogen dus **nooit bij elkaar worden opgeteld**. Dat raakt §5.3, §6.1 en §6.2. Of de bouw dit goed heeft staan is nog niet vastgesteld; dat is urgent punt AK-a. Zie blok AK.
>
> **Ook medewerkers krijgen een eigen set lijstbegrippen.** Op 7 oktober 2026 is besloten de bestaande begrippen van de loonaangifte te vervangen door een eigen set, **Profit Id 6.821 tot en met 6.827**, per dienstverband (*sinds blok AN: per inkomstenverhouding*). Zeven begrippen voor acht grootheden: 6.822 levert zowel LnLbPh als LnTabBB, zonder en met een filter op het tarief. De reden is dat die set **openstaat voor eigen intellingen**, zodat de klant correctie-looncomponenten kan laten meetellen die in de loonaangifterubriek niet op de juiste plek landen. Diezelfde dag is besloten dat ook de set voor **uitzendkrachten** opengaat, daar als **uitwijkmogelijkheid** voor een looninrichting die niet in de standaarddefinitie past. Daarmee staat er in dit ontwerp geen lijstbegrip meer dicht. Dat herziet de eerdere eis dat de kerngrootheden dichtstaan, en daarmee ook de redenering over de jaargrens in §4.4: volledigheid weegt zwaarder dan gegarandeerde uniformiteit, omdat het vergelijken binnen één omgeving gebeurt. De formules en het datamodel wijzigen niet. Dat raakt §1.4, hoofdstuk 2, §4.4, §5.3, §6.2 en hoofdstuk 10. De set voor medewerkers moet nog worden opgeleverd — blokkerend punt AL-a. Zie blok AL.
>
> **De percentages draaien op 7 oktober 2026 van teken.** Een positief loonverschil betekende tot nu toe dat vrouwen mínder verdienden, en een positief individueel verschil dat de medewerker mínder verdiende dan het gemiddelde van zijn functiecategorie. Voor de medewerker leest dat averechts. Bij soort rapportage **Recht op informatie** wisselt de teller daarom van volgorde: een **min** betekent voortaan dat vrouwen gemiddeld minder verdienen, en een **plus** dat de medewerker méér verdient dan het categoriegemiddelde. De noemer wijzigt niet en de formules blijven verder gelijk. Voor soort **Rapportage** blijft de wettelijke richting staan. Om te voorkomen dat die twee richtingen elkaar tegenkomen, tonen het dashboard en alle meegeleverde gegevensverzamelingen **uitsluitend** soort Recht op informatie. Bij het nalopen van de schermteksten zijn er drie punten bij gekomen: elk bijschrift krijgt een **derde variant** voor een uitkomst van nul, de aanspreekvorm ligt nu vast — **je** op de ESS-stamkaart en **de medewerker** op de MSS- en plaatsing-stamkaart — en tegel 4 blijft voortaan staan als een geslachtsgroep ontbreekt. Dat raakt hoofdstuk 2, §5.4, §5.5, §5.9, §6.5, §6.6, §6.9, §7.3, §8.2, §8.6, §8.7, §8.8, §9.2 en hoofdstuk 10 en 11. Zie blok AM.
>
> **De indeling in medewerkers en uitzendkrachten volgt op 13 oktober 2026 de verloning, en niet langer de aard arbeidsverhouding.** Onderzoek ON-10 laat zien dat de aard in de praktijk niet consequent wordt vastgelegd: uitzendkrachten bij declaratieverwerking staan in hele omgevingen op aard 1, en aard 11, 22 en 82 komen veel voor bij periodeverwerking zonder loon per plaatsing. De aard bepaalt daarom **niet langer de populatie**. Ze blijft wel een filter: alleen de codes uit het begrippenkader tellen mee, voor beide populaties samen, zodat fictieve dienstbetrekkingen buiten de dataset blijven. De indeling wordt: **declaratieverwerking** gaat altijd naar *bron uitzendkrachten*, **periodeverwerking** naar *bron medewerkers*, en de nieuwe verloningsvariant **Plaatsingen verwerken in periodeverloning** (RHR02179) naar **beide**: bron medewerkers met het totale loon van de inkomstenverhouding, bron uitzendkrachten met het deel per plaatsing, inclusief projecttoeslag. Die twee worden nooit bij elkaar opgeteld. Daarnaast komt er een **filter op soort medewerker** bij het vullen van de brontabellen: stagiairs met salaris en nabetalingen na uitdienst vallen af. Alle drie de filters — soort inkomstenverhouding, aard en soort medewerker — passen we toe **bij het vullen van de brontabellen**, zodat daar alleen staat wat meetelt. Verder leggen we vast dat bron medewerkers **per inkomstenverhouding** wordt gevuld, zodat subdienstverbanden al in de brontabel zijn samengenomen, en dat de stamkaart één **generieke melding** toont als er geen loongegevens zijn. Dat raakt hoofdstuk 2, §3.1, §3.2, §3.3, §3.5, §5.3, §5.4, §5.6, §5.9, §6.1, §6.2, §6.3, §6.7, §7.3, §7.7, §8.1, §8.6, §8.7, §8.8 en hoofdstuk 10, 11 en 12. Zie blok AN.
>
> **De teksten van de tegels liggen op 19 oktober 2026 vast.** De tegels krijgen een **vraag als titel**, met een eigen vorm op de ESS-stamkaart en op de MSS- en plaatsing-stamkaart bij de tegels 1 en 4. Tegel 1 krijgt het bijschrift *gemiddeld per uur*. Alle bedragen krijgen het **valutasymbool van de werkgever**, met de basisvaluta van de omgeving als terugval. De uitleg achter de info-iconen van tegel 1, 4 en 5 is vastgesteld; die van tegel 2 en 3 vervalt. De uitleg bij tegel 4 en 5 noemt het verschil als bedrag én als percentage, beide met teken, zodat één zin elke uitkomst dekt. De sectie krijgt een vaste **toelichting** per stamkaart, die met een script wordt geleverd. De periodeaanduiding *laatste 12 maanden* blijft ongewijzigd. Dat raakt §3.8, §5.9, §8.1, §8.2, §8.7, §8.8, §9.4 en hoofdstuk 12. Zie blok AO.
>
> **Ook de meldingen liggen op 19 oktober 2026 vast.** Elke melding hoort bij een toestand (*state*) en een tegel, met een je-vorm en een de-medewerkervorm. Twee dingen wijzigen in het gedrag: is de medewerker de **enige** in zijn functiecategorie, dan blijft tegel 4 staan met een melding in plaats van te vervallen, en buiten Nederland toont **Pocket** een melding in plaats van de pagina te verbergen. De melding over een functiewissel binnen het jaar staat alleen in Pocket. Dat raakt §8.2, §8.6, §8.7, §8.8, §9.4 en §9.6. Zie blok AP.
>
> Laag 0 is op 16 september 2026 herzien: de tabel heet **Loontransparantie rapportage**, krijgt een surrogaatsleutel **Rapportage ID** met een unieke sleutel op RSIN, werkgever, soort rapportage, jaar en volgnummer, en een expliciet veld **Soort rapportage** in plaats van de conventie rapportagejaar 0. Begindatum, einddatum en status vervallen. Zie blok T.
>
> **Laag 2, laag 3 en het vulproces zijn op 16 september 2026 herzien.** Beide tabellen krijgen een **GUID** als primaire sleutel met daarnaast een unieke sleutel; op laag 2 vervallen de velden Werkgever en Periodetabel, en de populatie wordt een codetabel **Populatie loontransparantie**. Het accorderen van de salarisverwerking werkt de tabellen niet langer direct bij, maar schrijft alleen triggerregels weg — ook voor tijdvakken die met terugwerkende kracht zijn geraakt. De **conversie naar Profit 9** vult de triggertabel over 2026, zodat de eerste dagovergang de tabellen opbouwt. Dat raakt hoofdstuk 1, 2, 4, 5, 7 en 10. Zie blok U.
>
> De versie van vóór deze herziening staat als momentopname in [_versies/20260916_05_Functionele_beschrijving.md](_versies/20260916_05_Functionele_beschrijving.md).
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

De gegevens die daarvoor nodig zijn, zitten al in Profit: in de salarisverwerking. Maar ze staan verspreid, per loontijdvak en per dienstverband. Elke presentatievorm zou die gegevens opnieuw moeten verzamelen, omrekenen en aggregeren. Dat is traag en het levert het risico op dat de KPI, een dashboard en een document verschillende uitkomsten tonen.

In dit ontwerp lossen we dat op met één voorbereide gegevensverzameling in vier lagen. We richten dit zo in dat de berekeningen één keer plaatsvinden, in een aparte wachtrijtaak buiten het salarisproces om, en dat elke presentatielaag daarna alleen nog leest.

**De Nederlandse implementatiewet is nog niet aangenomen.** De plenaire behandeling in de Tweede Kamer is verschoven van 11 januari 2027 naar 7 december 2026; daarna volgen de Eerste Kamer en de publicatie. Een datum van inwerkingtreding staat dus nog niet vast, en in de markt wordt al gespeculeerd dat 1 januari 2027 niet haalbaar is en 1 juli 2027 realistischer. We gaan ervan uit dat de rapportagelijn en de grondslagen uit het begrippenkader overeind blijven en bouwen daarom door op de keuzes in dit ontwerp. Wat die onzekerheid betekent voor het moment van uitleveren, staat als openstaand punt X6 in hoofdstuk 12.

### 1.2 Doel

Een gegevensmodel Recht op informatie neerzetten dat de actuele loontransparantiegegevens per arbeidsverhouding bevat, plus het proces dat het gevuld en actueel houdt. Op basis daarvan tonen we de medewerker KPI's met bijbehorende weergaven op de stamkaart.

### 1.3 Resultaat

Na oplevering geldt het volgende:

- Er zijn drie brontabellen loontransparantie: één voor eigen medewerkers, één voor uitzendkrachten en één voor geanonimiseerde gegevens van een uitlener. Ze leggen per medewerker, dienstverband en loontijdvak de verwerkte loongegevens vast, voor elk tijdvak waarvoor de salarisverwerking is geaccordeerd.
- Daarboven staat de tabel Loontransparantie per inkomstenverhouding met de waarden over de rapportageperiode, per functie en functiecategorie waarin de medewerker binnen die periode heeft gewerkt, en de tabel Loontransparantie per functiecategorie met de vergelijkingscijfers voor mannen en vrouwen.
- Bovenaan staat de rapportageperiode: de vastlegging van de afbakening waarover is gerekend. Daardoor kan DP2 – Rapportage later dezelfde tabellen gebruiken voor een afgesloten kalenderjaar, zonder dat het model wordt opengebroken.
- Een triggertabel houdt bij welke werkgever en welk loontijdvak zijn geraakt. Dat gebeurt bij het accorderen van de salarisverwerking — voor het geaccordeerde tijdvak én voor elk tijdvak dat met terugwerkende kracht is geraakt — maar ook bij een functiewijziging, bij een wijziging in de functiecategorie-inrichting en bij de twee Flex-gegevens waarmee de functiecategorie van een uitzendkracht wordt vastgelegd (§7.2).
- De wachtrijtaak **Bijwerken gegevens loontransparantie** vult op basis van die triggertabel de brontabellen en stelt de twee tabellen erboven opnieuw samen. Die taak wordt vanuit de dagovergang Vernieuwen actuele gegevens gestart en staat los van het salarisproces, zodat een fout in de eerstvolgende dagovergang vanzelf wordt hersteld.
- De medewerker ziet op de stamkaart een sectie Loontransparantie met vijf KPI-tegels, daaronder een pagina-onderdeel met de eigen functie en functiecategorie, een overzicht van de functies in die categorie en een actieknop om een vraag aan HR te stellen. Alle cijfers staan op uurbasis; een vergelijkingstabel is er niet (hoofdstuk 8).
- Voor **AFAS Pocket** is er een dataconnector met vier modi waarmee de app dezelfde gegevens ophaalt, per medewerker **en dienstverband**, plus de pagina's *tonen* en *aanpassen* voor het type dossieritem Vraag aan HR (§8.8).
- De brontabellen zijn direct bruikbaar als bron voor een Power BI-dashboard en voor latere documenten, zonder dat die opnieuw moeten rekenen.

### 1.4 Afbakening van dit document

In scope:

- Het gegevensmodel Recht op informatie: de vier lagen, hun sleutels, velden en betekenis, en per veld in welke fase het wordt gevuld.
- De drie nieuwe brontabellen loontransparantie, inclusief het vullen van de tabellen voor **eigen medewerkers** en voor **uitzendkrachten**.
- De berekeningen die bij het vullen van die lagen plaatsvinden.
- De populatie: welke medewerkers en dienstverbanden wel en niet in de tabel komen.
- De periode waarover we rekenen en de manier waarop we het venster bepalen.
- Het vulproces: de triggertabel, de wachtrijtaak vanuit de dagovergang, herberekening, correcties en de eenmalige vulling van de triggertabel in de conversie naar Profit 9.
- De KPI en de weergaven op de standaard stamkaarten in InSite: medewerker ESS, medewerker MSS en plaatsing.
- De **dataconnector voor Pocket**, met de modi waarmee de app per medewerker en dienstverband de KPI-gegevens en de functielijst ophaalt (§8.8).
- De pagina's *tonen* en *aanpassen* voor het type dossieritem **Vraag aan HR in Pocket**. Pocket toont standaard alleen onderwerp, toelichting en bijlage; de extra velden van dit technische type moeten erbij worden geprogrammeerd (§8.8).
- De landtoets waarmee de sectie alleen wordt getoond bij medewerkers onder Nederlandse wetgeving (§9.6).
- De gegevensverzamelingen waarmee laag 2 en laag 3 worden ontsloten voor weergaven en documenten. De brontabellen krijgen bewust geen gegevensverzameling (§5.9).
- Autorisatie, privacy en de groepsgrootte voor vergelijkingscijfers.

Buiten scope:

- **Andere landen dan Nederland.** De scope van dit deelproject is Nederland. Wat dat betekent voor België en de Caribbean staat in §9.6.
- De wettelijke rapportage over loonverschillen op organisatieniveau en de 5%-signalering. Die horen bij DP2 – Rapportage. DP2 rapporteert over een afgesloten kalenderjaar en gebruikt daarvoor dezelfde tabellen met een eigen rapportageperiode. Welke velden daarvoor in fase 2 worden toegevoegd staat in §5.7; het bouwen ervan valt buiten dit ontwerp.
- De brontabel **Loontransparantie bron extern**. De structuur staat op hoofdlijn in §5.3; invulling en realisatie horen bij DP2.
- De **gegevensuitwisseling tussen in- en uitlener**. Die hoort bij DP3. Het **vullen** van de brontabel voor uitzendkrachten hoort sinds 22 september 2026 wél bij dit ontwerp: het dient het recht op informatie van de uitzendkracht, en dat is het onderwerp van dit deelproject (§5.3).
- De **rapportage over uitzendkrachten door de inlener**. Die loopt via de brontabel *Loontransparantie bron extern* en hoort bij DP2. De uitlener rapporteert zelf niet over de uitzendkrachten die hij uitleent (§3.3).
- Het **maken van de lijstbegrippen**. Die komen van het cao-team; dit ontwerp levert de specificatie en de aanvraag. De set voor **uitzendkrachten** is op 29 september 2026 opgeleverd — zeven begrippen met Profit Id 6.782 t/m 6.788 — waarmee dat niet langer blokkerend is (§5.3, hoofdstuk 12 punt W1). Voor **medewerkers** komt er sinds 7 oktober 2026 ook een eigen set, Profit Id 6.821 t/m 6.827, zodat de klant er correctie-looncomponenten in kan tellen (hoofdstuk 12, blok AL).
- Het **functiegroepen-model**, het **uitvraagformulier gelijkwaardige beloning** en de resterende **gegevens op de plaatsing**. Die horen bij DP5 (hoofdstuk 11).
- Het type dossieritem waarmee een medewerker een vraag stelt. Dat is ontworpen in DP4 – Vraag aan HR. Dit ontwerp voegt de actieknop toe die dat proces start (§8.1) en de Pocket-pagina's waarmee zo'n item wordt getoond en aangepast (§8.8). Welíke extra velden op die pagina's staan, bepaalt DP4.
- De **schermen in de Pocket-app zelf**, de navigatie ertussen en de flow van het insturen. Die bouwt team Pocket, op de connector en de pagina's die wij leveren (§8.8).
- Het rapport **Loontransparantie medewerker**, de OutSite-route en de jaarlijkse notificatie. Deze raakvlakken benoemen we op hoofdlijn in hoofdstuk 11; de uitwerking volgt later.
- Het opnieuw ontwerpen van de functiecategorie-inrichting. Dat is de basis uit Profit 8 en die nemen we als gegeven.

### 1.5 Uitgangspunten

We richten dit ontwerp in op basis van zes uitgangspunten:

1. **Voorberekenen boven live rekenen.** We slaan de uitkomsten op die de KPI en het dashboard nodig hebben. Bij het uitlezen wordt niet gerekend.
2. **Verdichten mag nooit informatie weggooien die we nog nodig hebben.** Uit een gemiddelde kun je niet betrouwbaar een nieuw gemiddelde afleiden. We bewaren daarom de gegevens per loontijdvak, zodat het dashboard de vragen achter een KPI kan beantwoorden en een andere doorsnede alsnog mogelijk is. Verdichting komt daar bovenop, niet in de plaats van.
3. **Uitlegbaar boven compact.** Support en consultancy krijgen detailvragen over elke KPI. Het model moet zo zijn opgezet dat elk getoond getal herleidbaar is tot de onderliggende perioden en loonbegrippen.
4. **Actueel én vastgelegd.** De medewerker ziet altijd de actuele stand. Daarnaast moet het model een afgesloten kalenderjaar kunnen bevriezen, omdat de wettelijke rapportage dat vraagt. Wat er niet komt is een peildatumweergave waarmee je willekeurig kunt terugkijken naar een oude stand.
5. **Het salarisproces mag er geen last van hebben.** Het accorderen van de salarisverwerking signaleert alleen dát er iets is gewijzigd; het vullen én het rekenwerk gebeuren daarbuiten, in een aparte taak.
6. **Eén definitie, één berekening, één tabel.** Rekenen we over een andere periode, dan verschilt alleen de sleutel; niet de formule en niet de tabel. Daarmee bouwt DP2 verder op hetzelfde model in plaats van naast een eigen model.

---

## 2 Begrippen

> **Let op bij de term arbeidsverhouding.** Het begrippenkader loontransparantie en de wettelijke bronnen gebruiken **arbeidsverhouding** als rekeneenheid. Dat is in Profit de **inkomstenverhouding**. Profit kent daarnaast het veld **aard arbeidsverhouding** uit de loonaangifte (§3.3), en dat is iets heel anders: dat zegt wélk soort dienstbetrekking het is, niet om welke eenheid het gaat. Waar in dit document arbeidsverhouding staat, wordt steeds de inkomstenverhouding bedoeld; het loonaangiftekenmerk noemen we voluit aard arbeidsverhouding.
>
> Om dezelfde reden hanteren we consequent **soort inkomstenverhouding**. Het begrippenkader noemt dat kenmerk *soort arbeidsverhouding*, maar het is precies het veld dat in Profit soort inkomstenverhouding heet (§3.2). We nemen de bronterm niet over, omdat die in Profit naar het verkeerde veld wijst.

| Begrip | Betekenis in dit ontwerp |
| --- | --- |
| Recht op informatie | Het recht van een medewerker om het eigen loonniveau en het gemiddelde loonniveau per functiecategorie, uitgesplitst naar geslacht, op te vragen. |
| Loonniveau | Het loon uitgedrukt per verloond uur. Een eerdere versie van dit ontwerp ging uit van twee eenheden tegelijk — het bruto jaarloon én het bruto uurloon — maar voor het recht op informatie is daar geen juridische basis voor (§6.5). |
| Loonverschil | Het verschil tussen het gemiddelde loonniveau van mannen en dat van vrouwen, uitgedrukt als percentage van het gemiddelde van de mannen. De ministeriële regeling hanteert deze term; het wetsvoorstel en het begrippenkader spreken van loonkloof. Welk teken de uitkomst krijgt, hangt af van de rekenrichting hieronder. |
| Rekenrichting | De kant waarop een loonverschilpercentage telt. Bij soort rapportage *Recht op informatie* telt het vanuit de groep of de persoon die het percentage beschrijft: een **min** betekent minder verdienen, een **plus** meer. Bij soort *Rapportage* geldt de wettelijke richting, waarin een plus juist betekent dat vrouwen minder verdienen. De noemer en de rest van de formule zijn in beide gevallen gelijk (§6.5). |
| Mediaan | Het bedrag waarbij de ene helft van een groep meer verdient en de andere helft minder. Naast het gemiddelde een tweede maat voor het midden, die ongevoelig is voor enkele uitschieters. |
| Loonverschil uurloon | Het loonverschil berekend op het bruto uurloon, dus alleen op het basisloon. Wordt berekend en vastgelegd, maar niet meer als KPI getoond (§6.5). |
| Loonverschil totaal uurloon | Het loonverschil berekend op het gemiddelde totaal uurloon. Dit is het percentage dat de medewerker op de stamkaart ziet; een negatieve uitkomst betekent daar dat vrouwen gemiddeld minder verdienen dan mannen (§6.5, §8.2). |
| Individueel loonverschil | Het verschil tussen het eigen totaal uurloon en het gemiddelde totaal uurloon van de hele functiecategorie — alle geslachten samen — uitgedrukt als percentage van dat gemiddelde. Het geslacht van de medewerker speelt er geen rol in. Een positieve uitkomst betekent dat de medewerker **méér** verdient dan het categoriegemiddelde (§6.5). |
| Loonverschil jaarloon | Het loonverschil berekend op het bruto jaarloon. Wordt berekend en vastgelegd, maar niet als KPI getoond. |
| Jaaruren | De som van de verloonde uren over het venster. |
| Bruto jaarloon | De som van het brutoloon over het venster. |
| Bruto uurloon | Het bruto jaarloon gedeeld door de jaaruren. Hiermee vangen we het deeltijdeffect op; er is geen aparte deeltijdcorrectie op het jaarloon. |
| Jaarwaarde variabele componenten | De som van de looncomponenten bovenop het basisloon over het venster, zoals toeslagen en bonussen. |
| Uurwaarde variabele componenten | De jaarwaarde variabele componenten gedeeld door de jaaruren. |
| Totaal uurloon | Het bruto uurloon plus de uurwaarde variabele componenten: het volledige loon per verloond uur. Het kerngetal op de stamkaart en de grondslag van de twee percentages die de medewerker ziet (§6.1, §6.5). |
| Loonaangifte | De periodieke aangifte loonheffingen. In dit ontwerp geen bron meer voor de bedragen, maar wel de herkomst van de begrippen en van de lijstbegrippen voor medewerkers in §6.2. |
| Lijstbegrip | De gestandaardiseerde ontsluiting van een berekend salarisgegeven. AFAS levert de lijstbegrippen die dit ontwerp gebruikt standaard mee en vult ze. Elke populatie heeft een eigen set: voor medewerkers Profit Id 6.821 t/m 6.827 per inkomstenverhouding, voor uitzendkrachten 6.782 t/m 6.788 per plaatsing. Beide sets staan open voor eigen intellingen van de klant (§5.3). |
| Inkomstenverhouding (IKV) | De eenheid waarop de loonaangifte in Profit is opgebouwd. Een medewerker kan er meerdere hebben. Effectief is elk dienstverband een eigen inkomstenverhouding, behalve bij subdienstverbanden: die vallen samen met hun kapstokdienstverband onder één inkomstenverhouding. Dat doet zich vooral voor in het onderwijs. Ook de plaatsingsdienstverbanden van Plaatsingen verwerken in periodeverloning vallen onder de inkomstenverhouding van het hoofddienstverband. |
| Kapstokdienstverband | Het dienstverband waaronder één of meer subdienstverbanden hangen. De loonaangifte wordt op het kapstokdienstverband gedaan, inclusief de loongegevens van de subdienstverbanden eronder. |
| Subdienstverband | Een dienstverband dat onder een kapstokdienstverband hangt. Komt vooral voor in het onderwijs, waar een medewerker meerdere aanstellingen naast elkaar heeft binnen één inkomstenverhouding. |
| Hoofddienstverband | Het dienstverband dat als hoofddienstverband is aangemerkt. Een medewerker heeft er altijd precies één. |
| Formatieverdeling | De verdeling van een dienstverband over meerdere functies, kostenplaatsen of kostendragers. Bedoeld voor kostentoerekening en niet voor beloning; telt in dit ontwerp niet mee (§4.5). |
| Functiecategorie | De groepering van functies waarbinnen we medewerkers met elkaar vergelijken. Ingericht door de klant, op basis van Profit 8. |
| Toegekende functie | De functie die gold op de laatste dag van een loontijdvak. Het loon over dat hele tijdvak wordt aan die functie toegekend (§4.5). |
| Arbeidsverhouding | De rekeneenheid voor de gemiddelden, afkomstig uit het begrippenkader. In Profit is dat de **inkomstenverhouding**: één arbeidsverhouding is één inkomstenverhouding, niet één persoon. Een medewerker met twee inkomstenverhoudingen telt dus twee keer mee. Wisselt een arbeidsverhouding binnen de rapportageperiode van functie, dan levert dat per functie een eigen regel op die elk als volwaardige arbeidsverhouding meetelt (§6.3). Niet te verwarren met het loonaangiftekenmerk aard arbeidsverhouding. |
| Aard arbeidsverhouding | Het loonaangiftekenmerk dat aangeeft om wélk soort dienstbetrekking het gaat, zoals een arbeidsovereenkomst of een publiekrechtelijke aanstelling. Een filter bij het vullen van de brontabellen: alleen de codes uit het begrippenkader tellen mee (§3.2). Sinds 13 oktober 2026 bepaalt het **niet meer de populatie**, omdat het in de praktijk niet consequent wordt vastgelegd (§3.3). En evenmin de rekeneenheid hierboven. |
| Soort medewerker | Het kenmerk van het dienstverband dat aangeeft wat voor medewerker het is, zoals personeelslid, stagiair of nabetaling na uitdienst. Een filter bij het vullen van de brontabellen; het wordt zelf niet opgeslagen (§3.2). |
| Vergelijkingsgroep | De arbeidsverhoudingen waarmee het loonniveau van de medewerker wordt vergeleken: alle arbeidsverhoudingen in dezelfde functiecategorie, uitgesplitst naar geslacht. |
| Geslacht | Het geslacht zoals vastgelegd in de administratie van de werkgever. Het begrippenkader kent vier waarden: man, vrouw, X en niet ingevuld. Alleen man en vrouw gaan de vergelijkingscijfers in (§3.8). |
| Rapportageperiode | De afbakening waarover een complete set cijfers is berekend, vastgelegd als één regel in de tabel Loontransparantie rapportage. Het veld **Soort rapportage** bepaalt welke: *Recht op informatie* is het voortschrijdende venster, *Rapportage* is een afgesloten kalenderjaar voor de wettelijke rapportage (§5.2). |
| Venster | De rapportageperiode van dit ontwerp: de laatste twaalf maanden, of het aantal loontijdvakken dat bij de periodetabel van de werkgever bij een jaar hoort (§4.3). |
| Loontijdvak | Het tijdvak waarover de salarisverwerking is uitgevoerd. De eenheid waarop de brontabellen zijn opgebouwd. Niet te verwarren met het aangiftetijdvak: dat is het tijdvak van de loonaangifte, dat maar drie indelingen kent. |
| Periodetabel | De indeling die bepaalt hoe lang een loontijdvak is. Profit kent er acht en dit ontwerp ondersteunt ze alle acht (§4.3). |
| Land van wetgeving | Het land onder wiens wetgeving een medewerker valt. Profit legt dat per medewerker vast in het veld `AfasKnCountryByLaw`. Bepaalt of de medewerker meetelt in de berekening en of de sectie Loontransparantie wordt getoond (§9.6). |
| Klaargezette loonaangifte | Een aangiftetijdvak waarvoor de werkgever de loonaangifte heeft klaargezet. In eerdere versies van dit ontwerp het vulmoment en het eindpunt van het venster; sinds 15 september 2026 vervangen door de geaccordeerde salarisverwerking. Het **aangiftetijdvak** zelf speelt sinds 17 september 2026 helemaal geen rol meer: de brontabellen zijn opgebouwd per loontijdvak. |
| Geaccordeerde salarisverwerking | Een tijdvak waarvoor de werkgever de salarisverwerking heeft geaccordeerd. Dit is het moment waarop er triggerregels worden weggeschreven; het vullen gebeurt daarna in de dagovergang (§7.1). |
| Uitzendkracht | Een medewerker die via een plaatsing bij een inlener werkt en van wie het loon **per plaatsing** wordt berekend: bij declaratieverwerking of bij Plaatsingen verwerken in periodeverloning. Valt in dit ontwerp in een eigen brontabel en in een eigen populatie (§3.3, §5.3). |
| Plaatsing | De koppeling van een uitzendkracht aan een inlener, met een eigen functie en periode. Sleutelveld in de brontabel voor uitzendkrachten. |
| Verkooprelatie | De inlener bij wie een uitzendkracht via een plaatsing werkt. Het kenmerk waarop het recht op informatie van een uitzendkracht wordt afgebakend (§5.3). |
| Verloningsvariant | De manier waarop Profit het loon berekent: per medewerker, per dienstverband of per plaatsing. Bepaalt in welke brontabel de gegevens komen (§3.3). |
| Declaratieverwerking | De verloningsvariant waarin elke berekening uitgaat van een declaratie, en elke declaratie aan een plaatsing hangt. Gaat altijd naar de brontabel voor uitzendkrachten (§3.3). |
| Plaatsingen verwerken in periodeverloning | De verloningsvariant uit RHR02179, vanaf loonjaar 2027. Het vaste periodeloon staat op het hoofddienstverband; daarnaast is er per plaatsing een technische berekening op een plaatsingsdienstverband. Gaat naar beide brontabellen (§3.3). |
| Plaatsingsdienstverband | Het technische dienstverband waarop Profit bij Plaatsingen verwerken in periodeverloning het loon van één plaatsing berekent. Valt onder dezelfde inkomstenverhouding als het hoofddienstverband en is voor de gebruiker niet zichtbaar als dienstverband. |
| Projecttoeslag | Een toeslag die een gedetacheerde voor de duur van een plaatsing krijgt, bovenop het vaste periodeloon. Telt mee in het loon per plaatsing én in het totaal van de inkomstenverhouding (§3.3). |
| Kenmerk arbeidskracht | Het gepseudonimiseerde kenmerk waarmee de uitlener één arbeidskracht aanduidt in de gegevens die hij aan de inlener levert. Niet herleidbaar tot een persoon, maar wel stabiel over de tijdvakken heen, zodat de regels van één arbeidsverhouding bij elkaar horen (§5.3). |
| Triggertabel | De technische tabel waarin wordt bijgehouden welke combinatie van werkgever, periodetabel, jaar en periode is geraakt en dus moet worden bijgewerkt (§7.2). |
| Triggerregel | Één regel in die tabel. Wordt weggeschreven bij het accorderen of terugdraaien van een salarisverwerking, bij een functiewijziging, bij een wijziging in de functiecategorie-inrichting en bij een wijziging van de functiecategorie op de functie van de klantovereenkomst of van de afwijkende functiecategorie op de plaatsing (§7.2). |
| Soort trigger | Het kenmerk op een triggerregel dat vastlegt of er bedragen zijn gewijzigd (*Salarisgegevens*) of alleen de indeling (*Stamgegevens*). Bepaalt of de taak één tijdvak of het hele venster aan bronregels opnieuw wegschrijft (§7.2, §7.3). |
| Wachtrijtaak | De taak **Bijwerken gegevens loontransparantie**, die de brontabellen vult en de lagen 2 en 3 opnieuw samenstelt. Wordt uitsluitend vanuit de dagovergang Vernieuwen actuele gegevens gestart; er is geen knop om hem handmatig te starten (§7.3). |
| Populatie | Het onderscheid tussen eigen medewerkers en ter beschikking gestelde arbeidskrachten. Welke populatie een regel krijgt, volgt uit de verloningsvariant (§3.3). Vastgelegd in de codetabel **Populatie loontransparantie** en sleutelonderdeel van laag 3 (§5.4). |
| Dagovergang | De geplande taak Vernieuwen actuele gegevens, die de klant doorgaans elke nacht laat draaien. |
| Correctieperiode | Een periode waarmee achteraf een eerdere periode wordt gecorrigeerd, mogelijk over de jaargrens heen. |
| RSIN | Het Rechtspersonen en Samenwerkingsverbanden Informatienummer, toegekend door de Kamer van Koophandel. Het nummer waarop de wettelijke rapportage plaatsvindt. Meerdere werkgevers kunnen onder hetzelfde nummer vallen. We leiden het af uit de eerste negen posities van het loonheffingsnummer (§5.2). |
| Loonheffingsnummer | Het nummer waaronder een werkgever loonaangifte doet, vastgelegd per werkgever en periodetabel. De eerste negen posities zijn het fiscale nummer; het subnummer staat achter de L. De bron van het RSIN in dit ontwerp (§5.2). |
| Rapportage-eenheid | De groep werkgevers waarbinnen wordt vergeleken: alle combinaties van werkgever en periodetabel waarvan het loonheffingsnummer hetzelfde RSIN oplevert. Geen eigen veld, maar het veld RSIN op laag 0 (§5.2). |
| Loontransparantie rapportage | De tabel van laag 0, met per rapportage-eenheid één regel per rapportageperiode (§5.2). |
| Rapportage ID | De primaire sleutel van die tabel: een technisch volgnummer zonder betekenis, waarnaar laag 2 en 3 verwijzen. |
| Soort rapportage | Het veld dat vastlegt waarover een rapportageperiode gaat: *Recht op informatie* voor het voortschrijdende venster, *Rapportage* voor een afgesloten kalenderjaar (§5.2). |
| Brontabellen loontransparantie | De drie tabellen met de verwerkte loongegevens per medewerker, dienstverband en loontijdvak: één voor eigen medewerkers, één voor uitzendkrachten en één voor extern aangeleverde gegevens. De feitenlaag van het model; in dit document ook wel de brontabel (§5.3). |
| Loontransparantie per inkomstenverhouding | De tabel met per rapportageperiode, inkomstenverhouding, functie en functiecategorie één regel met de waarden over de tijdvakken die aan die functie zijn toegekend. In dit document kort: de regel per inkomstenverhouding. |
| Loontransparantie per functiecategorie | De tabel met de gemiddelden en de loonverschilpercentages per rapportageperiode en functiecategorie, met mannen en vrouwen naast elkaar op één regel. In dit document kort: de tabel per functiecategorie. |
| Totaal | Het aantal arbeidsverhoudingen in een functiecategorie samen, inclusief die met geslacht X of zonder ingevuld geslacht. Het totaal is dus niet de som van mannen en vrouwen. Van de gemiddelden en de medianen is er geen totaal (§5.5). |

---

## 3 Populatie

### 3.1 Wat we vastleggen

We nemen in de tabel de medewerkers op die onder de loontransparantieverplichting vallen. Dat is niet iedereen die in de verloning voorkomt. In de loonadministratie zitten ook personen die wel worden verloond, maar die geen medewerker in de zin van de richtlijn zijn.

We leggen per medewerker elke relevante arbeidsverhouding apart vast. Heeft een medewerker meerdere inkomstenverhoudingen, dan levert dat meerdere regels op. We voegen die regels niet samen. Dat is nodig omdat de loonaangifte in Profit per inkomstenverhouding wordt opgebouwd en omdat DP2 op dat niveau moet kunnen rapporteren.

De inkomstenverhouding is ook de rekeneenheid voor de gemiddelden. Het begrippenkader definieert de arbeidsverhouding als de inkomstenverhouding, dus een medewerker met twee inkomstenverhoudingen telt twee keer mee in het aantal arbeidsverhoudingen. Dat is bovendien inhoudelijk juist: functie en standplaats kunnen per arbeidsverhouding verschillen, en de vergelijking gaat over de functiecategorie waarin het loon is verdiend.

De brontabel voor medewerkers legt de gegevens vast **per inkomstenverhouding**, omdat de lijstbegrippen hun waarde per inkomstenverhouding leveren. Effectief is elk dienstverband een eigen inkomstenverhouding, behalve bij subdienstverbanden: die vallen samen met hun kapstokdienstverband onder één inkomstenverhouding, en zijn daardoor al in de brontabel gegroepeerd (§5.3). Dat speelt vooral in het onderwijs, waar subdienstverbanden onder één kapstokdienstverband hangen. Hoofdstuk 6 werkt dit uit. Wat de medewerker vervolgens op de KPI ziet, is een presentatiekeuze; die staat in hoofdstuk 8.

**Het kapstokdienstverband is leidend voor de kenmerken.** De loonaangifte wordt op het kapstokdienstverband gedaan, inclusief de loongegevens van de subdienstverbanden eronder. Wij volgen dat: de functie, de functiecategorie en de overige kenmerken op de regel per inkomstenverhouding komen van het kapstokdienstverband, en de loonbedragen en uren van alle dienstverbanden onder dezelfde inkomstenverhouding staan samen op de bronregel.

Dat is bewust. De subdienstverbanden vormen samen één arbeidsverhouding in de zin van het begrippenkader; ze apart meetellen zou de medewerker meerdere keren in dezelfde vergelijkingsgroep zetten en het gemiddelde omlaag trekken, omdat elk deel op zichzelf een klein loon heeft. De keerzijde is dat een medewerker met sterk verschillende aanstellingen onder één kapstok in de functiecategorie van de kapstok valt. Dat is de indeling die de werkgever zelf heeft gemaakt.

### 3.2 De filters op soort inkomstenverhouding, aard arbeidsverhouding en soort medewerker

We nemen niet iedereen op die in de verloning voorkomt. In de loonadministratie zitten ook personen die wel worden verloond, maar die geen eigen medewerker zijn in de zin van de richtlijn.

We filteren daarom op drie kenmerken: de **soort inkomstenverhouding**, de **aard arbeidsverhouding** en de **soort medewerker**. Alle drie liggen in Profit altijd vast en zijn per dienstverband eenduidig. Ze bepalen **wie** meetelt, niet in welke populatie; dat volgt uit de verloningsvariant (§3.3). Er komt geen handmatige aanvinkmogelijkheid voor de klant.

**Soort inkomstenverhouding**

Deze soorten tellen mee, voor beide populaties:

| Soort | Omschrijving |
| --- | --- |
| 11 | Loon/salaris ambtenaren in de zin van de Ambtenarenwet |
| 13 | Loon/salaris directeuren NV/BV verzekerd voor de werknemersverzekeringen |
| 15 | Loon/salaris niet hiervoor genoemde medewerkers |
| 17 | Loon/salaris directeuren NV/BV niet verzekerd voor de werknemersverzekeringen |

Alle andere soorten vallen af. Daarmee blijven onder meer uitkeringen, pensioenen, wachtgeld, transitievergoedingen en flexmedewerkers buiten de dataset.

Twee dingen zijn hierbij het opmerken waard:

- **Directeuren tellen wel mee**, zowel verzekerd (13) als niet verzekerd voor de werknemersverzekeringen (17). Een directeur-grootaandeelhouder valt daarmee binnen de populatie.
- **Dit filter geldt voor beide populaties.** Het begrippenkader maakt bij dit kenmerk geen onderscheid tussen eigen medewerkers en uitzendkrachten: §3.7.3 schrijft voor alle arbeidsverhoudingen dezelfde vier soorten voor, met dezelfde eisen dat loon en verloonde uren groter dan nul zijn. In welke populatie een arbeidsverhouding valt, volgt uit de **verloningsvariant** (§3.3).

Deze selectie sluit aan bij het begrippenkader loontransparantie, dat bij hetzelfde kenmerk dezelfde vier soorten inkomen noemt. Het kader spreekt daar van *soort arbeidsverhouding*; wij houden de Profit-term **soort inkomstenverhouding** aan (zie de opmerking bij hoofdstuk 2).

Van dit filter is één uitzondering nog niet uitgezocht. Een UMC heeft mogelijk afwijkende afspraken met de Belastingdienst, waardoor het een andere soort inkomstenverhouding gebruikt (vermoedelijk 35). Die medewerkers zouden dan buiten de populatie vallen terwijl ze er inhoudelijk wel in horen (hoofdstuk 12, punt AN-a).

**Aard arbeidsverhouding**

De soort inkomstenverhouding alleen is niet genoeg. Soort 15 is breed en laat ook fictieve dienstbetrekkingen door, zoals musicus, deelvisser en thuiswerker. Die horen niet tot de arbeidsverhoudingen in de zin van de richtlijn. We filteren daarom ook op de aard arbeidsverhouding, en nemen alleen de codes mee die het begrippenkader noemt (§3.7.2):

| Aard | Omschrijving |
| --- | --- |
| 1 | Arbeidsovereenkomst, exclusief BBL |
| 11 | Uitzendkracht |
| 18 | Publiekrechtelijke aanstelling |
| 21 | WSW beschut werk |
| 22 | WSW detachering bij een reguliere werkgever |
| 23 | WSW begeleid werk |
| 24 | Participatiewet beschut werk |
| 82 | Payrolling |
| 83 | Beroepspraktijkopleiding van de beroepsbegeleidende leerweg (BBL) |

Alle andere aarden vallen af. Daarmee verdwijnen onder meer deelvisser (4), musicus of artiest (6), stagiair (7), thuiswerker (8) en de overige fictieve dienstbetrekkingen (81) uit de dataset.

**Dit is één filter voor beide populaties.** Het begrippenkader verdeelt deze codes over eigen werknemers (1, 18, 21, 23, 24 en 83) en de uitzendketen (11, 22 en 82). Die verdeling nemen we **niet** over voor de indeling: de aard wordt in de praktijk niet consequent vastgelegd, en uitzendkrachten bij declaratieverwerking staan in hele omgevingen op aard 1 (§3.3). Welke van de negen codes iemand heeft, maakt voor de populatie dus niet uit; dát hij er één heeft, wel.

**Soort medewerker**

Het derde filter werkt op de soort medewerker van het dienstverband. Alleen de soorten die Profit verloont komen in aanmerking, en daarvan tellen er drie mee:

| Telt mee | Valt af |
| --- | --- |
| Personeelslid | Stagiair - met salaris/stagevergoeding |
| Ondernemer - met salaris | Nabetaling na uitdienst |
| Expat | |

De soorten die Profit niet verloont — zoals interimmer, uitzendkracht, van ander bedrijf of filiaal ingeleend, stagiair zonder salaris en ondernemer zonder salaris — leveren geen berekende salarisgegevens op en komen dus vanzelf niet in de brontabellen.

**Stagiairs met salaris vallen af.** In de praktijk krijgt een stagiair vaak de functie waarin hij meeloopt, zodat hij de juiste rechten krijgt. Telt hij mee, dan drukt zijn stagevergoeding het gemiddelde van die functiecategorie. Hem uitsluiten via de inrichting — een eigen functie zonder categorie — is foutgevoelig; een filter op de soort medewerker is eenduidig.

**Nabetalingen na uitdienst vallen af**, voor zowel witte als groene nabetalingen. Wat daar wordt uitbetaald — een eindafrekening, uitbetaald verlof, een bedrag uit een vaststellingsovereenkomst — zegt niets meer over het loonniveau in een functie. In een kleine groep kan één zo'n bedrag het gemiddelde flink scheeftrekken.

**Alle drie de filters werken bij het vullen van de brontabellen** (§7.3, stap 3). Een tijdvak met een soort inkomstenverhouding, aard arbeidsverhouding of soort medewerker die niet meetelt, levert geen bronregel op. In de brontabellen staat dus alleen wat meetelt.

Dat heeft twee redenen. Het **Power BI-dashboard** leest de brontabellen rechtstreeks uit (§5.9). Zou daar ook staan wat niet meetelt, dan moet het dashboard de filters zelf nabouwen, en dan ontstaat er een tweede waarheid naast de taak (hoofdstuk 10). En **één regel voor alle drie** is eenvoudiger uit te leggen dan twee filters op de ene plek en één op de andere.

De soort inkomstenverhouding en de aard blijven wél als veld op de bronregel staan, als kenmerk: welke van de toegestane codes iemand heeft. De soort medewerker leggen we **niet** vast; die voegt als kenmerk niets toe.

De keerzijde is dat een **verruiming** van een filter niet vanzelf over het verleden doorwerkt. Arbeidsverhoudingen die eerder afvielen hebben geen bronregel, en de brontabellen worden buiten het venster niet opnieuw opgebouwd. Wordt een filter later verruimd — bijvoorbeeld voor punt AN-a —, dan is een eenmalige vulling van de triggertabel nodig, zoals bij de conversie (§7.7). Datzelfde geldt voor DP2: de brontabellen bevatten geen arbeidsverhoudingen buiten deze filters (hoofdstuk 12, punt AN-g).

### 3.3 Medewerker of uitzendkracht: de indeling in brontabellen

Elke arbeidsverhouding die door de filters uit §3.2 komt, valt in één van twee populaties — *Medewerkers* of *Ter beschikking gestelde arbeidskrachten* — en daarmee in één van twee brontabellen (§5.3). In de lopende tekst noemen we die twee ook wel het bakje medewerkers en het bakje uitzendkrachten.

**De regel**

De indeling volgt de **verloningsvariant**: wordt het loon per plaatsing berekend, dan hoort het bij de uitzendkrachten; anders bij de medewerkers.

| Verloningsvariant | Wat de loonberekening doet | Brontabel |
| --- | --- | --- |
| Periodeverwerking | Eén berekening per medewerker | Bron medewerkers |
| Periodeverwerking met meerdere dienstverbanden | Een berekening per zichtbaar dienstverband | Bron medewerkers |
| Periodeverwerking met Flex | Eén berekening per medewerker; een plaatsing bestaat alleen administratief en wordt niet apart berekend | Bron medewerkers |
| Plaatsingen verwerken in periodeverloning (RHR02179, vanaf loonjaar 2027) | Het vaste periodeloon op het hoofddienstverband, plus een berekening per plaatsing op een plaatsingsdienstverband | **Beide**: bron medewerkers met het totaal, bron uitzendkrachten per plaatsing |
| Declaratieverwerking | Een berekening per declaratie, die altijd aan een plaatsing hangt | Bron uitzendkrachten |

Dat komt neer op drie zinnen. **Declaratieverwerking is altijd uitzenden** en komt nooit bij de medewerkers. **Periodeverwerking is altijd medewerker.** En wie in de periodeverloning **óók op de plaatsing wordt verloond**, staat in beide.

**Waarom niet indelen op aard arbeidsverhouding**

Een eerdere versie van dit ontwerp deelde de populaties in op de aard arbeidsverhouding uit de loonaangifte: aard 1, 18, 21, 23, 24 en 83 als eigen medewerker, aard 11, 22 en 82 als uitzendkracht. Dat volgde het begrippenkader (§3.7.2). Onderzoek ON-10 heeft die aard op AFAS Online naast de verloningsvariant gelegd, en de aard blijkt in de praktijk niet consequent te worden vastgelegd — ook niet binnen één werkgever met dezelfde cao en hetzelfde proces. Als indeling faalt de aard daardoor in twee richtingen tegelijk:

- **Echte uitzendkrachten komen bij de medewerkers.** Bij declaratieverwerking staan in hele omgevingen de uitzendkrachten op aard 1, alleen al in twee omgevingen ruim 4.700.
- **Medewerkers zonder plaatsing komen in een bakje dat niet te vullen is.** Aard 22 is vrijwel altijd sociale werkvoorziening op periodeverwerking zonder plaatsing, en aard 11 en 82 komen veel voor op periodeverwerking zonder loon per plaatsing. De brontabel voor uitzendkrachten heeft plaatsing en verkooprelatie in de sleutel, dus voor hen is er geen regel te maken.

De verloningsvariant heeft dat probleem niet. Of het loon per plaatsing wordt berekend, is een feit in de salarisverwerking en geen registratiekeuze. En het sluit aan op de randvoorwaarde die er toch al is: wie in het bakje uitzendkrachten komt, moet een plaatsing hebben waaraan het loon is toegerekend.

**De aard arbeidsverhouding blijft wel een filter** (§3.2), op de negen codes uit het begrippenkader samen. Ze bepaalt alleen niet meer in welke populatie iemand valt. Het veld staat op de brontabellen en op laag 2 (§5.3, §5.4), en blijft daarmee ook beschikbaar voor analyse in het dashboard en voor DP2, als de rapportage de verdeling uit het begrippenkader alsnog nodig heeft.

**Wat dat betekent voor bijzondere groepen**

| Groep | Waar ze landen | Toelichting |
| --- | --- | --- |
| Uitzendkrachten bij declaratieverwerking, ongeacht welke van de negen aardcodes ze hebben | Uitzendkrachten | Precies waar ze horen; het loon is per plaatsing beschikbaar |
| Sociale werkvoorziening (aard 21, 22, 23) | Medewerkers | Altijd periodeverwerking, vrijwel altijd zonder plaatsing |
| Payrolling en detacheren op gewone periodeverwerking | Medewerkers | Wel een plaatsing, maar geen loon per plaatsing. Dat is technisch het enige wat kan, en het is nu een bewuste keuze. De weg naar een vergelijking per inlener is het aanzetten van de nieuwe variant |
| Detacheerders met Plaatsingen verwerken in periodeverloning | Beide | Zie hieronder |
| Fictieve dienstbetrekkingen met soort 15, zoals musicus, deelvisser of thuiswerker | Geen van beide | Vallen af via het filter op aard arbeidsverhouding (§3.2) |

**Detacheerders: eerst eigen organisatie, daarnaast per plaatsing**

Bij uitzenden in de zuivere vorm is er geen vast eigen loon: alles hangt aan de plaatsing, en de uitzendkracht wordt vergeleken met de andere uitzendkrachten bij dezelfde inlener. Bij detacheren ligt dat anders. Een gedetacheerde heeft een vast loon bij zijn eigen werkgever, dat ook doorloopt als hij tijdelijk niet geplaatst is, en een functie in het functiehuis van die werkgever. Hij wil zich in de eerste plaats vergelijken met de collega's in zijn eigen functiecategorie; bij een opdracht is hij vaak de enige vanuit zijn werkgever.

Daarom staat een detacheerder in de nieuwe variant in **beide** bakjes:

- **Bron medewerkers bevat altijd het totaal.** De lijstbegrippen voor medewerkers leveren hun waarde per inkomstenverhouding, en de plaatsingsdienstverbanden vallen onder dezelfde inkomstenverhouding als het hoofddienstverband. Daarmee zitten het vaste loon én de projecttoeslagen van de plaatsingen in dit bedrag, met de functie van het hoofddienstverband.
- **Bron uitzendkrachten bevat per plaatsing het toegerekende deel.** Dat is het deel van het vaste loon dat de looninrichting aan de plaatsing toerekent, plus de projecttoeslag. De projecttoeslag laten we bewust niet weg: die is onderdeel van wat de gedetacheerde voor zijn werk bij die inlener ontvangt, en een vergelijking zonder dat deel zegt niets over gelijkwaardig belonen.

Een voorbeeld, met bedragen ter illustratie:

| | Bron medewerkers | Bron uitzendkrachten |
| --- | --- | --- |
| Vast periodeloon € 3.000, waarvan € 2.400 toegerekend aan plaatsing A | € 3.000 | € 2.400 |
| Projecttoeslag plaatsing A € 250 | € 250 | € 250 |
| **Totaal** | **€ 3.250** | **€ 2.650** |

**De twee bedragen worden nooit bij elkaar opgeteld.** Het bedrag in bron uitzendkrachten is een deel van het bedrag in bron medewerkers, geen bedrag ernaast. Binnen het recht op informatie gaat dat goed, omdat de twee populaties nergens samen worden genomen: elke vergelijking blijft binnen één populatie en één functiecategorie (§6.3). Voor de wettelijke rapportage ligt dat anders; daar moet DP2 voorkomen dat deze persoon twee keer meetelt (hoofdstuk 11).

**Uitgangspunt is dat de toerekening er komt.** Het cao-team levert een aanvullende looninrichting waarmee een deel van het vaste loon aan de plaatsing wordt toegerekend, met een rekencomponent die het salaris terugverdeelt naar het plaatsingsdienstverband (hoofdstuk 10). Zonder die toerekening zou het loon per plaatsing vrijwel alleen uit de projecttoeslag bestaan.

Op de stamkaart betekent dit dat dezelfde persoon twee sets cijfers kan hebben: op de stamkaart van de medewerker die van zijn eigen functiecategorie, op de stamkaart van de plaatsing die van zijn werk bij die inlener (§8.1).

**Een bewust uitlegbare regel**

Wet- en regelgeving zeggen niet hoe een gedetacheerde met een gewone arbeidsovereenkomst moet worden ingedeeld, en ook niet waar het loon bij leegloop of intern werk thuishoort. Dat is bij het ministerie aangekaart, maar duidelijkheid op korte termijn wordt niet verwacht. We kiezen daarom voor de regel die in één zin uit te leggen is en die aansluit op wat Profit werkelijk berekent. Komt er later duidelijkheid, dan is de indeling bij te sturen zonder dat het datamodel verandert (hoofdstuk 12, punt AN-d).

**Wie waarover gaat: recht op informatie en rapportage**

Het begrippenkader noemt bij uitzendarbeid de toevoeging dat die **alleen bij de inlener** moet worden meegenomen en niet bij de uitlener (§3.7.2). Dat gaat over de **rapportage**, niet over de brontabel.

Dat onderscheid is belangrijk, want het bepaalt wie waarover gaat:

- De **uitlener** heeft de loongegevens van zijn uitzendkrachten wél — ze staan in zijn eigen salarisverwerking — en heeft ze nodig om die uitzendkrachten hun **recht op informatie** te kunnen geven. Zijn brontabel voor uitzendkrachten wordt dus gewoon gevuld.
- De **rapportage** over uitzendkrachten ligt bij de **inlener**. Het begrippenkader is daar expliciet over: de uitlener rapporteert alleen over zijn eigen werknemers en over de uitzendkrachten die hij zélf heeft ingeleend, niet over degenen die hij uitleent (§3.7.13). De inlener doet dat op basis van gegevens die de uitlener aanlevert; die komen in de brontabel *Loontransparantie bron extern* terecht en horen bij DP2.

De beperking uit het begrippenkader passen we dus pas toe bij het samenstellen van de rapportageregels, en niet bij het vullen van de brontabel.

### 3.4 Aanvullende selectiecriteria

Het begrippenkader stelt bij dezelfde selectie nog twee eisen: het loon moet groter dan nul zijn en het aantal verloonde uren moet groter dan nul zijn. We nemen die over. Een arbeidsverhouding zonder loon of zonder verloonde uren levert geen zinvol loonniveau op en zou de gemiddelden in de vergelijkingsgroep vertekenen.

We passen deze eisen toe op het venster als geheel, niet per tijdvak. Een medewerker die één tijdvak zonder uren had maar de rest van het jaar wel, telt dus gewoon mee.

### 3.5 Wanneer we het filter toepassen

De twee filters uit §3.2 werken op een ander niveau dan de twee eisen hierboven.

**Soort inkomstenverhouding, aard arbeidsverhouding en soort medewerker toetsen we per tijdvak.** Een medewerker kan er binnen het venster van wisselen — bijvoorbeeld van een stage met salaris naar een dienstverband als personeelslid. Alleen de tijdvakken waarin de arbeidsverhouding kwalificeert tellen mee in de bedragen en de uren.

De taak toetst alle drie bij het **vullen van de brontabellen**: een tijdvak dat niet kwalificeert levert geen bronregel op (§7.3, stap 3). Laag 2 leest daarna alleen tijdvakken die al meetellen.

Wijzigt een van de drie kenmerken met terugwerkende kracht, dan werkt dat door zodra stap 3 die tijdvakken opnieuw wegschrijft: bij een salarisgegevens-trigger op dat tijdvak, of bij een stamgegeven-trigger voor het hele venster. Kwalificeert een tijdvak dan niet meer, dan **verwijdert** stap 3 de bestaande bronregel; kwalificeert het juist wél, dan ontstaat er een nieuwe.

Dat is nauwkeuriger dan één keer toetsen op de stand aan het einde van het venster. Zouden we dat doen, dan telt bij een wisseling loon mee uit tijdvakken waarin de medewerker niet onder de regeling viel, of valt loon weg uit tijdvakken waarin dat juist wel zo was.

**Loon en uren toetsen we over het venster als geheel**, zoals hierboven beschreven. Die twee eisen gaan over de vraag of er een zinvol loonniveau te berekenen valt, en dat is een eigenschap van het totaal.

Op de regel per inkomstenverhouding leggen we de soort inkomstenverhouding en de aard arbeidsverhouding vast zoals ze aan het einde van het venster golden (§5.4). Dat zijn kenmerken voor herleidbaarheid en niet de waarden waarop is gefilterd. Wisselde iemand binnen het venster, dan kan de vastgelegde waarde dus afwijken van de waarde waarmee een deel van de tijdvakken is meegeteld.

### 3.6 Medewerkers die niet het hele jaar meetellen

Het venster van twaalf maanden loopt niet voor iedereen vol. Iemand kan halverwege in dienst zijn gekomen, uit dienst zijn gegaan of tussentijds van werkgever zijn gewisseld.

Voor het wisselen van werkgever is de oplossing al bepaald: werkgever zit in de sleutel, zodat gegevens van de ene werkgever niet worden overschreven door die van de andere.

We nemen een medewerker mee zolang er binnen het venster loon is verwerkt. Iemand die in de derde maand van het venster uit dienst ging, telt dus mee met het loon dat die persoon in het venster heeft gehad. Zo blijft de vergelijkingsgroep compleet en missen we geen collega's die een groot deel van het jaar wel meetelden.

Dit betekent dat het bruto jaarloon van zo'n medewerker lager uitvalt dan dat van iemand die het hele venster in dienst was. Juist daarom tonen we het loonverschil op het bruto uurloon; dat corrigeert vanzelf voor een korter dienstverband en voor deeltijd. Hoe we daarmee omgaan in de vergelijkingscijfers werken we uit in hoofdstuk 6.

### 3.7 Medewerkers zonder functiecategorie

De functiecategorie-inrichting is de verantwoordelijkheid van de klant. Er zullen medewerkers zijn met een functie die nog niet aan een categorie is gekoppeld.

We nemen deze medewerkers gewoon op in de tabellen. Hun eigen loongegevens worden berekend en vastgelegd. Alleen de vergelijkingscijfers blijven leeg, want er is geen groep om mee te vergelijken. Op de stamkaart tonen de KPI's daardoor niets.

We signaleren dit niet aan de klant. Een functie zonder categorie valt eenvoudigweg nergens onder; het gevolg is zichtbaar doordat de medewerker geen loonverschilcijfers ziet. De klant bepaalt zelf of en wanneer hij de functiecategorie-inrichting compleet maakt. Doet hij dat, dan werkt het bij de eerstvolgende dagovergang door: een wijziging in de functiecategorie-inrichting laat alle werkgevers opnieuw doorrekenen (§7.2).

### 3.8 Medewerkers met geslacht X of zonder ingevuld geslacht

De vergelijkingscijfers zijn uitgesplitst naar man en vrouw. Het begrippenkader kent bij geslacht vier waarden — man, vrouw, X en niet ingevuld — maar rekent uitsluitend met de groep die als man is gekenmerkt en de groep die als vrouw is gekenmerkt. Medewerkers die zich als non-binair hebben laten registreren en medewerkers bij wie het geslacht niet is ingevuld vallen daarmee buiten beide groepen.

Dat is een bewuste keuze van de wetgever. De memorie van toelichting stelt dat de richtlijn is gericht op gelijk loon voor mannen en vrouwen en dat werkgevers niet hoeven te rapporteren over de loonverschillen van non-binaire personen. Het recht op informatie geldt voor hen wél: de toelichting schrijft dat een non-binaire medewerker om een vergelijking met **zowel de groep mannen als de groep vrouwen** binnen de categorie kan vragen.

Wij volgen dat zo:

- Deze medewerkers komen gewoon in de tabellen en zien hun eigen loongegevens: jaaruren, bruto jaarloon, bruto uurloon, de jaar- en uurwaarde variabele componenten en het totaal uurloon.
- De tegels *Hoeveel verdien ik per uur?*, *Gemiddeld uurloon binnen functiecategorie*, *Samenstelling functiecategorie* en *Wat is het verschil tussen mannen en vrouwen?* zijn voor hen gewoon zichtbaar. Ze krijgen daarmee ongevraagd de vergelijking met beide groepen, precies wat de toelichting als recht beschrijft. Er is dus geen keuze te maken en niets extra's aan te vragen.
- **De tegel *Verdien ik meer of minder dan mijn collega's?* is voor hen gewoon zichtbaar.** Die zet de medewerker af tegen het gemiddelde van de **hele** functiecategorie, en daar tellen zij volwaardig in mee (§6.5). Ze zien dus hetzelfde als iedereen.
- Ze komen niet voor in de donut van *Samenstelling functiecategorie*, omdat die alleen mannen en vrouwen telt (§8.2).
- Ze tellen niet mee in de gemiddelden per geslacht en niet in de loonverschilpercentages, omdat ze in geen van beide groepen vallen. Zo blijven die cijfers zuiver en sluiten ze aan op de wettelijke rapportage van DP2.
- Ze tellen wél mee in het totale aantal arbeidsverhoudingen van de functiecategorie (§5.5). Dat totaal is daardoor niet de som van mannen en vrouwen.

**We faciliteren geen keuze om als man of vrouw te worden meegeteld.** De toelichting laat toe dat iemand die zich als non-binair heeft geregistreerd zelf aangeeft in welke groep hij voor de rapportage wil meetellen, en verbiedt de werkgever om dat af te dwingen. Wij leggen die keuze niet vast: er komt geen extra veld en geen extra vraag aan de medewerker. Het geslacht in de administratie is leidend. AFAS heeft in de verdiepingssessie met het ministerie aangegeven deze constructie onwenselijk te vinden, omdat ze de medewerker dwingt zich alsnog als man of vrouw te positioneren en de werkgever extra administratie oplevert.

We tonen hierover geen aparte melding op de stamkaart. De medewerker ziet dezelfde tabel als iedereen, alleen zonder een groep waarin hij zichzelf terugvindt. Of daar tekst bij hoort is punt H3 in §12.

---

## 4 Periode en venster

### 4.1 Terugkijktermijn: een jaar

We rekenen steeds over het laatste jaar. Dat is een voortschrijdend venster, geen kalenderjaar.

De wet legt voor het recht op informatie geen vaste referentieperiode vast. Voor de wettelijke rapportage in DP2 ligt het voorgaande kalenderjaar wél vast. Door hier voor een voortschrijdend jaar te kiezen, krijgt de medewerker een actueel beeld in plaats van cijfers die tot anderhalf jaar oud kunnen zijn.

**We tellen in tijdvakken en niet in maanden.** Het venster loopt van het laatste geaccordeerde tijdvak zoveel tijdvakken terug als er bij de periodetabel in een jaar gaan (§4.3). Voor een maandverloner kómt dat neer op de laatste twaalf maanden; voor een weekverloner op tweeënvijftig weken en voor een kwartaalverloner op vier kwartalen. In de lopende tekst van dit document staat vaak *twaalf maanden* omdat dat het meest voorkomende geval is; bedoeld is steeds het venster van één jaar in tijdvakken van de eigen periodetabel.

### 4.2 Eindpunt: de laatste geaccordeerde salarisverwerking

Het venster eindigt bij het laatste tijdvak waarvoor de werkgever de salarisverwerking heeft **geaccordeerd**. Vanaf dat punt tellen we een jaar aan tijdvakken terug; hoeveel dat er zijn hangt af van de periodetabel (§4.3).

Dat moment is bewust gekozen. De brontabellen bevatten precies de tijdvakken waarvoor is geaccordeerd (§7.1), dus het venster reikt nooit verder dan de gegevens. Accorderen is bovendien de laatste stap waarin de berekende salarisgegevens definitief worden; daarna verandert er aan dat tijdvak niets meer tenzij het wordt teruggedraaid.

**Dit herziet de eerdere keuze voor het klaarzetten van de loonaangifte.** Die keuze hoorde bij een ontwerp dat de bedragen uit de loonaangifte haalde. Nu de bedragen uit de berekende salarisgegevens komen (§5.3), zou wachten op het klaarzetten betekenen dat de medewerker cijfers ziet die achterlopen op wat er al is verwerkt — en dat een uitzendkracht helemaal niets ziet, want zijn gegevens staan niet op plaatsingniveau in de aangifte.

We gebruiken bewust niet het tijdvak waarop een correctie betrekking heeft. Een correctie kan over de jaargrens gaan en raakt vaak maar een kleine groep medewerkers. Corrigeert een werkgever periode 12 van 2025 terwijl periode 3 van 2026 al is geaccordeerd, dan blijft periode 3 van 2026 het eindpunt. De correctie telt wel mee in de bedragen, maar verschuift het venster niet.

Het eindpunt geldt per werkgever. Werkgevers binnen dezelfde omgeving kunnen dus op verschillende perioden staan.

### 4.3 Het venster per periodetabel

De brontabel legt de gegevens per **loontijdvak** vast, en de **periodetabel** van de werkgever bepaalt hoe lang zo'n tijdvak is. Profit kent acht periodetabellen en we ondersteunen ze alle acht:

| Periodetabel | Venster | Aantal tijdvakken |
| --- | --- | --- |
| Jaar | Het laatste jaar | 1 |
| Halfjaar | De laatste twee halfjaren | 2 |
| Kwartaal | De laatste vier kwartalen | 4 |
| Maand | De laatste twaalf maanden | 12 |
| Halve maand | De laatste vierentwintig halve maanden | 24 |
| Vier weken | De laatste dertien perioden | 13, of 14 met een restperiode |
| Twee weken | De laatste zesentwintig perioden | 26, of 27 met een restperiode |
| Week | De laatste tweeënvijftig weken | 52, of 53 in een jaar met een 53e week |

**Dit herziet de beperking tot maand, vier weken en week.** Die beperking hoorde bij een ontwerp dat de gegevens per **aangiftetijdvak** vastlegde. De loonaangifte kent maar drie tijdvakindelingen, dus meer hoefden we niet te ondersteunen. Nu we per loontijdvak vastleggen, volgt het tijdvak de periodetabel van de salarisverwerking en kunnen alle acht indelingen in de brontabel terechtkomen. Een werkgever met kwartaalverloning zou dan een lege sectie zien terwijl zijn gegevens er wél staan.

Er is bovendien geen reden meer om ze uit te sluiten. Het venster is voor elke indeling hetzelfde principe — tel terug tot je ongeveer een jaar hebt — en het enige wat per tabel verschilt is het aantal tijdvakken uit de kolom hierboven. Dat is één tabel in de taak en geen aparte omrekenregel per indeling.

**Dertien perioden is geen aparte periodetabel.** Dat is het aantal tijdvakken dat de vierwekentabel per jaar oplevert. In eerdere versies van dit document stond het als aparte indeling; dat was onjuist.

**Bij weekverloning groeperen we niets meer.** Een eerdere versie hergroepeerde de weken naar perioden van vier weken, zodat een weekverloner dezelfde periodestructuur kreeg als een vierwekenverloner. Dat is niet meer nodig: het loontijdvak ís de week, en het venster is simpelweg de laatste tweeënvijftig weken. Hergroeperen zou nu juist een bewerking toevoegen die de herleidbaarheid naar de onderliggende salarisverwerking verstoort.

**De 53e week.** Een jaar telt niet altijd 52 weken. Bij weekverloning levert dat een 53e tijdvak op en beslaat het venster 53 weken in plaats van 52. Bij de vier- en tweewekentabel vangt Profit het op met een restperiode aan het einde van het jaar; het veld Week53Processing op de periodetabel bepaalt hoe die wordt verwerkt. Valt zo'n restperiode binnen het venster, dan telt hij mee als extra tijdvak: veertien in plaats van dertien, of zevenentwintig in plaats van zesentwintig.

Dat is bewust. Zouden we altijd het vaste aantal terugtellen, dan mist een weekverloner in zo'n jaar precies één week loon terwijl de uren wel zijn verantwoord. Het bruto uurloon blijft dan kloppen, maar het bruto jaarloon valt te laag uit — en dat is het bedrag dat in het document *Loontransparantie medewerker* en in het dashboard terugkomt.

Elk venster beslaat daarmee ongeveer een jaar, waardoor de uitkomsten tussen werkgevers met verschillende periodetabellen vergelijkbaar blijven. De periodetabel leggen we vast op de **bronregel** (§5.3), zodat per tijdvak herleidbaar is hoe lang het was. Op de regel per inkomstenverhouding staat hij niet; wat daar over het venster te zeggen valt, staat in de begin- en einddatum en het aantal toegekende tijdvakken (§5.4).

**Een jaarverloner is een randgeval.** Bij de jaartabel bestaat het venster uit één tijdvak. De berekening werkt gewoon — jaaruren, bruto jaarloon en bruto uurloon komen uit dat ene tijdvak — maar er valt niets te verdelen als iemand binnen het jaar van functie wisselt: het hele bedrag gaat naar de functie op de laatste dag van dat tijdvak (§4.5). Dat is de consequentie van de gekozen toekenning en geen apart geval.

**Meerdere periodetabellen bij één werkgever.** Een werkgever kan maandbetaalden en weekbetaalden naast elkaar hebben. Het laatste geaccordeerde tijdvak wordt dan per periodetabel bepaald, en dus ook het venster. Twee medewerkers bij dezelfde werkgever kunnen daardoor een venster hebben dat op een andere datum eindigt. Wat dat betekent voor de rapportageperiode staat in §5.2.

### 4.4 De jaargrens

Een venster van twaalf maanden loopt bijna altijd over twee kalenderjaren. Voor de berekening maakt dat niets uit. De brontabellen leggen de bedragen per loontijdvak vast; de taak leest de tijdvakken van beide jaren en telt ze op.

De bedragen komen uit lijstbegrippen (§5.3), en lijstbegrippen worden per kalenderjaar ingericht. Dat zou een jaargrensprobleem kunnen opleveren: wijzigt de inrichting tussen twee jaren, dan tellen we bedragen op die niet hetzelfde betekenen.

**Dat probleem is met de eigen sets niet meer uitgesloten.** Eerder was het argument dat AFAS de begrippen meelevert en de klant ze niet kan aanpassen, dus dat de definitie in elk jaar dezelfde is. Sinds beide sets openstaan voor eigen intellingen (§5.3) geldt dat niet meer: een klant kan in jaar twee een component toevoegen die in jaar één niet meetelde, en dan telt het venster over de jaargrens bedragen op die niet precies hetzelfde betekenen.

**We rekenen dat niet glad, en dat is aanvaard.** Het gaat om een aanvulling en niet om een andere grondslag: de klant voegt componenten toe die inhoudelijk al bij het loon horen maar in de standaarddefinitie niet op de juiste plek landden. Het effect is dat het venster in de tijdvakken ná de wijziging iets vollediger is dan daarvoor — vergelijkbaar met een klant die zijn looninrichting aanpast. Wie de cijfers over de jaargrens tot op de cent wil kunnen verklaren, moet weten of er aan de inrichting is gesleuteld; dat hoort bij de help.

Wijzigt **AFAS** de meegeleverde definitie zelf — bijvoorbeeld omdat een loonaangifterubriek wijzigt — dan is dat een bewuste, gedocumenteerde wijziging die voor alle klanten tegelijk geldt en die bij de eerstvolgende run over het hele venster doorwerkt.

### 4.5 De functie per loontijdvak

De loonrekening in Profit is niet per functie opgebouwd, maar per inkomstenverhouding. Voor dit ontwerp moeten we toch bepalen bij welke functie het loon hoort.

**We bepalen de functie per loontijdvak, op de laatste dag van dat tijdvak**, en leggen hem meteen op de bronregel vast (§5.3). Het loon over dat hele tijdvak wordt aan die functie toegekend. Wisselt iemand halverwege een tijdvak van functie, dan verdelen we het loon binnen dat tijdvak niet naar rato; het gaat volledig naar de functie waarin de medewerker het tijdvak afsloot.

**Hoe grof die toekenning uitvalt, hangt af van de periodetabel.** Bij weekverloning gaat het om hooguit een week loon die bij de verkeerde functie landt; bij jaarverloning om een heel jaar. Een fijnere verdeling zou vragen dat we binnen een tijdvak naar rato gaan rekenen, en dan is het bedrag niet meer terug te voeren op één verwerkte salarisregel. Uitlegbaarheid weegt hier zwaarder (uitgangspunt 3).

Bij een **uitzendkracht** komt de functie niet van het dienstverband maar van de **plaatsing** (§5.3). Dat is de functie die hij bij de inlener uitoefent, en dus de functie waarmee hij moet worden vergeleken.

**We kijken alleen naar de functie van het dienstverband; formatieverdeling telt niet mee.** Een klant kan een dienstverband via formatieverdeling over meerdere functies verdelen. Die regels laten we buiten beschouwing: de functie op de bronregel is altijd die van het dienstverband zelf.

Dat is een bewuste keuze. Formatieverdeling is bedoeld voor kostentoerekening en niet voor beloning. De werkwijze die AFAS adviseert is dat een medewerker die in twee functies werkt met verschillende salarissen daarvoor twee dienstverbanden heeft; is het salaris gelijk, dan gaat het puur om een kostenverdeling en verandert er aan het loonniveau niets. Zouden we de verdeling wél volgen, dan vallen er meerdere functies onder één inkomstenverhouding en is niet te bepalen welk deel van het loon bij welke functie hoort — laat staan dat zo'n verdeelde arbeidsverhouding nog te vergelijken is met een collega die zijn uren niet verdeelt.

Een klant kan hier in zijn inrichting van afwijken. Doet hij dat, dan valt de hele arbeidsverhouding in de functiecategorie van de functie op het dienstverband, en ziet hij de verdeling niet terug in de loontransparantiecijfers.

Wisselt iemand binnen het venster van functie, dan worden de tijdvakken daarmee over twee of meer functies verdeeld. Laag 2 groepeert op die functie en schrijft per functie een eigen regel, met alleen de bedragen en uren van de tijdvakken die aan die functie zijn toegekend (§5.4). Het loon telt dus niet dubbel: het wordt verdeeld, niet gekopieerd.

**Dit herziet de eerdere keuze om de functie ultimo venster te bepalen.** Die keuze schoof het loon uit de oude functie mee naar de nieuwe functiecategorie. Bij een promotie of een overstap naar een heel ander vak vertekent dat precies de categorie waarover het loonverschil wordt berekend: het lagere loon uit de oude functie drukt het gemiddelde van de nieuwe categorie, terwijl de oude categorie een deelnemer mist die er wel degelijk loon heeft verdiend. Met de toekenning per tijdvak landt elk bedrag in de categorie waarin het is verdiend.

De prijs is dat een arbeidsverhouding binnen één venster in twee functiecategorieën kan vallen. Die regels tellen elk als volwaardige arbeidsverhouding mee in de vergelijkingscijfers (§6.3), met een bruto jaarloon over een deel van het venster. Wat dat betekent voor de gemiddelden staat in §6.8; welke regel de medewerker op de stamkaart ziet, staat in §8.5.

De functiecategorie hoort bij de functie. We nemen daarvoor de koppeling zoals die op de laatste dag van de rapportageperiode geldt, zodat een herindeling van functiecategorieën meteen over de hele periode doorwerkt en niet leidt tot regels die deels in de oude en deels in de nieuwe indeling vallen.

**Bij een uitzendkracht komt de functiecategorie van de plaatsing.** Binnen Flex kan daar een andere categorie worden vastgelegd dan die bij de functie hoort. Twee plaatsingen in dezelfde functie kunnen daardoor in verschillende functiecategorieën vallen, ook bij dezelfde inlener. De functie bepaalt dus niet altijd de categorie, en laag 2 groepeert daarom op functie **én** functiecategorie (§5.4).

De overige kenmerken die binnen het venster kunnen wijzigen — geslacht, soort inkomstenverhouding en aard arbeidsverhouding — blijven een momentopname op het einde van de rapportageperiode (§5.4).

---

## 5 Gegevensmodel: Recht op informatie

### 5.1 Opzet in vier lagen

Het model bestaat uit vier lagen. De onderste drie zijn elk een verdichting van de laag eronder; de bovenste laag legt vast **waarover** is gerekend.

| Laag | Wat erin staat | Niveau uit ON-09 | Waarvoor |
| --- | --- | --- | --- |
| 0. Loontransparantie rapportage | Per rapportage-eenheid de afbakening waarover een complete set cijfers is berekend | N5 | Onderscheid tussen het venster en een afgesloten kalenderjaar |
| 1. De brontabellen loontransparantie | Per werkgever, medewerker, dienstverband en loontijdvak de verwerkte loongegevens, gescheiden naar medewerkers, uitzendkrachten en extern aangeleverde gegevens | N1 | Herleidbaarheid, dashboardanalyses en het opnieuw samenstellen van de lagen erboven |
| 2. Loontransparantie per inkomstenverhouding | Per rapportageperiode, inkomstenverhouding, functie en functiecategorie de waarden over de tijdvakken die aan die functie zijn toegekend | N2 | De eigen waarden van de medewerker op de stamkaart |
| 3. Loontransparantie per functiecategorie | Per rapportageperiode en functiecategorie de gemiddelden, de aantallen en de loonverschilpercentages, met mannen en vrouwen naast elkaar | N3 en N4 | De vergelijkingscijfers en de KPI's op de stamkaart |

De kolom **Niveau uit ON-09** legt de koppeling met het onderzoek naar het begrippenkader. Op één punt wijken we daar bewust van af: ON-09 adviseert het groepsaggregaat (N3) te berekenen en niet op te slaan. Wij slaan het wél op, omdat de KPI anders bij elke pagina-opening over de hele functiecategorie moet optellen en omdat DP2 een bevroren stand nodig heeft. Dat volgt uitgangspunt 1: voorberekenen boven live rekenen. Het stamgegeven arbeidsjaareenheid uit fase 2 is niveau N0.

**Waarom er een vierde laag boven zit.** Het verschil tussen dit ontwerp en de wettelijke rapportage van DP2 is geen verschil in gegevens, maar in afbakening: hetzelfde bruto jaarloon van dezelfde arbeidsverhouding, één keer gemeten over een voortschrijdend venster en één keer over een kalenderjaar. Zetten we het venster vast in de tabelstructuur, dan past die tweede afbakening er niet naast en heeft DP2 een eigen model nodig. Door de rapportageperiode een gegeven te maken in plaats van een aanname, is één model genoeg.

In dit ontwerp — fase 1 — bestaat er per rapportage-eenheid precies één rapportageperiode, met soort **Recht op informatie**. In fase 2 komen daar regels met soort **Rapportage** bij. Dat vraagt geen nieuwe tabellen en geen sleutelwijziging, alleen extra regels en extra velden. Per veld is hieronder aangegeven in welke fase het wordt gevuld.

We slaan de brongegevens per loontijdvak op en niet alleen het venstertotaal. De reden is dat verdichting informatie weggooit die we niet kunnen terughalen: uit een gemiddelde is geen nieuw gemiddelde af te leiden zonder rekenfouten, en een andere doorsnede is dan niet meer te maken. Het dashboard moet juist de vragen achter een KPI kunnen beantwoorden, zoals of een verschil samenhangt met dienstjaren, of het in bepaalde perioden piekt en wat er gebeurde na een functiewijziging. Dat kan alleen met gegevens per tijdvak.

Laag 1 bestaat uit **drie tabellen** en niet uit één: een tabel voor eigen medewerkers, een voor uitzendkrachten en een voor geanonimiseerde gegevens van een uitlener. Uitzendkrachten vragen extra sleutelvelden die een gewone medewerker niet heeft, en de twee populaties worden ook in de rapportage gescheiden gehouden. De onderbouwing staat in §5.3.

De tabel per functiecategorie ligt er bovenop voor performance en voor de uitlegbaarheid. De KPI leest daaruit één regel per functiecategorie en rekent zelf niets uit. Zonder die laag zou elke pagina-opening over de hele functiecategorie moeten optellen.

### 5.2 Laag 0: Loontransparantie rapportage

De tabel **Loontransparantie rapportage** legt vast waarover een complete set cijfers is berekend. Eén regel is één **rapportageperiode**: één afbakening voor één rapportage-eenheid. De lagen 2 en 3 hangen eraan; laag 1 niet, want dat zijn feiten en geen perspectief.

In dit document gebruiken we *Loontransparantie rapportage* als tabelnaam en *rapportageperiode* als begrip voor één regel, net als bij de lagen erboven.

**Primaire sleutel: Rapportage ID**

De tabel heeft één sleutelveld: **Rapportage ID**, een technisch volgnummer zonder betekenis. De lagen 2 en 3 verwijzen daarnaar.

Dat is een bewuste keuze voor een surrogaatsleutel. De natuurlijke sleutel bestaat uit vijf velden, waarvan er twee leeg kunnen zijn. Die in elke onderliggende laag herhalen zou de sleutel van laag 2 fors verbreden en van elke koppeling een samengestelde join op deels lege velden maken. Met één verwijzing blijft dat overzichtelijk, en een latere uitbreiding van de natuurlijke sleutel raakt de lagen erboven niet.

**Unieke sleutel**

Daarnaast leggen we een unieke sleutel op vijf velden, zodat er nooit twee rapportageperioden voor hetzelfde geval kunnen ontstaan:

| Onderdeel | Fase 1 | Fase 2 |
| --- | --- | --- |
| RSIN | De eerste negen posities van het loonheffingsnummer; altijd gevuld | Idem |
| Werkgever | Altijd leeg; het veld blijft behouden voor mogelijk later gebruik | Idem |
| Soort rapportage | Altijd Recht op informatie | Ook Rapportage |
| Jaar | Altijd leeg | Leeg bij Recht op informatie, een jaartal bij Rapportage |
| Volgnummer | Altijd 1 | Loopt op bij een correctie na vaststelling |

**Het RSIN alleen bakent de rapportage-eenheid af**: de groep waarbinnen wordt vergeleken. Eén regel gaat over alle werkgevers met dat nummer samen. Waarom Werkgever daarbij leeg blijft staat hieronder.

Dit vervangt de eerdere opzet met een sleutelonderdeel *Soort rapportage-eenheid* naast een veld *Rapportage-eenheid*, waarin de betekenis van de waarde afhing van het soort. Twee gescheiden velden zijn eenvoudiger te lezen en te filteren: wie op RSIN wil selecteren hoeft niet eerst het soort te controleren, en er staat nooit een werkgeverscode in een veld dat RSIN heet.

**Soort rapportage**

Soort rapportage is een codetabel met twee waarden:

| Waarde | Betekenis |
| --- | --- |
| Recht op informatie | Het voortschrijdende venster van dit ontwerp (§4.1) |
| Rapportage | Een afgesloten kalenderjaar voor de wettelijke rapportage (DP2) |

In fase 1 bestaat er per rapportage-eenheid precies één rapportageperiode, met soort **Recht op informatie**. In fase 2 komen daar regels met soort **Rapportage** bij.

**Dit herziet de keuze om de soort uit het jaartal af te leiden.** Een eerdere versie kende geen soortveld en gebruikte rapportagejaar **0** als aanduiding voor het venster; elk ander getal stond voor een kalenderjaar. Dat werkte, maar het maakte de betekenis afhankelijk van een magische waarde. Wie de tabel leest zonder dit document erbij ziet een jaartal 0 en moet raden wat dat betekent, en elke query en elk filter moet die conventie kennen. Met een expliciet soort staat er wat het is.

Het soort zit **in de unieke sleutel** en niet alleen op de regel. Daarmee is de uniciteit niet afhankelijk van de afspraak dat het jaar leeg blijft bij een venster: ook als beide soorten ooit hetzelfde jaartal zouden voeren, blijven ze uit elkaar.

Het **veld Jaar blijft leeg bij Recht op informatie**. Een voortschrijdend venster hoort bij geen enkel kalenderjaar; het loopt er bijna altijd doorheen (§4.4). Een 0 invullen zou suggereren dat er wél een jaar is.

In de tekst blijven we spreken van **vensterregels** en **kalenderjaarregels**. Dat zijn leesbegrippen, afgeleid uit de soort rapportage, en geen apart opgeslagen gegeven.

**De rapportage-eenheid: het RSIN uit het loonheffingsnummer**

De wettelijke rapportage gaat per RSIN, en dat is ook het niveau waarop wij vergelijken (§6.3). Het **recht op informatie** kent de grens van honderd werknemers niet: het geldt voor elke medewerker, bij elke werkgever, ongeacht organisatiegrootte. We moeten het RSIN dus voor iedere werkgever kunnen bepalen, uit een gegeven dat er altijd is.

**Het veld Fiscaal nummer op de organisatie kan dat niet.** Profit bewaakt dat veld met een **integriteitsregel**: hetzelfde fiscale nummer mag bij maar één organisatie voorkomen. Die regel kunnen we niet wijzigen. Hangt een concern met één RSIN in Profit onder meerdere organisaties, dan is het nummer bij hooguit één daarvan in te vullen en blijft het bij de rest leeg. Juist de gevallen die we willen samenvoegen zijn dus de gevallen waarin het veld niet overal gevuld kán zijn. Als groeperingssleutel is het daarmee onbruikbaar.

**We leiden het RSIN daarom af uit het loonheffingsnummer.** De eerste negen posities daarvan zijn het fiscale nummer; bij een rechtspersoon is dat het RSIN. Het subnummer achter de L laten we weg. Het loonheffingsnummer ligt vast per **werkgever en periodetabel** en is altijd gevuld zodra er wordt verloond.

**We bepalen het per werkgever én periodetabel, en niet per werkgever.** Dat is nodig vanwege de derde inrichting hieronder:

| Inrichting | Wat we aantreffen | Rapportage-eenheid |
| --- | --- | --- |
| 1. Eén werkgever met per periodetabel een eigen subnummer (L01, L02, L03) | Drie loonheffingsnummers met dezelfde eerste negen posities | Eén |
| 2. Twee werkgevers met hetzelfde RSIN, administratief gesplitst op periodetabel | Twee werkgevers, met loonheffingsnummers die dezelfde eerste negen posities voeren | Eén; de twee werkgevers vallen samen |
| 3. Eén werkgever met twee loonheffingsnummers waarvan het RSIN verschilt | Twee verschillende eerste negen posities binnen dezelfde werkgever | Twee; de werkgever valt uiteen |

De eerste twee inrichtingen vragen dat we **breder** kijken dan de werkgever, de derde dat we **fijner** kijken. Alleen de combinatie van werkgever en periodetabel beantwoordt beide. Die combinatie staat ook op de bronregel (§5.3), dus elke bronregel is eenduidig aan één rapportage-eenheid toe te wijzen.

**Het veld Werkgever blijft leeg.** Per RSIN kunnen meerdere werkgevers voorkomen die juist één rapportage-eenheid moeten vormen (inrichting 2); een werkgeverscode zou die eenheid weer uit elkaar trekken. We behouden het veld wel, voor het geval het later van waarde blijkt, en het blijft in de unieke sleutel staan zodat die sleutel niet wijzigt als het ooit wél wordt gevuld.

**Het RSIN is daarmee altijd gevuld.** De eerdere terugval op de werkgeverscode vervalt: er is geen geval meer waarin we geen RSIN kunnen bepalen. Is er geen loonheffingsnummer, dan is er ook niet verloond en bestaan er geen bronregels; de taak slaat die combinatie van werkgever en periodetabel dan over (§7.3). De klant hoeft hiervoor niets aan te passen: aan de inrichting die er voor de loonaangifte toch al moet zijn, verandert niets.

**Bij een eenmanszaak staat er een BSN in het veld RSIN.** De eerste negen posities van het loonheffingsnummer zijn daar niet het RSIN maar het **burgerservicenummer** van de ondernemer, en die twee zijn niet van elkaar te onderscheiden: beide zijn negencijferige nummers met dezelfde elfproef. Dat was eerder precies de reden om het loonheffingsnummer níét te gebruiken (hoofdstuk 12, punt J3), om drie bezwaren:

- Een BSN mag alleen worden verwerkt waar dat wettelijk is voorgeschreven. De loonaangifte is zo'n grondslag; een groeperingssleutel in een loontransparantietabel is dat niet.
- Het veld staat in laag 0 en laag 3, en die zijn ontsloten via weergaven, gegevensverzamelingen en Power BI (§9.2). Een BSN in een veld dat RSIN heet wordt daar door niemand als BSN herkend en dus nergens afgeschermd.
- In fase 2 is dit veld de sleutel van de aanlevering aan het monitoringsorgaan. De memorie van toelichting merkt het BSN expliciet aan als identificerend nummer dat niet openbaar wordt gemaakt, ook niet van iemand met een eenmanszaak.

**Die bezwaren staan nog overeind, maar er is geen alternatief.** De integriteitsregel sluit het Fiscaal nummer uit, en zonder groeperingssleutel is er geen vergelijkingsgroep en dus geen recht op informatie. **Dat gevolg aanvaarden we, zonder beperkende maatregel.** Het RSIN blijft gewoon beschikbaar in de gegevensverzamelingen (§5.9) en waar van toepassing op het scherm. Het veld afschermen zou de herkomst van een vergelijkingsgroep onnavolgbaar maken, terwijl het nummer in de loonadministratie toch al in beeld is.

**Subheffingsnummers vallen vanzelf samen.** Een RSIN kan meerdere loonheffingsnummers hebben die alleen in het subnummer achter de L verschillen — inrichting 1 hierboven. Omdat we alleen de eerste negen posities gebruiken, komen die op hetzelfde RSIN uit. Dat volgt het begrippenkader, dat voorschrijft dat subheffingsnummers met het hoofdheffingsnummer worden samengevoegd.

**Een wijzigend loonheffingsnummer verplaatst de werkgever.** We leggen het nummer zelf niet vast; de taak leidt het RSIN bij elke run opnieuw af uit de actuele inrichting (§5.3). Wijzigt dat nummer, dan valt de werkgever bij de eerstvolgende run onder een andere rapportage-eenheid. De oude rapportageperiode blijft dan leeg achter; we ruimen hem niet op (§5.8). Dat geval is zeldzaam genoeg om er geen routine voor te bouwen.

In fase 2 is dit veld de sleutel van de aanlevering aan het monitoringsorgaan. De bepaling blijft dan dezelfde; DP2 werkt uit wat dat voor de aanlevering betekent (§5.7).

**Velden**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Rapportage ID | Getal | 1 | Primaire sleutel. Technisch volgnummer zonder betekenis; laag 2 en 3 verwijzen hiernaar. |
| RSIN | Tekst | 1 | Onderdeel van de unieke sleutel. De eerste negen posities van het loonheffingsnummer van de werkgever en periodetabel. Altijd gevuld. |
| Werkgever | Verwijzing | 1 | Onderdeel van de unieke sleutel. **Altijd leeg**; behouden voor mogelijk later gebruik. Eén rapportage-eenheid kan meerdere werkgevers bevatten, dus een werkgeverscode zou die eenheid uit elkaar trekken. |
| Soort rapportage | Code | 1 | Onderdeel van de unieke sleutel. Codetabel met Recht op informatie en Rapportage. In fase 1 altijd Recht op informatie. |
| Jaar | Getal | 1 | Onderdeel van de unieke sleutel. Het kalenderjaar waarover is gerapporteerd. Leeg bij soort Recht op informatie. |
| Volgnummer | Getal | 1 | Onderdeel van de unieke sleutel. Altijd 1; loopt in fase 2 op bij een correctie na vaststelling. |
| Aantal arbeidsverhoudingen totaal | Getal | 1 | Alle regels per inkomstenverhouding in deze rapportageperiode, ook die zonder functiecategorie. Groter dan of gelijk aan de som van de totalen op laag 3 (§6.7). |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze rapportageperiode voor het laatst heeft samengesteld. |
| Aantal medewerkers in fte | Getal | 2 | De som van de jaaruren gedeeld door de arbeidsjaareenheid (§6.7). Bepaalt of en hoe vaak de werkgever rapportageplichtig is. |

**Er staat geen begin- en einddatum op deze laag.** Die stonden er eerder wel, als indicatie van het bereik waarover is gerekend. Ze vervallen om twee redenen.

Ze zijn niet betrouwbaar te bepalen. Een werkgever kan meerdere periodetabellen naast elkaar hebben (§4.3), en het venster eindigt dan per periodetabel op een andere datum. Eén begindatum en één einddatum op deze laag kunnen dus per definitie niet voor alle onderliggende regels kloppen; bij een rapportage-eenheid met meerdere werkgevers wordt dat nog schever.

En ze voegen niets toe. De exacte grenzen staan al op de regel per inkomstenverhouding (§5.4), per arbeidsverhouding en dus altijd juist. Wie wil weten waarover is gerekend, leest ze daar.

**Er staat ook geen status op deze laag.** Het veld *Status rapportageperiode* — in bewerking, vastgesteld, ingediend, gecorrigeerd — stond eerder als fase 2-veld in het model. Dat schrappen we hier. Welke statussen de wettelijke rapportage nodig heeft en welke overgangen daarbij horen, is in dit deelproject niet te overzien; dat komt in DP2 aan de orde. Een statusveld nu al vastleggen zou een keuze maken die we niet kunnen onderbouwen en die DP2 waarschijnlijk toch zou herzien.

Wie een kalenderjaar heeft vastgesteld en wanneer, leggen we niet in eigen velden vast. Daarvoor gebruiken we de standaard loggingvelden.

Deze laag levert drie dingen op die het model anders niet heeft: een vensterstand en een jaarstand die naast elkaar bestaan, historie doordat elk gerapporteerd jaar een eigen rapportageperiode is, en versiebeheer op de plek waar het hoort. Ook het opschonen wordt er eenvoudiger van: een rapportageperiode verwijderen is de hele set verwijderen.

### 5.3 Laag 1: de brontabellen loontransparantie

Laag 1 bestaat uit **drie eigen brontabellen**: één voor eigen medewerkers, één voor uitzendkrachten en één voor geanonimiseerde gegevens van een uitlener. Ze leggen alle drie per loontijdvak vast wat er aan loon en uren is verwerkt, en ze vormen samen de feitenlaag van het model.

De rapportageperiode zit **niet** in de sleutel van deze tabellen. Deze laag bevat feiten, geen perspectief. Zowel de vensterstand als een latere jaarstand leest dezelfde regels.

**Waarom eigen tabellen en niet de bestaande tabel Loonaangifte uren per medewerker**

Een eerdere versie van dit ontwerp gebruikte de bestaande tabel `AfasHrTaxHoursPerEmployee`, uitgebreid met zeven loonaangifterubrieken. Dat werkt voor eigen medewerkers, maar niet voor uitzendkrachten.

Het recht op informatie van een uitzendkracht moet worden **gefilterd op één verkooprelatie**: de inlener bij wie hij werkt. De loonaangifte kent die afbakening niet — die bevat alleen het totaal aan loongegevens over alle plaatsingen heen. Binnen één verkooprelatie kan een uitzendkracht bovendien meerdere plaatsingen hebben, in verschillende functies en dus in verschillende functiecategorieën. Uit de loonaangifte is niet af te leiden welk deel van het loon bij welke plaatsing hoort.

Daarmee valt de loonaangifte als bron af en moeten de bedragen uit de **berekende salarisgegevens** komen. Die zijn wél per dienstverband en per plaatsing beschikbaar.

**Waarom drie tabellen en niet één**

Uitzendkrachten vragen extra sleutelvelden die een gewone medewerker niet heeft. Die in één tabel opnemen maakt het datamodel onnodig complex voor verreweg de grootste groep, terwijl de twee populaties in de rapportage toch al fysiek gescheiden zijn: er is geen inzicht nodig dat over de combinatie van beide bronnen gaat, en ook in het dashboard blijven ze uit elkaar. Laag 3 draagt het sleutelonderdeel populatie al mee (§5.5), dus de scheiding loopt door tot boven in het model.

**Welke berekening in welke tabel komt**

De indeling volgt de verloningsvariant (§3.3). Bij het vullen kijkt de taak naar de berekende salarisgegevens zelf:

- **Hangt de berekening aan een plaatsing**, dan gaat ze naar *Loontransparantie bron uitzendkrachten*, met één regel per plaatsing. Dat geldt voor declaratieverwerking en voor de plaatsingsdienstverbanden van *Plaatsingen verwerken in periodeverloning*.
- **Is het een periodeverwerking**, dan gaat ze naar *Loontransparantie bron medewerkers*. Dat geldt ook voor een periodeverwerking waarin plaatsingen alleen administratief zijn vastgelegd, en voor het hoofddienstverband van *Plaatsingen verwerken in periodeverloning*.

Bij die laatste variant komt dezelfde inkomstenverhouding dus in **beide** tabellen. In bron medewerkers staat het **totaal**: de lijstbegrippen voor medewerkers leveren hun waarde per inkomstenverhouding, en de plaatsingsdienstverbanden vallen onder dezelfde inkomstenverhouding als het hoofddienstverband. Het vaste loon en de projecttoeslagen zitten daar dus allebei in. In bron uitzendkrachten staat per plaatsing het deel dat daaraan is toegerekend, inclusief de projecttoeslag van die plaatsing. Dat deel zit al in het totaal, en de twee tabellen mogen daarom **nooit bij elkaar worden opgeteld** (§3.3).

Een declaratieverwerking komt nooit in bron medewerkers, en een periodeverwerking zonder loon per plaatsing nooit in bron uitzendkrachten.

**Filters bij het vullen.** Alleen tijdvakken die voldoen aan de filters op soort inkomstenverhouding, aard arbeidsverhouding en soort medewerker leveren een bronregel op (§3.2). Wat in de brontabellen staat, telt dus mee; het dashboard hoeft niets na te filteren. De soort medewerker zelf staat niet in de tabellen.

**Loontransparantie bron medewerkers**

**Sleutel:** werkgever, periodetabel, jaar, periode, medewerker en volgnummer dienstverband. De bedragen komen per **inkomstenverhouding** uit de lijstbegrippen; het volgnummer is dat van het dienstverband waarop de inkomstenverhouding is vastgelegd.

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Werkgever | Verwijzing | 1 | Sleutelonderdeel. De werkgever die de salarisverwerking heeft geaccordeerd. |
| Periodetabel | Verwijzing | 1 | Sleutelonderdeel. Eén van de acht periodetabellen (§4.3). Bepaalt hoe lang het tijdvak is en hoeveel tijdvakken er in een venster gaan. |
| Jaar | Getal | 1 | Sleutelonderdeel. Het kalenderjaar waarin het tijdvak valt. |
| Periode | Getal | 1 | Sleutelonderdeel. Het volgnummer van het tijdvak binnen het jaar. |
| Medewerker | Verwijzing | 1 | Sleutelonderdeel. |
| Volgnummer dienstverband | Getal | 1 | Sleutelonderdeel. Per inkomstenverhouding en tijdvak is er precies één regel. Bij subdienstverbanden staat hier het kapstokdienstverband, bij Plaatsingen verwerken in periodeverloning het hoofddienstverband (§3.1). |
| Nummer inkomstenverhouding | Getal | 1 | De rekeneenheid voor laag 2 en 3. Per nummer en tijdvak één regel, omdat de lijstbegrippen per inkomstenverhouding leveren (§3.1). |
| Soort inkomstenverhouding | Code | 1 | Kenmerk. Het filter is bij het vullen al toegepast, dus alleen 11, 13, 15 of 17 komen voor (§3.2, §3.5). |
| Aard arbeidsverhouding | Code | 1 | Kenmerk. Het filter is bij het vullen al toegepast, dus alleen de negen codes uit het begrippenkader komen voor (§3.2, §3.5). Bepaalt niet de populatie (§3.3). |
| Functie | Verwijzing | 1 | De functie zoals die gold op de laatste dag van dit tijdvak (§4.5). Leeg als er geen functie was gekoppeld. |
| Functiecategorie | Verwijzing | 1 | De categorie waarin die functie valt. Leeg als de functie niet gekoppeld is (§3.7). |
| Geslacht | Code | 1 | Nodig voor de uitsplitsing in de vergelijkingscijfers (§3.8). |
| Verloonde uren | Aantal | 1 | De noemer van het uurloon. |
| Loon LB/PH | Bedrag | 1 | LnLbPh: het totale loon loonbelasting/premie volksverzekeringen, **inclusief** het deel onder bijzonder tarief (§6.2). |
| Loon LB/PH bijzonder tarief | Bedrag | 1 | LnTabBB: het deel van dat loon dat tegen bijzonder tarief is belast. Een **deelverzameling** van het veld hierboven en geen bedrag ernaast (§6.2). |
| Vakantiebijslag | Bedrag | 1 | De uitbetaalde vakantiebijslag; gaat er in de formule af (§6.1). |
| Opgebouwd recht vakantiebijslag | Bedrag | 1 | Het opgebouwde recht; gaat er in de formule bij. |
| Waarde niet in geld uitgekeerd loon | Bedrag | 1 | Telt mee in de waarde variabele componenten. |
| Opname arbeidsvoorwaardenbedrag | Bedrag | 1 | Gaat er in de formule af. |
| Opbouw arbeidsvoorwaardenbedrag | Bedrag | 1 | Gaat er in de formule bij. |
| Langdurige ziekte | Bedrag | 1 | Verklarend bedrag, zie hieronder. Duidt een loonverschil door langdurige ziekte. |
| Onbetaald verlof | Bedrag | 1 | Verklarend bedrag. Onderscheiden van ouderverlof en van het kopen of verkopen van uren. |
| Ouderverlof | Bedrag | 1 | Verklarend bedrag. Overkoepelend voor (aanvullend) geboorteverlof en voor betaald en onbetaald ouderschapsverlof. |
| Kopen van uren | Bedrag | 1 | Verklarend bedrag. Kan een salarisverlaging verklaren; de waarde volgt uit uren maal uurloon. |
| Verkopen van uren | Bedrag | 1 | Verklarend bedrag. Kan juist een inkomstenverhoging verklaren. |
| Inhouding i.v.m. uitruil | Bedrag | 1 | Verklarend bedrag. Bruto inhouding tegenover een onbelaste uitbetaling, zoals keuzemodel of 30%-regeling. |
| Incidentele uitkering | Bedrag | 1 | Verklarend bedrag. Neutrale categorie voor onder meer bonus, winstuitkering, gratificatie en jubileumuitkering. |
| Bijtelling vervoermiddel | Bedrag | 1 | Verklarend bedrag. Auto, motor of fiets van de zaak. |
| Vrije rubriek | Bedrag | 1 | Verklarend bedrag. De klant geeft er een eigen invulling en omschrijving aan. |

**Het loon staat er één keer als totaal en één keer als deel.** *Loon LB/PH* is het hele bedrag; *Loon LB/PH bijzonder tarief* is daarvan het stuk dat tegen bijzonder tarief is belast. Het bijzondere bedrag zit dus in beide velden. Dat is geen dubbele opslag die we kunnen vermijden, maar het gevolg van de bron: hetzelfde lijstbegrip levert zonder filter het totaal en met een filter op het tarief het bijzondere deel. Een begrip dat alleen het **normale** tarief oplevert bestaat niet (§6.2).

Dat betekent ook dat de twee velden **niet bij elkaar mogen worden opgeteld**. Wie dat doet telt het bijzondere tarief twee keer mee in het loon, en de formule in §6.1 haalt het er maar één keer uit.

De bedragen staan **per inkomstenverhouding** op de regel. De lijstbegrippen voor medewerkers leveren hun waarde per inkomstenverhouding, dus per inkomstenverhouding en tijdvak is er precies één regel. Het volgnummer dienstverband in de sleutel is dat van het dienstverband waarop de inkomstenverhouding is vastgelegd.

Effectief is elk dienstverband een eigen inkomstenverhouding. De uitzondering zijn **subdienstverbanden**, vooral in het onderwijs: die vallen samen met hun kapstokdienstverband onder één inkomstenverhouding, en de loonaangifte wordt op het kapstokdienstverband gedaan, inclusief de loongegevens eronder. Doordat we de lijstbegrippen per inkomstenverhouding ophalen, zijn de subdienstverbanden **al in de brontabel gegroepeerd**: er is één regel, met het kapstokdienstverband in de sleutel en de bedragen en uren van de hele groep. Voor de kenmerken — en dus voor de functie — volgt de regel het kapstokdienstverband (§3.1). Hetzelfde mechanisme neemt bij Plaatsingen verwerken in periodeverloning de plaatsingsdienstverbanden mee in het totaal (§3.3).

**De functie staat wél in deze laag.** Dat is anders dan in de opzet op de loonaangifte, waar de functie geen onderdeel van de bron was en laag 2 hem uit de functiehistorie moest afleiden. Nu we per salarisperiode wegschrijven, leggen we de functie meteen vast zoals die op de laatste dag van dat tijdvak gold (§4.5), samen met de functiecategorie waarin die functie valt. Dat scheelt een afleiding bij elke run en maakt achteraf navolgbaar aan welke functie een bedrag is toegekend.

**De stamgegevens op een bronregel zijn geen bevroren momentopname.** Naast de verwerkte bedragen staan hier de functie, de functiecategorie, het geslacht, de soort en de aard van de inkomstenverhouding — en bij een uitzendkracht de plaatsing en de verkooprelatie. Die kunnen wijzigen zonder dat er aan een bedrag wordt gerekend. Gebeurt dat, dan schrijft de taak de bronregels van **alle tijdvakken binnen het venster** opnieuw weg, zodat de hele vensterperiode op dezelfde indeling staat (§7.3). Buiten het venster houdt een bronregel de waarde die er stond toen hij voor het laatst is weggeschreven.

**Loontransparantie bron uitzendkrachten**

**Sleutel:** werkgever, periodetabel, jaar, periode, medewerker, volgnummer dienstverband en **plaatsing**.

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Werkgever | Verwijzing | 1 | Sleutelonderdeel. De uitlener die verloont. |
| Periodetabel | Verwijzing | 1 | Sleutelonderdeel. |
| Jaar | Getal | 1 | Sleutelonderdeel. |
| Periode | Getal | 1 | Sleutelonderdeel. |
| Medewerker | Verwijzing | 1 | Sleutelonderdeel. |
| Volgnummer dienstverband | Getal | 1 | Sleutelonderdeel. |
| Plaatsing | Verwijzing | 1 | Sleutelonderdeel, extra ten opzichte van de tabel voor medewerkers. Eén dienstverband kan binnen hetzelfde tijdvak meerdere plaatsingen hebben. |
| Nummer inkomstenverhouding | Getal | 1 | De rekeneenheid voor laag 2 en 3. |
| Soort inkomstenverhouding | Code | 1 | Kenmerk; net als bij eigen medewerkers komen alleen 11, 13, 15 of 17 voor (§3.2). |
| Aard arbeidsverhouding | Code | 1 | Kenmerk; hetzelfde filter als bij medewerkers is bij het vullen al toegepast (§3.2). Bepaalt niet de populatie: bij declaratieverwerking komt in de praktijk ook aard 1 voor (§3.3). |
| Verkooprelatie | Verwijzing | 1 | De inlener die bij deze plaatsing hoort. Het kenmerk waarop het recht op informatie wordt afgebakend. |
| Functie | Verwijzing | 1 | De functie **uit de plaatsing**, niet van het dienstverband. |
| Functiecategorie | Verwijzing | 1 | De categorie **uit de plaatsing**. Kan afwijken van de categorie die bij de functie hoort, dus twee plaatsingen in dezelfde functie kunnen in verschillende categorieën vallen (§4.5). |
| Geslacht | Code | 1 | Nodig voor de uitsplitsing in de vergelijkingscijfers. |
| Verloonde uren | Aantal | 1 | Per plaatsing. |
| Brutoloon | Bedrag | 1 | De looncomponenten onder het reguliere belastingtarief, per plaatsing. **Niet** hetzelfde als LnLbPh bij een medewerker: het deel onder bijzonder tarief zit er niet in (§6.2). Ook **niet** gelijk aan het bruto jaarloon op laag 2: de twee reserveringen komen er in §6.1 nog bij. |
| Brutoloon bijzonder tarief | Bedrag | 1 | De looncomponenten onder het tarief bijzondere beloningen, per plaatsing. Vormt de grondslag voor de variabele componenten (§6.1). |
| Vakantiebijslag | Bedrag | 1 | De uitbetaalde vakantiebijslag, per plaatsing. Valt onder bijzonder tarief en gaat er bij de variabele componenten af. |
| Opgebouwd recht vakantiebijslag | Bedrag | 1 | Per plaatsing. In het kader uitzendkrachten de *reservering vakantiegeld*; telt mee in het bruto jaarloon. |
| Opname arbeidsvoorwaardenbedrag | Bedrag | 1 | Per plaatsing. Valt onder bijzonder tarief en gaat er bij de variabele componenten af. |
| Opbouw arbeidsvoorwaardenbedrag | Bedrag | 1 | Per plaatsing. In het kader uitzendkrachten de *reservering arbeidsvoorwaardenbedrag*; telt mee in het bruto jaarloon. |
| Langdurige ziekte | Bedrag | 1 | Verklarend bedrag, per plaatsing. Zelfde lijstbegrip als bij medewerkers, zie hieronder. |
| Onbetaald verlof | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Ouderverlof | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Kopen van uren | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Verkopen van uren | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Inhouding i.v.m. uitruil | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Incidentele uitkering | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Bijtelling vervoermiddel | Bedrag | 1 | Verklarend bedrag, per plaatsing. |
| Vrije rubriek | Bedrag | 1 | Verklarend bedrag, per plaatsing. |

De **plaatsing** is het extra sleutelveld. Eén dienstverband kan binnen hetzelfde tijdvak meerdere plaatsingen hebben, en het loon wordt per plaatsing vastgelegd. De **verkooprelatie** is de inlener die bij die plaatsing hoort en is het kenmerk waarop het recht op informatie wordt afgebakend. De **functie komt uit de plaatsing** en niet van het dienstverband: de uitzendkracht werkt bij de inlener in de functie die op de plaatsing staat, en dat is de functie waarmee hij moet worden vergeleken.

**Deze tabel kent geen waarde niet in geld uitgekeerd loon.** Dat is bewust. Dat bedrag wordt op arbeidsvoorwaardenniveau berekend en is niet naar een plaatsing te herleiden. Wat dat betekent voor de berekening van de variabele componenten staat in §6.1.

**De twee loonvelden heten hier anders dan bij medewerkers, omdat ze iets anders betekenen.** Bij een eigen medewerker staat in *Loon LB/PH* het hele loon LB/PH en is *Loon LB/PH bijzonder tarief* daarvan een deelverzameling — één lijstbegrip, met en zonder een filter op het tarief. Bij een uitzendkracht komen de twee bedragen uit **twee losse lijstbegrippen**, overlappen ze elkaar niet en vormen ze samen géén loon LB/PH: onbelaste componenten en componenten onder nultarief zitten in geen van beide, en het werknemersdeel pensioen en de bijtelling vervoermiddel zijn eruit gelaten omdat ze niet aan één inlener zijn toe te rekenen (hoofdstuk 12, punt W1).

De toevoeging *LB/PH* verwijst naar een rubriek uit de loonaangifte, en dat is precies wat deze bedragen niet zijn — de loonaangifte kent de plaatsing niet. Daarom heten ze hier **Brutoloon** en **Brutoloon bijzonder tarief**, in de termen van het kader uitzendkrachten. Dezelfde naam voeren als bij medewerkers zou suggereren dat beide populaties hetzelfde gegeven vastleggen, en juist bij deze twee velden is dat niet zo.

**Het veld Brutoloon is niet het volledige brutoloon.** Het bevat de looncomponenten onder het reguliere tarief; het **bruto jaarloon** op laag 2 is dat bedrag plús de reservering vakantiegeld en de reservering arbeidsvoorwaardenbedrag (§6.1). Wie die twee overslaat omdat het veld al *Brutoloon* heet, komt te laag uit. Welke lijstbegrippen de bedragen leveren staat in §6.2.

Hetzelfde geldt voor de overige intellingen op arbeidsvoorwaardenniveau, zoals een auto van de zaak en de pensioenpremie. Ook die sluiten we uit, om dezelfde reden. Alleen intellingen die **per dienstverband** zijn berekend tellen mee.

**Het ontwerpen én het vullen van deze tabel horen bij dit deelproject.** Dat was eerder anders: de structuur lag hier vast en de vulling bij DP3. Sinds 22 september 2026 vult dit ontwerp de tabel zelf, omdat ze het **recht op informatie** van de uitzendkracht dient en dat het onderwerp van dit deelproject is. Alleen de **uitwisseling** tussen in- en uitlener blijft bij DP3 (§11).

**Verklarende bedragen**

Naast de grootheden hierboven leggen beide tabellen **negen verklarende bedragen** vast. Die dienen het Power BI-dashboard: ze maken een deel van een loonverschil zichtbaar, zodat een leidinggevende niet voor elk verschil aanvullende informatie hoeft op te vragen. Het zijn **indicaties** en geen volledige verantwoording — voor de details blijft de route naar de stamkaart of de salarisinformatie van de medewerker open.

Ze komen uit dezelfde bron en langs dezelfde route als de overige bedragen: de berekende salarisgegevens, ontsloten via lijstbegrippen.

| Lijstbegrip | Veld | Profit Id |
| --- | --- | --- |
| Loontransparantie: langdurige ziekte | Langdurige ziekte | 6.773 |
| Loontransparantie: onbetaald verlof | Onbetaald verlof | 6.774 |
| Loontransparantie: ouderverlof | Ouderverlof | 6.775 |
| Loontransparantie: kopen van uren | Kopen van uren | 6.776 |
| Loontransparantie: verkopen van uren | Verkopen van uren | 6.777 |
| Loontransparantie: inhouding i.v.m. uitruil | Inhouding i.v.m. uitruil | 6.778 |
| Loontransparantie: incidentele uitkering | Incidentele uitkering | 6.779 |
| Loontransparantie: bijtelling vervoermiddel | Bijtelling vervoermiddel | 6.780 |
| Loontransparantie: vrije rubriek | Vrije rubriek | 6.781 |

**Dit is één set voor beide populaties.** Anders dan bij de kerngrootheden hieronder gebruiken medewerkers en uitzendkrachten hier dezelfde lijstbegrippen. Ze zijn zowel per inkomstenverhouding als per plaatsing beschikbaar, dus beide brontabellen worden er langs dezelfde weg mee gevuld. Voor bron medewerkers halen we ze — net als de kerngrootheden — **per inkomstenverhouding** op, zodat ook deze bedragen van subdienstverbanden al in de bronregel zijn samengenomen.

**Drie begrippen zijn bewust gesplitst.** Onbetaald verlof, kopen van uren en verkopen van uren vielen tot nu toe onder één brede categorie incidentele inkomstenvermindering. Die is te grof: ze verklaren elk iets anders, en verkopen van uren werkt zelfs de andere kant op — dat verhoogt het inkomen in plaats van het te verlagen. **Ouderverlof** is juist samengevoegd tot één overkoepelend begrip, zodat het dashboard niet drie vrijwel gelijke rubrieken naast elkaar zet.

Zwangerschap en bevalling is als afzonderlijk begrip overwogen, maar het bestaande begrip is leeg. Dat valt daarom buiten dit ontwerp (hoofdstuk 12, punt AE-c).

**AFAS onderhoudt deze negen lijstbegrippen, maar ze staan open.** De klant kan er eigen intellingen aan toevoegen. Dat geldt voor de hele set en niet alleen voor de vrije rubriek. Het gevolg is dat de inhoud per omgeving kan verschillen — en dat is precies waarom deze bedragen **nooit** in een gemiddelde, een mediaan of een loonverschilpercentage terechtkomen. Ze verklaren de eigen situatie van één medewerker; ze zijn geen grondslag om medewerkers op te vergelijken. Wat dat voor de berekening betekent staat in §6.1 en §6.2.

**Loontransparantie bron extern krijgt ze niet.** Die tabel bevat geanonimiseerde gegevens van een uitlener en dient de rapportageverplichting van de inlener, niet het dashboard. Bovendien zou een veld waaraan de uitlener eigen intellingen heeft toegevoegd bij de inlener iets anders betekenen. Of de verklarende bedragen daar alsnog een plaats krijgen, hoort bij DP2 (hoofdstuk 12, punt AE-b).

**Loontransparantie bron extern**

In deze tabel kunnen **geanonimiseerde brongegevens worden geïmporteerd die van de uitlener afkomstig zijn**. De inlenende werkgever heeft die nodig om aan zijn eigen rapportageverplichting te voldoen: hij moet over de uitzendkrachten rapporteren die bij hem werken, maar verloont ze niet zelf.

De indeling hieronder is een **richting** en geen vastgelegd ontwerp. De sleutel is gedacht als: RSIN, periodetabel, jaar, periode, kenmerk arbeidskracht, nummer inkomstenverhouding, soort inkomstenverhouding, aard arbeidsverhouding, verkooprelatie, functiecategorie en geslacht.

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| RSIN | Tekst | 2 | Sleutelonderdeel. Het RSIN van de inlenende werkgever; er staat geen werkgeverscode in, want de gegevens komen van buiten. |
| Periodetabel | Verwijzing | 2 | Sleutelonderdeel. |
| Jaar | Getal | 2 | Sleutelonderdeel. |
| Periode | Getal | 2 | Sleutelonderdeel. |
| Kenmerk arbeidskracht | Tekst | 2 | Sleutelonderdeel. Het gepseudonimiseerde kenmerk waarmee de uitlener één arbeidskracht aanduidt. Zie de toelichting hieronder. |
| Nummer inkomstenverhouding | Getal | 2 | Sleutelonderdeel. Van de uitlener afkomstig. |
| Soort inkomstenverhouding | Code | 2 | Sleutelonderdeel en populatiefilter. |
| Aard arbeidsverhouding | Code | 2 | Sleutelonderdeel en filter. In de eigen brontabellen bepaalt de aard sinds 13 oktober 2026 niet meer de populatie (§3.3); of dat hier ook zo is, beslist DP2. |
| Verkooprelatie | Verwijzing | 2 | Sleutelonderdeel. De inlener waarop de gegevens betrekking hebben. |
| Functiecategorie | Verwijzing | 2 | Sleutelonderdeel. De categorie die de inlener heeft doorgegeven bij de plaatsing (hoofdstuk 12, punt Q1). |
| Geslacht | Code | 2 | Sleutelonderdeel. |
| Verloonde uren | Aantal | 2 | Van de uitlener aangeleverd. De noemer van het uurloon. |
| Brutoloon | Bedrag | 2 | Van de uitlener aangeleverd. |
| Brutoloon bijzonder tarief | Bedrag | 2 | Van de uitlener aangeleverd. |
| Vakantiebijslag | Bedrag | 2 | Van de uitlener aangeleverd. |
| Opgebouwd recht vakantiebijslag | Bedrag | 2 | Van de uitlener aangeleverd. |
| Opname arbeidsvoorwaardenbedrag | Bedrag | 2 | Van de uitlener aangeleverd. |
| Opbouw arbeidsvoorwaardenbedrag | Bedrag | 2 | Van de uitlener aangeleverd. |

**De loongegevens zijn dezelfde grootheden als in de tabel voor uitzendkrachten.** Ook hier ontbreekt de waarde niet in geld uitgekeerd loon, om dezelfde reden: dat bedrag wordt op arbeidsvoorwaardenniveau berekend en is niet naar een plaatsing te herleiden. De bedragen gelden per tijdvak en per sleutelregel, zodat laag 2 ze op dezelfde manier kan optellen als bij de eigen populaties (§6.1).

**Er staat geen medewerker in**, want de gegevens zijn geanonimiseerd. De regels moeten wél per individu van elkaar te onderscheiden zijn, en daarvoor is het **kenmerk arbeidskracht** nodig.

Zonder dat veld kan dat niet. Het nummer van de inkomstenverhouding wordt per medewerker uitgegeven en begint bij elke arbeidskracht opnieuw bij één, dus twee verschillende personen bij dezelfde inlener vallen daarmee op dezelfde sleutel. De overige velden zijn groepskenmerken: twee mannen in dezelfde functiecategorie, met dezelfde soort en aard, zijn er niet uit elkaar te houden. Hun regels zouden op elkaar vallen of bij het importeren moeten worden opgeteld, en dan is er geen arbeidsverhouding meer om over te rekenen — terwijl de gemiddelden, de medianen en de tellingen juist per arbeidsverhouding gaan (§6.3, §6.6, §6.7).

Aan het kenmerk stellen we twee eisen. Het moet **niet herleidbaar** zijn tot een persoon, want dat is precies wat het anonimiseren moet voorkomen. En het moet **stabiel** zijn over de tijdvakken en over de aanleveringen heen: dezelfde arbeidskracht hoort in elk tijdvak hetzelfde kenmerk te krijgen, anders valt één arbeidsverhouding in laag 2 uiteen in losse regels per tijdvak en klopt het jaarloon niet meer. Hoe de uitlener zo'n kenmerk bepaalt en hoe het wordt uitgewisseld, hoort bij de uitwerking hieronder.

**Invulling en realisatie van deze tabel worden in DP2 uitgewerkt.** We benoemen hem hier omdat hij tot dezelfde laag hoort en het model anders onvolledig oogt; dit ontwerp legt er verder niets over vast.

**Waar de bedragen vandaan komen**

De loongegevens komen uit de **berekende salarisgegevens**, ontsloten via **lijstbegrippen**. Dat is nodig voor uitzendkrachten (zie hierboven), en we hanteren dezelfde route voor eigen medewerkers zodat er één werkwijze is en niet twee.

**De twee populaties gebruiken niet dezelfde lijstbegrippen.** Dat geldt voor de kerngrootheden hieronder; de negen verklarende bedragen zijn wél één gedeelde set (§5.3, *Verklarende bedragen*).

| Populatie | Lijstbegrippen | Status |
| --- | --- | --- |
| Medewerkers | Een **eigen** set; acht grootheden per inkomstenverhouding uit zeven begrippen | Profit Id 6.821 t/m 6.827 |
| Uitzendkrachten | Een **eigen** set; zeven grootheden per plaatsing | Profit Id 6.782 t/m 6.788 |

Voor **eigen medewerkers** gebruikten we eerst de lijstbegrippen die er al waren voor de loonaangifte. Dat werkte, maar het bond de loontransparantie aan de inrichting van de aangifte. Er komt daarom ook voor deze populatie een eigen set:

| Lijstbegrip | Veld | Profit Id |
| --- | --- | --- |
| Loontransparantie - verloonde uren | Verloonde uren | 6.821 |
| Loontransparantie - loon LB/PH | Loon LB/PH | 6.822 |
| Loontransparantie - loon LB/PH | Loon LB/PH bijzonder tarief | 6.822, alleen het deel onder bijzonder tarief |
| Loontransparantie - vakantiebijslag | Vakantiebijslag | 6.823 |
| Loontransparantie - opgebouwd recht vakantiebijslag | Opgebouwd recht vakantiebijslag | 6.824 |
| Loontransparantie - waarde niet in geld uitgekeerd loon | Waarde niet in geld uitgekeerd loon | 6.825 |
| Loontransparantie - opname arbeidsvoorwaardenbedrag | Opname arbeidsvoorwaardenbedrag | 6.826 |
| Loontransparantie - opbouw arbeidsvoorwaardenbedrag | Opbouw arbeidsvoorwaardenbedrag | 6.827 |

**Zeven begrippen voor acht grootheden.** Begrip 6.822 wordt twee keer uitgelezen: zonder filter levert het LnLbPh, het totale loon LB/PH, en met een filter op het tarief levert het LnTabBB (§6.2). Dat is dezelfde opzet als bij de loonaangifte en de reden dat de brontabel een totaal en een deelverzameling vastlegt in plaats van twee helften.

**De reden voor een eigen set is dat de klant erin moet kunnen intellen.** Een salarisadministratie kent **correctie-looncomponenten** die in de loonaangifterubriek niet op de juiste plek landen of er helemaal buiten vallen. Met de bestaande begrippen was daar niets aan te doen: die horen bij de aangifte en mogen daarvoor niet worden aangepast. Met een eigen set kan de klant die componenten alsnog laten meetellen voor de loontransparantie, zonder dat het de loonaangifte raakt.

Voor **uitzendkrachten** bestonden die lijstbegrippen niet. De loonaangifte kent de plaatsing niet, dus er was ook geen lijstbegrip dat een bedrag per plaatsing oplevert. Daar kwam bij dat de **definitie inhoudelijk afwijkt**: wat er voor een uitzendkracht in het loonbegrip hoort te zitten is niet hetzelfde als voor een eigen medewerker. Daarom is er een eigen set gemaakt, op plaatsingniveau en met een eigen definitie:

| Lijstbegrip | Veld | Profit Id |
| --- | --- | --- |
| Flex loontransparantie - verloonde uren | Verloonde uren | 6.782 |
| Flex loontransparantie - loon LB/PH | Brutoloon | 6.783 |
| Flex loontransparantie - loon LB/PH BT | Brutoloon bijzonder tarief | 6.784 |
| Flex loontransparantie - vakantiebijslag | Vakantiebijslag | 6.785 |
| Flex loontransparantie - opgebouwd recht vakantiebijslag | Opgebouwd recht vakantiebijslag | 6.786 |
| Flex loontransparantie - opname arbeidsvoorwaardenbedrag | Opname arbeidsvoorwaardenbedrag | 6.787 |
| Flex loontransparantie - opbouw arbeidsvoorwaardenbedrag | Opbouw arbeidsvoorwaardenbedrag | 6.788 |

**Het zijn er zeven en geen acht.** *Waarde niet in geld uitgekeerd loon* ontbreekt, om dezelfde reden als hierboven: dat bedrag wordt op arbeidsvoorwaardenniveau berekend en is niet naar een plaatsing te herleiden. Wat dat voor de berekening betekent staat in §6.1. Welke grootheid elk begrip levert staat in §6.2.

**Twee sets houden de looninrichting van beide populaties uit elkaar.** Dat is de reden om niet één gedeelde set te maken voor de kerngrootheden. De definities lopen nu niet door elkaar, en een wijziging aan de ene kant raakt de andere niet.

Dat de twee sets van elkaar verschillen is geen probleem, omdat de uitkomsten van medewerkers en uitzendkrachten **nooit met elkaar worden vergeleken** (§6.2). Het model houdt die scheiding vast via het sleutelonderdeel populatie op laag 3 (§5.5).

Deze set was **blokkerend voor dit ontwerp**, omdat dit deelproject de brontabel voor uitzendkrachten zelf vult (§1.4): zonder die set is de tabel niet te vullen en blijft het recht op informatie voor uitzendkrachten leeg. Met de oplevering op 29 september 2026 is die blokkade weg (hoofdstuk 12, punt W1).

**AFAS levert deze lijstbegrippen standaard mee en vult ze.** Dat geldt voor beide sets. De klant hoeft ze niet in te richten en krijgt bij oplevering dezelfde definitie als iedereen.

**Maar beide sets staan wél open voor eigen intellingen.** Dat is sinds 7 oktober 2026 juist de reden dat ze er zijn. Bij **medewerkers** kan de klant er correctie-looncomponenten aan toevoegen die in de loonaangifterubriek niet op de juiste plek landen. Bij **uitzendkrachten** gaat het om een uitwijkmogelijkheid: de looninrichting van een uitzendorganisatie laat zich niet altijd in de standaarddefinitie vangen, en zonder die ruimte zou zo'n klant met cijfers blijven zitten die hij niet kan herstellen.

Het is in beide gevallen dezelfde afweging: **volledigheid weegt zwaarder dan gegarandeerde uniformiteit**.

De keerzijde is dat de betekenis van het bruto jaarloon per omgeving kan verschillen. Dat is aanvaard om drie redenen:

- **Binnen één omgeving blijft de definitie gelijk.** Het vergelijken gebeurt binnen een rapportage-eenheid en dus binnen één omgeving (§6.3). Een intelling die de klant toevoegt, geldt daar voor iedereen tegelijk.
- **De klant vult aan, hij vervangt niet.** AFAS levert de intellingen; wat de klant toevoegt komt erbij.
- **Zonder die ruimte zijn de cijfers aantoonbaar onvolledig.** Een correctiecomponent die buiten de aangifterubriek valt, ontbreekt dan gewoon in het loon — en een te laag loon is geen betere vergelijking dan een afwijkend gedefinieerd loon.

Wat dat betekent voor de jaargrens staat in §4.4. Welke lijstbegrippen het zijn en hoe ze de formules vullen staat in §6.2.

**De negen verklarende bedragen stonden al open.** Daarmee is er nu geen lijstbegrip in dit ontwerp meer dat dichtstaat. Het onderscheid tussen de kerngrootheden en de verklarende bedragen blijft wél bestaan, alleen niet langer op dit punt: de verklarende bedragen komen in geen enkele formule voor omdat ze bedragen duiden die al in de kerngrootheden besloten liggen (§6.2), en niet omdat ze opener zouden zijn.

De tabellen worden gevuld door de taak **Bijwerken gegevens loontransparantie**, voor elk tijdvak waarvoor er een triggerregel openstaat (§7.2). Meestal is dat het accorderen van de salarisverwerking — het moment waarop de berekende gegevens definitief zijn — maar een wijziging in de indeling schrijft er ook een weg, en herbouwt dan het hele venster (§7.3). Het vullen gebeurt in beide gevallen daarna, in de eerstvolgende dagovergang.

**Wat we bewust niet vastleggen**

- **Geen berekende bedragen.** Het brutoloon en de waarde variabele componenten leggen we hier niet vast. De brontabellen bevatten alleen de verwerkte grootheden; het rekenwerk gebeurt in laag 2. Wijzigt een definitie, dan hoeft de historie niet te worden herschreven. De verklarende bedragen zijn ook zulke verwerkte grootheden en geen uitkomsten, dus ze vallen niet onder deze uitsluiting.
- **Geen loonheffingsnummer.** We leggen het nummer niet op de bronregel vast. De taak leidt er wel het RSIN uit af om de rapportage-eenheid te bepalen (§5.2), maar doet dat bij elke run opnieuw uit de actuele inrichting van de werkgever en periodetabel.
- **Geen contracturen en kalenderdagen.** Die stonden in de oude brontabel voor de WAB en hebben in dit ontwerp geen functie.
- **Geen correctie-indicatie en geen vastlegtijdstip.** Wat dat betekent voor correcties en voor het dashboard staat in §7.5.

Fase 2 vraagt op de tabel voor medewerkers geen enkele uitbreiding. De populatie volgt uit de brontabel zelf (§3.3).

### 5.4 Laag 2: Loontransparantie per inkomstenverhouding

Deze tabel bevat per rapportageperiode, per inkomstenverhouding, per functie en per functiecategorie één regel met de stand over die periode. De taak stelt die samen uit de tijdvakken in de brontabel.

**Primaire sleutel: een GUID**

De tabel heeft één sleutelveld: een **GUID**, een technische sleutel zonder betekenis.

Dat is dezelfde keuze als op laag 0 en om dezelfde reden. De natuurlijke sleutel telt zes velden, waarvan er drie leeg kunnen zijn. Eén regel aanwijzen — vanuit een weergave, een document of een logregel — gaat met één veld eenvoudiger dan met zes, en een latere uitbreiding van de natuurlijke sleutel raakt de verwijzingen niet.

We kiezen hier een **GUID** en geen oplopend volgnummer zoals op laag 0. Laag 0 telt weinig regels en die worden per rapportage-eenheid één keer aangemaakt. Deze tabel wordt bij elke run voor veel werkgevers tegelijk opnieuw opgebouwd, en runs voor verschillende rapportage-eenheden mogen naast elkaar lopen (§7.4). Een centrale teller zou dan precies het punt zijn waar die runs op elkaar staan te wachten.

**Unieke sleutel**

Daarnaast leggen we een unieke sleutel op zes velden:

| Onderdeel | Toelichting |
| --- | --- |
| Rapportage ID | De rapportageperiode waar deze regel bij hoort (§5.2) |
| Medewerker | De medewerker waarop de regel betrekking heeft |
| Nummer inkomstenverhouding | De rekeneenheid: één regel is één arbeidsverhouding (§3.1) |
| Verkooprelatie | De inlener; alleen gevuld bij populatie Ter beschikking gestelde arbeidskrachten |
| Functie | De functie waaraan de tijdvakken op deze regel zijn toegekend (§4.5) |
| Functiecategorie | De categorie waarin die tijdvakken vallen; bij een uitzendkracht niet per se de categorie die bij de functie hoort (§4.5) |

Het **Rapportage ID** is de verwijzing naar de rapportageperiode op laag 0 (§5.2). Daarmee ligt vast of deze regel bij het voortschrijdende venster hoort of bij een afgesloten kalenderjaar, zonder dat de vijf velden van de natuurlijke sleutel van laag 0 hier worden herhaald.

**Werkgever zit niet in de sleutel en staat niet op de regel.** Het inkomstenverhoudingnummer wordt per medewerker uitgegeven, dus de combinatie van medewerker en nummer is binnen één rapportageperiode al eenduidig; werkgever zou daar niets aan toevoegen. Welke werkgever erbij hoort is bovendien af te leiden: de rapportage-eenheid staat op laag 0 en de werkgever per tijdvak staat op de bronregel (§5.3). Opslaan zou betekenen dat we hetzelfde gegeven op twee plekken bijhouden.

De brontabel voor medewerkers levert al regels **per inkomstenverhouding**: subdienstverbanden onder één kapstok zijn daar samengenomen, met de kenmerken van het kapstokdienstverband (§5.3). De taak hoeft op deze laag dus geen dienstverbanden meer op te tellen; ze groepeert de tijdvakken op inkomstenverhouding, functie en functiecategorie, en bij uitzendkrachten daarnaast op verkooprelatie. Dat is inhoudelijk juist: de inkomstenverhouding is de arbeidsverhouding uit het begrippenkader en daarmee de rekeneenheid voor de gemiddelden.

**De functie zit wél in de sleutel.** Elk loontijdvak hoort bij de functie die op de laatste dag van dat tijdvak gold (§4.5) en die functie staat op de bronregel (§5.3). De taak groepeert daarop. Wisselde de arbeidsverhouding binnen de rapportageperiode van functie, dan levert dat dus meerdere regels op: per functie één, met alleen de tijdvakken die aan die functie zijn toegekend.

Het loon telt daarbij niet dubbel. Elk tijdvak wordt aan precies één functie toegekend, dus de regels verdelen de rapportageperiode; ze overlappen niet. De som van de regels van één inkomstenverhouding **binnen één populatie** is nog steeds het totaal over die periode.

Is de medewerker in een tijdvak niet aan een functie gekoppeld, dan blijft de functie op die regel leeg. Die regel bestaat dus wel, maar valt in geen enkele functiecategorie (§3.7).

**De functiecategorie zit er apart in, omdat ze niet altijd uit de functie volgt.** Bij een eigen medewerker is dat wel zo: de categorie hangt aan de functie, dus groeperen op functie levert vanzelf één categorie op en voegt dit sleutelonderdeel niets toe. Binnen **Flex** kan op de plaatsing een **afwijkende functiecategorie** worden vastgelegd (§4.5, §5.3). Heeft een uitzendkracht bij dezelfde inlener twee plaatsingen in dezelfde functie maar in verschillende functiecategorieën, dan vallen die twee plaatsingen zonder dit sleutelonderdeel op één regel samen.

Dat mag niet gebeuren, want de functiecategorie bepaalt de vergelijkingsgroep (§6.3). De twee plaatsingen horen in twee verschillende groepen thuis, en met één samengevoegde regel zou het loon van beide in de categorie van de willekeurig gekozen regel terechtkomen — dezelfde fout die de verkooprelatie tussen twee inleners voorkomt. Met de functiecategorie in de sleutel ontstaan er **twee regels per inkomstenverhouding**, elk met de tijdvakken die aan die categorie zijn toegekend. Het loon telt ook hier niet dubbel: elk tijdvak hoort bij precies één plaatsing en dus bij precies één regel.

Een functieregel en een categorieregel zijn daarmee hetzelfde soort regel: beide tellen als volwaardige arbeidsverhouding mee in hun eigen functiecategorie (§6.3).

**De verkooprelatie zit ook in de sleutel, maar is alleen voor uitzendkrachten gevuld.** Bij een eigen medewerker blijft hij leeg en verandert er niets aan de regels. Bij een uitzendkracht is hij nodig: iemand kan binnen dezelfde rapportageperiode bij twee inleners werken, en het recht op informatie wordt per verkooprelatie afgebakend (§5.3). Zonder dat sleutelonderdeel zouden die twee plaatsingen op één regel samenvallen en zou het loon van de ene inlener in de vergelijking van de andere terechtkomen.

**Eén inkomstenverhouding kan regels in beide populaties hebben.** Bij *Plaatsingen verwerken in periodeverloning* komt dezelfde inkomstenverhouding uit beide brontabellen (§5.3). Dat levert één regel met populatie *Medewerkers* op, met het totale loon en de functie van het hoofddienstverband, en per verkooprelatie en functiecategorie een regel met populatie *Ter beschikking gestelde arbeidskrachten*, met het deel dat aan die plaatsingen is toegerekend. De unieke sleutel blijft daarbij eenduidig: op de regel voor medewerkers is de verkooprelatie leeg, op de regels voor uitzendkrachten gevuld. De bedragen van de twee populaties overlappen elkaar wél, en worden daarom nooit opgeteld (§3.3).

Ten opzichte van een model zonder rapportageperiode zijn er vier sleutelonderdelen bij gekomen: het Rapportage ID, de verkooprelatie, de functie en de functiecategorie. Daarmee kan dezelfde arbeidsverhouding één of meer vensterregels hebben en later ook kalenderjaarregels.

**De periodetabel staat niet meer op deze regel.** Die stond er eerder wel, om vast te leggen hoe de rapportageperiode was bepaald. Hij vervalt om twee redenen. De periodetabel zegt iets over een tijdvak en hoort dus thuis op de bronregel (§5.3), waar hij ook sleutelonderdeel is. En hij is op deze regel niet altijd eenduidig: stapt een werkgever binnen het venster over van vier weken naar maand, dan bevat één regel tijdvakken uit twee periodetabellen en klopt één waarde per definitie niet. Wat er over de rapportageperiode te zeggen valt, staat in de begindatum, de einddatum en het aantal toegekende tijdvakken hieronder.

**Velden**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| GUID | GUID | 1 | Primaire sleutel. Technische sleutel zonder betekenis. |
| Rapportage ID | Getal | 1 | Onderdeel van de unieke sleutel. Verwijzing naar de rapportageperiode op laag 0 (§5.2). |
| Medewerker | Verwijzing | 1 | Onderdeel van de unieke sleutel. |
| Nummer inkomstenverhouding | Getal | 1 | Onderdeel van de unieke sleutel. De rekeneenheid: één regel is één arbeidsverhouding (§3.1). |
| Verkooprelatie | Verwijzing | 1 | Onderdeel van de unieke sleutel. De inlener waarvoor deze regel geldt. Alleen gevuld bij populatie Ter beschikking gestelde arbeidskrachten; bij een eigen medewerker leeg. |
| Functie | Verwijzing | 1 | Onderdeel van de unieke sleutel. De functie waaraan de tijdvakken op deze regel zijn toegekend (§4.5). Leeg als er in die tijdvakken geen functie was gekoppeld. |
| Functiecategorie | Verwijzing | 1 | Onderdeel van de unieke sleutel. De categorie waarin de tijdvakken op deze regel vallen, op de laatste dag van de rapportageperiode. Bij een eigen medewerker volgt die uit de functie; bij een uitzendkracht komt ze van de plaatsing en kan ze daarvan afwijken (§4.5). Leeg als er geen categorie is gekoppeld. |
| Geslacht | Code | 1 | Nodig voor de uitsplitsing in de vergelijkingscijfers. |
| Soort inkomstenverhouding | Code | 1 | Ultimo-waarde. Legt vast waarom een regel meetelt (11, 13, 15 of 17). |
| Aard arbeidsverhouding | Code | 1 | Ultimo-waarde. Legt vast waarom een regel meetelt (§3.2); bepaalt niet de populatie (§3.3). |
| Populatie | Code | 1 | Codetabel Populatie loontransparantie, zie hieronder. Beide waarden komen voor. |

De kenmerken onder de sleutel leggen we vast als momentopname op het einde van de rapportageperiode. De functie, de functiecategorie en de verkooprelatie horen bij de sleutel en gelden voor de tijdvakken op deze regel. Daarmee blijft de regel zelfstandig leesbaar en hoeft de KPI niet te koppelen aan andere tabellen. De keerzijde is dat een wijziging in de stamgegevens pas doorwerkt na de volgende run van de taak.

**De codetabel Populatie loontransparantie**

De populatie legt vast uit welke bron een regel is opgebouwd. Het is een codetabel met twee waarden:

| Waarde | Betekenis |
| --- | --- |
| Medewerkers | Eigen medewerkers van de werkgever, opgebouwd uit de brontabel Loontransparantie bron medewerkers (§5.3) |
| Ter beschikking gestelde arbeidskrachten | Uitzendkrachten en andere ter beschikking gestelde arbeidskrachten, opgebouwd uit de brontabellen voor uitzendkrachten en extern (§5.3) |

We nemen de wettelijke term **ter beschikking gestelde arbeidskracht** over en niet het spraakgebruik *uitzendkracht*. De regeling rekent er meer onder dan alleen uitzendarbeid — payrolling en detachering horen er ook bij — en het is de term die in de rapportage terugkomt. In de lopende tekst van dit document blijven we van uitzendkracht spreken, omdat dat leesbaarder is; in de codetabel en op het scherm staat de volledige term.

**Welke arbeidsverhoudingen in Profit onder die populatie vallen, volgt uit de verloningsvariant en niet uit de wettelijke omschrijving** (§3.3). Payrolling of detachering op een gewone periodeverwerking valt daardoor onder *Medewerkers*, omdat er geen loon per plaatsing is om mee te vergelijken.

**Beide waarden komen in de uitlevering van dit deelproject voor.** *Medewerkers* voor de eigen medewerkers van de werkgever, *Ter beschikking gestelde arbeidskrachten* voor de uitzendkrachten die hij uitleent. Dat was eerder anders: tot 22 september 2026 vulde dit ontwerp alleen de eerste populatie en zou DP3 de tweede toevoegen.

Voor de tweede populatie vult dit ontwerp alleen de regels met soort **Recht op informatie**, want dat is wat de uitlener zijn uitzendkrachten moet bieden. De **rapportageregels** over uitzendkrachten ontstaan aan inlenerzijde uit *Loontransparantie bron extern* en horen bij DP2 (§3.3). Het veld wordt hoe dan ook altijd gevuld en niet leeg gelaten, omdat het op laag 3 sleutelonderdeel is (§5.5) en de twee populaties daar altijd gescheiden blijven.

Gegevens die altijd actueel moeten zijn, leggen we hier bewust **niet** vast. Of dit het hoofddienstverband is, en de datum in en uit dienst, halen we bij het opbouwen van de KPI op uit de stamgegevens. Zouden we ze opslaan, dan zouden we ze ook moeten bijwerken zodra ze wijzigen, en dat is niet wat deze taak doet. Uit welke dienstverbanden een regel is opgebouwd, is af te leiden uit de brontabel.

Het RSIN staat niet op deze regel: dat zit in de unieke sleutel van de rapportageperiode.

**Berekende waarden**

Deze waarden gelden over de tijdvakken binnen de rapportageperiode die aan de functie en de functiecategorie op deze regel zijn toegekend. Wisselde de arbeidsverhouding niet van functie of categorie, dan is dat de volledige rapportageperiode. De taak berekent per tijdvak eerst het brutoloon en de waarde variabele componenten uit de loongegevens in de brontabel, en telt die daarna op (§6.1).

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Jaaruren | Aantal | 1 | De verloonde uren over de toegekende tijdvakken. |
| Bruto jaarloon | Bedrag | 1 | Het brutoloon over de toegekende tijdvakken. |
| Bruto uurloon | Bedrag | 1 | Bruto jaarloon gedeeld door jaaruren. |
| Jaarwaarde variabele componenten | Bedrag | 1 | Het deel van het loon dat bovenop het basisloon komt. |
| Uurwaarde variabele componenten | Bedrag | 1 | De jaarwaarde gedeeld door de jaaruren. |
| Totaal uurloon | Bedrag | 1 | Bruto uurloon plus uurwaarde variabele componenten: het volledige loon per verloond uur (§6.1). |
| Individueel loonverschil | Percentage | 1 | De eigen positie ten opzichte van het gemiddelde totaal uurloon van de hele functiecategorie, ongeacht geslacht. Bij soort rapportage *Recht op informatie* betekent een positieve uitkomst dat de medewerker **méér** verdient dan dat gemiddelde (§6.5). Wordt in een **tweede rekenslag** gevuld, omdat daarvoor een gemiddelde van laag 3 nodig is (§7.3). |
| Aantal toegekende tijdvakken | Getal | 1 | Hoeveel loontijdvakken aan deze functie en functiecategorie zijn toegekend. Maakt zichtbaar over hoeveel van de rapportageperiode deze regel gaat, ook als de periodetabel een ander aantal tijdvakken per jaar kent (§4.3). |
| Begindatum | Datum | 1 | De eerste dag van het eerste toegekende tijdvak. Legt vast vanaf wanneer is gerekend, zodat dat bij de informatie kan worden vermeld. |
| Einddatum | Datum | 1 | De laatste dag van het laatste toegekende tijdvak. |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze regel voor het laatst heeft samengesteld. |

Het aantal toegekende tijdvakken leggen we wél vast, anders dan de tellingen die eerder zijn geschrapt. Zonder dit veld is niet te zien of een regel over een deel of over het hele venster gaat, en dat is precies wat een lager bruto jaarloon verklaart. Het is ook niet uit één vast getal af te leiden, want hoeveel tijdvakken een vol venster telt verschilt per periodetabel (§4.3). De begin- en einddatum volstaan er evenmin voor, omdat een medewerker binnen één venster van functie kan wisselen en later kan terugkeren. Het is wel uit de brontabel af te leiden — de functie staat daar sinds de herziening van 15 september 2026 in — maar dan moet iedereen die de regel leest die telling zelf maken.

De kwartielverdeling, de arbeidsjaarfractie en de vastlegging of iemand variabele componenten heeft ontvangen, horen bij de wettelijke rapportage. Die werken we in DP2 uit; ze zijn af te leiden uit de velden hierboven.

**Verklarende bedragen**

Deze tabel draagt ook de negen verklarende bedragen uit §5.3. De taak telt ze op over **dezelfde toegekende tijdvakken** als de berekende waarden hierboven, dus per functieregel.

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Langdurige ziekte | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Onbetaald verlof | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Ouderverlof | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Kopen van uren | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Verkopen van uren | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Inhouding i.v.m. uitruil | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Incidentele uitkering | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Bijtelling vervoermiddel | Bedrag | 1 | Som over de toegekende tijdvakken. |
| Vrije rubriek | Bedrag | 1 | Som over de toegekende tijdvakken. |

Op deze bedragen passen we de rekenregels van §6.1 **niet** toe. Er is geen ondergrens op nul, er gaat niets vanaf en er komt geen uurwaarde naast. Alleen de afronding is gelijk: twee decimalen bij het wegschrijven. Ze staan los naast het bruto jaarloon en de variabele componenten en tellen daar niet in mee.

Ze staan hier omdat het dashboard niet de enige afnemer is. Het rapport *Loontransparantie medewerker* en de route van DP4 lezen laag 2 (§5.9) en moeten dezelfde duiding kunnen geven, zonder zelf de tijdvakken uit de brontabel op te tellen.

Welke loongegevens precies het basisloon en de variabele componenten vormen, werken we uit in hoofdstuk 6.

### 5.5 Laag 3: Loontransparantie per functiecategorie

Deze tabel bevat de uitkomsten die de KPI-tegels op de stamkaart tonen. De taak stelt hem samen uit de regels per inkomstenverhouding.

**Primaire sleutel: een GUID**

Net als laag 2 heeft deze tabel één sleutelveld: een **GUID**, een technische sleutel zonder betekenis. De afweging is dezelfde (§5.4): één veld om een regel mee aan te wijzen, en geen centrale teller waar parallel lopende runs op moeten wachten.

**Unieke sleutel**

| Onderdeel | Invulling |
| --- | --- |
| Rapportage ID | Verwijst naar de rapportageperiode. In fase 1 altijd één met soort Recht op informatie; in fase 2 ook één met soort Rapportage |
| Populatie | *Medewerkers* of *Ter beschikking gestelde arbeidskrachten*. **Niet fase-afhankelijk**; beide waarden komen vanaf de eerste uitlevering voor |
| Functiecategorie | In fase 1 altijd gevuld; in fase 2 ook leeg, voor de organisatiebrede kengetallen (§5.7) |
| Verkooprelatie | Gevuld bij populatie *Ter beschikking gestelde arbeidskrachten* **én** soort Recht op informatie; in alle andere gevallen leeg. **Niet fase-afhankelijk**; zie de toelichting hieronder |

**Velden**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| GUID | GUID | 1 | Primaire sleutel. Technische sleutel zonder betekenis. |
| Rapportage ID | Getal | 1 | Onderdeel van de unieke sleutel. Verwijzing naar de rapportageperiode op laag 0 (§5.2). |
| Populatie | Code | 1 | Onderdeel van de unieke sleutel. Codetabel Populatie loontransparantie (§5.4). Beide waarden komen voor. |
| Functiecategorie | Verwijzing | 1 | Onderdeel van de unieke sleutel. De categorie waarover deze regel gaat. In fase 2 ook leeg, voor de organisatiebrede kengetallen (§5.7). |
| Verkooprelatie | Verwijzing | 1 | Onderdeel van de unieke sleutel. De inlener waarbinnen wordt vergeleken. Zie de toelichting hieronder. |

**Toelichting op het sleutelveld Verkooprelatie.** Het **recht op informatie** wordt gegroepeerd op verkooprelatie: de vergelijkingsgroep van een ter beschikking gestelde arbeidskracht is de functiecategorie **binnen één inlener** (§5.3) en niet de functiecategorie over alle inleners heen. Zonder dat sleutelonderdeel zou het loonniveau bij de ene inlener in de vergelijking van de andere terechtkomen.

De **rapportage** wordt níét gegroepeerd op verkooprelatie. Die gaat over de rapportage-eenheid als geheel, en een inlener is daarin geen indelingskenmerk. Op een regel met soort Rapportage blijft de verkooprelatie dus leeg.

**Het veld is niet fase-afhankelijk.** Dat is een punt om vast te houden, want het ligt voor de hand om te denken dat de verkooprelatie pas in fase 2 nodig is. Het omgekeerde is waar: het recht op informatie van een ter beschikking gestelde arbeidskracht heeft soort *Recht op informatie* — fase 1 dus — en juist dáár is de verkooprelatie onmisbaar, omdat de uitlener per inlener moet kunnen vergelijken (§5.3). Op een regel met soort Rapportage blijft hij leeg, in welke fase dan ook.

Dat de verkooprelatie bij een eigen medewerker leeg blijft, komt dus niet door de fase maar door de populatie: er is dan geen inlener. Bij een uitzendkracht wordt hij vanaf de eerste uitlevering gevuld, omdat dit deelproject die populatie zelf vult (§5.4).

**Geslacht zit niet in de sleutel.** Eén functiecategorie levert precies één regel op, met de cijfers voor mannen en vrouwen naast elkaar in aparte velden.

**De rapportage-eenheid staat niet op deze regel.** Die volgt uit het Rapportage ID: laag 0 bevat het RSIN (§5.2). Een weergave of dashboard dat wil tonen om welk RSIN het gaat, koppelt daarvoor naar laag 0.

Dat is een bewuste keuze. Het RSIN hier herhalen zou het gegeven op twee plekken zetten, met het risico dat ze uiteenlopen zodra het loonheffingsnummer van een werkgever wijzigt. De verdichting gaat per functiecategorie **binnen** een rapportage-eenheid, en die eenheid is precies wat het Rapportage ID aanwijst.

Werkgever staat er om dezelfde reden **niet** als apart veld op. Eén regel gaat over alle werkgevers binnen die eenheid samen, dus er is geen werkgever die erbij hoort. Zouden we hem toch opnemen, dan valt de vergelijkingsgroep uiteen in een groep per werkgever en klopt het gemiddelde niet meer (§6.3).

Het sleutelonderdeel populatie en de **verkooprelatie** worden beide vanaf de eerste uitlevering gevuld: dit deelproject levert beide populaties op. Voor de kwartielverdeling doen we dit niet: die hoort bij de wettelijke rapportage en wordt in DP2 uitgewerkt, inclusief de sleuteluitbreiding die daarvoor nodig is.

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
| Gemiddeld totaal uurloon mannen | Bedrag | 1 | Gemiddeld bruto uurloon mannen plus gemiddelde uurwaarde variabele componenten mannen (§6.3). |
| Gemiddeld totaal uurloon vrouwen | Bedrag | 1 | Idem, voor de vrouwen. |
| Gemiddeld totaal uurloon categorie | Bedrag | 1 | Het gemiddelde van het veld Totaal uurloon over **alle** regels in de functiecategorie, ongeacht geslacht. Grondslag van het individuele loonverschil (§6.5). Het achtervoegsel is bewust *categorie* en niet *totaal*: in deze veldnaam zou dat woord twee dingen tegelijk betekenen. |
| Mediaan bruto jaarloon mannen | Bedrag | 1 | Niet af te leiden uit gemiddelden; wordt berekend uit de regels per inkomstenverhouding (§6.6). |
| Mediaan bruto jaarloon vrouwen | Bedrag | 1 | Idem. |
| Mediaan bruto uurloon mannen | Bedrag | 1 | Idem. |
| Mediaan bruto uurloon vrouwen | Bedrag | 1 | Idem. |
| Mediane jaarwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Mediane jaarwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |
| Mediane uurwaarde variabele componenten mannen | Bedrag | 1 | Idem. |
| Mediane uurwaarde variabele componenten vrouwen | Bedrag | 1 | Idem. |
| Mediaan totaal uurloon mannen | Bedrag | 1 | De mediaan van het **totaal uurloon per arbeidsverhouding**, en nadrukkelijk niet de som van twee medianen (§6.6). |
| Mediaan totaal uurloon vrouwen | Bedrag | 1 | Idem. |

Dat zijn zesentwintig velden, alle in fase 1.

**De medianen per functiecategorie gaan verder dan het begrippenkader.** Dat kent de mediaan uitsluitend op organisatieniveau: de C- en D-reeks gelden voor de hele populatie eigen werknemers. Binnen een arbeidscategorie kent het alleen gemiddelden, de G-reeks (§6.9). Een mediaan per functiecategorie komt dus nooit in de wettelijke rapportage terecht.

We leggen hem toch vast, om drie redenen. Het is een bruikbaar gegeven voor het dashboard: staat het gemiddelde ver van de mediaan, dan is de verdeling binnen die functiecategorie scheef en trekt bijvoorbeeld één hoog salaris het gemiddelde omhoog. Dat is precies de vraag achter een opvallend loonverschilpercentage. Verder is een mediaan niet achteraf uit een gemiddelde te reconstrueren, dus wie hem later wil hebben mist de tussenliggende perioden voorgoed. En de kosten zijn beperkt: de taak heeft de regels per inkomstenverhouding op dat moment toch al in handen, en het gaat om sorteren binnen één functiecategorie.

**De organisatiebrede medianen die DP2 wél moet aanleveren komen in fase 2.** Die vullen dezelfde velden op een regel met een **lege functiecategorie** (§5.7). De rekenwijze is identiek; alleen de selectie is breder. Er komt dus geen apart veld en geen aparte tabel voor.

**Er is geen mediaan van de jaaruren.** Het begrippenkader kent die niet. Het kent medianen op precies de vier maatstaven waarop ook het loonverschil wordt berekend. Van de gemiddelden zijn er daarom zes per geslacht en van de medianen vijf; het totaal uurloon is in beide reeksen een eigen uitbreiding van dit ontwerp (§6.5). Daar komt één gemiddelde bij dat niet per geslacht gaat: *Gemiddeld totaal uurloon categorie*.

**Één gemiddelde krijgt ook een categoriebrede variant.** Verder komt er van de gemiddelden en de medianen géén totaal.

De reden voor die uitzondering is het **individuele loonverschil** (§6.5). Dat zet de medewerker af tegen het gemiddelde van de hele functiecategorie, en dat getal bestaat alleen als we het vastleggen. Voor de andere maatstaven geldt de oorspronkelijke redenering nog wel: de tegels zetten de eigen waarde tegen Mannen en Vrouwen af (§8.2), de percentages rekenen mannen tegen vrouwen af (§6.5), en ook de wettelijke rapportage in DP2 zet die twee groepen tegen elkaar. Een categoriebreed gemiddelde beantwoordt daar geen vraag. Blijkt later, bijvoorbeeld in het dashboard, dat er meer totalen nodig zijn, dan is dat een veld erbij op dezelfde regel: geen sleutel- of tabelwijziging.

De reden dat het **aantal** wél een totaal krijgt, is dubbel. Het zegt hoe groot de categorie is, en het verschil met de som van mannen en vrouwen laat zien hoeveel arbeidsverhoudingen geslacht X of geen ingevuld geslacht hebben (§3.8). Hoeveel dat er zijn leggen we dus niet apart vast. Voor DP2 is dit totaal bovendien de noemer bij het aandeel ontvangers van variabele componenten en bij de kwartielverdeling.

**Het totaal is niet de som van mannen en vrouwen.** Arbeidsverhoudingen met geslacht X of zonder ingevuld geslacht tellen wel mee in het totale aantal, maar in geen van beide geslachtsgroepen. Het aantal arbeidsverhoudingen totaal is dus groter dan of gelijk aan de som van de twee.

**Velden die één keer voorkomen**

| Veld | Type | Fase | Toelichting |
| --- | --- | --- | --- |
| Loonverschil jaarloon | Percentage | 1 | Op gemiddeld bruto jaarloon. |
| Loonverschil uurloon | Percentage | 1 | Op gemiddeld bruto uurloon. |
| Loonverschil componenten jaarwaarde | Percentage | 1 | Op de gemiddelde jaarwaarde variabele componenten. |
| Loonverschil componenten uurwaarde | Percentage | 1 | Op de gemiddelde uurwaarde variabele componenten. |
| Loonverschil totaal uurloon | Percentage | 1 | Op het gemiddelde totaal uurloon. Dit is het percentage dat de medewerker op de stamkaart ziet (§8.2). |
| Mediane loonverschil jaarloon | Percentage | 1 | Op mediaan bruto jaarloon. |
| Mediane loonverschil uurloon | Percentage | 1 | Op mediaan bruto uurloon. |
| Mediane loonverschil componenten jaarwaarde | Percentage | 1 | Op de mediane jaarwaarde variabele componenten. |
| Mediane loonverschil componenten uurwaarde | Percentage | 1 | Op de mediane uurwaarde variabele componenten. |
| Mediane loonverschil totaal uurloon | Percentage | 1 | Op de mediaan totaal uurloon. |
| Datum laatste berekening | Datum en tijd | 1 | Wanneer de taak deze regel voor het laatst heeft samengesteld. |

**De richting van deze tien percentages hangt af van de soort rapportage.** Op een regel die bij een rapportageperiode met soort *Recht op informatie* hoort, telt het percentage vanuit de vrouwen: een **min** betekent dat zij gemiddeld minder verdienen dan de mannen. Op een regel met soort *Rapportage* geldt de wettelijke richting en betekent een **plus** precies hetzelfde. Alleen de volgorde van de teller verschilt; de noemer, de afrondingsregel en de regels bij een lege groep zijn gelijk (§6.5). Dat één veld twee richtingen kan hebben is een bewuste keuze met een harde randvoorwaarde: het dashboard en alle meegeleverde gegevensverzamelingen tonen uitsluitend soort Recht op informatie, zodat de twee nooit in één overzicht naast elkaar staan (§5.9).

Daarmee is het setje compleet. Het begrippenkader kent acht genderloonverschillen op organisatieniveau: vier op gemiddelden en vier op medianen. Binnen een arbeidscategorie kent het er vier, alle op gemiddelden. Wij leggen alle acht per functiecategorie vast — waarmee de vier mediane percentages een eigen uitbreiding zijn (§6.9) — en daar komen de twee percentages op het **totaal uurloon** bij, ook een eigen uitbreiding. Van die tien komt er één op de stamkaart: *Loonverschil totaal uurloon*. De andere negen zijn er voor het dashboard en voor DP2.

De 5%-signalering, de kwartielgrenzen, de onderbouwing bij een overschrijding en de status van de beoordeling horen bij de wettelijke rapportage. Die velden nemen we hier niet op; DP2 werkt ze uit.

**Waarom één regel en geen regel per geslacht.** De eerdere opzet had geslacht in de sleutel en dus drie regels per functiecategorie: mannen, vrouwen en een totaalregel. Dat leverde één tabel op met twee soorten regels die elk andere velden vulden — de gemiddelden alleen op de geslachtsregels, de loonverschilpercentages alleen op de totaalregel. Wie zo'n tabel leest, moet altijd eerst weten welk soort regel hij voor zich heeft. Dat is lastig uit te leggen aan een consultant en foutgevoelig in een weergave of dashboardquery.

Met één regel per functiecategorie verdwijnt dat onderscheid. Daar komt bij:

- **De KPI leest één regel.** Alle vier de tegels die de functiecategorie gebruiken worden uit dezelfde regel gevuld, in plaats van uit drie regels die eerst bij elkaar gezocht moeten worden.
- **Een ontbrekende groep is een leeg veld, geen ontbrekende regel.** Zijn er geen mannen in de categorie, dan blijven de mannenvelden leeg. In de oude opzet ontbrak de regel en moest elke lezer daarop voorbereid zijn. Dat maakt de afhandeling uit §8.6 eenvoudiger.
- **De verhouding is direct zichtbaar.** Het aantal mannen, het aantal vrouwen en het totale aantal staan naast elkaar op één regel en zijn dus meteen tegen elkaar te controleren.
- **Het sluit aan bij wat de rapportage vraagt.** De wettelijke rapportage vraagt steeds het aandeel of het gemiddelde van mannen náást dat van vrouwen. Ook de kwartielverdeling in DP2 vraagt per kwartiel het aandeel mannen en vrouwen; met deze opzet is dat één regel per kwartiel in plaats van twee.

De prijs is dat de tabel breed wordt en dat een derde geslachtscategorie een tabelwijziging zou vragen in plaats van een extra regel. Dat laatste risico is klein: de richtlijn schrijft de uitsplitsing naar mannen en vrouwen voor, en medewerkers met geslacht X of zonder ingevuld geslacht tellen volgens §3.8 alleen in het totale aantal mee.

**Herzien: we leggen de loonverschilpercentages wél vast.** Eerder was het argument dat een percentage aan twee regels tegelijk hangt en dus nergens thuishoort. Met één regel per functiecategorie is dat bezwaar helemaal weg: het percentage hoort bij precies deze regel. Vastleggen is bovendien consistent met uitgangspunt 1, de KPI leest en rekent niet. En het is noodzakelijk voor fase 2, want een vastgestelde rapportage moet het percentage bevatten dat destijds is verstrekt, ook als een definitie later wijzigt.

De mediaan blijft buiten de stamkaart (§6.4). We berekenen en bewaren hem wel vanaf fase 1, voor het dashboard en voor DP2. De rekenwijze staat in §6.6.

### 5.6 Bewaartermijn

De brontabellen worden **niet opgeschoond**. Regels blijven staan zolang de salarisverwerking niet wordt teruggedraaid.

Dat is ruimer dan het venster nodig heeft — voor het recht op informatie volstaan de tijdvakken van één jaar — maar het levert twee voordelen op. Er is altijd een compleet afgesloten kalenderjaar aanwezig op het moment dat DP2 dat jaar wil vaststellen, en een correctie die na de jaargrens binnenkomt kan nog worden verwerkt.

We bouwen dus bewust **geen opruimroutine**. Dat zou een parameter vragen, een geplande taak en een afweging over wat er met een lopend rapportagejaar gebeurt, terwijl de winst alleen in schijfruimte zit. De omvang is bovendien voorspelbaar: per inkomstenverhouding of plaatsing komen er per jaar zoveel regels bij als de periodetabel tijdvakken kent — twaalf bij maandverloning, drieënvijftig bij weekverloning (§4.3, §10).
De twee tabellen erboven bewaren voor de **vensterregels** geen historie. Bij elke run stelt de taak ze opnieuw samen en overschrijft de vorige waarde. Dat past bij het doel: de medewerker wil weten hoe het er nu voor staat, niet hoe het er een jaar geleden voor stond.

In fase 2 komen daar kalenderjaarregels bij. Die blijven staan zolang de bijbehorende rapportageperiode bestaat, en dat is het rapportagejaar plus vier voorgaande jaren. Dat volgt uit de verplichting om ook over de vier voorgaande jaren informatie te kunnen verstrekken.

**Let op:** de mediaan en de kwartielverdeling worden berekend uit de **regels per inkomstenverhouding**, niet uit de brontabellen. De meerjarige bewaring die de rapportage nodig heeft, geldt dus voor de twee tabellen daarboven. De brontabellen dienen voor herleidbaarheid, correctieverwerking en het dashboard.

### 5.7 Wat fase 2 toevoegt

DP2 – Rapportage moet rapporteren over een **afgesloten kalenderjaar**. Dit ontwerp werkt met een voortschrijdend venster dat eindigt bij de laatste geaccordeerde salarisverwerking. Die twee vallen niet samen, maar het zijn wel dezelfde gegevens over een andere afbakening. DP2 krijgt daarom geen eigen structuur, maar een tweede rapportageperiode op dezelfde vier lagen.

Wat fase 2 toevoegt, is daarmee overzichtelijk:

| Wijziging | Aard |
| --- | --- |
| Rapportageperioden met soort Rapportage | Extra regels op laag 0 |
| Status van de rapportage | Nieuw veld op laag 0, uit te werken in DP2 (§5.2) |
| Aantal medewerkers in fte | Extra veld op laag 0 |
| Kalenderjaarregels per arbeidsverhouding | Extra regels op laag 2 |
| Regels met lege functiecategorie: de organisatiebrede A-, B-, C- en D-reeks | Extra regels op laag 3 |
| Loontransparantie bron extern: de geïmporteerde gegevens van de uitlener | Uit te werken in DP2 (§5.3) |
| Kwartielverdeling, 5%-signalering, kwartielgrenzen, onderbouwing en aandeel ontvangers | Uit te werken in DP2, inclusief het kwartiel als extra sleutelonderdeel op laag 3 |
| Arbeidsjaareenheid: het aantal uren per fte per werkgever per jaar | Nieuw stamgegeven |
| Gegevensverzamelingen met een filter op soort Rapportage | Varianten naast de bestaande (§5.9) |
| Bewaartermijn van de kalenderjaarregels | Parameterwijziging |

Op de tabellen voor medewerkers en uitzendkrachten verandert er in fase 2 niets: die bevatten dan al alle loongegevens die de rapportage nodig heeft. Wat er wél bij komt is de derde brontabel, *Loontransparantie bron extern*, waarvan de structuur in §5.3 op hoofdlijn staat en de invulling bij DP2 ligt. De sleutel van laag 0 en laag 2 wijzigt niet; laag 3 krijgt het kwartiel erbij zodra DP2 de kwartielverdeling uitwerkt. Dat is het punt van de rapportageperiode.

Wat DP2 daarnaast hergebruikt zijn de definities, de lijstbegrippen en de rekenwijze uit hoofdstuk 6. Die moeten identiek zijn, anders leggen de KPI en de wettelijke rapportage verschillende uitkomsten naast elkaar. Voor de vulling betekent dat één rekenroutine met het periodebereik als parameter: het venster in fase 1, het kalenderjaar in fase 2. Let daarbij op de periodetabel: het venster telt een aantal loontijdvakken terug (§6.1), terwijl een kalenderjaar een datumbereik is. Dat zijn twee manieren om hetzelfde bereik af te bakenen en ze moeten in de rekenroutine naast elkaar kunnen bestaan.

Voor DP2 blijft één punt open. Het moment waarop een kalenderjaar definitief wordt ligt nog niet vast; het voorstel is na afloop van de correctietermijn op de loonaangifte, met een handmatige vaststelling door de werkgever.

De medianen en de mediane loonverschilpercentages waren eerder aan fase 2 toegewezen. Die vullen we nu al in fase 1 (§5.5), zodat het dashboard er meteen over beschikt. Dat betreft wél de medianen **per functiecategorie**; de organisatiebrede varianten die de rapportage vraagt komen in fase 2, op regels met een lege functiecategorie (§6.9).

De arbeidscategorie uit het begrippenkader is géén apart begrip: het is dezelfde groepering als de functiecategorie. In Profit hanteren we consequent de term functiecategorie. Er komt dus geen extra veld en geen extra sleutelonderdeel voor.

### 5.8 Opschonen

Een arbeidsverhouding kan uit de selectie vallen: de medewerker is uit dienst en het venster is voorbij zijn laatste loon geschoven, of de soort inkomstenverhouding is gewijzigd naar een soort die niet meetelt. Ook kan een functieregel vervallen doordat het venster is opgeschoven en er geen tijdvakken meer aan die functie zijn toegekend.

De taak verwijdert dan de betreffende regel per inkomstenverhouding. We laten geen regels staan met bevroren cijfers, want die zouden op de stamkaart een actueel beeld suggereren dat niet meer klopt. De medewerker ziet dan de melding uit §8.6 in plaats van verouderde bedragen.

Raakt een functiecategorie leeg, dan verwijdert de taak ook de bijbehorende regels uit de tabel per functiecategorie.

De brontabellen raken we hierbij niet aan. Die volgen de salarisverwerking: een tijdvak verdwijnt alleen als die verwerking wordt teruggedraaid (§7.6).

Dit opschonen raakt alleen de **vensterregels**. Kalenderjaarregels worden nooit opgeschoond op grond van de actuele situatie: die zijn een vastlegging van hoe het toen was. Ze verdwijnen alleen als de hele rapportageperiode buiten de bewaartermijn valt.

### 5.9 Gegevensverzamelingen

De tabellen zijn alleen bruikbaar als ze ook ontsloten worden. We leveren daarom vier gegevensverzamelingen mee: drie op laag 2 en één op laag 3. Die verzamelingen vormen tegelijk de **enige** route naar die twee lagen: eigen weergaven rechtstreeks op de tabellen sluiten we af (§9.2).

De drie op laag 2 zijn: **twee varianten voor presentatie**, één per populatie, die precies de regel van de actuele functie opleveren, en **één voor analyse**, die alle functieregels van beide populaties toont.

De rapportageperiode (laag 0) krijgt geen eigen gegevensverzameling. Die laag bevat geen cijfers, alleen de afbakening. De kenmerken ervan — RSIN, soort rapportage, jaar en datum laatste berekening — nemen we mee in de verzamelingen erboven, zodat altijd zichtbaar is waarover en wanneer is gerekend. Het veld Werkgever laten we weg: dat is altijd leeg (§5.2).

**De brontabellen (laag 1) krijgen geen gegevensverzameling.** Niet voor medewerkers, niet voor uitzendkrachten en niet voor *bron extern*. Deze gegevens stellen we niet binnen Profit beschikbaar: ze bevatten individuele beloningsinformatie per loontijdvak en dat is de gevoeligste laag van het model (§9.2). De enige afnemer die ze nodig heeft is het **Power BI-dashboard**, en dat leest de tabellen rechtstreeks uit.

Dat scheelt bovendien onderhoud. Een gegevensverzameling op laag 1 zou alleen door het dashboard worden gebruikt, terwijl de afscherming ervan — medewerkerautorisatie op loongegevens per tijdvak — wél voor elke Profit-gebruiker moet kloppen. Die verhouding weegt niet op tegen de winst.

**Loontransparantie per inkomstenverhouding (actuele functie)**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per inkomstenverhouding (§5.4) |
| Standaardfilter | Soort rapportage = Recht op informatie, **populatie** en de **actuele functie** van de medewerker |
| Filterautorisatie | Medewerkerautorisatie bij het lezen |
| Velden | Alle kenmerken, berekende waarden en verklarende bedragen uit §5.4, aangevuld met de kenmerken van de rapportageperiode |
| Sortering | Medewerker, inkomstenverhouding |
| Gebruik | De tegels *Hoeveel verdien ik per uur?*, *Gemiddeld uurloon binnen functiecategorie* en *Verdien ik meer of minder dan mijn collega's?* (§8.2), het pagina-onderdeel *Functie* (§8.3), het rapport Loontransparantie medewerker en de gegevensverzameling van DP4 – Vraag aan HR |

Deze verzameling kent drie standaardfilters. Ze doen elk iets anders en ze zijn geen van drieën te missen.

**Het filter op soort rapportage** doet twee dingen. Het voorkomt dubbeling, omdat in fase 2 kalenderjaarregels in dezelfde tabel komen: zonder filter zou een medewerker zijn eigen loon meerdere keren zien, één keer per rapportageperiode. En het houdt de twee **rekenrichtingen** uit elkaar — bij soort Recht op informatie tellen de loonverschilpercentages de andere kant op dan bij soort Rapportage (§6.5). DP2 levert een eigen variant met een filter op soort Rapportage.

**Elke ontsluiting toont één soort rapportage tegelijk.** Dat geldt voor de meegeleverde verzamelingen hierboven, voor elke weergave die daarop wordt gebouwd en nadrukkelijk ook voor het **Power BI-dashboard**: dat toont uitsluitend soort *Recht op informatie*. Zou een overzicht beide soorten tonen, dan zouden twee percentages met dezelfde veldnaam tegengesteld tellen, en dat is in een grafiek of een optelling niet meer te zien. De wettelijke rapportage krijgt in DP2 een eigen ontsluiting met een eigen filter; de twee komen elkaar daardoor nergens tegen.

**Het filter op de actuele functie** zorgt ervoor dat elke presentatievorm dezelfde functieregel gebruikt. Laag 2 bevat per functie een regel (§5.4), dus zonder filter zou een medewerker die van functie is gewisseld zijn loon over twee regels verdeeld zien.

Het filter vergelijkt het veld **Functie** op de regel met de functie die op het moment van opvragen geldt. Die functie staat niet op de regel: laag 2 legt de functie vast waaraan de tijdvakken zijn toegekend, en dat is per definitie een gegeven uit het verleden (§4.5). De actuele functie komt daarom uit de **stamgegevens van het dienstverband**. De verzameling koppelt daarvoor naar het dienstverband; welke vorm die koppeling krijgt — een gekoppeld veld of een berekend veld in de verzameling — hoort bij het technisch ontwerp (§12, punt AC-c).

We nemen de **actuele** functie en niet de functie op de laatste dag van het venster: het venster eindigt bij het laatste geaccordeerde tijdvak en loopt dus achter op vandaag. Vraagt de medewerker zijn gegevens op, dan hoort hij te worden vergeleken met de collega's in de functie die hij op dat moment heeft.

**Bij subdienstverbanden geldt de functie van het kapstokdienstverband.** De regel gaat over een inkomstenverhouding, terwijl de functie aan het dienstverband hangt. Hangen meerdere subdienstverbanden onder één kapstok, dan zijn er dus meerdere actuele functies bij één regel. De taak stelt de regel samen met de kenmerken van het **kapstokdienstverband** (§5.4); het filter moet diezelfde keuze volgen, anders vindt het geen regel.

Dat betekent ook dat een recente functiewijziging tot een lege uitkomst kan leiden. Is er nog geen salarisverwerking geaccordeerd waarin de nieuwe functie valt, dan bestaat er nog geen regel voor die functie. Wat de medewerker dan ziet, staat in §8.5 en §8.6.

**Het filter op populatie** houdt de twee populaties uit elkaar. Beide staan in dezelfde tabel (§5.4), en één persoon kan in beide voorkomen. Een uitzendbureau kan iemand in dienst hebben als eigen medewerker en diezelfde persoon daarnaast via declaratieverwerking ter beschikking stellen. En bij *Plaatsingen verwerken in periodeverloning* staat dezelfde inkomstenverhouding met het totaal bij de medewerkers en met het plaatsingsdeel bij de uitzendkrachten (§3.3). Zonder filter zou de stamkaart er willekeurig één van tonen.

De populatie volgt uit de **stamkaart**:

| Stamkaart | Populatie |
| --- | --- |
| Medewerker ESS en medewerker MSS | Medewerkers |
| Plaatsing | Ter beschikking gestelde arbeidskrachten |

Omdat een standaardfilter één vaste waarde kent, leveren we van deze verzameling **twee varianten** mee, één per populatie. Ze verschillen uitsluitend in die filterwaarde; basistabel, velden, autorisatie en de twee andere filters zijn identiek.

**Wat deze verzameling niet afbakent**

De verzameling levert **één regel per inkomstenverhouding**, en dat kunnen er meer zijn dan één. Een medewerker met twee inkomstenverhoudingen krijgt twee regels, en een ter beschikking gestelde arbeidskracht die bij twee inleners werkt ook, omdat de verkooprelatie in de sleutel zit (§5.4).

Dat kan zich ook **binnen één inlener** voordoen. Is iemand daar in dezelfde functie op twee plaatsingen geplaatst met een verschillende functiecategorie, dan zijn dat twee regels, omdat ook de functiecategorie in de sleutel zit (§5.4). Het filter op de actuele functie zeeft die niet uit elkaar; welke regel bij welke plaatsing hoort, volgt uit de functiecategorie van die plaatsing.

Dat is bewust. Welke van die regels op de stamkaart komt — die van het **hoofddienstverband** — wordt bepaald bij het opbouwen van de tegels, uit de stamgegevens (§5.4, §8.5). Zouden we dat in de verzameling zetten, dan zou ook het rapport *Loontransparantie medewerker* nog maar één dienstverband tonen, terwijl dat juist de route is waarlangs de medewerker bij al zijn dienstverbanden komt (§8.5).

De drie filters hierboven bakenen dus af **welke soort regel** je krijgt; ze kiezen niet welke regel wordt getoond. Wie deze verzameling in een eigen weergave of rapport gebruikt, moet daar rekening mee houden.

**Loontransparantie per inkomstenverhouding (alle functies)**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per inkomstenverhouding (§5.4) |
| Standaardfilter | Soort rapportage = Recht op informatie |
| Filterautorisatie | Medewerkerautorisatie bij het lezen |
| Velden | Gelijk aan de verzameling hierboven |
| Sortering | Medewerker, inkomstenverhouding, functie |
| Gebruik | Weergaven en analyses waarin alle functieregels binnen het venster nodig zijn, en de weergave *Functies in functiecategorie* (§8.4) |

Deze derde verzameling op laag 2 laat het filter op de functie **en** dat op de populatie weg. Ze toont dus alle functieregels binnen het venster, voor beide populaties. Juist de vergelijking tussen de regel vóór en ná een functiewijziging laat zien wat er met het loonniveau is gebeurd; met alleen de actuele functieregel is die vraag niet te beantwoorden. En wie een uitzendbureau analyseert wil de eigen medewerkers en de ter beschikking gestelde arbeidskrachten naast elkaar kunnen zetten, ook al worden ze nooit met elkaar vergeleken (§6.2).

Deze verzameling is dus voor **analyse** en niet voor presentatie. Wie één populatie wil zien, filtert daar zelf op; het veld Populatie staat op de regel.

De verzamelingen verschillen **uitsluitend** in filters. Basistabel, velden en autorisatie zijn identiek, dus er is geen tweede definitie te onderhouden en er kunnen geen twee waarheden ontstaan. De medewerkerautorisatie geldt ook hier: wie deze verzameling gebruikt ziet alleen de medewerkers waarvoor hij geautoriseerd is (§9.2).

Wie deze verzameling gebruikt moet er rekening mee houden dat één medewerker meerdere regels kan hebben. Optellen over de regels van één inkomstenverhouding geeft het totaal over het venster; middelen erover geeft een getal dat nergens op slaat, omdat de regels een verschillend aantal tijdvakken beslaan. Het veld Aantal toegekende tijdvakken (§5.4) maakt dat zichtbaar.

**Loontransparantie per functiecategorie**

| Kenmerk | Invulling |
| --- | --- |
| Basistabel | Loontransparantie per functiecategorie (§5.5) |
| Standaardfilter | Soort rapportage = Recht op informatie |
| Filterautorisatie | Niet van toepassing; de regel gaat over een groep en niet over een medewerker |
| Velden | Alle velden uit §5.5, aangevuld met de kenmerken van de rapportageperiode |
| Sortering | RSIN, functiecategorie |
| Gebruik | De tegels *Gemiddeld uurloon binnen functiecategorie*, *Samenstelling functiecategorie*, *Verdien ik meer of minder dan mijn collega's?* en *Wat is het verschil tussen mannen en vrouwen?* (§8.2) |

Medewerkerautorisatie kan hier niet: er staat geen medewerker op de regel. De afscherming loopt dus volledig via de autorisatie op de gegevensverzameling zelf. Dat is bewust, want een gemiddelde in een kleine categorie is herleidbaar tot een individuele collega (§9.3).

**Ook hier bakent het filter niet af wélke regel wordt getoond.** De tegels hebben één regel nodig: die van de functiecategorie van de medewerker, in zijn populatie en — bij een ter beschikking gestelde arbeidskracht — bij zijn inlener. Die drie waarden staan op de regel per inkomstenverhouding die de tegels toch al lezen (§5.4). Het opbouwen van de tegels zoekt daarmee de bijbehorende regel op laag 3; een vast filter kan dat niet, omdat de waarden per medewerker verschillen.

Een populatiefilter als standaardfilter heeft hier dus geen zin: de tegels zoeken toch al gericht. Voor wie deze verzameling in een eigen weergave gebruikt staan Populatie en Verkooprelatie gewoon als veld op de regel.

**Geen variant zonder autorisatie.** Een verzameling zonder medewerkerautorisatie zou handiger zijn voor wie breed wil rapporteren, maar dan is de afweging uit §9.2 te omzeilen. Een HR-medewerker die over de hele organisatie mag rapporteren, is voor al die medewerkers geautoriseerd en ziet met de gewone verzameling dus alles wat hij nodig heeft. Wie dat niet is, hoort die gegevens ook in een weergave niet te zien.

---

## 6 Berekeningen

### 6.1 Het venster en de waarden van de medewerker zelf

**Eerst het venster.** Voordat er iets te berekenen valt, moet vaststaan welke tijdvakken meetellen. Dat is de eerste stap van de taak en het is de stap waarin de **periodetabel** bepalend is. De taak doet dat per werkgever **en periodetabel**:

1. bepaal het laatste tijdvak waarvoor de salarisverwerking is geaccordeerd (§4.2);
2. zoek bij de periodetabel het aantal tijdvakken dat bij een jaar hoort (§4.3);
3. tel vanaf dat laatste tijdvak zoveel tijdvakken terug, over de jaargrens heen als dat nodig is (§4.4).

**Het aantal tijdvakken is geen vast getal.** Sinds de brongegevens per **loontijdvak** worden vastgelegd in plaats van per aangiftetijdvak, kunnen alle acht periodetabellen in de brontabel voorkomen. Een maandverloner heeft twaalf tijdvakken in zijn venster, een vierwekenverloner dertien, een weekverloner tweeënvijftig en een jaarverloner één. De taak mag dus nergens uitgaan van twaalf of dertien; ze leest het aantal uit de tabel in §4.3.

**De restperiode telt mee als extra tijdvak.** Bij de week-, twee- en vierwekentabel kan een jaar een tijdvak extra opleveren. Valt dat binnen het venster, dan telt het gewoon mee: 53 in plaats van 52, 27 in plaats van 26, 14 in plaats van 13. Daarmee is het venster nooit korter dan een jaar en mist het bruto jaarloon geen week loon (§4.3).

**Dit raakt zowel laag 2 als laag 3.** Laag 2 gebruikt het venster om te bepalen welke bronregels op de regel per inkomstenverhouding worden opgeteld. Laag 3 telt en middelt daarna over die regels (§6.3). Rekent de taak met een verkeerd aantal tijdvakken, dan werkt dat door in beide lagen: eerst in een te laag of te hoog bruto jaarloon, en daarna in het gemiddelde en het loonverschilpercentage van de hele functiecategorie.

**Binnen één functiecategorie kunnen vensters verschillen.** Twee medewerkers in dezelfde categorie kunnen een andere periodetabel hebben, en dan eindigt hun venster op een andere datum en beslaat het een ander aantal tijdvakken. We rekenen dat niet glad. Elk venster beslaat ongeveer een jaar, dus de bedragen blijven onderling vergelijkbaar; het bruto uurloon — de grondslag van de KPI's (§6.5) — is er helemaal ongevoelig voor, omdat het loon en uren tegen elkaar afzet.

**Dan de waarden.** De loongegevens staan **per loontijdvak** in de brontabel. De taak berekent daaruit per tijdvak het brutoloon en de waarde variabele componenten, groepeert de tijdvakken op de functie die erbij hoort (§4.5), en telt daarna per functie op tot de waarden op de regel per inkomstenverhouding:

| Waarde | Formule medewerkers | Formule uitzendkrachten |
| --- | --- | --- |
| Jaaruren | Som van AantVerlU | Som van AantVerlU |
| Bruto jaarloon | Som van (LnLbPh − VakBsl + OpgRchtVakBsl − OpnAvwb + OpbAvwb) − [Jaarwaarde variabele componenten] | Som van ([Brutoloon] + OpgRchtVakBsl + OpbAvwb) |
| Bruto uurloon | [Bruto jaarloon] / [Jaaruren] | [Bruto jaarloon] / [Jaaruren] |
| Jaarwaarde variabele componenten | Som van (WrdLn + LnTabBB − VakBsl − OpnAvwb) | Som van ([Brutoloon bijzonder tarief] − VakBsl − OpnAvwb) |
| Uurwaarde variabele componenten | [Jaarwaarde variabele componenten] / [Jaaruren] | [Jaarwaarde variabele componenten] / [Jaaruren] |
| Totaal uurloon | [Bruto uurloon] + [Uurwaarde variabele componenten] | [Bruto uurloon] + [Uurwaarde variabele componenten] |

**Elke afkorting in de kolom voor medewerkers is één veld in de brontabel.** LnLbPh is het veld *Loon LB/PH* en LnTabBB het veld *Loon LB/PH bijzonder tarief* (§5.3); de overige zes staan er onder hun eigen naam. Er wordt in deze formules dus nergens iets opgeteld dat de taak zelf nog moet samenstellen. Bij uitzendkrachten bestaan die afkortingen niet, dus daar staan de veldnamen tussen blokhaken.

**LnTabBB zit in LnLbPh.** Het bijzondere tarief maakt deel uit van het totaal en wordt in de formule voor het bruto jaarloon precies één keer afgetrokken, namelijk via de jaarwaarde variabele componenten. De twee velden mogen daarom **niet bij elkaar worden opgeteld** (§5.3, §6.2).

**De verklarende bedragen staan buiten deze formules.** Ze duiden bedragen die al in de grootheden hierboven besloten liggen; ze er apart bij optellen zou hetzelfde loon twee keer laten meetellen. De taak neemt ze ongewijzigd over naar de regel per inkomstenverhouding (§5.4) en rekent er verder niets mee.

**Bij uitzendkrachten wordt het bruto jaarloon opgeteld en niet afgeleid.** Dat is het grootste verschil tussen de twee kolommen, en het volgt uit de bron. Bij een eigen medewerker staat in LnLbPh het hele loon, inclusief het deel onder bijzonder tarief; het brutoloon ontstaat daar door de variabele componenten eraf te trekken. Bij een uitzendkracht bestaat dat totaalbedrag niet. Lijstbegrip 6.783 levert **uitsluitend** de looncomponenten onder het reguliere tarief, en het bijzondere deel komt uit een tweede, apart begrip (§5.3, §6.2). Het brutoloon is daar dus een optelling — de reguliere componenten plus de twee reserveringen — en niet het restant na aftrek.

Dat volgt het kader uitzendkrachten van 3 maart 2026 (hoofdstuk 12, punt W1). Zouden we de formule van de medewerkers aanhouden, dan trekt de taak een bedrag af dat er nooit bij is opgeteld, en valt het bruto jaarloon van elke uitzendkracht te laag uit — precies met de waarde van zijn variabele componenten. Dat is geen afrondingskwestie maar een systematische afwijking die bij de vergelijkingscijfers van de hele functiecategorie terechtkomt.

**Het veld Brutoloon is niet het hele brutoloon.** Ondanks de naam bevat het alleen de looncomponenten onder het reguliere tarief. Het **bruto jaarloon** is dat bedrag plús de twee reserveringen, en dat is precies wat de formule hierboven doet. Sla die twee over en het bedrag valt te laag uit.

**VakBsl en OpnAvwb staan daarom niet in de formule voor het bruto jaarloon.** Beide vallen onder het bijzondere tarief en zitten dus al in [Brutoloon bijzonder tarief]; ze gaan er bij de variabele componenten af. Ze bij het brutoloon nóg een keer aftrekken zou ze dubbel laten meetellen. Wat er wél in gaat zijn de **reserveringen**: het opgebouwde recht vakantiebijslag en de opbouw van het arbeidsvoorwaardenbedrag. Het kader schrijft dat zo voor, omdat het bedrag moet horen bij de periode waarin het is opgebouwd en niet bij de periode waarin het is uitbetaald.

**WrdLn vervalt uit de formule voor de jaarwaarde.** De waarde niet in geld uitgekeerd loon staat niet in hun brontabel, omdat dat bedrag op arbeidsvoorwaardenniveau wordt berekend en niet naar een plaatsing te herleiden is; hun set lijstbegrippen telt er daarom zeven in plaats van acht (§5.3). Dat is een bewuste onvolledigheid: liever een bedrag dat aantoonbaar bij deze inlener hoort dan een bedrag dat over alle plaatsingen heen is uitgesmeerd.

**Onbelaste componenten en componenten onder nultarief tellen bij een uitzendkracht niet mee.** Ze vallen onder geen van beide tarieven en komen dus in geen van de twee lijstbegrippen terecht. Hetzelfde geldt voor het werknemersdeel pensioen en de bijtelling vervoermiddel, die het kader expliciet uitzondert omdat ze niet aan één inlener zijn toe te rekenen.

De optellingen gebeuren op de bedragen per tijdvak, niet op de uurwaarden. Het bruto uurloon over het venster is dus het opgetelde jaarloon gedeeld door de opgetelde uren, en nadrukkelijk niet het gemiddelde van de losse periode-uurlonen. Dat laatste zou een tijdvak met weinig uren even zwaar laten wegen als een volle periode, en het zou bij weekverloning over tweeënvijftig getallen middelen en bij maandverloning over twaalf.

Bij medewerkers zijn de dienstverbanden onder dezelfde inkomstenverhouding — de kapstok met zijn subdienstverbanden — al in de bronregel samengenomen (§5.3). De taak telt daarom alleen de tijdvakken op die aan dezelfde functie zijn toegekend. Zo staat op elke regel per inkomstenverhouding het volledige loon van die arbeidsverhouding over de tijdvakken waarin de medewerker die functie had.

Deze opbouw volgt het begrippenkader loontransparantie. Daarin is het brutoloon gedefinieerd als het loon verminderd met de waarde variabele componenten, met als toelichting dat dit in de Europese richtlijn het loonniveau of basisloon heet. Het bruto jaarloon is dus het basisloon; de variabele componenten staan er los naast en zijn er niet in begrepen. Het begrippenkader spreekt voluit van "aanvullende of variabele componenten"; in dit ontwerp korten we dat af tot **variabele componenten**, zodat de veldnamen en de schermteksten werkbaar blijven.

Het kader uitzendkrachten komt op dezelfde verhouding uit langs een andere weg: daar is het brutoloon rechtstreeks gedefinieerd en vormen brutoloon en variabele componenten samen het totale loon. De **betekenis** van de twee grootheden is in beide populaties gelijk; alleen de manier waarop ze uit de bron ontstaan verschilt.

De rekenvolgorde wijkt af van de leesvolgorde hierboven. Bij **medewerkers** bepaalt de taak eerst de uren, dan de waarde variabele componenten, en pas daarna het brutoloon, omdat die waarde daarvan wordt afgetrokken. Bij **uitzendkrachten** staan die twee los van elkaar en mogen ze in willekeurige volgorde worden bepaald. De twee uurwaarden volgen in beide gevallen daarna en het totaal uurloon als laatste; die drie berekenen we alleen op de regel per inkomstenverhouding, niet per tijdvak.

**Het totaal uurloon telt twee al afgeronde bedragen op.** Beide componenten staan op dat moment al op twee decimalen, dus de optelling is exact en er komt geen nieuwe afrondingsstap bij. Dat is precies de reden om dit veld als optelling vast te leggen en niet apart uit het jaarloon te herleiden: zo komt het getal op het scherm altijd overeen met de twee getallen waaruit het is opgebouwd (§8.2).

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

We passen geen deeltijdcorrectie toe op het bruto jaarloon. Het bruto uurloon vangt het deeltijdeffect vanzelf op. Het jaarloon laat zien wat iemand feitelijk heeft verdiend en blijft daarom vastgelegd, maar het is niet de maat waarin we het loonniveau uitdrukken: daarvoor gebruiken we het uurloon, en op de stamkaart het totaal uurloon (§6.5).

### 6.2 De gebruikte loonbegrippen

Alle waarden komen uit de **berekende salarisgegevens**, ontsloten via **lijstbegrippen** die AFAS standaard meelevert en vult (§5.3). De klant hoeft niets in te richten om de cijfers te krijgen. Hij **kan** wel intellen: beide sets staan open, bij medewerkers voor correctie-looncomponenten en bij uitzendkrachten als uitwijkmogelijkheid (§5.3). De negen verklarende bedragen uit §5.3 volgen een eigen regel, onderaan deze paragraaf.

**Voor medewerkers en uitzendkrachten zijn dat verschillende lijstbegrippen.** Beide populaties hebben een **eigen set**. Voor **medewerkers** is dat sinds 7 oktober 2026 zo: zeven begrippen met Profit Id 6.821 t/m 6.827, per inkomstenverhouding, waarvan er één twee grootheden levert. Daarvóór werden de bestaande begrippen van de loonaangifte gebruikt. Voor **uitzendkrachten** was een eigen set altijd al nodig, want de loonaangifte kent de plaatsing niet; die set is op 29 september 2026 opgeleverd en telt zeven begrippen. De Profit Id's staan in de tabel hieronder en in §5.3.

**De definitie verschilt per populatie, en dat mag.** De set voor uitzendkrachten is geen kopie van de bestaande op een ander niveau: wat er voor een uitzendkracht in het loonbegrip hoort te zitten wijkt inhoudelijk af van wat er voor een eigen medewerker in hoort. Dat is juist de reden dat er twee sets zijn en niet één — zo blijft de looninrichting van beide populaties uit elkaar te houden.

**We vergelijken de twee populaties nooit met elkaar.** Een uitzendkracht wordt vergeleken met de andere uitzendkrachten bij dezelfde inlener, een eigen medewerker met de eigen medewerkers van de werkgever. Het model houdt die scheiding vast: populatie is sleutelonderdeel op laag 3 (§5.5), en bij uitzendkrachten komt daar de verkooprelatie bij. Er bestaat dus geen gemiddelde en geen loonverschilpercentage waarin de twee door elkaar lopen.

Daarmee vervalt de eis dat de twee sets identiek moeten zijn. Wat wél moet: **binnen** één populatie is de definitie overal gelijk, want daar wordt wél onderling vergeleken.

De twee laatste kolommen geven per grootheid het lijstbegrip dat hem levert: voor **medewerkers** het begrip uit de eigen set, per inkomstenverhouding, en voor **uitzendkrachten** het begrip uit de eigen set, per plaatsing. De begripsnamen komen uit het begrippenkader loontransparantie en de wettelijke bronnen verwijzen ernaar; dat staat los van de vraag waar de bedragen vandaan komen, want die komen uit de berekende salarisgegevens en niet uit de loonaangifte (§5.3).

**Vijf grootheden leveren hetzelfde gegeven, het loon niet.** De verloonde uren, de vakantiebijslag, het opgebouwde recht vakantiebijslag en de twee arbeidsvoorwaardenbedragen betekenen in beide populaties hetzelfde; alleen het niveau verschilt — per inkomstenverhouding tegenover per plaatsing. Bij het **loon** ligt het anders, en WrdLn bestaat alleen bij medewerkers. Daar staan in de tabel hieronder dan ook geen gedeelde rijen met twee Profit Id's, maar aparte rijen per populatie.

| Begrip | Omschrijving | Profit Id medewerkers | Profit Id uitzendkrachten |
| --- | --- | --- | --- |
| AantVerlU | Aantal verloonde uren, afgerond | 6.821 | 6.782 |
| LnLbPh | Loon LB/PH, samen met de correctie kunstenaar en sporter. Het **totaal**, inclusief het deel onder bijzonder tarief. In de brontabel het veld Loon LB/PH (§5.3) | 6.822 | n.v.t. |
| LnTabBB | Loon belast volgens tabel bijzondere beloningen; het deel van LnLbPh met bijzonder tarief. Hetzelfde lijstbegrip, met een filter op het tarief. In de brontabel het veld Loon LB/PH bijzonder tarief (§5.3) | 6.822, deel BT | n.v.t. |
| Brutoloon | De looncomponenten onder het reguliere belastingtarief, per plaatsing. Geen tegenhanger bij medewerkers; dit is **niet** LnLbPh en ook niet het bruto jaarloon van laag 2 | n.v.t. | 6.783 |
| Brutoloon bijzonder tarief | De looncomponenten onder het tarief bijzondere beloningen, per plaatsing | n.v.t. | 6.784 |
| VakBsl | Vakantiebijslag | 6.823 | 6.785 |
| OpgRchtVakBsl | Opgebouwd recht vakantiebijslag; in het kader uitzendkrachten de *reservering vakantiegeld* | 6.824 | 6.786 |
| WrdLn | Waarde niet in geld uitgekeerd loon. Niet beschikbaar voor uitzendkrachten (§5.3) | 6.825 | n.v.t. |
| OpnAvwb | Opname arbeidsvoorwaardenbedrag | 6.826 | 6.787 |
| OpbAvwb | Opbouw arbeidsvoorwaardenbedrag; in het kader uitzendkrachten de *reservering arbeidsvoorwaardenbedrag* | 6.827 | 6.788 |

**Alleen intellingen per dienstverband of plaatsing tellen mee.** Intellingen die op arbeidsvoorwaardenniveau worden berekend — een auto van de zaak, de pensioenpremie — zijn niet naar een dienstverband of plaatsing te herleiden, en zouden bij een uitzendkracht dus aan de verkeerde inlener kunnen worden toegerekend.

Hoe streng die afbakening uitpakt verschilt per populatie, en dat is een gevolg van de bron. Bij een **uitzendkracht** vallen deze bedragen er volledig buiten: het kader zondert het werknemersdeel pensioen en de bijtelling auto expliciet uit, en de twee lijstbegrippen bevatten ze dus niet. Bij een **medewerker** komt een bijtelling voor een auto van de zaak wél mee, namelijk via WrdLn in de waarde variabele componenten — daar is het bedrag per dienstverband bekend en is er maar één werkgever om het aan toe te rekenen. De twee populaties worden nooit met elkaar vergeleken, dus dat verschil hoeft niet te worden gladgestreken.

**Bij medewerkers staan LnLbPh en LnTabBB niet voor niets op hetzelfde lijstbegrip.** Ze gaan over hetzelfde loon. LnTabBB is daarbinnen geen apart bedrag maar een **deelverzameling**: het deel dat tegen bijzonder tarief is belast. Het onderscheid ontstaat door een extra filter op het tarief, niet door een andere bron.

**Dat filter werkt maar één kant op.** Profit leest het begrip twee keer: zonder filter levert het LnLbPh, het **totale** loon LB/PH inclusief het bijzondere deel, en met het filter levert het LnTabBB. Er is géén variant die alleen het **normale** tarief oplevert. De brontabel legt daarom het totaal en het deel vast — *Loon LB/PH* en *Loon LB/PH bijzonder tarief* (§5.3) — en niet twee niet-overlappende helften.

**Het bijzondere bedrag staat dus in beide velden, en dat is aanvaard.** Het alternatief is het normale deel zelf uitrekenen als totaal min bijzonder, maar dan staat er een bedrag in de brontabel dat door geen enkel lijstbegrip wordt geleverd en dat niet terug te voeren is op één verwerkte salarisregel (uitgangspunt 3). De prijs van deze keuze is dat de twee velden **nooit bij elkaar mogen worden opgeteld**: dat zou het bijzondere tarief dubbel laten meetellen, terwijl de formule in §6.1 het maar één keer afhaalt.

**Bij uitzendkrachten zijn het geen deelverzameling maar twee losse bedragen.** Lijstbegrip 6.783 levert de looncomponenten onder het **reguliere tarief**, 6.784 die onder het tarief bijzondere beloningen. Ze overlappen elkaar niet. Er is geen begrip dat de twee samen levert, en de optelling van beide is ook niet gelijk aan LnLbPh: onbelaste componenten en componenten onder nultarief zitten in geen van beide, en het werknemersdeel pensioen en de bijtelling vervoermiddel zijn bewust weggelaten omdat ze niet aan één inlener zijn toe te rekenen.

De twee populaties leggen het loon dus **precies omgekeerd** vast. Bij een medewerker staat er een totaal met daarnaast een deel daarvan; bij een uitzendkracht staan er twee stukken die elkaar uitsluiten. Daarom wordt het bruto jaarloon in het ene geval afgeleid en in het andere opgeteld (§6.1).

**Daarom heten de velden in de brontabel voor uitzendkrachten anders**: *Brutoloon* en *Brutoloon bijzonder tarief*, zonder de toevoeging LB/PH (§5.3). Die toevoeging verwijst naar een rubriek uit de loonaangifte, en dat is precies wat deze bedragen niet zijn. Dezelfde naam voeren als bij medewerkers zou suggereren dat beide populaties hetzelfde gegeven vastleggen; bij deze twee velden is dat juist niet zo, en dat werkt rechtstreeks door in de formule voor het bruto jaarloon (§6.1).

Twee regels uit het begrippenkader horen bij de jaarwaarde variabele componenten en zijn in de formule zelf niet zichtbaar:

- De waarde kan **niet negatief** zijn. Komt de berekening onder nul uit, dan houden we nul aan.
- De opname van het arbeidsvoorwaardenbedrag trekken we **alleen af als die in de loonaangifte als loon bijzondere beloning is verantwoord**. Is dat niet zo, dan blijft de aftrek achterwege.

Vakantiebijslag en arbeidsvoorwaardenbedrag, inclusief een dertiende maand, horen bij het bruto jaarloon en niet bij de variabele componenten. Daarom worden ze in de formule voor de jaarwaarde weer in mindering gebracht.

**Negen verklarende bedragen staan hier los van.** Naast de acht grootheden hierboven leggen de brontabellen negen verklarende bedragen vast (§5.3). Die komen langs dezelfde route binnen — berekende salarisgegevens via lijstbegrippen — maar ze verschillen op drie punten van de acht:

- ze komen in **geen enkele formule** voor: niet in het bruto jaarloon, niet in de variabele componenten en niet in een percentage of gemiddelde;
- het is **één set voor beide populaties**, bij medewerkers opgehaald per inkomstenverhouding en bij uitzendkrachten per plaatsing;
- AFAS onderhoudt ze, maar ze **staan open** voor eigen intellingen van de klant.

Die drie hangen samen. Omdat de klant de inhoud kan aanvullen, kan de betekenis per omgeving verschillen — en dan valt er niets meer op te vergelijken. Juist daarom blijven ze buiten de berekening en dienen ze alleen als duiding bij de cijfers van één medewerker.

### 6.3 De vergelijkingsgroep

De medewerker wordt vergeleken met alle arbeidsverhoudingen in dezelfde functiecategorie, uitgesplitst naar geslacht. Alleen regels per inkomstenverhouding die aan het populatiefilter uit hoofdstuk 3 voldoen tellen mee. Medewerkers met geslacht X en medewerkers zonder ingevuld geslacht tellen niet mee in de gemiddelden per geslacht, wel in het totale aantal arbeidsverhoudingen (§3.8).

De groep loopt over alle werkgevers binnen dezelfde **rapportage-eenheid**: alle combinaties van werkgever en periodetabel waarvan het loonheffingsnummer hetzelfde RSIN oplevert (§5.2). Het RSIN is het niveau waarop de wettelijke rapportage plaatsvindt, dus zo sluiten het recht op informatie en de latere rapportage op elkaar aan. Het voorkomt ook dat een concern met veel kleine werkgevers per werkgever te kleine groepen overhoudt om nog iets te kunnen tonen.

Één werkgever kan daarbij over **twee** groepen uiteenvallen. Dat doet zich voor als hij twee loonheffingsnummers met een verschillend RSIN voert (§5.2, inrichting 3); zijn medewerkers worden dan niet met elkaar vergeleken, maar elk met de eigen rapportage-eenheid.

**We tellen per arbeidsverhouding, niet per persoon.** Het begrippenkader legt de arbeidsverhouding vast op het niveau van de inkomstenverhouding. Een medewerker met twee inkomstenverhoudingen levert dus twee regels op en telt twee keer mee in de vergelijkingsgroep. Vallen die twee in verschillende functiecategorieën, dan telt de medewerker in beide groepen mee, elk met het loon dat in die arbeidsverhouding is verdiend. Dat is geen dubbeltelling die we moeten wegwerken: het loon uit de ene arbeidsverhouding hoort inhoudelijk niet bij de functiecategorie van de andere.

**Elke functieregel telt als volwaardige arbeidsverhouding.** Wisselde een arbeidsverhouding binnen het venster van functie, dan levert dat meerdere regels op (§5.4). Elk van die regels telt in zijn eigen functiecategorie mee als één arbeidsverhouding, met het loon over de tijdvakken die aan die functie zijn toegekend. Ook hier is er geen dubbeltelling van bedragen: elk tijdvak zit in precies één regel.

Hetzelfde geldt voor een uitzendkracht die bij dezelfde inlener in twee functiecategorieën is geplaatst. Ook dat zijn twee regels, en ook die tellen elk in hun eigen categorie mee (§5.4).

**De vergelijkingsgroep ligt altijd binnen één populatie.** Een detacheerder met *Plaatsingen verwerken in periodeverloning* heeft een regel bij de medewerkers en regels bij de uitzendkrachten (§5.4). Elke regel telt mee in de functiecategorie van zijn eigen populatie, en de twee populaties worden nergens samen genomen. Voor het recht op informatie is dat geen dubbeltelling: de medewerker wordt in het ene bakje vergeleken met de collega's in zijn eigen functiecategorie, in het andere met de uitzendkrachten bij dezelfde inlener. Voor de wettelijke rapportage ligt dat anders (hoofdstuk 11, DP2).

Het gevolg is wél dat zo'n medewerker in twee functiecategorieën als deelnemer meetelt, met in beide een bruto jaarloon over een deel van het venster. Dat drukt het gemiddelde jaarloon van die categorieën. We corrigeren daar niet voor, om dezelfde reden als bij medewerkers die niet het hele venster in dienst waren: het uurloon vangt het effect op, en dat is de grondslag waarop we het loonverschil tonen (§6.8).

**Het gemiddelde is het gemiddelde van de individuele waarden.** We tellen de waarden van de arbeidsverhoudingen bij elkaar op en delen door het aantal arbeidsverhoudingen (§6.7):

> gemiddeld bruto uurloon van de mannen = som van de bruto uurlonen van de mannen / aantal mannelijke arbeidsverhoudingen

Dat volgt het begrippenkader. De andere mogelijkheid was het totale loon delen door de totale uren, maar dan weegt een voltijder zwaarder dan een deeltijder in hetzelfde gemiddelde. Het recht op informatie gaat over de vraag hoe individuele lonen zich tot elkaar verhouden, dus iedere arbeidsverhouding weegt even zwaar. DP2 moet dezelfde rekenwijze aanhouden.

**Het gemiddeld totaal uurloon is de som van twee gemiddelden.** Voor dit ene veld wijken we af van de regel hierboven:

> gemiddeld totaal uurloon mannen = gemiddeld bruto uurloon mannen + gemiddelde uurwaarde variabele componenten mannen

Rekenkundig maakt dat geen verschil: het gemiddelde van een som is gelijk aan de som van de gemiddelden. Het maakt wél verschil voor de **afronding**. Zouden we het gemiddelde nemen van de per persoon opgetelde uurlonen, dan kan de uitkomst een cent afwijken van de twee gemiddelden die we al hadden vastgelegd — en juist die twee staan als segmenten in de gestapelde balk op de stamkaart (§8.2). De medewerker zou dan twee segmenten zien die niet optellen tot het totaal ernaast. Door het veld als optelling te definiëren kan dat niet gebeuren.

**Voor de mediaan kan dat niet.** De mediaan van een som is niet de som van de medianen: de persoon met het mediane basisloon hoeft niet de persoon met de mediane variabele componenten te zijn. De mediaan totaal uurloon blijft daarom de echte mediaan van het per arbeidsverhouding opgetelde uurloon (§6.6). De twee reeksen op laag 3 zijn dus niet op dezelfde manier opgebouwd; dat is bewust.

**Het categoriebrede gemiddelde rekent wél rechtstreeks.** *Gemiddeld totaal uurloon categorie* is de som van het veld Totaal uurloon over alle regels in de functiecategorie, gedeeld door het aantal arbeidsverhoudingen totaal (§6.7). Hier speelt de afrondingsafweging van hierboven niet: dit getal staat nergens als gestapelde balk op het scherm, dus er is niets waarmee het tot op de cent moet aansluiten. Alle geslachten tellen mee, ook X en niet ingevuld.

### 6.4 De vergelijkingscijfers

De medewerker ziet zijn eigen waarde naast het gemiddelde van de **mannen** en dat van de **vrouwen** binnen zijn functiecategorie. Die twee gemiddelden komen uit de tabel per functiecategorie. Mannen staan eerst, omdat zij de referentiegroep zijn in alle loonverschilpercentages (§6.5).

Sinds de herziening van 23 september 2026 gebeurt dat in de tegel *Gemiddeld uurloon binnen functiecategorie*: een gestapelde balk per groep, opgebouwd uit het basisloon en de variabele componenten (§8.2). Alles staat daar op **uurbasis**.

**De vergelijkingstabel vervalt.** Een eerdere versie toonde vijf regels — jaaruren, bruto jaarloon, bruto uurloon, jaarwaarde en uurwaarde variabele componenten — maal drie kolommen. Vijftien getallen waarvan de medewerker de helft niet kan plaatsen, en waarin het onderscheid tussen jaar- en uurwaarde en tussen basisloon en variabele componenten hem eerder in de weg zat dan hielp. Op uurbasis blijven er zes getallen over, en die passen in één beeld. Hoofdstuk 8 werkt dat uit.

**De kolom Individueel verschil verviel eerder, en komt beperkt terug.** In de PM-terugkoppeling van 3 september 2026 is besloten dat een individueel percentage op elke regel van de tabel uitnodigt tot een conclusie die het niet kan dragen: wie onder het gemiddelde zit, kan gewoon minder ervaring of minder dienstjaren hebben. Dat bezwaar geldt nog steeds voor de vijf losse regels. Op 23 september 2026 is besloten dat er wél **één** individueel percentage komt, op het totaal uurloon en afgezet tegen het gemiddelde van de hele functiecategorie (§6.5). Dat is de vraag die de medewerker zelf stelt zodra hij de groepscijfers ziet, en die anders via een vraag aan HR terugkomt.

**De mediaan blijft buiten de stamkaart.** De mediaan van de hele categorie past niet bij de rapportagedefinitie, waarin de mediaan van de mannen tegen die van de vrouwen wordt afgezet. Beide medianen tonen zou een tweede reeks getallen opleveren die naast de gemiddelden weinig toevoegt voor de individuele medewerker. Het mediane loonverschil hoort thuis in de wettelijke rapportage van DP2 en in het dashboard. Het datamodel heeft er wel velden voor (§5.5); die worden vanaf fase 1 gevuld, zodat het dashboard erover beschikt.

### 6.5 De loonverschilpercentages

Het loonverschil zet het gemiddelde van de mannen af tegen dat van de vrouwen. De mannen zijn daarbij altijd de **noemer**: zij vormen de referentiegroep, wat aansluit bij de manier waarop het loonverschil gebruikelijk wordt uitgedrukt. De volgorde in de **teller** hangt af van de soort rapportage:

> soort *Recht op informatie*: loonverschil = (gemiddelde vrouwen − gemiddelde mannen) / gemiddelde mannen
>
> soort *Rapportage*: loonverschil = (gemiddelde mannen − gemiddelde vrouwen) / gemiddelde mannen

Dat levert hetzelfde getal op met een ander teken. Bij het recht op informatie betekent een **min** dat vrouwen gemiddeld minder verdienen dan mannen; bij de wettelijke rapportage betekent een **plus** precies dat.

**Waarom het recht op informatie de andere kant op telt.** De wettelijke richting komt uit het begrippenkader en is geschreven voor een rapportage die een beleidsmaker leest. Op de stamkaart leest datzelfde getal averechts: de medewerker ziet een plus en leest die als iets gunstigs, terwijl het betekent dat vrouwen achterblijven. Bij het individuele percentage hieronder was het nog sterker — daar betekende een plus dat je zelf mínder verdient dan je collega's. We draaien de teller daarom om voor alles wat onder soort *Recht op informatie* valt. Dat het recht op informatie en de wettelijke rapportage daarmee tegengesteld tellen is een bewuste keuze: het zijn twee losse onderdelen die zelden naast elkaar worden gelegd, en de rapportagecijfers zelf wijzigen niet. Dat de medewerker begrijpt waar hij naar kijkt weegt hier zwaarder dan dat beide onderdelen hetzelfde teken dragen.

**De wettelijke rapportage blijft ongemoeid.** De vier percentages met een nummer uit het begrippenkader (§6.9) houden op een regel met soort *Rapportage* onverkort de voorgeschreven formule. De omkering raakt uitsluitend regels die bij een rapportageperiode met soort *Recht op informatie* horen, en die regels komen in de rapportage niet voor. De randvoorwaarde daarbij is dat geen enkel overzicht de twee soorten door elkaar toont (§5.9).

We berekenen deze formule op **vijf grondslagen**:

| Percentage | Grondslag | Op de stamkaart |
| --- | --- | --- |
| Loonverschil totaal uurloon | Gemiddeld totaal uurloon | Ja, als KPI (§8.2) |
| Loonverschil uurloon | Gemiddeld bruto uurloon | Nee |
| Loonverschil componenten uurwaarde | Gemiddelde uurwaarde variabele componenten | Nee |
| Loonverschil jaarloon | Gemiddeld bruto jaarloon | Nee |
| Loonverschil componenten jaarwaarde | Gemiddelde jaarwaarde variabele componenten | Nee |

Deze vijf namen gebruiken we overal: als veldnaam in §5.5, als grondslag hier en als grondslag van de loonverschiltegel in §8.2.

De taak berekent deze vijf percentages en legt ze vast op de regel per functiecategorie (§5.5). De KPI leest ze en rekent zelf niets meer uit.

**Het totaal uurloon is de grondslag op de stamkaart.** Een eerdere versie van dit ontwerp toonde twee percentages naast elkaar: één op het basisloon en één op de variabele componenten. Dat liet zien waar een verschil vandaan komt, maar het vraagt van de medewerker dat hij eerst het onderscheid tussen die twee begrijpt — en juist de variabele componenten zeggen hem weinig. Twee percentages maken het recht op informatie daarmee complexer dan nodig.

We tonen daarom één percentage, op het loon dat de medewerker in zijn geheel herkent: alles wat hij per verloond uur verdient. Dat percentage komt **niet terug in de wettelijke rapportage**, want die kent deze grondslag niet. Dat is aanvaard: de rapportage schrijft niet voor welk percentage bij het recht op informatie wordt getoond, en voor de medewerker is dit de duidelijkste maat. Het onderscheid tussen basisloon en variabele componenten blijft wel zichtbaar, maar als bedrag in de gestapelde balk in plaats van als percentage (§8.2).

**Het uurloon blijft de basis, niet het jaarloon.** Een percentage op jaarbasis houdt geen rekening met het parttimepercentage en meet daardoor voor een deel een urenverschil in plaats van een loonverschil: vrouwen werken vaker in deeltijd, en wie halverwege in dienst kwam of binnen het venster van functie wisselde heeft een lager jaarloon. Het uurloon corrigeert daarvoor vanzelf (§6.8).

**Het jaarloon blijft wél berekend en vastgelegd.** Het staat in het datamodel (§5.5) en in het dashboard, en het laat zien wat iemand feitelijk heeft verdiend. Op de stamkaart komt het niet meer voor: er is voor het recht op informatie **geen juridische basis** die het bruto jaarloon voorschrijft. De aanname dat het loonniveau in twee eenheden tegelijk moest worden uitgedrukt, berustte op een misverstand. Wie het bedrag nodig heeft, vindt het in het document *Loontransparantie medewerker* (hoofdstuk 11).

**De variabele componenten houden hun eigen percentages, maar die zijn niet zichtbaar.** De wettelijke rapportage onderscheidt het basisloon van de variabele componenten, dus we berekenen en bewaren die percentages. Ze staan alleen niet meer op de stamkaart; daar is één percentage op het totaal uurloon voor in de plaats gekomen.

**Een percentage vraagt twee groepen.** Ontbreekt een van beide — geen mannen of geen vrouwen in de functiecategorie — dan blijft het percentage leeg. Hetzelfde geldt als het gemiddelde van de mannen nul is; delen door nul levert geen uitlegbaar getal op.

We tonen in die gevallen nadrukkelijk **geen 100%**. Rekenkundig zou je dat kunnen verdedigen als de vrouwengroep leeg is: het hele mannengemiddelde is dan het verschil. Maar voor de medewerker leest 100% als een maximaal loonverschil, terwijl er in werkelijkheid niets te vergelijken valt. Het gemiddelde van de groep die er wél is, blijft gewoon in de balk staan (§8.6).

**We slaan het percentage op als getal met twee decimalen.** Een loonverschil van 5,23% leggen we vast als 5,23 en niet als 0,0523. Het begrippenkader rekent de formule ook maal honderd procent. Zo staat er in de tabel hetzelfde getal als op het scherm en in de rapportage, en is er geen plek waar een factor honderd kan worden vergeten.

**Het individuele loonverschil**

Naast het groepsverschil berekenen we per arbeidsverhouding hoe de medewerker zelf zich verhoudt tot het gemiddelde van de **hele** functiecategorie:

> soort *Recht op informatie*: individueel loonverschil = (eigen totaal uurloon − gemiddeld totaal uurloon categorie) / gemiddeld totaal uurloon categorie
>
> soort *Rapportage*: individueel loonverschil = (gemiddeld totaal uurloon categorie − eigen totaal uurloon) / gemiddeld totaal uurloon categorie

Dit beantwoordt de vraag die de groepspercentages openlaten: *en ik dan?* Het staat op de regel per inkomstenverhouding (§5.4), niet op laag 3, want het is een individuele waarde.

**Het teken gaat uit van de eigen waarde, ongeacht geslacht.** Bij het recht op informatie betekent een **plus** dat de medewerker méér verdient dan het gemiddelde van zijn functiecategorie, en een **min** dat hij er minder verdient. Dat is de enige leesrichting die vanuit de medewerker klopt: zijn eigen bedrag is het onderwerp en het categoriegemiddelde is de maatstaf waartegen dat wordt gehouden. Geslacht komt er niet in voor, niet in de teller en niet in de noemer. De teksten bij dit percentage noemen daarom ook geen geslacht (§8.2, §8.7).

**De noemer is het gemiddelde van de héle functiecategorie**, alle geslachten samen, en niet dat van het eigen geslacht. Dat is een bewuste keuze en ze volgt de wet. De richtlijn gaat erover dat gelijk werk gelijk wordt beloond **ongeacht geslacht**. Een medewerker afzetten tegen het gemiddelde van zijn eigen geslacht zou die norm omdraaien: dan is de maatstaf wat mannen — of wat vrouwen — gemiddeld verdienen, en bevestigt het cijfer juist het onderscheid dat de wet wil opheffen. Een vrouw die onder het vrouwengemiddelde zit maar boven het mannengemiddelde, zou dan een negatief signaal krijgen terwijl ze in de zin van de wet niet wordt benadeeld.

Het categoriegemiddelde is bovendien de enige maat die voor iedereen hetzelfde betekent. Medewerkers met geslacht X of zonder ingevuld geslacht tellen er gewoon in mee (§3.8), dus zij krijgen dit percentage net zo goed te zien.

Dit staat los van de noemer bij het **groepsverschil**. Daar zijn de mannen de referentiegroep, omdat het loonverschil zo gebruikelijk wordt uitgedrukt en omdat de wettelijke rapportage die noemer voorschrijft. Dat percentage gaat over de groep; dit over de persoon.

**Dit percentage is niet af te leiden uit laag 3 alleen.** Het heeft zowel de individuele waarde van laag 2 als het categoriegemiddelde van laag 3 nodig. De taak vult het daarom in een tweede rekenslag, nadat laag 3 is samengesteld (§7.3).

**Het veld blijft alleen leeg als er geen categoriegemiddelde is.** Dat kan als de functie niet aan een categorie is gekoppeld (§3.7). Geslacht speelt hier geen rol meer: iedereen telt mee in het gemiddelde waartegen wordt afgezet.

### 6.6 De medianen

De mediaan is het bedrag waarbij de ene helft van de groep meer verdient en de andere helft minder. We berekenen hem per functiecategorie, per geslacht, uit de regels per inkomstenverhouding die aan het populatiefilter uit hoofdstuk 3 voldoen. Dezelfde vergelijkingsgroep dus als bij de gemiddelden (§6.3).

Het algoritme volgt het begrippenkader:

> Sorteer de waarden van laag naar hoog. Is het aantal oneven, neem dan de middelste waarde. Is het aantal even, neem dan het gemiddelde van de twee middelste waarden.

Twee dingen zijn hierbij van belang. De waarden hoeven **niet uniek** te zijn: verdienen drie mannen exact hetzelfde, dan staan die drie bedragen ook alle drie in de rij. En we sorteren de **individuele waarden per arbeidsverhouding**, niet per persoon — net als bij de gemiddelden telt een medewerker met twee arbeidsverhoudingen dus twee keer mee.

We berekenen de mediaan op vijf maatstaven: bruto jaarloon, bruto uurloon, jaarwaarde variabele componenten, uurwaarde variabele componenten en totaal uurloon. Voor de jaaruren doen we het niet; het begrippenkader kent die mediaan niet. De vijfde, het totaal uurloon, is een eigen uitbreiding die hoort bij de grondslag op de stamkaart (§6.5).

**De mediaan totaal uurloon sorteert op het opgetelde bedrag.** Anders dan bij het gemiddelde (§6.3) mogen we hier niet twee al berekende medianen bij elkaar optellen. De mediaan van een som is niet de som van de medianen: de persoon met het mediane basisloon hoeft niet degene te zijn met de mediane variabele componenten, en bij een scheve verdeling lopen die twee ver uiteen. De taak telt dus eerst per arbeidsverhouding het totaal uurloon op — dat veld staat al op laag 2 (§5.4) — en sorteert daarna die bedragen.

Is een geslachtsgroep leeg, dan blijft de mediaan leeg. We vullen geen nul, want nul zou betekenen dat er iemand is die niets verdient.

**Het mediane loonverschil** werkt net als het gewone loonverschil, maar dan op medianen in plaats van gemiddelden — inclusief de rekenrichting per soort rapportage (§6.5):

> soort *Recht op informatie*: mediane loonverschil = (mediaan vrouwen − mediaan mannen) / mediaan mannen
>
> soort *Rapportage*: mediane loonverschil = (mediaan mannen − mediaan vrouwen) / mediaan mannen

Ook deze vijf percentages slaan we op als getal met twee decimalen. Is de mediaan van de mannen leeg of nul, dan blijft het percentage leeg.

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

**We tellen regels, niet medewerkers.** Een medewerker die binnen het venster van functie wisselde heeft meerdere regels en telt dus in meerdere functiecategorieën mee (§6.3). Hetzelfde geldt voor een medewerker met twee inkomstenverhoudingen, en voor een detacheerder met *Plaatsingen verwerken in periodeverloning*, die in beide populaties een regel heeft (§5.4). Het aantal arbeidsverhoudingen is daarmee geen telling van personen, en de som over alle functiecategorieën kan hoger uitkomen dan het aantal medewerkers in de organisatie.

**Op de rapportageperiode (laag 0)** staat één aantal: het aantal arbeidsverhoudingen totaal. Dat is de telling van **alle** regels per inkomstenverhouding in deze rapportageperiode, over beide populaties; een detacheerder die in beide populaties een regel heeft, telt hier dus ook twee keer.

Dat getal is groter dan of gelijk aan de som van de totalen op laag 3. Medewerkers zonder functiecategorie krijgen namelijk wel een regel per inkomstenverhouding, maar komen in geen enkele functiecategorie terecht (§3.7). Wie de twee lagen naast elkaar legt en een verschil ziet, kijkt dus naar het aantal arbeidsverhoudingen waarvan de functie nog niet aan een categorie is gekoppeld. Dat is bruikbare stuurinformatie voor het dashboard.

**Het aantal medewerkers in fte** is een ander begrip en telt geen regels maar uren:

> aantal medewerkers in fte = som van de jaaruren / arbeidsjaareenheid

De arbeidsjaareenheid is het aantal uren dat een voltijdmedewerker in een jaar werkt, door de werkgever zelf bepaald. Dat stamgegeven bestaat nog niet in Profit en komt er in fase 2 bij; daarom is dit veld pas dan te vullen. Het begrippenkader noemt dit begrip *aantal werknemers*; wij houden de Profit-term aan, omdat "aantal werknemers" hier verwarrend is — het gaat om een fte-getal en niet om een telling van personen.

Dit getal bepaalt of en hoe vaak een werkgever rapportageplichtig is. Voor het recht op informatie speelt het geen rol.

### 6.8 Onvolledige vensters in de vergelijking

We nemen medewerkers mee zolang er loon in het venster valt. Wie halverwege in of uit dienst ging, heeft daardoor een lager bruto jaarloon en minder jaaruren dan een collega die het hele venster meedraaide. Hetzelfde geldt voor wie binnen het venster van functie wisselde: die heeft per functiecategorie een regel over een deel van het venster (§4.5).

We corrigeren daar niet voor en we tellen niemand apart. Iedereen in de functiecategorie telt mee in alle vergelijkingscijfers. Een aparte telling voor de jaarbedragen zou de groep verkleinen en het geheel moeilijker uitlegbaar maken.

Dit betekent dat de jaaruren, het bruto jaarloon en de jaarwaarde in de vergelijking een gemengd beeld geven: ze bevatten zowel volledige als gedeeltelijke arbeidsverhoudingen. **Dat is precies de reden dat we het loonverschil op uurbasis tonen en niet op jaarbasis** (§6.5). Het uurloon deelt door de uren die er daadwerkelijk zijn geweest en is daarmee ongevoelig voor de vraag of iemand het hele venster meedraaide.

De jaarcijfers blijven in het datamodel staan, voor wie wil zien wat er feitelijk is verdiend; op de stamkaart komen ze niet meer voor (§6.5). Wijken het jaar- en het uurpercentage sterk af, dan zit het verschil in de arbeidsomvang en niet in de beloning; dat is een bruikbaar signaal voor het dashboard.

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
| Loonverschil totaal uurloon | Geen; eigen uitbreiding |
| Mediane loonverschil jaarloon | Geen; eigen uitbreiding |
| Mediane loonverschil uurloon | Geen; eigen uitbreiding |
| Mediane loonverschil componenten jaarwaarde | Geen; eigen uitbreiding |
| Mediane loonverschil componenten uurwaarde | Geen; eigen uitbreiding |
| Mediane loonverschil totaal uurloon | Geen; eigen uitbreiding |

**Een G-nummer legt de formule vast, niet het teken.** Op een regel met soort *Rapportage* volgen de vier genummerde percentages letterlijk het begrippenkader. Op een regel met soort *Recht op informatie* staat dezelfde uitkomst met het omgekeerde teken (§6.5). De grondslag, de noemer en de vergelijkingsgroep zijn in beide gevallen identiek, dus een uitkomst blijft tot het nummer herleidbaar; alleen de leesrichting verschilt.

**De twee percentages op het totaal uurloon hebben geen nummer.** Het begrippenkader kent die grondslag niet — basisloon en variabele componenten staan daar los van elkaar. Het zijn eigen uitbreidingen voor de stamkaart en het dashboard, die nooit in de wettelijke rapportage terechtkomen (§5.5, §6.5).

**De vier mediane percentages hebben geen nummer.** Het begrippenkader kent de mediaan alleen organisatiebreed — C11, C21, D11 en D21 — en niet binnen een arbeidscategorie. Een mediaan per functiecategorie is dus een bewuste uitbreiding van ons model, die nooit in de wettelijke rapportage terechtkomt. Waarom we hem toch vastleggen staat in §5.5.

**De A-, B-, C- en D-reeks komen in fase 2.** Dat zijn dezelfde acht percentages, maar dan over de hele populatie. Ze vullen dezelfde velden op een regel met een **lege functiecategorie** (§5.7). De formule is identiek; alleen de selectie is breder.

De E-reeks (aandeel ontvangers van variabele componenten) en de F-reeks (F.111n tot en met F.141n, het aandeel mannen en vrouwen per kwartiel op jaar- en uurbasis) vallen buiten dit ontwerp en worden in DP2 uitgewerkt.

---

## 7 Vulproces

### 7.1 Wanneer de gegevens worden bijgewerkt

Alle lagen worden bijgewerkt door één wachtrijtaak: **Bijwerken gegevens loontransparantie**, gestart vanuit de dagovergang **Vernieuwen actuele gegevens**. Die draait doorgaans elke nacht.

Het **accorderen van de salarisverwerking** werkt de tabellen dus niet zelf bij. Het schrijft alleen triggerregels weg: voor het geaccordeerde tijdvak en voor elk eerder tijdvak dat met terugwerkende kracht is geraakt (§7.2). Meer gebeurt er op dat moment niet. De taak leest die triggerregels bij de eerstvolgende dagovergang, vult de brontabellen voor de betrokken tijdvakken en stelt de lagen erboven opnieuw samen.

Dat is een bewuste keuze om alle rekenkracht uit het salarisproces te halen:

- **Een rapportage-eenheid wordt maar één keer bijgewerkt.** Werkgevers die onder hetzelfde RSIN vallen worden doorgaans op dezelfde dag geaccordeerd, vaak door hetzelfde administratiekantoor. Door tot de dagovergang te wachten valt dat samen in één run in plaats van één run per werkgever. Ook een werkgever met meerdere periodetabellen — maand, vier weken en week naast elkaar — valt technisch onder één RSIN en wordt zo in één keer meegenomen.
- **De taak zit lopende processen niet in de weg.** Verlonen, accorderen, loonstroken genereren en de loonaangifte lopen allemaal via de batchservice. Administratiekantoren accorderen tientallen werkgevers per dag, waardoor die service overdag al zwaar belast is. Een berekening die daar direct bovenop meedraait, vertraagt processen waar de klant wél op staat te wachten.
- **De taak is opnieuw uit te voeren.** Gaat er iets mis, dan kan hij los worden gestart. Er hoeft niet eerst een salarisverwerking te worden geaccordeerd om een herstelrun uit te lokken.
- **Niet alleen de salarisverwerking is van invloed.** Een functiewijziging verandert de functie waaraan tijdvakken worden toegekend (§4.5) en daarmee de indeling in functiecategorieën; een wijziging in de functiecategorie-inrichting verandert de vergelijkingsgroep zelf; en bij een uitzendkracht doen de functiecategorie op de functie van de klantovereenkomst en de afwijkende functiecategorie op de plaatsing hetzelfde (§7.2). Die wijzigingen komen niet via het salarisproces binnen. Met een dagelijkse taak werken ze vanzelf door, en meestal eerder dan bij de eerstvolgende verwerking.

De prijs is actualiteit: de cijfers lopen maximaal één dagovergang achter op de geaccordeerde salarisverwerking. Voor het recht op informatie is dat ruim voldoende, want de wettelijke reactietermijn is twee maanden (§7.7).

**Dit herziet de eerdere keuze om laag 1 direct bij het accorderen te vullen.** Die keuze hield het salarisproces al grotendeels vrij — er werd alleen weggeschreven, niet gerekend — maar ze legde het schrijfwerk nog steeds in de accordeertaak. Met een werkgever per accordering betekende dat evenveel schrijfrondes als accorderingen, terwijl de gegevens daarna toch pas in de dagovergang bruikbaar werden. Nu doet het accorderen niets meer dan signaleren.

Het venster blijft eindigen bij het laatste **geaccordeerde** tijdvak (§4.2). De taak bepaalt dat bij elke run opnieuw en verschuift het venster dus niet zelf.

### 7.2 De triggertabel

De taak moet weten voor welke werkgevers er iets is veranderd. Zou hij elke nacht alle werkgevers volledig doorrekenen, dan doet hij bij verreweg de meeste runs werk dat niets oplevert.

Daarom houden we dat bij in een technische **triggertabel**. Die is niet zichtbaar voor de klant en wordt niet ontsloten via weergaven of gegevensverzamelingen. Hij hoort ook niet bij het gegevensmodel uit hoofdstuk 5: er staan geen loongegevens in, alleen werkvoorraad.

**Sleutel:** werkgever, periodetabel, jaar en periode. Daarnaast staat er één kenmerk op de regel: **Soort trigger**.

Eén regel zegt: voor deze werkgever is dit loontijdvak geraakt en moet worden meegenomen. Wélk proces de regel heeft weggeschreven doet niet ter zake, omdat de taak de betrokken werkgever toch volledig opnieuw doorrekent (§7.3). Dat houdt de tabel klein.

**Het kenmerk Soort trigger kent twee waarden.** Bij *Salarisgegevens* zijn de verwerkte bedragen van dit ene tijdvak gewijzigd. Bij *Stamgegevens* is er iets veranderd aan de indeling — een functie of een functiecategorie — zonder dat er aan een bedrag is gerekend. Het verschil bepaalt hoeveel bronregels de taak opnieuw wegschrijft (§7.3).

Dat onderscheid is nieuw. Eerder stond hier dat wát er is gewijzigd niet ter zake doet, en dat klopte zolang elke trigger hetzelfde deed. Sinds een stamgegeven-trigger het hele venster aan bronregels herbouwt, is het verschil wél van belang: zo'n trigger staat op het laatste geaccordeerde tijdvak en is zonder dit kenmerk niet te onderscheiden van een gewone accordering. Het alternatief — de schrijvende processen een regel per tijdvak in het venster laten wegschrijven — laat de triggertabel met twaalf tot drieënvijftig regels per werkgever groeien en botst met het uitgangspunt dat de werkvoorraad klein blijft (§7.4).

**We slaan het op periodeniveau op.** Vanuit de salarisverwerking is de periode direct voorhanden. Vanuit een functiewijziging moet hij worden opgezocht, maar dat is goed te doen omdat de periodetabel van het dienstverband bekend is. Bij de realisatie bepaalt de programmeur hoe dat precies wordt ingevuld.

Het alternatief — alleen de werkgever vastleggen — zou dat opzoekwerk besparen, maar dan valt de venstertoets uit §7.3 weg en rekent elke wijziging de werkgever volledig door, ook een correctie op een tijdvak van jaren geleden.

**Wanneer er een triggerregel wordt weggeschreven**

| Gebeurtenis | Welke regels | Soort trigger |
| --- | --- | --- |
| Accorderen van de salarisverwerking | Het geaccordeerde tijdvak, plus elk eerder tijdvak dat met terugwerkende kracht is geraakt | Salarisgegevens |
| Terugdraaien van een geaccordeerde salarisverwerking | Het teruggedraaide tijdvak | Salarisgegevens |
| Functiewijziging op het dienstverband: nieuw, gewijzigd of verwijderd | Alle loontijdvakken die de begin- en einddatum van de functie raken | Stamgegevens |
| Wijziging in de functiecategorie-inrichting | Voor **alle** werkgevers het laatste geaccordeerde tijdvak, per periodetabel | Stamgegevens |
| Functiecategorie gewijzigd op de functie van de klantovereenkomst | Voor elke werkgever met een plaatsing op die functie het laatste geaccordeerde tijdvak, per periodetabel | Stamgegevens |
| Afwijkende functiecategorie op de plaatsing gevuld, gewijzigd of leeggemaakt | Voor de werkgever van het dienstverband bij die plaatsing het laatste geaccordeerde tijdvak, per periodetabel | Stamgegevens |
| Conversie naar Profit 9 | Eenmalig alle periodes van 2026, per verloonde werkgever en periodetabel (§7.7) | Salarisgegevens |

**Terugwerkende kracht levert meerdere triggerregels op.** Een salarisverwerking corrigeert regelmatig eerdere tijdvakken: een mutatie met terugwerkende kracht, een nabetaling, een gecorrigeerde arbeidsvoorwaarde. De bedragen van die eerdere tijdvakken wijzigen daarmee, en dus moeten ook die bronregels opnieuw worden weggeschreven. Het accorderen bepaalt welke tijdvakken zijn geraakt en schrijft voor elk daarvan een triggerregel weg, naast die voor het tijdvak zelf.

Dat is precies waarom de triggertabel een periode bevat en niet alleen een werkgever. Zonder periode zou een correctie op een tijdvak van twee jaar geleden niet te onderscheiden zijn van een reguliere verwerking, en zou de venstertoets uit §7.3 niets meer kunnen filteren.

**Bij een functiewijziging leiden we de tijdvakken af uit de begin- en einddatum van de functie.** Elk loontijdvak waarin die periode valt levert een triggerregel op. Raakt de wijziging meerdere tijdvakken — een functiewijziging met terugwerkende kracht bijvoorbeeld — dan komen die er allemaal in. Bij het bijwerken bepaalt de taak vervolgens welke van die tijdvakken binnen het venster vallen en dus relevant zijn (§7.3).

Omdat de functie sinds de herziening van 15 september 2026 op de bronregel staat (§5.3), moet een functiewijziging met terugwerkende kracht ook die bronregels bijwerken. De triggerregel zorgt daarvoor: de taak schrijft de bronregels van de geraakte tijdvakken opnieuw weg en stelt de lagen erboven daarna opnieuw samen.

**Een contractwijziging schrijft géén triggerregel.** Nieuw, eigenschappen wijzigen, verwijderen, contractverlenging en indienstmelding vallen er dus buiten. Twee redenen: een contractwijziging is niet per se een functiewijziging, en als hij de loongegevens raakt, leidt hij zelf al tot een correctie in de salarisverwerking — en die schrijft wél een triggerregel weg. We triggeren uitsluitend op gegevens die de indeling in functiecategorieën veranderen zonder dat er iets in de salarisverwerking gebeurt; bij een eigen medewerker is dat alleen de functie.

**Een nieuwe plaatsing of een andere inlener schrijft géén triggerregel.** Drie redenen:

- **Er valt nog niets te tonen.** Een plaatsing levert pas loongegevens op nadat er over is verloond. Tot dat moment zou een herberekening op precies dezelfde cijfers uitkomen.
- **Het accorderen vangt het vanzelf op.** Zodra de salarisverwerking waarin de plaatsing meeloopt is geaccordeerd, staat er een triggerregel en wordt de bronregel voor dat tijdvak weggeschreven — met de plaatsing, de verkooprelatie en de functie die er dan bij horen (§5.3).
- **Het mutatievolume is te hoog.** Plaatsingen wijzigen veelvuldig. Triggeren op elke mutatie zou betekenen dat de taak vrijwel dagelijks alle uitleners volledig doorrekent, zonder dat de uitkomst verandert.

Dat de KPI op de **actuele functie** filtert (§5.9) maakt dit sluitend: wisselt een uitzendkracht van plaatsing, dan volgt de stamkaart die wissel zodra er over de nieuwe plaatsing is verloond. Tot dat moment ziet hij de cijfers van de plaatsing waarover wél loon is verwerkt, met de melding uit §8.6 als er voor de nieuwe functie nog niets is.

**Twee gegevens uit Flex schrijven wél een triggerregel.** Dat zijn de twee plekken waar DP5 de functiecategorie van een uitzendkracht vastlegt. Ze doen bij een uitzendkracht precies wat de functiewijziging bij een eigen medewerker doet: ze verplaatsen de arbeidsverhouding naar een andere vergelijkingsgroep, zonder dat er iets in de salarisverwerking gebeurt. Zonder triggerregel zou die verplaatsing pas bij de eerstvolgende verwerking zichtbaar worden — en bij een uitzendkracht die niet meer wordt verloond helemaal niet.

- **De functiecategorie op de functie van de klantovereenkomst.** Koppelt de inlener een functie aan een andere categorie, dan verandert de vergelijkingsgroep van elke plaatsing op die functie. De functie hangt aan een klantovereenkomst en dus aan één verkooprelatie, maar de triggertabel gaat per **werkgever**. We leiden de betrokken uitleners daarom af uit de plaatsingen op die functie en schrijven per werkgever en periodetabel één regel weg, op het laatste geaccordeerde tijdvak. Dat is gerichter dan de wijziging in de functiecategorie-inrichting hieronder: die raakt de hele omgeving, deze alleen de uitleners die daadwerkelijk bij deze inlener plaatsen.
- **De afwijkende functiecategorie op de plaatsing.** Gevuld, gewijzigd of leeggemaakt — alle drie leiden ze tot een andere vergelijkingsgroep, want laag 2 groepeert op de functiecategorie van de plaatsing (§5.4). Leeghalen is net zo goed een wijziging als vullen: de plaatsing valt dan terug op de categorie van de functie. De plaatsing hangt aan een dienstverband en daarmee aan één werkgever; die krijgt per periodetabel één regel, op het laatste geaccordeerde tijdvak. Het gaat om een mutatie op een **bestaande** plaatsing; bij een nieuwe plaatsing valt er nog niets te herberekenen.

**Op de functie van de plaatsing triggeren we niet.** Die ligt na het aanmaken van de plaatsing vast en is niet meer te wijzigen, dus er is geen gebeurtenis om op te triggeren.

**Het volume blijft hanteerbaar.** Deze twee mutaties zijn zeldzaam vergeleken met plaatsingmutaties in het algemeen: een inlener herziet zijn functie-indeling niet dagelijks, en een afwijkende functiecategorie is per definitie een uitzondering. Het bezwaar hierboven — dat de taak dan vrijwel dagelijks alle uitleners zou doorrekenen — geldt hier dus niet.

**Een wijziging in de functiecategorie-inrichting raakt iedereen.** Koppelt de klant een functie aan een andere categorie, voegt hij een categorie toe of haalt hij er een weg, dan verandert de vergelijkingsgroep van elke medewerker met zo'n functie — en daarmee de gemiddelden van beide betrokken categorieën. Die wijziging hangt niet aan een werkgever en niet aan een tijdvak, dus is er geen kleinere afbakening te maken dan alle werkgevers.

We schrijven daarvoor per werkgever en periodetabel één regel weg, op het **laatste geaccordeerde tijdvak**. Dat tijdvak valt per definitie binnen het venster, dus de venstertoets uit §7.3 laat de regel altijd door. Meer regels zijn niet nodig: één triggerregel is genoeg om een werkgever volledig te laten doorrekenen. Werkgevers die nog nooit een salarisverwerking hebben geaccordeerd krijgen geen regel; daar valt ook niets te berekenen.

**Wijzigingen buiten het venster leiden niet tot herberekenen.** De bronregel wordt wel bijgewerkt, maar de lagen erboven niet. Dat filteren we niet bij het wegschrijven van de triggerregel maar bij het uitvoeren van de taak (§7.3). Het venster kan tussen die twee momenten namelijk verschuiven, en de schrijvende processen hoeven er geen weet van te hebben hoe het wordt bepaald.

**Opschonen.** Een triggerregel wordt verwijderd zodra de taak hem heeft verwerkt, ook als die verwerking niet verder komt dan het bijwerken van de bronregel omdat het tijdvak buiten het venster valt. Loopt de taak vast, dan blijven de regels staan en worden ze bij de volgende run alsnog meegenomen. Dat is precies waarvoor de tabel bestaat: hij maakt het bijwerken herstelbaar zonder dat iemand hoeft te achterhalen wat er is gemist.

### 7.3 Wat de taak doet

De taak Bijwerken gegevens loontransparantie werkt alle lagen bij:

1. leest de triggertabel en bepaalt de werkgevers waarvoor een regel openstaat;
2. bepaalt per werkgever en periodetabel het laatste geaccordeerde tijdvak, zoekt bij die periodetabel het aantal tijdvakken van een jaar op (§4.3) en telt dat aantal terug tot het begin van het venster (§6.1);
3. schrijft de bronregels opnieuw weg uit de berekende salarisgegevens (§5.3), of verwijdert ze als de salarisverwerking is teruggedraaid. Bij soort trigger *Salarisgegevens* gaat het om het tijdvak op de triggerregel; bij *Stamgegevens* om **alle tijdvakken binnen het venster** van die werkgever en periodetabel. Hier past de taak de **filters op soort inkomstenverhouding, aard arbeidsverhouding en soort medewerker** toe (§3.2) — een tijdvak dat niet meer kwalificeert verliest zijn bronregel — en bepaalt ze per berekening de **brontabel** (§3.3): een berekening die aan een plaatsing hangt naar bron uitzendkrachten, een periodeverwerking naar bron medewerkers, en bij *Plaatsingen verwerken in periodeverloning* naar allebei;
4. toetst per triggerregel of het tijdvak binnen dat venster valt; werkgevers waarvoor geen enkele regel binnen het venster valt, worden niet opnieuw doorgerekend;
5. bepaalt per werkgever en periodetabel het RSIN uit het loonheffingsnummer (§5.2) en werkt de bijbehorende rapportageperiode met soort Recht op informatie bij;
6. selecteert de arbeidsverhoudingen uit de brontabellen — de filters uit §3.2 zijn in stap 3 al toegepast — en laat daarbij medewerkers weg die niet onder Nederlandse wetgeving vallen (§9.6);
7. leest per arbeidsverhouding de tijdvakken binnen het venster uit de bijbehorende brontabel, zo nodig over twee kalenderjaren. Subdienstverbanden zijn daarin bij medewerkers al samengenomen (§5.3);
8. berekent per tijdvak het brutoloon en de waarde variabele componenten, telt die op per functie, per functiecategorie en per verkooprelatie, bepaalt de kenmerken en schrijft de regel per inkomstenverhouding;
9. stelt de tabel per functiecategorie opnieuw samen voor de geraakte rapportage-eenheden, inclusief de tien loonverschilpercentages in de rekenrichting die bij de soort rapportage hoort (§6.5);
10. gaat **terug naar laag 2** en vult per regel het individuele loonverschil, nu de groepsgemiddelden bekend zijn;
11. verwijdert de regels die niet meer aan de selectie voldoen en ruimt de verwerkte triggerregels op.

**Stap 10 is een tweede rekenslag over laag 2.** Het individuele loonverschil hoort bij de arbeidsverhouding en staat daarom op laag 2 (§5.4), maar het heeft het gemiddelde totaal uurloon van de hele functiecategorie nodig — en dat ontstaat pas in stap 9. De lagen worden dus niet strikt één keer van onder naar boven opgebouwd: laag 2 wordt aan het eind nog één keer aangeraakt. Alleen dat ene veld wordt dan geschreven; de rest van de regel blijft ongemoeid.

Het alternatief — het percentage bij het openen van de pagina berekenen — valt af op uitgangspunt 1: de KPI rekent niet. Het op laag 3 zetten kan niet, want laag 3 heeft één regel per functiecategorie en geen regel per medewerker.

**Het venster wordt nu vóór het bijwerken bepaald.** In een eerdere opzet gebeurde dat erna: de bronregels werden per triggerregel weggeschreven en pas daarna werd het venster vastgesteld. Dat kan niet meer, omdat stap 3 bij een stamgegeven-trigger moet weten welke tijdvakken in het venster vallen. De vensterbepaling is daarom van stap 3 naar stap 2 verplaatst; aan de bepaling zelf verandert niets.

**Stap 3 bevat de drie filters en de keuze van de brontabel.** Ze horen bij het vullen en niet bij het samenstellen erboven. Een tijdvak dat op soort inkomstenverhouding, aard of soort medewerker afvalt, krijgt geen bronregel, zodat de brontabellen — die het dashboard rechtstreeks leest — alleen bevatten wat meetelt (§3.2). Bestond er al een bronregel en kwalificeert het tijdvak niet meer, dan verwijdert stap 3 die. En welke tabel een berekening krijgt, is een eigenschap van die berekening: hangt ze aan een plaatsing of niet. Dat is alleen bij het lezen van de salarisgegevens te zien.

**De gebouwde taak deelt nog in op het type periodetabel.** Periodeverwerking gaat daar naar bron medewerkers, declaratieverwerking naar bron uitzendkrachten. Voor alle varianten behalve *Plaatsingen verwerken in periodeverloning* levert dat dezelfde uitkomst op. Die variant draait op een periodetabel van het type periodeverwerking, en zou dus alleen in bron medewerkers belanden. De aanpassing staat als punt AN-b in hoofdstuk 12.

**Stap 3 kent geen venstertoets.** De brontabel wordt bijgewerkt voor elke openstaande triggerregel, ook als het tijdvak ver buiten het venster ligt. Dat is nodig omdat de brontabellen niet worden opgeschoond (§5.6): DP2 moet later een compleet afgesloten kalenderjaar kunnen vaststellen, en een late correctie hoort ook dan nog in de feiten terecht te komen.

**Een stamgegeven-trigger herbouwt het hele venster aan bronregels.** Bij een salarisgegevens-trigger werkt stap 3 alleen het tijdvak op de triggerregel bij, want daar is precies dat ene tijdvak gewijzigd. Bij een stamgegeven-trigger ligt dat anders.

De reden zit in wat laag 1 vastlegt. Die tabellen bevatten naast de verwerkte bedragen ook **stamgegevens**: de functie, de functiecategorie, het geslacht, de soort en de aard van de inkomstenverhouding en — bij een uitzendkracht — de plaatsing en de verkooprelatie (§5.3). Aan de bedragen verandert een functiewijziging of een herindeling van functiecategorieën niets; aan die stamgegevens wél, en dan over alle tijdvakken waarin de medewerker in die functie werkte. Zouden we alleen het tijdvak op de triggerregel bijwerken, dan stond de nieuwe indeling op één bronregel en de oude op de tijdvakken daarvoor — en zou laag 2 het loon verdelen over twee functiecategorieën die in werkelijkheid één vergelijkingsgroep vormen (§5.4).

We halen de bronregels daarom voor het hele venster opnieuw op. De berekende bedragen worden daarbij ongewijzigd overgeschreven — dat kost rekentijd maar levert dezelfde waarden op (§7.4) — en de stamgegevens komen op de actuele stand.

Dit geldt voor soort rapportage **Recht op informatie**. Dat is de enige soort die dit deelproject vult (§5.2), en het venster is daar het voortschrijdende jaar. Buiten dat venster blijft de bronregel staan zoals hij was: oudere regels houden de functie en de functiecategorie die golden toen ze voor het laatst zijn weggeschreven. Voor dit ontwerp is dat geen probleem, want de medewerker ziet alleen het venster. Wat het betekent voor een afgesloten kalenderjaar met soort *Rapportage*, hoort bij DP2 (hoofdstuk 12, punt AI-a).

Stap 4 filtert pas daarna. Een correctie op een tijdvak van twee jaar geleden verandert niets aan wat de medewerker ziet en hoeft dus geen volledige doorrekening van die werkgever uit te lokken — maar de bronregel is dan wel bijgewerkt.

**Stap 6 bevat een landtoets.** In de opzet op de loonaangifte was die niet nodig: de brontabel werd alleen door de Nederlandse loonaangifte gevuld, dus de gegevens filterden zichzelf. Nu de brontabellen uit de salarisverwerking komen, gaat die vlieger niet meer op en moet de taak het land van wetgeving expliciet toetsen (§9.6).

De taak leest de berekende salarisgegevens en schrijft ze door naar de brontabellen; ze wijzigt die salarisgegevens zelf niet. Vanaf stap 6 is het puur leeswerk op de eigen tabellen.

De rekenroutine in stap 8 krijgt het periodebereik als parameter mee. In fase 1 is dat het venster. Datzelfde mechanisme vult in fase 2 een rapportageperiode met soort Rapportage, zonder tweede rekenimplementatie en dus zonder tweede waarheid.

**De soort rapportage gaat als tweede parameter mee**, naar de stappen 9 en 10. Die bepaalt de rekenrichting van de elf percentages: bij *Recht op informatie* telt de teller vanuit de vrouwen — en bij het individuele percentage vanuit de eigen waarde — en bij *Rapportage* andersom (§6.5). Het is dus geen tweede rekenimplementatie maar één routine met een omgekeerd teken, zodat er ook hier geen tweede waarheid ontstaat. De soort staat op de rapportageperiode die in stap 5 is bepaald en hoeft dus nergens te worden afgeleid.

De taak stelt de gegevens bij elke run volledig opnieuw samen voor de werkgevers die aan de beurt zijn. Er wordt niet bijgewerkt op basis van een vorige stand. Dat maakt het proces voorspelbaar: elke run geeft hetzelfde resultaat bij dezelfde brongegevens. Het maakt het ook uitlegbaar, want elk getal op het scherm is terug te volgen naar de perioden en loongegevens eronder.

**Er komt geen knop om de taak handmatig te starten.** De taak draait uitsluitend vanuit de dagovergang, op basis van de triggertabel. Een klant die zijn functiecategorieën heeft ingericht of die een correctie heeft doorgevoerd, wacht dus tot de eerstvolgende nacht. Dat is in de regel geen probleem: de wettelijke reactietermijn op een informatieverzoek is twee maanden (§7.1), en de cijfers lopen maximaal één dagovergang achter.

Dat betekent ook dat een run **niets doet als er geen triggerregel openstaat**. De taak begint met het lezen van de triggertabel (stap 1); is die leeg, dan is er niets te verwerken. Wie verwacht dat een run een afwijkend getal herstelt, moet dus eerst nagaan of de gebeurtenis die dat getal raakt wél een triggerregel heeft weggeschreven (§7.2).

De taak leest bestaande tabellen en schrijft uitsluitend naar de vier lagen en naar de triggertabel. Ze wijzigt geen salarisgegevens.

### 7.4 Omvang van een run

Stap 5 tot en met 8 raken alleen de werkgevers waarvoor een triggerregel binnen het venster openstond. Het venster wordt toch al per werkgever en periodetabel bepaald, en werkgevers zonder wijziging leveren dezelfde uitkomst als de vorige run.

De zwaarste run is die na een wijziging in de functiecategorie-inrichting: dan staan er triggerregels voor alle werkgevers open en rekent de taak de hele omgeving door (§7.2). Dat komt weinig voor — een klant herziet zijn functiecategorieën niet dagelijks — en het is de enige manier om de vergelijkingscijfers op de nieuwe indeling te krijgen. Bij een reguliere run gaat het om de werkgevers die die dag daadwerkelijk iets hebben gewijzigd.

**Een stamgegeven-trigger is zwaarder dan een salarisgegevens-trigger.** Niet in het aantal triggerregels, maar in stap 3: daar worden niet de bronregels van één tijdvak maar die van het hele venster opnieuw weggeschreven (§7.3). Bij maandverloning is dat twaalf keer zoveel schrijfwerk, bij weekverloning tweeënvijftig of drieënvijftig keer. Het rekenwerk eronder is er niet lichter op: de bedragen komen ongewijzigd terug, maar ze moeten wel opnieuw uit de berekende salarisgegevens worden opgehaald.

De twee Flex-triggers zijn dezelfde bewerking op een kleiner bereik. De trigger op de **functie van de klantovereenkomst** raakt alleen de uitleners die bij die ene inlener plaatsen, de trigger op de **afwijkende functiecategorie** maar één werkgever (§7.2). Beide herbouwen voor die werkgevers wél het hele venster.

Stap 9 is breder. De tabel per functiecategorie gaat per **rapportage-eenheid**, en meerdere werkgevers kunnen tot dezelfde eenheid horen. Verandert er iets bij één werkgever, dan verandert het gemiddelde van de hele groep. De taak stelt die regels daarom opnieuw samen op basis van de regels per inkomstenverhouding van **alle werkgevers binnen die eenheid**, ook al zijn die zelf niet opnieuw doorgerekend. Dat is een goedkope bewerking: het is een optelling over regels per inkomstenverhouding, niet over tijdvakken.

Beperken we die stap wel tot één werkgever, dan zouden de vergelijkingscijfers de bijdrage van de andere werkgevers verliezen. Daarom is dit de enige stap die buiten de eigen werkgever kijkt. Omgekeerd kan één werkgever ook over **twee** rapportage-eenheden verdeeld zijn, als hij twee loonheffingsnummers met een verschillend RSIN voert (§5.2); stap 9 raakt dan beide eenheden.

**Bij een uitlener is de run structureel zwaarder.** Sinds 22 september 2026 vult dit deelproject ook de populatie *Ter beschikking gestelde arbeidskrachten* (§5.3). Dat verandert niets aan de **werkwijze** — dezelfde stappen, hetzelfde venster, dezelfde verdichting — maar wel aan de **omvang**, en op drie manieren tegelijk:

- **Meer regels per persoon.** De brontabel gaat per plaatsing en niet per dienstverband. Eén uitzendkracht die in een jaar bij vier inleners werkt, levert vier reeksen tijdvakken op in plaats van één.
- **Meer tijdvakken per jaar.** Uitzendkrachten worden overwegend per week verloond. Dat zijn 52 of 53 tijdvakken tegenover twaalf bij maandverloning (§4.3), dus per plaatsing ruim vier keer zoveel bronregels als bij een eigen medewerker.
- **Meer regels op laag 3.** Bij deze populatie zit de verkooprelatie in de sleutel (§5.5). Waar een werkgever met eigen medewerkers één regel per functiecategorie en geslacht krijgt, krijgt een uitlener er één per inlener daarbinnen.

Wat **niet** toeneemt, is het aantal triggerregels: die gaan per werkgever, periodetabel en tijdvak, en niet per persoon of plaatsing (§7.2). Een uitzendbureau dat duizend uitzendkrachten in één weekverwerking verloont, schrijft daarvoor één triggerregel weg, net als een werkgever met tien eigen medewerkers. De werkvoorraad groeit dus niet; de hoeveelheid werk per regel wél — en bij een stamgegeven-trigger sterker dan bij een salarisgegevens-trigger.

Voor het bouwen betekent dit dat de taak niet mag uitgaan van de ordegrootte die bij eigen medewerkers hoort. De zwaarste denkbare run is niet de wijziging in de functiecategorie-inrichting bij een doorsnee werkgever, maar diezelfde wijziging bij een uitzendbureau met weekverloning: voor alle werkgevers in de omgeving drieënvijftig tijdvakken aan bronregels, per plaatsing.

**Gelijktijdige runs binnen één rapportage-eenheid.** Met één taak vanuit de dagovergang is dit grotendeels opgelost: de taak verwerkt de rapportage-eenheden één voor één, dus twee werkgevers binnen hetzelfde concern kunnen elkaars verdichting niet meer overschrijven. In de eerdere opzet — één wachtrijtaak per verwerking — kon dat wel, en dat herstelde zich niet vanzelf.

De eis blijft toch staan dat er per rapportage-eenheid nooit meer dan één run tegelijk loopt. Met alleen de dagovergang als startmoment is dat geval zeldzaam — er is geen handmatige start die ermee kan samenvallen (§7.3) — maar het is niet uitgesloten: een zware run kan nog lopen wanneer de volgende dagovergang begint, en bij beheer kan een taak opnieuw worden aangeboden. De eis luidt daarom:

- Start een taak terwijl er al een run bezig is die dezelfde rapportage-eenheid raakt, dan **wacht** die tot de lopende klaar is. Ze wordt niet afgebroken en niet overgeslagen.
- Staan er meerdere runs te wachten, dan is één keer doorrekenen genoeg. De taak stelt alles volledig opnieuw samen (§7.3), dus de laatste wachtende run levert hetzelfde resultaat als alle wachtende runs achter elkaar.
- Het wachten geldt voor de **hele** run, niet alleen voor stap 9. De stappen ervoor schrijven de bronregels en de regels per inkomstenverhouding waar de verdichting op steunt.
- Runs voor **verschillende** rapportage-eenheden mogen wel gelijktijdig lopen. Die raken elkaars regels niet.

Hoe dat wachten wordt gerealiseerd — een lock op de rapportage-eenheid of een wachtrij met één actieve taak — hoort bij het technisch ontwerp (§12, punt E1). Het wachten is voor de gebruiker onzichtbaar: de taak loopt buiten het salarisproces om.

### 7.5 Correcties

Corrigeert een salarisverwerking een eerder tijdvak, dan schrijft het accorderen daarvoor een eigen triggerregel weg, naast die voor het tijdvak zelf (§7.2). Bij de eerstvolgende run overschrijft de taak de bestaande regel in de brontabel met de gecorrigeerde stand; er komt geen tweede regel bij. De brontabel bevat daarmee altijd de **laatste verwerkte stand** per tijdvak.

De taak stelt de twee tabellen erboven in dezelfde run opnieuw samen, dus de bedragen worden vanzelf goed. Dat geldt ook voor een **jaaroverschrijdende** correctie: die volgt dezelfde route en hoeft niet apart te worden afgehandeld.

Dit heeft twee gevolgen die we accepteren:

- **Er is geen correctiehistorie.** Wat er eerder is verstrekt, is niet meer op te vragen. Dat is functioneel gewenst — de medewerker hoort de juiste bedragen te zien — maar het betekent ook dat het dashboard een piek in een tijdvak niet als correctie kan herkennen.
- **Het venster begrenst wat meetelt.** Valt het gecorrigeerde tijdvak buiten het venster, dan werkt de taak de regel in de brontabel wel bij, maar telt hij niet mee in de regel per inkomstenverhouding (§7.3). Dat is de consequentie van een venster van één jaar en het geldt voor elke correctie die verder terugreikt. De feiten blijven wel vastgelegd, zodat DP2 er later over kan rapporteren.

De correctie verschuift het venster niet. Het eindpunt blijft het laatste geaccordeerde reguliere tijdvak. Zo voorkomen we dat een correctie op bijvoorbeeld periode 12 van 2025 het venster terugzet terwijl de werkgever al op periode 3 van 2026 zit. Een correctietijdvak raakt bovendien vaak maar een kleine groep medewerkers en is dus geen geschikt ijkpunt.

### 7.6 Terugdraaien van een salarisverwerking

Een werkgever kan een geaccordeerde salarisverwerking terugdraaien. Het terugdraaien schrijft daarvoor een triggerregel weg, net als het accorderen. Bij de eerstvolgende run verwijdert de taak de bijbehorende regels uit de brontabel, bepaalt opnieuw wat het laatste geaccordeerde tijdvak is en schuift het venster een tijdvak terug. De medewerker ziet daardoor tijdelijk oudere cijfers, tot er opnieuw is geaccordeerd.

Dat is bewust: het venster volgt altijd het laatste geaccordeerde tijdvak. Cijfers laten staan van een tijdvak dat is teruggedraaid, zou betekenen dat we loongegevens tonen die niet meer zijn verwerkt.

Tot de eerstvolgende dagovergang staan de teruggedraaide bedragen nog in de tabellen. Dat is dezelfde vertraging als bij elke andere wijziging (§7.1) en raakt hooguit de dag waarop wordt teruggedraaid.

### 7.7 Hoe de tabellen vollopen

De brontabellen zijn nieuw en beginnen dus **leeg**, bij iedere klant. Om te voorkomen dat elke klant een jaar moet wachten tot het venster vol is, vullen we in de **conversie naar Profit 9** de triggertabel.

**Wat de conversie doet.** Ze schrijft triggerregels weg voor alle **periodes van 2026**, per verloonde werkgever en per periodetabel. Ze vult zelf geen loongegevens en rekent niets uit; ze zet alleen werkvoorraad klaar.

**De eerstvolgende dagovergang doet de rest.** De taak leest die triggerregels, bouwt daarmee de brontabel op uit de berekende salarisgegevens van 2026 (§7.3, stap 3) en stelt de lagen erboven samen. Na één nacht staat er dus een gevuld venster in plaats van een lege tabel.

Dat kan omdat de taak de brontabel sowieso al uit de berekende salarisgegevens opbouwt. Er is geen aparte conversieroutine nodig die dezelfde bedragen op een tweede manier bepaalt, en dus ook geen tweede definitie die kan afwijken van de reguliere weg. De conversie hoeft alleen te weten *welke* werkgevers, periodetabellen en periodes er in 2026 zijn verloond.

**Dit herziet de keuze om helemaal geen conversie te doen.** Het eerdere argument was dat een conversie de bedragen niet betrouwbaar zou kunnen reconstrueren. Dat argument gold voor een conversie die zelf gaat rekenen of die uit de loonaangiftegegevens put. Hier gebeurt dat niet: de gegevens worden door de reguliere taak langs de reguliere weg opgehaald. Wat er in een omgeving niet meer staat — een verwijderde verwerking — levert simpelweg geen bronregel op, precies zoals bij een reguliere run.

**Alleen 2026.** Tijdvakken van vóór 2026 vullen we niet. Valt het begin van het venster in 2025, dan blijven die tijdvakken leeg en rekent de taak met de tijdvakken die er wél zijn. Dat lost zichzelf op naarmate het venster opschuift.

**Nieuwe klanten hebben geen conversie.** Die beginnen leeg en lopen vol vanaf de eerste geaccordeerde salarisverwerking: elk geaccordeerd tijdvak voegt er één toe, en na ongeveer een jaar is het venster volledig gevuld.

**De overstap naar Plaatsingen verwerken in periodeverloning.** Deze variant wordt ondersteund vanaf loonjaar 2027. Een detacheerder die hem aanzet, verloont in 2026 nog op gewone periodeverwerking en vanaf 2027 ook per plaatsing. Het venster van een jaar loopt over die grens heen. Voor de twee populaties pakt dat verschillend uit:

- **Bron medewerkers loopt zonder breuk door.** Daarin staat zowel vóór als na de overstap het totale loon van de inkomstenverhouding (§3.3). Het venster blijft vol en de vergelijking binnen de eigen functiecategorie verandert niet van grondslag.
- **Bron uitzendkrachten begint pas in 2027.** Over 2026 is er geen loon per plaatsing, dus het venster voor deze populatie loopt vanaf de overstap vol, net als bij een nieuwe klant. Dat aanvaarden we, om dezelfde reden als bij de uitzendkrachten in de conversie (hoofdstuk 10): eerst de opslag, dan een volledig venster.

Er is daarom geen aparte conversie voor deze overstap nodig.

Wat de medewerker ziet zolang er nog weinig tijdvakken zijn, staat in §8.6. Het uurloon en de loonverschilpercentages op uurbasis zijn vanaf het eerste tijdvak zinvol, omdat ze loon en uren tegen elkaar afzetten. Het bruto jaarloon en de jaarwaarde zijn dat pas als het venster vol is; die komen niet op het scherm (§8.2).

Dat een venster tijdelijk niet vol is, is ook wettelijk geen probleem. De werkgever moet een informatieverzoek beantwoorden binnen een redelijke termijn en uiterlijk binnen **twee maanden** na de datum van het verzoek. Dat staat in artikel 10b, derde lid van het wetsvoorstel en volgt artikel 7, vierde lid van de richtlijn.

### 7.8 Als de taak niet slaagt

De bestaande gegevens blijven staan tot de nieuwe generatie compleet is. Een mislukte run mag er nooit toe leiden dat de medewerker een lege of half gevulde KPI ziet.

Daarvoor werkt de taak **transactioneel per rapportage-eenheid**. Binnen één transactie schrijft en stelt ze achtereenvolgens opnieuw samen:

1. de bronregels van de tijdvakken die uit de openstaande triggerregels volgen — het tijdvak zelf bij soort trigger *Salarisgegevens*, het hele venster bij *Stamgegevens* (§7.3);
2. de regels per inkomstenverhouding van de werkgevers die aan de beurt zijn;
3. de regels per functiecategorie van de hele rapportage-eenheid;
4. de rapportageperiode, met de datum van de laatste berekening als laatste schrijfactie.

Slaagt een van die stappen niet, dan rolt de hele transactie terug en blijft de vorige generatie ongewijzigd staan. Er is dus geen tussenstand waarin de brontabel al een nieuw tijdvak bevat en laag 2 nog niet, of waarin een deel van de functiecategorieën nieuw is en een deel oud.

**De triggerregels blijven bij een fout staan.** Ze worden pas opgeruimd als de transactie voor die rapportage-eenheid is geslaagd. Daardoor pakt de volgende dagovergang precies op waar het misging, zonder dat iemand hoeft te achterhalen welke werkgevers zijn overgeslagen en zonder dat de taak handmatig opnieuw hoeft te worden gestart. Loopt een rapportage-eenheid vast, dan gaat de taak wel door met de overige eenheden; één probleemgeval mag de rest niet blokkeren.

De datum van de laatste berekening schrijven we bewust als laatste. Die datum is daarmee het bewijs dat de hele set compleet is: staat er een oude datum, dan is de laatste run niet geslaagd, en dat is zichtbaar in de weergaven en bij de informatie die aan de medewerker wordt verstrekt.

De taak schrijft alleen naar de vier lagen en naar de triggertabel. De berekende salarisgegevens waaruit ze de brontabel vult, leest ze alleen; een mislukte run kan die dus nooit raken.

De verwerking is idempotent. De taak stelt alles volledig opnieuw samen en werkt niet bij op basis van een vorige stand, dus een mislukte run kan zonder voorbereiding opnieuw worden gestart en levert bij dezelfde brongegevens hetzelfde resultaat. Er is geen herstelroutine nodig die een halve stand repareert.

De omvang van de transactie is de betrokken werkgevers voor laag 1 en 2 en één rapportage-eenheid voor laag 3. Bij een concern met veel werkgevers kan dat een lange transactie opleveren. Dat raakt het salarisproces niet, omdat de taak daarbuiten loopt, maar het is wel de reden om de verdichting per rapportage-eenheid te serialiseren (§7.4).

Op de rapportageperiode staat de datum van de laatste berekening, en op de regel per inkomstenverhouding staan daarnaast de begin- en einddatum van het venster (§5.4). Daarmee is altijd zichtbaar hoe actueel de gegevens zijn, ook als een run is mislukt.

## 8 Presentatie: stamkaart en Pocket

### 8.1 Waar de medewerker het vindt

Er komt een sectie **Loontransparantie** op de **standaard** stamkaarten in InSite. Op drie ervan:

| Stamkaart | Wie kijkt |
| --- | --- |
| Medewerker stamkaart ESS | De medewerker zelf |
| Medewerker stamkaart MSS | De leidinggevende of HR, kijkend naar een medewerker |
| Plaatsing stamkaart | De intercedent of HR bij de uitlener, kijkend naar een ter beschikking gestelde arbeidskracht |

**Welke stamkaart cijfers toont, volgt uit de populatie** (§3.3, §5.9). De medewerker-stamkaarten tonen de populatie *Medewerkers*, de plaatsing-stamkaart de populatie *Ter beschikking gestelde arbeidskrachten*. Bij declaratieverwerking staan er dus alleen cijfers op de plaatsing, bij gewone periodeverwerking alleen op de medewerker.

**Een detacheerder met Plaatsingen verwerken in periodeverloning heeft cijfers op beide.** Op de stamkaart van de medewerker staan zijn totale loon en de vergelijking met zijn eigen functiecategorie; op de stamkaart van de plaatsing het deel dat aan die plaatsing is toegerekend, vergeleken met de uitzendkrachten bij dezelfde inlener. Die twee sets verschillen per definitie: ze gaan over een ander loon en over een andere vergelijkingsgroep. Dat moet in de help en in de uitleg bij de tegels te volgen zijn, zodat niemand het verschil voor een fout aanziet (hoofdstuk 12, punt AN-e).

**Alleen op de standaard stamkaart.** We maken de KPI's niet beschikbaar op vrije stamkaarten die een klant zelf heeft ingericht. Zo houden we één plek waar deze cijfers staan, met één set teksten en één autorisatie erop. Het gaat om gevoelige beloningsinformatie; die willen we niet op onbekende plekken laten opduiken.

**Het tabblad staat onder Salaris, als laatste.** *Loontransparantie* komt op de onderste plek in die groep, onder de bestaande tabbladen zoals Salaris, Voorschot, Declaratie en Loonbeslag. Onder Salaris omdat het over beloning gaat; onderaan omdat het geen tabblad is dat een medewerker dagelijks nodig heeft. De tabbladen erboven horen bij lopende zaken — een declaratie, een voorschot, de loonstrook — en die wil je niet naar beneden duwen voor een pagina die een paar keer per jaar wordt geopend.

**Opbouw van de sectie**, van boven naar beneden:

1. De vijf **KPI-tegels** (§8.2).
2. Het pagina-onderdeel **Functie** met de functie, de functiecategorie en de toelichting daarop (§8.3).
3. De weergave **Functies in functiecategorie** (§8.4).
4. De actieknop **Vraag aan HR**.

**De tegels staan bovenaan omdat het niet anders kan.** Op de standaard stamkaart staan de KPI's altijd boven aan de pagina; daarboven is geen titel of tekst te plaatsen. De omschrijving van de functiecategorie en de toelichting daarop komen daarom als **pagina-onderdeel** erónder te staan.

Dat is de omgekeerde volgorde van wat inhoudelijk het prettigst leest. Zonder te weten met wíe hij wordt vergeleken, is een percentage voor de medewerker betekenisloos. We vangen dat op in de **subtitel van de tegels**: die noemt de functiecategorie bij naam (§8.2). Wat daar niet in past is de toelichting bij die categorie; die staat pas onder de tegels. Dat is de prijs van deze beperking.

**De sectie krijgt een vaste toelichting.** Naast de toelichting die de werkgever bij de functiecategorie vastlegt (§8.3), krijgt de sectie zelf een vaste tekst. Die zegt waar de pagina over gaat: de medewerker heeft vanuit de richtlijn recht op inzicht, zijn salaris wordt vergeleken met dat van collega's in dezelfde functiecategorie, en de werkgever bepaalt welke functies daarin vallen. De tekst verschilt per stamkaart. Op ESS staat hij in de je-vorm, op MSS in de de-medewerkervorm. Op de plaatsing-stamkaart noemt hij de **opdrachtgever** in plaats van de werkgever, omdat de vergelijkingsgroep daar de functiecategorie binnen één inlener is (§6.3). De teksten staan in §8.7.

De twee toelichtingen zijn verschillende dingen. Die van de sectie is een vaste tekst van AFAS, gelijk voor iedere klant. Die in het pagina-onderdeel *Functie* is een vrije tekst van de werkgever over één functiecategorie.

**De toelichting wordt met een script geleverd.** De tekst is nog niet als metagegeven in te checken. Daarom zet een script hem op de drie standaard stamkaarten. Op welk record hij landt, stemmen we af met de programmeur (punt AO-a, actie 46).

**De actieknop Vraag aan HR** start de **profielkeuzepagina** van het type dossieritem Vraag aan HR (DP4). De medewerker kiest daar zelf welk profiel hij nodig heeft.

We starten bewust **niet** direct het profiel *Recht op informatie* op. Dat profiel levert dezelfde cijfers op als de pagina waar de medewerker net vandaan komt, alleen in een rapport. Wie op deze pagina op *Vraag aan HR* klikt, heeft juist vaak een **andere** vraag: waarom het verschil er is, hoe zijn functie is ingedeeld, of iets wat helemaal los staat van loontransparantie. Door de profielkeuze te tonen komt die vraag bij het juiste profiel terecht in plaats van in een verzoek om informatie die hij al heeft gezien.

Dat is de aanvullende route uit de praatplaat: de KPI's zijn de laagdrempelige basis, de vraag aan HR is de weg voor wie meer wil weten of meerdere dienstverbanden heeft (§8.5).

De medewerker ziet het eigen loonniveau en de vergelijkingscijfers van de eigen functiecategorie. Alle getoonde waarden komen uit één regel per inkomstenverhouding en één regel per functiecategorie; er wordt bij het openen van de pagina niets herberekend. Ook de loonverschilpercentages en het individuele loonverschil zijn voorberekend (§5.4, §5.5). Welke regel per inkomstenverhouding dat is als er meerdere zijn, staat in §8.5.

De cijfers zijn zo actueel als de laatste geslaagde run van de taak Bijwerken gegevens loontransparantie (§7.1). Die draait doorgaans elke nacht vanuit de dagovergang, maar hij werkt alleen bij wat is geraakt: de taak leest de triggertabel (§7.2) en rekent alleen de werkgevers door waarvoor een triggerregel openstaat.

In de praktijk worden de gegevens dus bijgewerkt na het **accorderen van een salarisverwerking** — de gebeurtenis die de triggerregels wegschrijft, voor het geaccordeerde tijdvak en voor elk tijdvak dat met terugwerkende kracht is geraakt. Daarnaast schrijven een functiewijziging, een wijziging in de functiecategorie-inrichting en de twee Flex-gegevens uit §7.2 een triggerregel weg. Gebeurde er geen van die dingen, dan verandert er aan de getoonde cijfers niets, hoe vaak de dagovergang ook draait. Gebeurde er wél iets, dan is dat de eerstvolgende nacht zichtbaar.

### 8.2 De vijf KPI-tegels

De tegels staan in twee rijen, in deze volgorde:

| Rij | Nr. | Titel ESS | Titel MSS en plaatsing | Type | Wat de tegel toont |
| --- | --- | --- | --- | --- | --- |
| 1 | 1 | Hoeveel verdien ik per uur? | Hoeveel verdient de medewerker per uur? | Value | Het eigen totaal uurloon |
| 1 | 2 | Gemiddeld uurloon binnen functiecategorie | Gelijk aan ESS | Chart, gestapelde horizontale staaf | Het eigen uurloon naast dat van de mannen en de vrouwen, elk gesplitst in basisloon en extra's |
| 1 | 3 | Samenstelling functiecategorie | Gelijk aan ESS | Chart, donut | Het aantal mannen en vrouwen in de functiecategorie |
| 2 | 4 | Verdien ik meer of minder dan mijn collega's? | Verdient de medewerker meer of minder dan collega's? | Value | Het individuele loonverschil ten opzichte van het gemiddelde van de functiecategorie |
| 2 | 5 | Wat is het verschil tussen mannen en vrouwen? | Gelijk aan ESS | Value | Het loonverschilpercentage op het gemiddelde totaal uurloon |

**De titel stelt de vraag die de tegel beantwoordt.** Tegel 1 en 4 gaan over de medewerker zelf en hebben daarom twee vormen, net als de teksten (§8.7). De tegels 2, 3 en 5 gaan over een groep en heten op elke stamkaart hetzelfde.

**Eerst de feiten, dan de conclusies.** De bovenste rij beantwoordt drie feitelijke vragen: *wat verdien ik* (1), *hoe verhoudt zich dat tot mijn functiecategorie* (2) en *hoe groot is die groep* (3). De onderste rij trekt daar twee conclusies uit, van persoonlijk naar collectief: *hoe sta ik ervoor binnen mijn functiecategorie* (4) en *is er een verschil tussen mannen en vrouwen* (5).

Die volgorde is bewust. Een percentage zegt niets zonder de bedragen en de groepsgrootte waar het uit voortkomt. Door de feiten boven de percentages te zetten, leest de medewerker eerst waar de conclusie op rust. Het maakt ook de overgang naar het pagina-onderdeel eronder logisch: dat legt uit welke functies in de categorie vallen waar alles over ging.

**Alles staat op uurbasis.** Geen enkele tegel toont een jaarbedrag of een aantal uren. Die zijn nodig om te kunnen rekenen, maar niet om te kunnen begrijpen, en ze leidden in eerdere versies vooral af. De verloonde uren staan nog wél in de uitleg achter het info-icoon van tegel 1, zodat het uurloon na te rekenen blijft.

**De subtitel noemt de vergelijkingsgroep.** Omdat er niets boven de tegels kan staan (§8.1), draagt de subtitel de context. Bij de tegels 2 tot en met 5 is dat de **functiecategorie**: *Management · laatste 12 maanden*. Bij tegel 1 is dat de **eigen functie**: *Teamleider · laatste 12 maanden*. Dat onderscheid is nodig, want tegel 1 gaat niet over de categorie maar over het eigen dienstverband; de categorie in die subtitel zou suggereren dat het bedrag een groepsgemiddelde is.

De functie in die subtitel doet nog iets: ze maakt zichtbaar wélk dienstverband de medewerker ziet. Bij meerdere gelijktijdige dienstverbanden tonen we het hoofddienstverband (§8.5), en dit is de enige plek op de pagina waar dat blijkt.

**Tegel 1: Hoeveel verdien ik per uur?**

| Kenmerk | Invulling |
| --- | --- |
| Type | Value |
| Subtitel | De eigen functieomschrijving, gevolgd door *laatste 12 maanden* |
| Waarde | Het totaal uurloon van de regel per inkomstenverhouding (§5.4) |
| Waardetype | Currency, met het valutasymbool van de werkgever (zie *Het valutasymbool* hieronder) |
| Bijschrift onder de waarde | *gemiddeld per uur* |
| Info-icoon | De opbouw uit basissalaris en extra's per uur, plus het aantal verloonde uren (§8.7) |

Dit is het enige bedrag op de pagina dat alleen over de medewerker zelf gaat. Het is bewust het **totaal** en niet het basisloon: wat iemand per uur verdient is voor hem één getal, niet twee. De splitsing komt in de tegel ernaast terug, als beeld in plaats van als begrip.

**Het bijschrift zegt dat het om een gemiddelde gaat.** De titel stelt een vraag en noemt geen gemiddelde meer. Zonder bijschrift zou het bedrag lezen als het actuele uurtarief. Wie in de afgelopen twaalf maanden een periodiek of een promotie kreeg, ziet een bedrag dat tussen het oude en het nieuwe in ligt; *gemiddeld per uur* maakt dat verklaarbaar.

**Tegel 2: Gemiddeld uurloon binnen functiecategorie**

| Kenmerk | Invulling |
| --- | --- |
| Type | Chart, chartType `StackedHorizontalBar` |
| Subtitel | De functiecategorie, gevolgd door *laatste 12 maanden* |
| Categorieën (verticale as) | Jij of Medewerker, Mannen, Vrouwen — in die volgorde |
| Datasets | Basisloon per uur en Extra's per uur, gestapeld |
| Waardetype | Currency, met het valutasymbool van de werkgever |
| Bron | De balk Jij uit de regel per inkomstenverhouding (§5.4); de balken Mannen en Vrouwen uit de tabel per functiecategorie (§5.5) |
| Grootte | Wide |
| Hamburger | Klapt om naar de onderliggende gegevens: basisloon, extra's en totaal per uur voor de drie groepen |
| Info-icoon | Geen. De legenda en de hamburger laten al zien wat er naast elkaar staat en waaruit elke balk is opgebouwd |

Deze tegel vervangt de vergelijkingstabel uit de eerdere versie (§6.4). Zes getallen in plaats van vijftien, en als verhouding in plaats van als cijferveld.

**Het stapelen is rekenkundig zuiver.** Basisloon en variabele componenten zijn per definitie disjunct: het bruto jaarloon is het loon **verminderd met** de variabele componenten (§6.1). De twee segmenten tellen dus precies op tot het totaal, en dat totaal is hetzelfde getal als in tegel 1. Voor de gemiddelden is dat gegarandeerd doordat het gemiddeld totaal uurloon als som van de twee gemiddelden is gedefinieerd (§6.3).

**De as begint bij nul.** Een verschil van enkele procenten oogt daardoor bescheiden. Dat is inhoudelijk juist en we corrigeren het niet: de as afkappen zou het beeld vertekenen en een klein verschil groot laten lijken. Dat de balken op elkaar lijken is precies wat er aan de hand is.

De eerste categorie heet **Jij** op de ESS-stamkaart en **Medewerker** op de MSS- en de plaatsing-stamkaart, om dezelfde reden als bij de teksten (§8.7). De volgorde is eerst de eigen waarde, dan de referentiegroep, dan de groep die daartegen wordt afgezet.

**De hamburger toont alleen wat in de grafiek zit.** Verloonde uren en bruto jaarloon kunnen daar technisch niet bij. De omklap toont dus dezelfde drie regels als de balk: basisloon, extra's en totaal per uur.

Ontbreekt een geslachtsgroep, dan vervalt die balk. Is er nog geen eigen regel, bijvoorbeeld na een recente functiewijziging, dan vervalt de balk Jij en blijven de twee gemiddelden staan (§8.5).

**Tegel 3: Samenstelling functiecategorie**

| Kenmerk | Invulling |
| --- | --- |
| Type | Chart, chartType `Donut` |
| Subtitel | De functiecategorie, gevolgd door *laatste 12 maanden* |
| Categorieën | Mannen, Vrouwen |
| Waarde | Aantal arbeidsverhoudingen mannen en vrouwen, uit de tabel per functiecategorie (§5.5) |
| Waardetype | Number |
| Info-icoon | Geen. Dat de donut arbeidsverhoudingen telt en geen personen, staat in de help |

**De donut telt alleen mannen en vrouwen.** Arbeidsverhoudingen met geslacht X of zonder ingevuld geslacht laten we buiten de grafiek, ook al tellen ze wel mee in het veld Aantal arbeidsverhoudingen totaal (§3.8, §6.7). De richtlijn splitst uit naar mannen en vrouwen, en de tegel hoort bij de percentages eronder die over diezelfde twee groepen gaan. Ook daarin is geen rekening gehouden met geslacht X; een derde partje zou de tegel als enige laten afwijken. Daar komt bij dat zo'n partje in de praktijk vaak uit één persoon bestaat en dan rechtstreeks naar een collega wijst.

Het totaal onder de donut is dus de som van mannen en vrouwen, en niet het veld Aantal arbeidsverhoudingen totaal. Dat verschil is klein en zelden zichtbaar, maar wie de tegel naast het dashboard legt moet het weten.

**Dit betekent dat we aantallen per geslacht tonen.** Dat deden we tot nu toe niet (§9.4). We doen het wél, omdat de percentages eronder zonder groepsgrootte niet te duiden zijn. Een verschil van acht procent in een categorie met drie arbeidsverhoudingen is iets heel anders dan hetzelfde percentage in een categorie met tweehonderd. Dat de aantallen in een kleine categorie herleidbaar zijn tot een individuele collega, is dezelfde afweging die bij de gemiddelden al is gemaakt en aanvaard (§9.3).

**Tegel 4: Verdien ik meer of minder dan mijn collega's?**

| Kenmerk | Invulling |
| --- | --- |
| Type | Value |
| Subtitel | De functiecategorie, gevolgd door *laatste 12 maanden* |
| Waarde | Het individuele loonverschil van de regel per inkomstenverhouding (§5.4, §6.5) |
| Waardetype | Percentage |
| Bijschrift onder de waarde | Drie varianten, één per teken: meer dan, minder dan of evenveel als het gemiddelde in de functiecategorie (§8.7) |
| Info-icoon | Het eigen uurloon, het gemiddelde van de functiecategorie en het verschil daartussen, als bedrag en als percentage (§8.7) |

Deze tegel beantwoordt de vraag die de groepscijfers openlaten: *en ik dan?* Hij zet de medewerker af tegen het gemiddelde van de **hele functiecategorie**, alle geslachten samen.

**Een positieve uitkomst betekent dat de medewerker méér verdient.** Het teken gaat uit van de eigen waarde: een plus staat boven het categoriegemiddelde, een min eronder (§6.5). Het bijschrift zegt hetzelfde in woorden, zodat de medewerker het teken niet hoeft te interpreteren.

**Nul is een eigen geval.** Komt het percentage op 0,00 uit, dan verdient de medewerker precies het categoriegemiddelde. Een bijschrift met *meer* of *minder* is dan onjuist, dus er is een derde variant (§8.7). Dit is iets anders dan de situatie waarin de medewerker de **enige** in zijn categorie is — het percentage is dan ook nul, maar daar toont de tegel geen percentage en staat er een melding (§8.6).

**Deze tegel toont het geslacht van de medewerker niet.** Dat was in een eerdere opzet wel zo, toen er tegen het eigen geslacht werd afgezet. Nu is de vergelijkingsmaat voor iedereen dezelfde, dus de tekst hoeft nergens "de mannen" of "de vrouwen" te noemen.

**Iedereen ziet deze tegel.** Ook medewerkers met geslacht X of zonder ingevuld geslacht: zij tellen mee in het categoriegemiddelde (§3.8). De tegel blijft alleen leeg als er geen functiecategorie is (§8.6).

**Tegel 5: Wat is het verschil tussen mannen en vrouwen?**

| Kenmerk | Invulling |
| --- | --- |
| Type | Value |
| Subtitel | De functiecategorie, gevolgd door *laatste 12 maanden* |
| Waarde | Het veld Loonverschil totaal uurloon, gelezen van de regel per functiecategorie (§5.5, §6.5) |
| Waardetype | Percentage |
| Bijschrift onder de waarde | Drie varianten, één per teken: vrouwen verdienen gemiddeld minder, meer, of evenveel als mannen (§8.7) |
| Info-icoon | De twee gemiddelden en het verschil daartussen, als bedrag en als percentage van het gemiddelde van de mannen (§8.7) |

Dit is het wettelijke kerngetal van de pagina: het loonverschil tussen mannen en vrouwen binnen de functiecategorie. De grondslag is het **totaal uurloon**, dus basisloon en variabele componenten samen (§6.5).

**Er is geen tweede percentage meer.** Een eerdere versie toonde het loonverschil apart op het basisloon en op de variabele componenten. Die splitsing is voor de medewerker moeilijk te plaatsen en maakt het recht op informatie complexer dan nodig. Het onderscheid blijft zichtbaar in de gestapelde balk van tegel 2, als bedrag in plaats van als percentage. De vier andere percentages worden wel berekend en vastgelegd, voor het dashboard en voor DP2 (§5.5).

Is de uitkomst **negatief**, dan verdienen vrouwen in deze categorie gemiddeld minder dan mannen. Dat is de gebruikelijke situatie. Is de uitkomst **positief**, dan draait het bijschrift om naar *Vrouwen verdienen gemiddeld meer dan mannen*. Teken en bijschrift wijzen daarmee dezelfde kant op: de min hoort bij minder, de plus bij meer. Komt het percentage op **0,00** uit, dan verdienen beide groepen gemiddeld evenveel; daar hoort een derde bijschrift bij (§8.7).

**De vrouwen blijven in alle drie de bijschriften het onderwerp.** Dat is dezelfde groep die in de teller van de formule vooraan staat (§6.5), dus het bijschrift leest in dezelfde volgorde als er gerekend wordt. Het alternatief — bij een plus overstappen op *Mannen verdienen gemiddeld minder dan vrouwen* — wisselt halverwege van onderwerp en dwingt de medewerker elke keer opnieuw te bepalen over wie het gaat.

**Het onderwerp van dit percentage zijn de vrouwen, niet de lezer.** Een man in een categorie waar vrouwen minder verdienen ziet dus een min, terwijl hij zelf meer verdient. Juist daarom benoemt het bijschrift de twee groepen en staat dit percentage nooit zonder bijschrift op het scherm. Zijn eigen positie leest hij in tegel 4, en die telt wél vanuit hemzelf.

**Het scherm en het opgeslagen veld tonen hetzelfde getal.** De omkering zit in de berekening en niet in de presentatie: het veld Loonverschil totaal uurloon is op een regel met soort Recht op informatie al met dat teken weggeschreven (§6.5). De KPI draait er niets aan om, conform uitgangspunt 1. De wettelijke rapportage van DP2 rekent de andere kant op, maar die cijfers staan op een andere regel en komen in deze ontsluiting niet voor (§5.9).

Is er geen gemiddelde voor een van beide groepen, dan blijft de tegel leeg met de melding uit §8.6.

**De bedragen achter de percentages staan in het info-icoon**

De tegels 4 en 5 zijn Value-tegels. Daar is **geen hamburger** op mogelijk: een Value-tegel toont één waarde en heeft geen onderliggende dataset om naar om te klappen. De bedragen waaruit het percentage volgt — de twee gemiddelden en het verschil, als bedrag en als percentage — staan daarom in de uitleg achter het **info-icoon**.

Dat vraagt wel dat die uitleg per medewerker wordt samengesteld, want de bedragen verschillen. Het is dus geen vaste vertaalde zin maar een tekst met ingevulde waarden. Dat is aanvaard, omdat een percentage zonder bedrag voor de medewerker weinig betekent: 8,59% klinkt fors, maar in euro's kan het om zeventien cent per uur gaan.

**Het verschil staat er met teken.** Het bedrag is het verschil tussen de twee getoonde bedragen, in dezelfde richting als het percentage: bij tegel 4 het eigen uurloon min het categoriegemiddelde, bij tegel 5 het gemiddelde van de vrouwen min dat van de mannen (§6.5). Bedrag en percentage wijzen dus dezelfde kant op, en één zin klopt bij een plus, een min en bij nul.

**Het valutasymbool**

Elk bedrag op de pagina krijgt het valutasymbool van de **werkgever** van het getoonde dienstverband: het veld *Valutasymbool* op de werkgever (AfasHrCurrencyId), met het symbool van die valuta. Is dat veld leeg, dan nemen we het symbool van de **basisvaluta** van de omgeving. Dat geldt voor tegel 1, tegel 2 en de uitleg achter de info-iconen van tegel 1, 4 en 5.

Op de plaatsing-stamkaart is dat de werkgever van het dienstverband van de uitzendkracht, dus de uitlener. De groepsgemiddelden in tegel 2 en in de uitleg bij tegel 4 en 5 krijgen hetzelfde symbool als de eigen bedragen. We rekenen niets om: het symbool zegt in welke valuta de bedragen staan, het verandert ze niet. In de praktijk is dat de euro, want de scope is Nederland (§9.6).

**De periode in de subtitel**

Na de functie of de functiecategorie volgt steeds **laatste 12 maanden**. Bij een andere periodetabel gaat het feitelijk om een ander aantal tijdvakken — dertien perioden, tweeënvijftig weken of vier kwartalen (§4.3) — maar voor de medewerker is dat steeds ongeveer een jaar. Daarom staat er één aanduiding op alle vijf de tegels en niet een aparte tekst per periodetabel. Een jaartal zou niet kloppen bij een voortschrijdend venster dat over twee kalenderjaren loopt.

**We noemen bij de tegels geen begin- en einddatum.** De tegels 2 tot en met 5 lezen de tabel per functiecategorie, en die heeft geen datums: ze zijn op dat niveau niet te bepalen (§5.2). Binnen één categorie kan het venster bovendien per arbeidsverhouding op een andere datum beginnen of eindigen — bij een andere periodetabel, of bij iemand die halverwege in dienst kwam. Eén datumbereik bij een groepscijfer zou dus per definitie voor een deel van de groep onjuist zijn.

De **eigen** begin- en einddatum zijn er wel: die staan op de regel per inkomstenverhouding (§5.4) en worden vermeld bij de informatie die aan de medewerker wordt verstrekt. Op de tegels gebruiken we ze ook bij tegel 1 niet. De gegevens gaan steeds over het afgelopen jaar, en één aanduiding op alle vijf de tegels leest rustiger dan één tegel met een eigen periode. Om dezelfde reden noemt de uitleg achter het info-icoon van tegel 1 vast *12 maanden* (blok AO, punt AO4).

### 8.3 Pagina-onderdeel Functie

Onder de tegels staat een pagina-onderdeel met drie niet-bewerkbare velden:

| Veld | Inhoud |
| --- | --- |
| Functie | De omschrijving van de actuele functie van de medewerker |
| Functiecategorie | De omschrijving van de functiecategorie waarin die functie valt |
| Toelichting | De toelichting die de werkgever bij die functiecategorie heeft vastgelegd |

**Dit onderdeel draagt de context die niet boven de tegels kon staan** (§8.1). Het legt de keten vast die de hele pagina bepaalt: de functie leidt naar de functiecategorie, en die bepaalt met wie de medewerker wordt vergeleken.

**De functie staat als eerste.** Dat is het gegeven dat de medewerker herkent, en het is de schakel naar de rest. De functiecategorie is een indeling die de werkgever maakt; zonder de functie ernaast is niet te zien waaróm iemand in die categorie valt.

**De titel is *Functie* en niet *Mijn functie*.** Dezelfde sectie staat op de ESS-, de MSS- en de plaatsing-stamkaart (§8.1). Op de laatste twee kijkt niet de medewerker zelf mee maar een leidinggevende, HR of een intercedent, en dan klopt *mijn* niet. Met een neutrale titel hoeven we het onderdeel niet per stamkaart anders te benoemen. Om dezelfde reden heet de weergave eronder *Functies in functiecategorie* (§8.4).

**De toelichting nemen we één op één over.** Het is een vrije tekst van de werkgever die uitlegt wat er in de categorie valt. We maken hem niet bewerkbaar en korten hem niet in.

**De vergelijkingstabel vervalt.** Een eerdere versie toonde hier vijf regels maal drie kolommen: jaaruren, bruto jaarloon, bruto uurloon en de jaar- en uurwaarde variabele componenten, voor de medewerker, de mannen en de vrouwen. Die tabel is vervangen door de tegels in §8.2. De onderbouwing staat in §6.4; kort gezegd: vijftien getallen waarvan de helft voor de medewerker niet te plaatsen is, tegenover zes getallen in één beeld.

Daarmee verdwijnen het bruto jaarloon, de jaaruren en de jaarwaarde variabele componenten van het scherm. Dat mag: er is voor het recht op informatie geen juridische basis die het jaarloon voorschrijft (§6.5). De eigen verloonde uren staan nog in de uitleg bij tegel 1; de volledige cijfers staan in het document *Loontransparantie medewerker* (hoofdstuk 11).

**We tonen geen vrije velden van de functiecategorie.** Klanten kunnen vrije velden op de functiecategorie maken, en die zouden op zichzelf best bij de omschrijving en de toelichting kunnen staan. Voorwaarde is dan wel dat de klant zelf kan sturen wélke van die vrije velden worden getoond, en dat is naar verwachting niet mogelijk. Zonder die sturing zou elk vrij veld dat iemand op de functiecategorie aanmaakt automatisch naast iemands loongegevens verschijnen, ook als het voor een heel ander doel is bedoeld. Dat risico wegen we zwaarder dan het gemak.

Is de functie van de medewerker niet aan een categorie gekoppeld, dan blijven de velden Functiecategorie en Toelichting leeg en verschijnt de melding uit §8.6.

### 8.4 Weergave Functies in functiecategorie

Onder het pagina-onderdeel *Functie* staat een weergave met de functies die tot dezelfde functiecategorie behoren als de medewerker. Zo ziet de medewerker met welke functies zijn loon wordt vergeleken.

| Kenmerk | Invulling |
| --- | --- |
| Titel | Functies in functiecategorie |
| Bron | De regels per inkomstenverhouding (§5.4), gekoppeld aan de functiecategorie-inrichting. Bij een uitzendkracht is dat de DP5-verzameling *Functies per functiecategorie (klantovereenkomst)* |
| Kolom | Omschrijving |
| Sortering | Alfabetisch op omschrijving |
| Aantal regels | Elke functie één keer; bij een lange lijst scrollt de weergave |

**We lezen de lijst uit de regels per inkomstenverhouding.** De weergave koppelt de functiecategorie-inrichting aan laag 2 en toont alleen de functies waarvoor in het venster daadwerkelijk een regel bestaat. Daarmee ziet de medewerker de functies die **meetellen** in de cijfers erboven, en niet de functies die de werkgever ooit aan de categorie heeft gekoppeld.

Dat lost twee dingen op. Functies waarop niemand werkt verdwijnen uit de lijst, en oude inrichting die nooit is opgeruimd blijft niet eeuwig zichtbaar. Beide zouden de medewerker een vergelijkingsgroep voorspiegelen die groter of anders is dan de groep waarop de gemiddelden zijn berekend.

**De afbakening is dezelfde als bij de vergelijkingscijfers** (§6.3). De lijst volgt dus de functiecategorie, de **populatie** en — bij een ter beschikking gestelde arbeidskracht — de **verkooprelatie** van de medewerker. Anders zou de lijst functies tonen van collega's die niet in zijn gemiddelde zitten.

**Bij een uitzendkracht komt de inrichtingskant uit DP5.** De functies horen daar bij een klantovereenkomst en niet bij de werkgever, en er is geen HRM-inrichting om op te koppelen. DP5 levert daarvoor de gegevensverzameling **Functies per functiecategorie (klantovereenkomst)**: per functie van een klantovereenkomst de categorie waarin die is ingedeeld, over alle klantovereenkomsten van de verkooprelatie (DP5, US18). Bij een eigen medewerker blijft de HRM-inrichting de bron.

**De categorie waarop we filteren is die van de pláátsing.** Is er op de plaatsing een afwijkende functiecategorie vastgelegd, dan wordt de uitzendkracht in die categorie vergeleken — en dus met de functies die dáárin zijn ingedeeld. Dat de afwijking op zijn plaatsing staat maakt zijn eigen functie geen onderdeel van die categorie. Zijn functie kan daardoor buiten de lijst vallen, en dat is juist: de lijst beschrijft de vergelijkingsgroep en niet zijn eigen indeling. Laag 2 draagt die categorie al als sleutelonderdeel (§5.4), dus het filter is er zonder extra afleiding.

**De lijst gaat over het hele venster en niet over de actuele functie.** Wie binnen het venster van functie wisselde heeft twee regels, en beide tellen mee in de categorie waarin ze vallen (§6.3). Die twee functies horen dus allebei in de lijst. De weergave gebruikt daarom alle functieregels binnen het venster, niet alleen die van de actuele functie.

Elke functie komt **één keer** in de lijst, hoeveel arbeidsverhoudingen er ook onder vallen. De eigen functie van de medewerker krijgt geen aparte markering en staat niet bovenaan. De lijst is puur alfabetisch.

De weergave toont alleen functieomschrijvingen. Er staan geen aantallen, namen of bedragen per functie in, omdat dat tot herleidbare gegevens zou leiden.

**Dit herziet besluit D7.** Dat koos de functiecategorie-inrichting als bron, met als argument dat een lijst uit de regels zichtbaar zou maken hoe klein de vergelijkingsgroep feitelijk is. Dat argument weegt niet meer zo zwaar: sinds de tegel *Samenstelling functiecategorie* erbij kwam, staat het aantal arbeidsverhoudingen per geslacht al op het scherm (§8.2, §9.4). De groepsgrootte is dus hoe dan ook bekend. Wat de lijst toevoegt is wélke functies bezet zijn, en dat weegt niet op tegen het risico dat de medewerker zich vergelijkt met functies waarop niemand werkt.

Is de functie van de medewerker niet aan een categorie gekoppeld, dan is er geen lijst en blijft de weergave leeg. Dat past bij §3.7: er is dan ook geen vergelijking.

In alle andere gevallen bevat de lijst **minstens één regel**: de eigen functie van de medewerker. Die heeft immers zelf een regel per inkomstenverhouding in die categorie. Een lege lijst bij een gevulde functiecategorie kan dus niet voorkomen.

**Op één geval na.** Is er op de plaatsing van een uitzendkracht een **afwijkende functiecategorie** vastgelegd, dan wordt hij vergeleken in een categorie waarin zijn eigen functie niet hoeft te zijn ingedeeld. De lijst kan dan zijn functie missen, en bij een nog lege categorie zelfs helemaal leeg zijn. Dat is geen fout maar het gevolg van de afwijking: hij is bewust in een andere groep geplaatst (DP5, US12 en US18).

### 8.5 Meerdere regels per medewerker

Een medewerker kan meerdere regels per inkomstenverhouding hebben, om twee redenen: hij heeft meerdere inkomstenverhoudingen, of hij is binnen het venster van functie gewisseld (§5.4). Op de stamkaart tonen we op dit moment altijd één regel.

**Welke regel dat is**, bepalen we in twee stappen:

1. de inkomstenverhouding van het **hoofddienstverband**;
2. daarbinnen de regel van de **actuele functie**: de functie die geldt op het moment van opvragen.

We kijken bewust naar de actuele functie en niet naar de functie op de laatste dag van het venster. Het venster eindigt bij het laatste geaccordeerde tijdvak en loopt dus achter op vandaag. Vraagt de medewerker zijn gegevens op, dan hoort hij te worden vergeleken met de collega's in de functie die hij op dat moment heeft.

**De twee stappen liggen op verschillende plekken.** Stap 2, het filter op de actuele functie, zit op de gegevensverzameling (§5.9). Daardoor gebruiken de tegels, het rapport en de route van DP4 alle drie dezelfde functieregel. Stap 1, de keuze voor het hoofddienstverband, zit daar **niet**: die wordt gemaakt bij het opbouwen van de tegels. Het rapport toont daarom wél alle inkomstenverhoudingen, en dat is precies de bedoeling — het is de route waarlangs de medewerker bij zijn andere dienstverbanden komt.

Wisselde de medewerker binnen het venster van functie, dan ziet hij dus de cijfers van zijn huidige functie, over de tijdvakken waarin hij die functie had. Het aantal toegekende tijdvakken staat op de regel (§5.4), zodat te verklaren is waarom het bruto jaarloon lager uitvalt dan een vol jaar.

**Bij een recente functiewijziging is er mogelijk nog geen regel.** Is er nog geen salarisverwerking geaccordeerd waarin de nieuwe functie valt, dan heeft de taak voor die functie nog niets kunnen berekenen. De medewerker ziet dan geen eigen bedragen.

De **vergelijkingscijfers zijn er wel**. De tegels 3 en 5 lezen alleen de tabel per functiecategorie (§5.5) en hebben de eigen regel niet nodig; welke categorie dat is, leiden we af uit de actuele functie. Van tegel 2 vervalt alleen de balk Jij; de twee gemiddelden staan er gewoon. Tegel 1 en tegel 4 blijven leeg, want die gaan over de eigen waarde. De medewerker ziet dus meteen waar zijn nieuwe functiecategorie staat, ook al ontbreekt zijn eigen loon nog. Dat vult zich vanzelf zodra de eerstvolgende salarisverwerking is geaccordeerd en de taak daarna heeft gedraaid.

Welk dienstverband het hoofddienstverband is, staat niet op de regel zelf. De KPI haalt dat bij het opbouwen op uit de stamgegevens (§5.4), zodat een wijziging meteen doorwerkt en niet pas na de volgende run van de taak.

**Meerdere actuele dienstverbanden: alleen het hoofddienstverband**

Bij een medewerker met meerdere actuele dienstverbanden zou je het recht op informatie **per dienstverband** willen inzien. De loonniveaus kunnen per dienstverband sterk verschillen, en het dienstverband dat níét wordt getoond kan juist het dienstverband zijn waar de vraag over gaat.

**Wisselen tussen dienstverbanden is technisch niet mogelijk.** Op de standaard stamkaart is er geen manier om binnen de sectie van dienstverband te wisselen en daarbij de tegels, het pagina-onderdeel en de weergave mee te laten verversen. De eerder uitgewerkte richting met tabbladen per dienstverband — één tabblad per actief (neven)dienstverband, met de functieomschrijving als titel — komt daarmee te vervallen. Ook het herhalen van de pagina-onderdelen per dienstverband valt af: dat maakt de pagina lang en bij drie of meer dienstverbanden onoverzichtelijk.

**We tonen daarom het hoofddienstverband**, met het document *Loontransparantie medewerker* en de actieknop *Vraag aan HR* (§8.1) als route naar de rest.

**Er komt geen melding op het scherm.** Een eerdere versie toonde de tekst "Je hebt meer dan één dienstverband. Hier zie je de gegevens van je hoofddienstverband." Die vervalt, om twee redenen. De activering *Meerdere dienstverbanden* geldt maar voor een deel van de klanten, dus de melding zou voor de meeste medewerkers nooit verschijnen. En dat het om één dienstverband gaat blijkt al uit de **functieomschrijving in de subtitel van tegel 1** (§8.2). De uitleg hoort in de help en niet op de pagina.

**Subdienstverbanden spelen hier geen rol.** De cijfers staan per inkomstenverhouding vast (§5.4), niet per dienstverband. Hangen meerdere subdienstverbanden onder één kapstok, dan is er voor die groep samen maar één regel, met de functie van het kapstokdienstverband (§3.1).

Wat hier níét speelt is de vraag of een KPI-tegel meerdere waarden kan tonen. Een tegel toont één waarde; er is dus hoe dan ook één set tegels per dienstverband, en niet één tegel met meerdere getallen.

### 8.6 Als er geen gegevens zijn

De medewerker kan om verschillende redenen geen volledige informatie zien. We tonen in alle gevallen een melding, zodat het scherm niet zomaar leeg is. Waar de reden voor de medewerker iets betekent — zoals een ontbrekende functiecategorie — noemen we die; anders volstaat een generieke melding:

| Situatie | Wat de medewerker ziet |
| --- | --- |
| Er zijn geen loongegevens: er is nog geen salarisverwerking geaccordeerd, de taak heeft nog niet gedraaid, of de arbeidsverhouding valt buiten de regeling | Eén **generieke melding** dat er (nog) geen loongegevens te tonen zijn. We maken geen onderscheid naar de reden. Buiten de regeling valt een arbeidsverhouding bij een soort inkomstenverhouding, aard arbeidsverhouding of soort medewerker die niet meetelt (§3.2), en als er over het venster geen loon of geen verloonde uren zijn (§3.4) |
| De functie is niet aan een functiecategorie gekoppeld | Alleen tegel 1 met het eigen uurloon en de melding dat vergelijken niet mogelijk is; de tegels 2 tot en met 5 vervallen. In *Functie* blijven Functiecategorie en Toelichting leeg en de functielijst is leeg |
| De medewerker is recent van functie gewisseld en er is nog geen salarisverwerking over die functie geaccordeerd | Tegel 1 en tegel 4 tonen geen waarde maar de melding dat de eigen gegevens nog volgen, en in tegel 2 vervalt de balk Jij; de tegels 3 en 5 en de twee gemiddelden in tegel 2 zijn er wél |
| Er zijn geen mannen in de functiecategorie | Geen percentage in tegel 5, met de melding dat er niets te vergelijken valt; tegel 2 toont de eigen balk en die van de vrouwen, tegel 3 toont alleen de vrouwen. **Tegel 4 blijft gewoon staan**: die rekent tegen het categoriegemiddelde, en dat bestaat ongeacht de samenstelling |
| Er zijn geen vrouwen in de functiecategorie | Idem, met mannen en vrouwen omgedraaid |
| De medewerker heeft geslacht X of geen ingevuld geslacht | Alle vijf de tegels zijn er gewoon; hij telt mee in het categoriegemiddelde van tegel 4, maar niet in de gemiddelden per geslacht (§3.8) |
| De medewerker is de enige in zijn functiecategorie | Tegel 4 toont geen percentage maar de melding dat de functiecategorie te klein is om te vergelijken. De andere tegels zijn er gewoon |
| De medewerker valt niet onder Nederlandse wetgeving | De sectie Loontransparantie wordt niet getoond (§9.6). In Pocket ziet de medewerker een melding (§8.8) |

**Een lege geslachtsgroep werkt beide kanten op.** Ontbreekt een van de twee groepen, dan blijven de **groepspercentages** leeg — ook als er wel een gemiddelde voor de andere groep is. Zo'n percentage vraagt immers twee groepen. De gevulde balk tonen we wél: die informatie is er en heeft waarde, ook zonder vergelijking. Datzelfde geldt voor de donut in tegel 3: die toont dan één segment. Dat dit segment honderd procent beslaat is geen fout, maar precies wat er aan de hand is. We tonen nooit 100% als loonverschil wanneer de ene groep ontbreekt; dat zou lezen als een maximaal loonverschil terwijl er in werkelijkheid niets te vergelijken valt.

**Het individuele percentage van tegel 4 raakt dit niet.** Dat zet de eigen waarde af tegen het gemiddelde van de héle functiecategorie, en dat gemiddelde bestaat ook als er maar één geslachtsgroep in zit (§6.5). Hier stond eerder dat tegel 4 dan óók leeg bleef; dat dateerde uit de tijd dat de tegel tegen het gemiddelde van het eigen geslacht rekende.

**Tegel 4 toont geen percentage als de medewerker de enige in zijn functiecategorie is.** Het categoriegemiddelde is dan gelijk aan zijn eigen uurloon en het individuele loonverschil komt op nul uit. Dat is rekenkundig juist maar nietszeggend. In plaats van de tegel te laten vervallen, toont hij de melding dat de functiecategorie te klein is om te vergelijken. Zo blijft de pagina steeds gelijk opgebouwd en ziet de medewerker waarom er geen percentage staat. Dat hij alleen staat, blijkt ook al uit tegel 3.

**Ontbrekende eigen gegevens blokkeren de vergelijking niet.** Bij een recente functiewijziging is er nog geen regel per inkomstenverhouding voor de nieuwe functie, maar de tabel per functiecategorie is er wel. De tegels 3 en 5 lezen alleen die tabel, dus die vullen we gewoon (§8.5). Zouden we het hele blok verbergen, dan zag de medewerker niets terwijl de informatie waar hij recht op heeft — het loonverschil in zijn functiecategorie — beschikbaar is.

**Een deels gevuld venster is geen aparte situatie.** Bij een nieuwe klant is het venster in het eerste jaar nog niet vol, en bij een bestaande klant ontbreken de tijdvakken van vóór 2026 (§7.7). De cijfers zijn dan gewoon zichtbaar, over de tijdvakken die er zijn. Dat alles op **uurbasis** staat helpt daarbij: een uurloon over drie maanden is een zinvol getal, een jaarloon over drie maanden niet. Dit is een tweede reden om het jaarloon van het scherm te houden.

**Er is geen melding voor nul verloonde uren.** Die situatie stond hier eerder wel, maar kan niet optreden: verloonde uren groter dan nul is een selectiecriterium (§3.4), dus wie geen uren heeft komt niet in de tabellen en valt onder de tweede situatie hierboven.

### 8.7 Teksten

De titels, het bijschrift van tegel 1, de toelichting van de sectie, de uitleg achter de info-iconen en de meldingen liggen sinds 19 oktober 2026 vast (blok AO en AP). Alleen de bijschriften van tegel 4 en 5 zijn nog een voorstel; team Content scherpt ze aan.

**Meldingen**

De kolom *State* noemt de toestand die de bouw per tegel bepaalt; de Pocket-connector geeft dezelfde toestand terug als reden (§8.8).

| Situatie | State | Waar | ESS-stamkaart | MSS- en plaatsing-stamkaart |
| --- | --- | --- | --- | --- |
| Geen loongegevens | NoPayrollYet | Tegel 1; de tegels 2 tot en met 5 vervallen | Er zijn (nog) geen salarisgegevens om te tonen. Heb je hier vragen over? Stel ze aan HR. | Gelijk aan ESS |
| Functie niet gekoppeld aan een functiecategorie | NoJobCategory | Tegel 1 | Je salaris is nog niet vergeleken met dat van je collega's. Je functie hoort namelijk nog niet bij een functiecategorie. Vraag je werkgever hiernaar. | Het salaris is nog niet vergeleken met dat van de collega's. De functie hoort namelijk nog niet bij een functiecategorie. Vraag de werkgever hiernaar. |
| Recent van functie gewisseld, eigen gegevens nog niet berekend | RecentFunctionChange | Tegel 1 en tegel 4 | Je hebt onlangs een andere functie gekregen. Je salaris in die functie zie je hier zodra je werkgever je salaris weer heeft verwerkt. | De medewerker heeft onlangs een andere functie gekregen. Het salaris in die functie zie je hier zodra de werkgever het salaris weer heeft verwerkt. |
| Geen mannen in de functiecategorie | Available, geen mannen | Tegel 5 | In deze functiecategorie werken op dit moment geen mannen. Daarom is er geen vergelijking van het salaris tussen mannen en vrouwen. | Gelijk aan ESS |
| Geen vrouwen in de functiecategorie | Available, geen vrouwen | Tegel 5 | In deze functiecategorie werken op dit moment geen vrouwen. Daarom is er geen vergelijking van het salaris tussen mannen en vrouwen. | Gelijk aan ESS |
| De enige in de functiecategorie | Available, alleen | Tegel 4 | Je functiecategorie is te klein om je salaris met het gemiddelde te vergelijken. | De functiecategorie is te klein om het salaris met het gemiddelde te vergelijken. |
| Binnen het jaar van functie gewisseld | Available, functie gewisseld | Alleen in Pocket | Je hebt afgelopen jaar een andere functie gekregen. Hier zie je de gegevens van je huidige functie. | De medewerker heeft afgelopen jaar een andere functie gekregen. Hier zie je de gegevens van de huidige functie. |
| Valt niet onder Nederlandse wetgeving | NotApplicable | Alleen in Pocket; op de stamkaart wordt de sectie niet getoond | Deze cijfers gelden alleen voor werk dat onder de Nederlandse wet valt. Voor jou zijn er daarom geen cijfers. | Deze cijfers gelden alleen voor werk dat onder de Nederlandse wet valt. Voor de medewerker zijn er daarom geen cijfers. |
| Actieknop Vraag aan HR | — | Onder de weergave | Vraag aan HR | Gelijk aan ESS |

**De melding over meerdere dienstverbanden is vervallen.** Die stond hier eerder wel, maar komt niet meer op het scherm (§8.5). De uitleg dat alleen het hoofddienstverband wordt getoond, hoort in de help.

De melding bij "geen loongegevens" is bewust **generiek** gehouden. Of er nog geen salarisverwerking is, of de arbeidsverhouding buiten de regeling valt: de onderliggende reden — een soort inkomstenverhouding, aard arbeidsverhouding of soort medewerker die niet meetelt — zegt de medewerker niets en zou tot vragen leiden die hij zelf niet kan oplossen. Daarom maken we er ook geen onderscheid in. De tekst spreekt van **salarisgegevens** en belooft geen moment waarop ze verschijnen, zodat hij ook klopt voor een arbeidsverhouding die buiten de regeling valt en nooit cijfers krijgt. De verwijzing naar HR is er om die vraag op de juiste plek te laten landen.

In de meldingen spreken we van **salarisgegevens** en van het **verwerken van het salaris**, en niet van accorderen. Accorderen is een term uit de backoffice; de medewerker weet niet wat het betekent en kan er niets mee.

De meldingen hebben een **je-vorm** voor de ESS-stamkaart en een **de-medewerkervorm** voor de MSS- en de plaatsing-stamkaart. Dat is dezelfde splitsing als bij de eerste categorie van tegel 2, die op ESS *Jij* heet en elders *Medewerker* (§8.2). De meldingen bij geen loongegevens en bij een lege geslachtsgroep zijn overal gelijk.

**Twee meldingen staan alleen in Pocket.** Dat de medewerker binnen het jaar van functie wisselde, is op de stamkaart al te zien aan de functie in de subtitel van tegel 1 (§8.2). En buiten Nederland toont de stamkaart de sectie niet (§9.6); de app heeft wel een melding nodig, omdat de medewerker daar zelf naar de pagina navigeert (§8.8).

**Toelichting van de sectie**

| Stamkaart | Tekst |
| --- | --- |
| Medewerker ESS | Vanuit de richtlijn loontransparantie heb je recht op inzicht. Je salaris wordt vergeleken met dat van collega’s in dezelfde functiecategorie. Je werkgever heeft bepaald welke functies in de functiecategorie vallen. |
| Medewerker MSS | Vanuit de richtlijn loontransparantie heeft de medewerker recht op inzicht. Het salaris wordt vergeleken met dat van collega’s in dezelfde functiecategorie. De werkgever heeft bepaald welke functies in de functiecategorie vallen. |
| Plaatsing | Vanuit de richtlijn loontransparantie heeft de medewerker recht op inzicht. Het salaris wordt vergeleken met dat van collega’s in dezelfde functiecategorie bij dezelfde opdrachtgever. De opdrachtgever heeft bepaald welke functies in de functiecategorie vallen. |

**Titels en bijschriften**

| Onderdeel | ESS-stamkaart | MSS- en plaatsing-stamkaart |
| --- | --- | --- |
| Titel tegel 1 | Hoeveel verdien ik per uur? | Hoeveel verdient de medewerker per uur? |
| Subtitel tegel 1 | \[functieomschrijving\] · laatste 12 maanden | Gelijk aan ESS |
| Bijschrift tegel 1 | gemiddeld per uur | Gelijk aan ESS |
| Titel tegel 2 | Gemiddeld uurloon binnen functiecategorie | Gelijk aan ESS |
| Legenda tegel 2 | Basisloon · Extra's | Gelijk aan ESS |
| Titel tegel 3 | Samenstelling functiecategorie | Gelijk aan ESS |
| Titel tegel 4 | Verdien ik meer of minder dan mijn collega's? | Verdient de medewerker meer of minder dan collega's? |
| Bijschrift tegel 4 | Zie de tabel met bijschriften hieronder | Idem |
| Titel tegel 5 | Wat is het verschil tussen mannen en vrouwen? | Gelijk aan ESS |
| Bijschrift tegel 5 | Zie de tabel met bijschriften hieronder | Idem |
| Subtitel tegel 2 tot en met 5 | \[functiecategorie\] · laatste 12 maanden | Gelijk aan ESS |
| Titel pagina-onderdeel | Functie | Gelijk aan ESS |
| Veldnamen pagina-onderdeel | Functie · Functiecategorie · Toelichting | Gelijk aan ESS |
| Titel weergave | Functies in functiecategorie | Gelijk aan ESS |

**De tegeltitels zijn vragen, de overige koppen benoemen het onderdeel.** Een tegeltitel stelt de vraag die de medewerker heeft, en de tegel geeft het antwoord. Gaat die vraag over de medewerker zelf, zoals bij tegel 1 en 4, dan volgt de titel de aanspreekvorm van de stamkaart: *ik* op ESS, *de medewerker* op MSS en plaatsing. Het pagina-onderdeel *Functie* en de weergave *Functies in functiecategorie* houden een neutrale kop; die zijn op alle drie de stamkaarten gelijk (§8.3).

**De bijschriften van tegel 4 en 5** [voorstel]

Elke tegel heeft **drie varianten**, één per teken. De kolom ESS is de je-vorm; de kolom MSS geldt op de MSS- en de plaatsing-stamkaart.

| Tegel | Uitkomst | ESS-stamkaart | MSS- en plaatsing-stamkaart |
| --- | --- | --- | --- |
| 4 | Positief | Je verdient meer dan het gemiddelde in jouw functiecategorie | De medewerker verdient meer dan het gemiddelde in de functiecategorie |
| 4 | Negatief | Je verdient minder dan het gemiddelde in jouw functiecategorie | De medewerker verdient minder dan het gemiddelde in de functiecategorie |
| 4 | Nul | Je verdient evenveel als het gemiddelde in jouw functiecategorie | De medewerker verdient evenveel als het gemiddelde in de functiecategorie |
| 5 | Negatief | Vrouwen verdienen gemiddeld minder dan mannen | Gelijk aan ESS |
| 5 | Positief | Vrouwen verdienen gemiddeld meer dan mannen | Gelijk aan ESS |
| 5 | Nul | Mannen en vrouwen verdienen gemiddeld evenveel | Gelijk aan ESS |

**Tegel 5 kent maar één vorm.** Dat bijschrift gaat over twee groepen en spreekt niemand aan, dus er valt geen je- of de-medewerkervorm van te maken. Alleen tegel 4 gaat over een persoon en heeft daarom twee vormen.

**Nul komt zelden voor, maar moet kloppen.** Zonder derde variant zou er bij 0,00% in tegel 5 *Vrouwen verdienen gemiddeld minder dan mannen* staan, en in tegel 4 dat de medewerker meer of minder verdient terwijl hij precies op het gemiddelde zit. Bij tegel 4 is dit iets anders dan de medewerker die alleen in zijn categorie staat; daar staat geen percentage maar een melding (§8.6).

**De bijschriften trekken de conclusie.** "Vrouwen verdienen gemiddeld minder dan mannen" is stelliger dan een neutrale beschrijving, en dat is de bedoeling: een kaal percentage laat de medewerker zelf raden welke kant het op wijst. De nuance dat een verschil verklaarbaar kan zijn, hoort in de help en bij het gesprek met HR.

**Het bijschrift wijst dezelfde kant op als het teken.** Een min hoort bij "minder", een plus bij "meer" (§6.5). Daarbij verschillen de twee tegels in onderwerp, en dat moet in elke herformulering overeind blijven: tegel 4 gaat over de medewerker **zelf** en noemt daarom geen geslacht, tegel 5 gaat over de **vrouwen als groep** en benoemt beide groepen. Verdwijnt dat onderscheid uit de tekst, dan leest de medewerker het teken van tegel 5 als een uitspraak over zichzelf.

**Uitleg achter de info-iconen**

De waarden tussen vierkante haken worden per medewerker ingevuld; de getallen zijn een voorbeeld. Elk bedrag krijgt het valutasymbool uit §8.2.

| Tegel | ESS-stamkaart | MSS- en plaatsing-stamkaart |
| --- | --- | --- |
| 1 | Dit is wat je gemiddeld per uur hebt verdiend in de afgelopen 12 maanden (berekend over \[2.080\] uur). Je basissalaris is \[€ 33,21\] per uur. Daar komen de extra's bij die bestaan uit bijzondere beloningen en loon in natura: \[€ 1,94\] per uur. | Dit is wat de medewerker gemiddeld per uur heeft verdiend in de afgelopen 12 maanden (berekend over \[2.080\] uur). Het basissalaris is \[€ 33,21\] per uur. Daar komen de extra's bij die bestaan uit bijzondere beloningen en loon in natura: \[€ 1,94\] per uur. |
| 4 | Hoe je uurloon zich verhoudt tot het gemiddelde uurloon van iedereen in de functiecategorie \[Leidinggevend\], ongeacht het geslacht. Jij verdient \[€ 38,31\] per uur, het gemiddelde is \[€ 41,02\]. Het verschil is \[€ -2,71\] per uur (\[-6,61%\]). | Hoe het uurloon van de medewerker zich verhoudt tot het gemiddelde uurloon van iedereen in de functiecategorie \[Specialistisch uitvoerend\], ongeacht het geslacht. De medewerker verdient \[€ 23,83\] per uur, het gemiddelde is \[€ 38,98\]. Het verschil is \[€ -15,15\] per uur (\[-38,87%\]). |
| 5 | Vrouwen verdienen gemiddeld \[€ 37,87\] per uur, mannen gemiddeld \[€ 41,65\] per uur. Het verschil is \[€ -3,78\] per uur (\[-9,08%\] ten opzichte van het gemiddelde van de mannen). | Gelijk aan ESS |

De ingevulde waarden komen uit de voorberekende velden; de tegel rekent alleen het verschil in euro's uit, als aftrekking van de twee getoonde bedragen (§8.2).

| Waarde | Veld |
| --- | --- |
| Uren bij tegel 1 | Jaaruren van de regel per inkomstenverhouding (§5.4), op hele uren |
| Basissalaris per uur | Bruto uurloon van die regel |
| Extra's per uur | Uurwaarde variabele componenten van die regel |
| Eigen uurloon bij tegel 4 | Totaal uurloon van die regel |
| Gemiddelde bij tegel 4 | Gemiddeld totaal uurloon categorie (§5.5) |
| Percentage bij tegel 4 | Individueel loonverschil (§5.4) |
| Vrouwen en mannen bij tegel 5 | Gemiddeld totaal uurloon vrouwen en Gemiddeld totaal uurloon mannen (§5.5) |
| Percentage bij tegel 5 | Loonverschil totaal uurloon (§5.5) |

**Tegel 2 en 3 hebben geen info-icoon.** De gestapelde balk heeft een legenda en een hamburger die de bedragen toont; de donut toont de aantallen zelf. Een uitleg daarachter zou herhalen wat er al staat.

**Eén zin voor elke uitkomst.** De uitleg bij tegel 4 en 5 noemt het verschil als bedrag én als percentage, beide met teken. Daardoor klopt dezelfde zin bij een plus, een min en bij nul, en zijn er geen varianten met *meer* of *minder* nodig. Het bijschrift onder de waarde houdt zijn drie varianten wel: daar staat het percentage zonder bedrag, en dan moet de tekst zeggen welke kant het op wijst.

**De aanspreekvorm volgt de stamkaart.** Op de MSS- en de plaatsing-stamkaart worden *je*, *jij* en *jouw* vervangen door **de medewerker**. Dat raakt de uitleg bij tegel 1 en 4; die bij tegel 5 gaat over een groep en is overal gelijk.

**De teksten worden samengesteld en zijn geen vaste zin.** Alle drie bevatten bedragen die per medewerker verschillen (§8.2). Dat is aanvaard omdat een percentage zonder bedrag voor de medewerker weinig betekent.

**Hover bestaat niet op elk apparaat.** Op Pocket en op een tablet moet het info-icoon op tik openen, anders zijn de bedragen daar onbereikbaar. Te bevestigen bij de bouw.

**Een tooltip is niet te kopiëren.** Wie het bedrag wil bewaren of doorsturen, moet het overtypen. Voor dat gebruik blijft het document *Loontransparantie medewerker* de aangewezen route (hoofdstuk 11).

**"Extra's" dekt meer dan alleen bijzondere beloningen.** Er zit ook waarde niet in geld uitgekeerd loon in, zoals een auto van de zaak. De uitleg bij tegel 1 noemt daarom "bijzondere beloningen en loon in natura".

### 8.8 Pocket

De medewerker ziet zijn loontransparantiegegevens ook in **AFAS Pocket**, naast zijn loonstrook en jaaropgave, en kan er een vraag aan HR insturen. De app is voor veel medewerkers het enige kanaal waarin ze hun eigen loongegevens bekijken; het recht op informatie hoort daar dus net zo goed te landen als op de stamkaart.

**Wie wat bouwt**

| Onderdeel | Waar het hoort |
| --- | --- |
| De dataconnector waarmee Pocket de gegevens ophaalt | Dit deelproject |
| De pagina's *tonen* en *aanpassen* voor het type dossieritem Vraag aan HR in Pocket | Dit deelproject |
| De schermen in de app, de navigatie en de flow van het insturen | Team Pocket |
| Het type dossieritem Vraag aan HR zelf: velden, profielen en workflow | DP4 – Vraag aan HR |

**De dataconnector**

Pocket haalt de gegevens op via een **dataconnector**. Dat is het bestaande patroon voor Pocket: een interne connector met een parameter **Modus**, die per modus een andere uitsnede teruggeeft. Bestaande voorbeelden zijn de connectors voor medewerkergegevens, uren en kosten en cursussen.

Er komen vier modi:

| Modus | Wat hij teruggeeft | Bron |
| --- | --- | --- |
| Dienstverbanden | De arbeidsverhoudingen van de ingelogde medewerker waarvoor een regel bestaat, met de functieomschrijving en de functiecategorie. Hiermee bouwt Pocket de navigatie tussen dienstverbanden op | Laag 2 |
| Eigen loongegevens | Voor één dienstverband: basisloon per uur, extra's per uur, totaal uurloon, jaaruren, het individuele loonverschil, het aantal toegekende tijdvakken, de einddatum van het venster, de datum van de laatste berekening en het valutasymbool. Voedt tegel 1 en tegel 4 | Laag 2 (§5.4) |
| Vergelijkingscijfers | Voor de functiecategorie van dat dienstverband: de gemiddelden van mannen en vrouwen, elk gesplitst in basisloon en extra's, het gemiddeld totaal uurloon categorie, de aantallen mannen, vrouwen en totaal, het loonverschil totaal uurloon en het valutasymbool. Voedt tegel 2, 3 en 5 | Laag 3 (§5.5) |
| Functies in de functiecategorie | De lijst functies die binnen het venster in de categorie bezet zijn, zonder aantallen (§8.4) | Laag 3 met laag 2 |

**De connector rekent niet.** Hij leest de voorberekende velden, net als de tegels op de stamkaart (uitgangspunt 1). Zou Pocket zelf een percentage uitrekenen, dan ontstaat er een tweede waarheid naast de taak en kunnen app en stamkaart verschillende getallen tonen.

**Het valutasymbool komt uit de connector.** Hij bepaalt het zoals in §8.2: dat van de werkgever, en anders dat van de basisvaluta. Pocket zoekt het niet zelf op.

Dat geldt ook voor het **teken**. De omkering uit §6.5 zit al in de opgeslagen waarde, dus Pocket draait er niets aan om en toont dezelfde percentages als de stamkaart, inclusief het minteken bij tegel 5. De connector levert uitsluitend regels met soort rapportage *Recht op informatie* (§5.9).

**Waarom laag 2 en laag 3 in aparte modi zitten.** Ze zijn niet altijd allebei beschikbaar. Wisselt een medewerker van functie, dan bestaat de eigen regel nog niet terwijl de vergelijkingscijfers er wel zijn (§8.5). Zaten ze in één modus, dan zou de app in dat geval óf niets tonen óf zelf moeten uitzoeken welk deel er wel is. Met twee modi is dat geen vraag: de ene levert niets, de andere gewoon zijn gegevens.

**Het dienstverband is een parameter, en dat is nieuw voor Pocket.** De bestaande Pocket-connectors leiden de medewerker af uit de ingelogde gebruiker en bepalen het dienstverband zelf, op de actuele datum. Een parameter voor het dienstverband kennen ze niet. Hier moet die er wel komen, omdat Pocket — anders dan de stamkaart — wél tussen dienstverbanden kan navigeren.

**De medewerker blijft uit de gebruiker komen.** Er komt geen parameter voor de medewerker. De connector leidt die af uit de ingelogde gebruiker, zoals de andere Pocket-connectors dat doen.

**Het meegegeven dienstverband moet worden getoetst.** Dit is de belangrijkste eis aan deze connector. Zodra het dienstverband van buiten komt, kan een gebruiker een willekeurig nummer meesturen. Zonder toets levert de connector dan de loongegevens van een collega op — precies de gegevens die §9.2 binnen Profit langs geen enkele weg beschikbaar stelt.

De connector moet daarom bij **elke** modus die het dienstverband als parameter kent, vaststellen dat dat dienstverband bij de medewerker van de ingelogde gebruiker hoort. Is dat niet zo, dan geeft hij een fout terug en geen gegevens. De toets hoort in de connector en niet in de app: de app draait op een apparaat dat wij niet beheersen.

**De connector geeft niets terug wat niet getoond mag worden.** De regels uit §8.6 over het verbergen van tegels moeten in de connector zitten, niet in de app. Ontbreekt een geslachtsgroep, of is de medewerker de enige in zijn categorie, dan laat de connector de betreffende waarden weg. Zou de app dat beslissen, dan reizen de gegevens alsnog naar het apparaat en is de afweging over herleidbaarheid uit §9.3 te omzeilen door mee te kijken op de verbinding.

**Elke modus geeft ook een reden terug als er niets is.** De toestanden uit §8.7 — NoPayrollYet, NoJobCategory, RecentFunctionChange, NotApplicable, en bij Available de kenmerken geen mannen, geen vrouwen, alleen en functie gewisseld — moeten als reden meekomen, zodat Pocket dezelfde melding kan tonen als de stamkaart. Anders moet de app de logica overdoen, of ziet de medewerker een leeg scherm zonder uitleg. De melding over een functiewissel binnen het jaar toont alleen Pocket (§8.7).

**De landtoets geldt ook hier.** Valt de medewerker niet onder Nederlandse wetgeving, dan geeft de connector geen gegevens maar de reden NotApplicable, en toont Pocket de melding uit §8.7 in plaats van cijfers (§9.6). Zonder die toets ziet een Belgische medewerker in de app een melding die voor hem onjuist is.

**De connector is niet klant-zichtbaar.** Hij wordt intern geregistreerd, net als de andere Pocket-connectors, en komt niet als GetConnector beschikbaar voor klanten. Dat is bewust: de klant kan deze gegevens niet via de connector ontsluiten, net zomin als via een gegevensverzameling (§9.2).

**Er komt een eigen Pocket-autorisatierol**, zoals elke Pocket-functionaliteit die heeft. Daarmee kan de klant loontransparantie in Pocket apart uitzetten, net als de sectie op de stamkaart (§9.1).

**Pocket toont hiermee méér dan de stamkaart**

Op de standaard stamkaart is wisselen tussen dienstverbanden technisch niet mogelijk; daar tonen we alleen het hoofddienstverband (§8.5, punt R1). In Pocket kan dat wel. Een medewerker met twee dienstverbanden ziet in de app dus beide, en op de stamkaart één.

Dat is een aanvaard gevolg en geen ontwerpfout: het recht op informatie wordt in Pocket vollediger ingevuld dan in InSite, niet beperkter. Wel betekent het dat de stamkaart niet langer het rijkste kanaal is, en dat de route "vraag het via een dossieritem aan HR" voor die medewerkers alleen in InSite nodig blijft. Bij het schrijven van de help moet daarmee rekening worden gehouden; de uitleg dat je alleen je hoofddienstverband ziet (§8.5) geldt niet voor Pocket.

**Vraag aan HR in Pocket**

De medewerker moet vanuit Pocket een dossieritem **Vraag aan HR** kunnen insturen. Het insturen zelf en de plek in de app pakt team Pocket op.

**Wat wij leveren zijn de pagina's *tonen* en *aanpassen*.** Vraag aan HR is een **technisch type dossieritem**: een type met eigen, extra velden bovenop het gewone dossieritem. Pocket toont voor een dossieritem standaard alleen **Onderwerp**, **Toelichting** en **Bijlage**. De extra velden van dit type komen daar niet vanzelf bij; die moeten per type worden geprogrammeerd.

**Pocket hergebruikt de schermdefinitie van InSite.** De pagina's worden niet los van InSite opgebouwd: per type dossieritem bestaat er één definitie die zowel de InSite-webform als de Pocket-pagina voedt. Pocket krijgt die definitie als JSON binnen en rendert hem zelf. Dat betekent twee dingen. De velden en hun volgorde hoeven maar op één plek te worden vastgelegd, en wat Pocket kan tonen is begrensd door wat dat model aankan — een veldsoort die daar niet in zit, komt ook niet in de app.

**Dit is blokkerend afhankelijk van DP4.** Wij kunnen de pagina's pas bouwen als vaststaat welke extra velden het type Vraag aan HR heeft, welke daarvan de medewerker zelf invult en welke alleen ter inzage zijn. Dat wordt in DP4 bepaald. Zolang die velden niet vastliggen, is er niets te programmeren.

**De profielkeuze werkt in Pocket anders dan op de stamkaart.** Op de stamkaart start de actieknop de profielkeuzepagina, zodat de medewerker zelf het passende profiel kiest (§8.1). Of Pocket zo'n keuzepagina kent, en zo niet hoe de medewerker daar bij het juiste profiel komt, is nog niet bekend. Dit moet met team Pocket en DP4 worden afgestemd voordat de pagina's worden gebouwd.

---

## 9 Autorisatie, privacy en groepsgrootte

### 9.1 Wie wat ziet

De gegevens op de stamkaart gaan over het loon van de medewerker zelf en over gemiddelden van collega's. Dat is gevoelige informatie.

We stellen de sectie beschikbaar aan de medewerker zelf, aan HR en aan de manager. HR moet informatieverzoeken kunnen beantwoorden en de manager moet het gesprek over beloning kunnen voeren met de eigen medewerkers. Welke stamkaart daarbij hoort staat in §8.1.

De sectie Loontransparantie is **autoriseerbaar**. De klant bepaalt zelf per rol of hij zichtbaar is. Wil een klant hem niet voor managers openstellen, dan kan dat.

**In Pocket loopt dat via een eigen autorisatierol** (§8.8). Dat is een aparte knop: een klant kan loontransparantie in de app uitzetten terwijl de sectie op de stamkaart aan blijft staan, of andersom. Dat is inherent aan de manier waarop Pocket autoriseert en niet iets wat we hier introduceren.

### 9.2 Afscherming van de tabellen zelf

De brontabel en de regels per inkomstenverhouding bevatten loongegevens van alle medewerkers. Zonder afscherming zouden die via een eigen weergave of gegevensverzameling te benaderen zijn, en dan is de afweging over herleidbaarheid uit §9.3 te omzeilen.

Dit vraagt bijzondere aandacht, omdat de brontabellen individuele beloningsinformatie **per loontijdvak** bevatten. Dat is gevoeliger dan de verdichte cijfers erboven: wie deze tabel kan lezen, ziet het loonverloop van een collega door het jaar heen. We ontsluiten die tabellen daarom **helemaal niet** binnen Profit: er komt geen gegevensverzameling (§5.9), geen view in de querywizard en geen InSite-datamodeldefinitie. Daarmee is er binnen Profit geen enkele route naar deze gegevens.

De enige afnemer is het **Power BI-dashboard**, dat de tabellen rechtstreeks uitleest. Die route staat alleen open voor **applicatiebeheerders die BI-modellen mogen aanmaken**. Dat is een beperkte groep die vandaag al bij gegevensverzamelingen met salarisgegevens kan. De eindgebruiker kan geen BI-model aanmaken en komt dus langs geen enkele weg bij deze tabellen.

We zien hierin daarom geen extra risico. De afscherming is niet zwakker dan die van de salarisgegevens die dezelfde groep nu al kan ontsluiten; wat we voorkomen is dat de loongegevens per loontijdvak daarnaast ook binnen Profit beschikbaar komen.

Dat de tabellen nieuw zijn helpt hierbij. In een eerdere opzet breidden we de bestaande tabel Loonaangifte uren per medewerker uit, die al via een view en een datamodeldefinitie was ontsloten voor uren en contractkenmerken. Daar moest de bestaande ontsluiting worden herzien voordat er loonbedragen in kwamen te staan. Met eigen tabellen bestaat die erfenis niet en richten we de afscherming meteen goed in.

We ontsluiten de gegevens van laag 2 en laag 3 verder uitsluitend via de meegeleverde weergaven en gegevensverzamelingen (§5.9). Op die gegevensverzamelingen passen we **medewerkerautorisatie** toe bij het lezen: een gebruiker ziet alleen de gegevens van de medewerkers waarvoor hij geautoriseerd is.

De tabel per functiecategorie bevat geen individuele gegevens, alleen gemiddelden per groep. Die valt onder dezelfde afscherming, omdat een gemiddelde in een kleine groep alsnog herleidbaar is (§9.3).

### 9.3 Groepsgrootte

We hanteren **geen ondergrens** voor de vergelijkingscijfers. Zodra er een functiecategorie is, tonen we de gemiddelden, ook als een geslachtsgroep uit één persoon bestaat.

De afweging tussen privacy en het recht op gelijk loon is al door de wetgever gemaakt. De toelichting bij het wetsvoorstel stelt dat het recht op gelijk loon de doorslag geeft en dat de verwerking van persoonsgegevens noodzakelijk is om aan de wettelijke verplichting te voldoen. Wij maken die afweging dus niet opnieuw en zetten er ook geen eigen drempel overheen. Een ondergrens van bijvoorbeeld vijf medewerkers zou het recht in kleine en scheef verdeelde organisaties structureel uithollen, precies daar waar een loonverschil het hardst aankomt.

Dit betekent dat de gegevens in kleine categorieën herleidbaar zijn tot een individuele collega. Bij één vrouw in de categorie is het gemiddelde van de vrouwen simpelweg haar salaris, en dat is dan zichtbaar voor iedereen in die categorie.

Dat is een bewust aanvaard risico. Wat we er wel tegenover zetten: de gegevens worden alleen voor dit doel gebruikt en zijn afgeschermd zoals beschreven in §9.2. De klant kan bovendien zelf sturen via de indeling van zijn functiecategorieën.

### 9.4 Wat we niet tonen

We tonen geen namen, geen bedragen per functie en geen hoogste of laagste waarde binnen de groep. De medewerker ziet alleen gemiddelden, nooit de onderliggende individuele waarden van collega's.

**De aantallen per geslacht tonen we wél**, in de tegel Samenstelling functiecategorie (§8.2). Dat deden we in een eerdere versie van dit ontwerp niet. We doen het nu wel, omdat de twee percentages eronder zonder groepsgrootte niet te duiden zijn: hetzelfde percentage betekent iets anders in een categorie met drie inkomstenverhoudingen dan in een categorie met tweehonderd. Dat die aantallen in een kleine categorie naar een individuele collega wijzen, is dezelfde afweging die bij de gemiddelden al is gemaakt en aanvaard (§9.3).

Het gaat daarbij om een aantal per groep, nooit om een aantal per persoon, per functie of per bedrag. De grafiek toont alleen mannen en vrouwen; geslacht X en niet ingevuld blijven eruit, juist omdat die groepen vaak uit één persoon bestaan (§3.8).

**De functielijst toont wélke functies bezet zijn, niet hoeveel.** Sinds 23 september 2026 komt die lijst uit de regels per inkomstenverhouding en niet meer uit de functiecategorie-inrichting (§8.4). Daarmee is zichtbaar welke functies in het venster daadwerkelijk meetellen. Er staan geen aantallen bij: hoeveel collega's op een functie zitten blijft onbekend. De groepsgrootte als geheel stond al op het scherm, in de tegel hierboven.

**Het individuele loonverschil toont geen gegevens van een collega.** De tegel *Verdien ik meer of minder dan mijn collega's?* zet de medewerker af tegen het gemiddelde van de hele functiecategorie. Is hij de enige in die categorie, dan is dat gemiddelde zijn eigen loon en is het percentage nul; in dat geval toont de tegel geen percentage maar een melding (§8.6).

### 9.5 Uitlevering

We leveren de functionaliteit generiek uit onder de bestaande HR-conditie. Er komt geen aparte activering. Het gaat om een wettelijke verplichting die voor alle klanten geldt, dus iedere klant krijgt het meteen.

De klant houdt grip via de autorisatie op de sectie en via de eigen inrichting van de functiecategorieën.

### 9.6 Landafhankelijkheid

**De scope van dit deelproject is Nederland.**

De begrippen waarmee we rekenen zijn Nederlands: loon LB/PH, vakantiebijslag, arbeidsvoorwaardenbedrag en verloonde uren komen uit het Nederlandse loonbegrippenkader (§6.2). Dat verandert niet doordat we de bedragen uit de berekende salarisgegevens halen in plaats van uit de loonaangifte.

**België valt buiten scope.** De Europese regelgeving geldt daar ook, maar het is niet bekend hoe België er invulling aan geeft. AFAS verwerkt de Belgische loongegevens niet zelf; dat loopt via het sociaal secretariaat. Een denkbare route is om de berekende gegevens die het sociaal secretariaat terugkoppelt te onttrekken en daarmee dezelfde brontabellen te vullen — dan lift België mee op de KPI's op de standaard stamkaart, zonder dat het model wordt opengebroken. Vooralsnog doen we daar niets aan.

**De Caribbean vallen niet onder deze Europese regelgeving** en blijven dus sowieso buiten beeld.

**Het datamodel blijft landonafhankelijk.** Er zit geen landafhankelijk sleutelonderdeel of veld in de vier lagen. Komt er later een Belgische bron, dan vult die dezelfde tabellen.

**De taak heeft wél een landtoets nodig.** In de opzet op de loonaangifte was dat niet zo: de brontabel werd uitsluitend gevuld bij het klaarzetten van de Nederlandse loonaangifte, dus medewerkers buiten die wetgeving kregen vanzelf geen regel. De gegevens filterden zichzelf. Nu de brontabellen uit de salarisverwerking worden gevuld (§7.1), gaat dat niet meer op en moet de taak het land van wetgeving expliciet toetsen bij het selecteren van de arbeidsverhoudingen (§7.3, stap 6).

**Daarnaast blijft de toets bij het tonen staan.** Zonder die toets ziet een Belgische medewerker een sectie met de melding dat er (nog) geen salarisgegevens zijn (§8.6, §8.7). Die melding is voor hem onjuist en wekt een verwachting die nooit wordt ingelost. In Pocket, waar de medewerker zelf naar de pagina navigeert, ziet hij in plaats daarvan een melding dat de cijfers alleen gelden voor werk onder de Nederlandse wet (§8.7, §8.8).

Beide toetsen gebruiken hetzelfde gegeven: het **land van wetgeving van de medewerker**.

| Onderwerp | Invulling |
| --- | --- |
| Gegeven | `AfasKnCountryByLaw` op `AfasKnBasicContact`, te bereiken via `AfasKnEmployee.AfasKnBasicContactId` |
| Waarden | ISO-landcodes van twee posities; in de praktijk `NL` en `BE` |
| Leeg | Behandelen als `NL`, conform de bestaande conventie in HR (`ISNULL(AfasKnCountryByLaw, 'NL')`) |
| Gedrag | Is de waarde niet `NL`, dan telt de medewerker niet mee in de berekening en tonen we de sectie Loontransparantie niet |
| Bestaande functie | `GetEmployeesCountryByLaw(employeeId)` in `AfasHrGeneralLib`, beschikbaar vanuit webforms |

Dit is een bestaand patroon en niet iets nieuws. HR gebruikt dit veld op tientallen plekken om Nederlandse en Belgische functionaliteit te scheiden, en er is een KPI die precies dit doet: **Saldi geboorteverlof** leest het land van wetgeving van de medewerker, toont de Nederlandse variant bij `NL`, de Belgische bij `BE`, en toont niets bij een ander land.

**Waarom niet het land van wetgeving op de administratie** (`CoLa`, businesscomponent `KnUnp`). Dat veld bestaat en HR gebruikt het ook, maar het geldt voor de hele administratie. Eén administratie kan werkgevers en medewerkers uit meerdere landen bevatten, en dan valt de toets de verkeerde kant op: óf een Belgische medewerker krijgt de sectie alsnog, óf een Nederlandse medewerker in een als Belgisch ingerichte administratie krijgt hem ten onrechte niet. Het medewerkerveld is fijnmazig genoeg en het enige dat de vraag beantwoordt die wij stellen.

---

## 10 Randvoorwaarden en performance

- **Het salarisproces gaat voor.** Het accorderen van de salarisverwerking schrijft alleen triggerregels weg; meer doet het niet. Het vullen én het rekenwerk gebeuren in een aparte wachtrijtaak daarbuiten. Duurt een run lang, dan mag dat het accorderen niet raken.
- **De batchservice is overdag al zwaar belast.** Administratiekantoren accorderen tientallen werkgevers per dag, naast verlonen, loonstroken genereren en de loonaangifte. Daarom draait de taak in de dagovergang en niet direct na het accorderen (§7.1).
- **De gegevens zijn maximaal één dagovergang oud.** De taak draait vanuit Vernieuwen actuele gegevens (§7.1). Dat geldt voor alle lagen, ook voor de brontabellen.
- **De taak moet herstartbaar zijn.** Bij een fout blijven de triggerregels staan, zodat de eerstvolgende dagovergang de taak opnieuw uitvoert (§7.8). Er mag geen handmatige reparatie nodig zijn om een gemiste werkgever alsnog mee te nemen.
- **De triggertabel blijft klein, behalve vlak na de conversie.** Regels worden opgeruimd zodra ze zijn verwerkt (§7.2). De conversie zet er eenmalig regels in voor alle periodes van 2026, per verloonde werkgever en periodetabel (§7.7); die zijn na de eerste dagovergang weer weg. Groeit de tabel daarna toch, dan is dat een signaal dat de taak niet slaagt.
- **Het kenmerk Soort trigger moet kloppen.** Een stamgegeven-trigger herbouwt het hele venster aan bronregels, een salarisgegevens-trigger alleen één tijdvak (§7.3). Staat het kenmerk verkeerd, dan is dat niet zichtbaar in een foutmelding maar in de cijfers: een deel van het venster blijft dan op de oude indeling staan, of de taak doet twaalf tot drieënvijftig keer zoveel werk als nodig.
- **Bij het uitlezen wordt niet gerekend.** De KPI en de weergaven lezen kant-en-klare waarden uit twee regels: die per inkomstenverhouding en die per functiecategorie. Ook de tien loonverschilpercentages en het individuele loonverschil zijn voorberekend — inclusief het **teken**, dat bij soort rapportage *Recht op informatie* omgekeerd is ten opzichte van de wettelijke richting (§6.5). Geen enkele presentatielaag draait een teken om.
- **Elke ontsluiting toont één soort rapportage tegelijk.** Dat geldt voor de gegevensverzamelingen, voor elke weergave daarop, voor de Pocket-connector en nadrukkelijk ook voor het **Power BI-dashboard**, dat uitsluitend soort *Recht op informatie* toont (§5.9). Zou een overzicht beide soorten tonen, dan staan er twee percentages met dezelfde veldnaam in tegengestelde richting naast elkaar, en dat is in een grafiek of een optelling niet meer te zien.
- **De brontabellen groeien met de tijd.** We schonen ze niet op (§5.6). Het aantal regels neemt per jaar toe met het aantal dienstverbanden maal het aantal tijdvakken van de periodetabel — twaalf bij maandverloning, tot drieënvijftig bij weekverloning (§4.3); voor uitzendkrachten met het aantal **plaatsingen** daarbinnen, en die combinatie — veel plaatsingen én weekverloning — komt bij uitleners juist samen.
- **De ordegrootte bij een uitlener verschilt van die bij een gewone werkgever.** De brontabel gaat per plaatsing, de verloning is meestal per week en op laag 3 zit de verkooprelatie in de sleutel. Een uitzendbureau levert daardoor een veelvoud van de regels op van een werkgever met evenveel mensen in vaste dienst (§7.4). De taak mag bij het bouwen en het testen niet uitgaan van de aantallen die bij eigen medewerkers horen.
- **Het aantal triggerregels groeit niet mee met de populatie.** Triggerregels gaan per werkgever, periodetabel en tijdvak, niet per persoon of plaatsing (§7.2). Duizend uitzendkrachten in één weekverwerking leveren één triggerregel op. De werkvoorraad blijft dus klein; alleen het werk per regel neemt toe — en bij een stamgegeven-trigger is dat het hele venster in plaats van één tijdvak.
- **De taak mag nergens een vast aantal tijdvakken aannemen.** Het venster loopt per periodetabel over een ander aantal tijdvakken, inclusief een restperiode in een jaar met een 53e week (§6.1). Een hard gecodeerde twaalf of dertien levert een te kort of te lang venster op en werkt door in laag 2 én laag 3.
- **De eerste dagovergang na de conversie is zwaar.** De conversie vult de triggertabel over heel 2026, dus die run bouwt voor alle werkgevers de brontabel en de lagen erboven op (§7.7). Dat is een eenmalige piek, maar wel de zwaarste run die de taak ooit draait.
- **De lijstbegrippen worden door AFAS meegeleverd en gevuld.** De klant hoeft niets in te richten om de cijfers te krijgen. **Beide sets staan wél open** voor eigen intellingen: bij medewerkers om correctie-looncomponenten te laten meetellen, bij uitzendkrachten als uitwijkmogelijkheid voor een looninrichting die niet in de standaarddefinitie past (§5.3). Dat betekent dat de inhoud per omgeving kan verschillen; binnen één omgeving — en dus binnen een vergelijkingsgroep — blijft de definitie gelijk.
- **Medewerkers en uitzendkrachten hebben elk een eigen set lijstbegrippen.** Voor medewerkers Profit Id 6.821 t/m 6.827 per inkomstenverhouding, voor uitzendkrachten 6.782 t/m 6.788 per plaatsing, met een eigen definitie (§5.3, §6.2). Die scheiding houdt de looninrichting van beide populaties uit elkaar en is toegestaan, omdat de uitkomsten van beide populaties nooit met elkaar worden vergeleken. De set voor uitzendkrachten is op 29 september 2026 opgeleverd (§12, punt W1 en actie 26); de set voor medewerkers is op 7 oktober 2026 besloten en moet nog worden bevestigd (§12, punt AL-a en actie 35).
- **Bij Plaatsingen verwerken in periodeverloning wordt het vaste loon toegerekend aan de plaatsing.** Dat is een uitgangspunt: het cao-team levert een aanvullende looninrichting waarmee een deel van het vaste loon wordt toegerekend aan een plaatsing, met een rekencomponent die het salaris terugverdeelt naar het plaatsingsdienstverband (§3.3, actie 39). De lijstbegrippen voor uitzendkrachten lezen dat toegerekende deel en de projecttoeslag; zonder die toerekening zou het loon per plaatsing vrijwel alleen uit de projecttoeslag bestaan.
- **Bij die variant groeien beide brontabellen.** Dezelfde inkomstenverhouding staat in bron medewerkers en, per plaatsing, in bron uitzendkrachten (§5.3). Dat geldt ook voor laag 2. Het gaat om een kleine doelgroep — detacheerders, meestal met één lopende plaatsing — maar de taak moet er bij het bouwen en testen van uitgaan dat één persoon in beide tabellen voorkomt.
- **De conversie levert voor uitzendkrachten geen volledig venster op, en dat is aanvaard.** Ze zet triggerregels klaar per verloonde werkgever en periodetabel (§7.7), dus de plaatsingen van 2026 komen mee voor zover de gegevens er zijn. Maar de functiecategorie bij plaatsing wordt pas in DP5 vastgelegd. Voor tijdvakken uit 2026 ontbreekt die indeling daardoor vaak, en zonder functiecategorie valt de regel in geen vergelijkingsgroep (§3.7). **De cijfers voor deze populatie worden dus pas bruikbaar na DP5** (besluit 99). Dat is bewust zo gekozen: eerst de opslag en de berekening, dan de indeling die ze betekenis geeft. De brontabel loopt intussen gewoon vol; alleen de vergelijking volgt later.
- **De verdichting kijkt breder dan één werkgever.** De tabel per functiecategorie gaat per rapportage-eenheid. Een run raakt daardoor ook regels van werkgevers die zelf niet zijn doorgerekend (§7.4).
- **Een wijziging in de functiecategorie-inrichting rekent de hele omgeving door.** Dat is de zwaarste run (§7.2). Hij past binnen het tijdvenster van de dagovergang en komt weinig voor, maar het is wel het geval waarmee bij het bouwen rekening moet worden gehouden — en het ongunstigste geval is die wijziging bij een uitzendbureau met weekverloning (§7.4). Omdat het een stamgegeven-trigger is, herbouwt hij voor elke werkgever ook het hele venster aan bronregels.
- **Inrichtingswerk aan de klantovereenkomst kan een run uitlokken.** Wijzigt de functiecategorie op de functie van een klantovereenkomst, dan worden alle werkgevers met een plaatsing op die functie doorgerekend, over hun hele venster (§7.2). Dat gebeurt buiten het salarisproces om, en degene die de mutatie doet — een medewerker van de uitlener of de inlener zelf via InSite — ziet er niets van. Beide Flex-mutaties zijn zeldzaam, maar het is wel een pad waarlangs een ogenschijnlijk kleine inrichtingswijziging een zware run veroorzaakt.
- **De berekening staat op één plek.** De taak rekent, de presentatielagen lezen. Het dashboard mag de berekeningen uit hoofdstuk 6 niet opnieuw implementeren in eigen queries; dan ontstaan er twee waarheden die apart onderhouden moeten worden.
- **Elk getal moet uitlegbaar zijn.** Support en consultancy krijgen vragen als "wat zit er in deze KPI" en "hoe komt dit percentage tot stand". De keten van loonbegrip naar periode naar venster naar gemiddelde moet daarom navolgbaar zijn zonder in de code te kijken.
- **De klant richt de functiecategorieën in.** Zonder die koppeling zijn er geen vergelijkingscijfers. Profit vult die koppeling niet automatisch aan.
- **Het loonheffingsnummer bepaalt de breedte van de vergelijking.** De taak leidt er per werkgever en periodetabel het RSIN uit af, en alle combinaties die op hetzelfde RSIN uitkomen vormen één vergelijkingsgroep (§5.2). Daardoor kan één werkgever over twee groepen uiteenvallen, en kunnen twee werkgevers juist samenvallen. Er is geen inrichting die de klant hiervoor hoeft aan te passen; wijzigt het nummer, dan verhuist de werkgever bij de volgende run naar een andere groep.
- **De gegevens zijn zo actueel als het laatste geaccordeerde tijdvak, en zo vers als de laatste geslaagde run.** Op de regel per inkomstenverhouding staan de einddatum en de datum van de laatste berekening, zodat dat bij de informatie kan worden vermeld.

---

## 11 Raakvlakken

| Onderwerp | Raakvlak |
| --- | --- |
| DP2 – Rapportage | Gebruikt dezelfde vier lagen met een rapportageperiode met **soort Rapportage** en een gevuld jaar (§5.2). Fase 2 voegt alleen regels en velden toe; er komt geen nieuwe tabel bij, op het stamgegeven arbeidsjaareenheid na (§5.7). De sleutel van laag 0 en laag 2 wijzigt niet; laag 3 krijgt het kwartiel erbij zodra DP2 de kwartielverdeling uitwerkt. **DP2 moet dezelfde functietoekenning per loontijdvak aanhouden** (§4.5), anders wijken de vergelijkingscijfers en de wettelijke rapportage van elkaar af en telt een medewerker die van functie wisselde in beide een andere categorie mee. DP2 hergebruikt ook de definities, de lijstbegrippen en de rekenwijze uit hoofdstuk 6; die moeten identiek zijn, anders leggen de KPI en de wettelijke rapportage verschillende uitkomsten naast elkaar. **DP2 moet er ook rekening mee houden dat het bruto jaarloon niet de wettelijk voorgeschreven maat is** (§6.5); welke grondslag de rapportage wél voorschrijft moet daar opnieuw worden vastgesteld. **De rekenrichting van de percentages verschilt per soort rapportage** (§6.5): op regels met soort *Rapportage* geldt onverkort de wettelijke richting uit het begrippenkader, op regels met soort *Recht op informatie* is het teken omgekeerd. DP2 moet daarom een **eigen ontsluiting** meeleveren met een filter op soort Rapportage en mag de verzamelingen uit §5.9 niet hergebruiken. De kwartielverdeling en de 5%-signalering worden in DP2 uitgewerkt. De medianen en de mediane loonverschilpercentages zitten al in het model, maar worden in fase 1 alleen **per functiecategorie** gevuld; het begrippenkader kent de mediaan uitsluitend organisatiebreed (§6.9). DP2 hoeft er dus geen velden voor toe te voegen, maar moet ze wél zelf vullen op de regels met een lege functiecategorie. **Geslacht X en niet ingevuld vragen in DP2 om extra aandacht:** deze arbeidsverhoudingen blijven buiten de berekening van het loonverschil (§3.8), maar tellen volgens de memorie van toelichting en de ministeriële regeling wél mee bij het aantal werknemers dat de rapportageplicht bepaalt, én in de noemer van het aandeel ontvangers van variabele componenten en van de kwartielverdeling. Teller en noemer lopen daar dus niet over dezelfde populatie. **De rapportage-eenheid wordt in DP2 op dezelfde manier bepaald** als hier (§5.2): uit de eerste negen posities van het loonheffingsnummer per werkgever en periodetabel. Daarmee is het RSIN altijd gevuld en hoeft DP2 het vullen van een veld nergens af te dwingen. Twee punten vragen daar wél aandacht. Bij een **eenmanszaak** staat er feitelijk een BSN in dat veld (§5.2); voor de rapportage speelt dat naar verwachting niet, omdat zo'n organisatie de grens van honderd werknemers niet haalt, maar DP2 moet vaststellen wat er gebeurt als die aanname niet opgaat. En DP2 moet bepalen of het **loonheffingsnummer zelf** bij de aanlevering moet worden meegegeven; dit ontwerp legt dat nummer niet vast. **De rapportage over uitzendkrachten hoort in haar geheel ook hier**, en niet bij de uitlener: het begrippenkader legt die verplichting bij de inlener (§3.3). Dat geldt zowel voor de rapportage die uit de brontabel *Loontransparantie bron extern* wordt gevoed — geparkeerd tot het ministerie en ABU/NBBU duidelijkheid geven over het aanleverformaat — als voor de scheiding tussen de populaties *Medewerkers* en *Ter beschikking gestelde arbeidskrachten* binnen de rapportage, die leunt op laag 2 en laag 3 zoals dit ontwerp ze vult. **Bij Plaatsingen verwerken in periodeverloning staat dezelfde inkomstenverhouding in beide populaties** (§3.3, §5.4): bij de medewerkers met het totale loon, bij de uitzendkrachten met het deel per plaatsing. Voor het recht op informatie is dat juist, maar in de rapportage mag deze arbeidsverhouding niet twee keer meetellen — niet in de aantallen en niet in de bedragen. DP2 moet bepalen in welke populatie zo iemand voor de rapportage telt. **De aard arbeidsverhouding bepaalt niet meer de populatie** (§3.3). Ze blijft een filter op de codes uit het begrippenkader en staat op laag 1 en laag 2, zodat de rapportage er zo nodig alsnog op kan indelen. **De drie filters uit §3.2 werken bij het vullen**: arbeidsverhoudingen buiten die filters staan niet in de brontabellen. DP2 moet bevestigen dat de rapportage ze nergens voor nodig heeft, ook niet voor de drempel van de rapportageplicht (punt AN-g). |
| RHR02179 – Plaatsingen verwerken in periodeverloning | Levert de verloningsvariant waarbij het loon van een gedetacheerde vanaf loonjaar 2027 zowel op het hoofddienstverband als per plaatsing wordt berekend. Deze variant gaat als enige naar **beide** brontabellen (§3.3, §5.3). Drie punten moeten daar kloppen: de taak moet een berekening op een **plaatsingsdienstverband** kunnen herkennen en aan de plaatsing kunnen koppelen; de plaatsingsdienstverbanden vallen onder dezelfde **inkomstenverhouding** als het hoofddienstverband, zodat het totaal in bron medewerkers compleet is; en de **looninrichting** van het cao-team rekent een deel van het vaste loon toe aan de plaatsing (hoofdstuk 10). Binnen één werkgever sluit deze variant declaratieverwerking en zichtbare neven- en subdienstverbanden uit, dus de combinaties blijven beperkt. |
| Cao-team | Levert de lijstbegrippen voor beide populaties (§5.3, §6.2) en, voor *Plaatsingen verwerken in periodeverloning*, een standaard looninrichting voor de projecttoeslag met een rekencomponent die het vaste loon terugverdeelt naar de plaatsing. De looninrichting voor de Basis CAO StiPP Algemeen is daarvoor al aangevuld. |
| DP3 – Uitzendkrachten | Alleen de **uitwisseling tussen in- en uitlener** blijft hier. Het ontwerpen **én** het vullen van de brontabel *Loontransparantie bron uitzendkrachten* horen sinds 22 september 2026 bij dit deelproject (§5.3), net als het vullen van laag 2 en laag 3 met populatie *Ter beschikking gestelde arbeidskrachten*; de rapportage hoort sinds 23 september in haar geheel bij DP2. Twee punten om voor DP3 vast te houden: de functie komt uit de **plaatsing** en niet van het dienstverband, en het recht op informatie wordt afgebakend per **verkooprelatie** — dat is de reden dat verkooprelatie in de sleutel van laag 2 en laag 3 zit (§5.4, §5.5). Wat DP3 toevoegt is de route waarlangs de uitlener zijn gegevens bij de inlener krijgt: formaat, frequentie en de anonimisering die het begrippenkader vraagt. |
| DP5 – Functiecategorie en flex | Levert de inrichting die dit ontwerp als gegeven aanneemt maar die nog niet compleet is: het **functiegroepen-model**, het **uitvraagformulier gelijkwaardige beloning** richting de inlener en de resterende **gegevens op de plaatsing**. Dat laatste raakt dit ontwerp rechtstreeks: de brontabel voor uitzendkrachten leest de functie van de plaatsing (§5.3), en zonder vastgelegde functiecategorie bij plaatsing valt een uitzendkracht in geen enkele vergelijkingsgroep (§3.7). **Tijdkritisch:** die vastlegging moet staan vóór de gegevens over 2027 worden opgebouwd, anders mist het eerste rapportagejaar de indeling. DP5 komt daarom tussen DP1 en DP2. DP5 levert daarnaast de gegevensverzameling **Functies per functiecategorie (klantovereenkomst)**, die de weergave en het rapport uit §8.4 bij een uitzendkracht van de inrichtingskant voorzien (DP5, US18). |
| DP4 – Vraag aan HR | Het type dossieritem Vraag aan HR is de route voor medewerkers die meer willen weten of meerdere dienstverbanden hebben. De **actieknop Vraag aan HR** op de stamkaart start de **profielkeuzepagina**, zodat de medewerker zelf het passende profiel kiest en niet automatisch in *Recht op informatie* belandt (§8.1). DP4 gebruikt twee gegevensverzamelingen uit dit ontwerp: **Loontransparantie per inkomstenverhouding (actuele functie)** — de variant van de populatie waar de medewerker in valt — en **Loontransparantie per functiecategorie** (§5.9). Daarmee is de gegevensverzameling die DP4 eerder alleen had gereserveerd concreet ingevuld. **DP4 moet de extra velden van het type vaststellen vóór wij de Pocket-pagina's kunnen bouwen** (§8.8): welke velden het type heeft, welke de medewerker zelf invult en welke alleen ter inzage zijn. Ook de vraag hoe de medewerker in Pocket bij het juiste profiel komt — er is daar geen profielkeuzepagina zoals in InSite — hoort bij DP4 en team Pocket samen. |
| Power BI | De brontabellen zijn opgezet als directe bron voor een dashboard. Het dashboard leest **de tabellen van laag 1 rechtstreeks** uit; er komt voor die laag geen gegevensverzameling (§5.9). Voor de verdichte cijfers kan het de verzamelingen op laag 2 en laag 3 gebruiken. Het beantwoordt de vragen die de KPI's oproepen: waar zit het verschil, hangt het samen met dienstjaren, piekt het in bepaalde perioden, wat gebeurde er na een functiewijziging. Ook de twee percentages op **jaarbasis** en de vier mediane percentages, die niet op de stamkaart staan (§8.2), zijn hier beschikbaar. Het dashboard leest en rekent niet opnieuw wat de taak al heeft berekend. **Het toont uitsluitend soort rapportage *Recht op informatie*** (§5.9, §6.5): de percentages tellen daar de andere kant op dan in de wettelijke rapportage, en twee richtingen in één grafiek of optelling zijn niet meer uit elkaar te houden. De route naar laag 1 staat alleen open voor applicatiebeheerders die BI-modellen mogen aanmaken; dat is geen extra risico, want die groep kan vandaag al bij salarisgegevens en de eindgebruiker kan geen BI-model aanmaken (§9.2). |
| Rapport Loontransparantie medewerker | Het gegenereerde rapport toont alle arbeidsverhoudingen naast elkaar — elk op de **actuele functie**, net als de KPI —, waar de stamkaart alleen die van het hoofddienstverband toont (§8.5). Het leest de gegevensverzameling Loontransparantie per inkomstenverhouding (§5.9). **Het wordt een rapport en geen document.** Sinds Profit 9 kan de workflow-editor een rapport genereren, en omdat er niets in het document hoeft te worden bewerkt is dat de betere keuze: er is geen conversie van DOCX naar PDF nodig, wat op AFAS Online merkbaar in de performance scheelt, en er is geen koppeling tussen de workflow en een type document nodig. Wil een klant er toch een vrije toelichting bij, dan kan dat via een memoveld dat op het rapport wordt opgenomen. Het rapport zelf wordt in **DP4** meegeleverd; team Content maakt het op. |
| Pocket | De medewerker ziet zijn loontransparantiegegevens in Pocket, naast zijn loonstrook en jaaropgave, en kan van daaruit direct een vraag aan HR insturen. Sinds 24 september 2026 hoort een deel daarvan **bij dit deelproject**: de **dataconnector** met vier modi en de pagina's *tonen* en *aanpassen* voor het type dossieritem Vraag aan HR (§8.8). De schermen in de app, de navigatie en de flow van het insturen bouwt team Pocket. De connector leest dezelfde regels als de stamkaart — laag 2 en laag 3 — en rekent zelf niets uit, zodat Pocket en de stamkaart nooit verschillende getallen tonen. **Pocket kan wél tussen dienstverbanden navigeren**, wat op de standaard stamkaart niet kan (§8.5); de connector krijgt daarom een dienstverband-parameter, met de toets dat dat dienstverband bij de ingelogde medewerker hoort. **Welke extra velden de Pocket-pagina's tonen, bepaalt DP4** en dat is blokkerend voor het bouwen ervan. |
| OutSite | De praatplaat voorziet in een route via OutSite voor accountants en inleners, op dezelfde gegevens. De uitwerking valt buiten deze beschrijving. |
| Jonas | Onderzocht wordt of Jonas boven de sectie in begrijpelijke taal kan uitleggen waar de medewerker naar kijkt, met eventueel een chatfunctie zoals die in Insight al bestaat. Aanleiding is dat een gemiddelde en een percentage niet voor iedere medewerker te duiden zijn, terwijl het recht op informatie juist voor iedereen geldt. Daarnaast is een tag *loontransparantie* in centraal bronbeheer geopperd, waarmee de klant zijn eigen beloningsstructuur en de wetgeving als context kan koppelen. Dit staat los van de basisfunctionaliteit, kan deels ná Profit 9 komen en valt **buiten scope van dit ontwerp**. Het raakt wel §8.7: hoeveel uitleg moet in de vaste teksten staan en hoeveel kan Jonas doen. |
| Jaarlijkse notificatie | De verplichting om medewerkers jaarlijks op hun recht te wijzen, automatiseren we niet in Profit. De klant vult dit zelf in, bijvoorbeeld met een bericht op het intranet. |

## 12 Openstaande keuzes

| Nr. | Onderwerp | Status |
| --- | --- | --- |
| D3b | Herleidbaarheid nu er geen ondergrens is (§9.3) | Besloten op 9 september 2026 · er komt geen ondergrens. Punt afgesloten. |
| E1 | Serialiseren van de verdichting per rapportage-eenheid (§7.4) | Open · beperkt na blok M en **verder beperkt op 23 september 2026**. Met één taak vanuit de dagovergang worden de rapportage-eenheden na elkaar verwerkt, dus twee werkgevers binnen één concern kunnen elkaars verdichting niet meer overschrijven. Nu er ook geen handmatige start komt (blok AC, punt AC13), blijft alleen het geval over waarin een zware run nog loopt als de volgende dagovergang begint. De eis — nooit meer dan één run tegelijk per rapportage-eenheid — hoort bij het technisch ontwerp. |
| F1 | Vulmoment van de brontabel (§7.1) | Herzien op 15 september 2026 · het vulmoment is het **accorderen van de salarisverwerking** · **opnieuw herzien op 16 september 2026**: het accorderen schrijft alleen triggerregels weg, de taak vult de brontabel in de dagovergang. Zie blok R punt R4 en blok U punt U7. Punt afgesloten. |
| F2 | Arbeidscategorie versus functiecategorie (§5.7) | Besloten op 9 september 2026 · het is hetzelfde begrip. Profit hanteert de term functiecategorie; er komt geen apart veld en geen apart sleutelonderdeel. |
| G1 | Eerste vulling bij bestaande klanten (§7.7) | Herzien op 15 september 2026 · de conversie vervalt · **opnieuw herzien op 16 september 2026**: er komt wél een conversie, maar die vult alleen de **triggertabel** over 2026. De eerstvolgende dagovergang bouwt de tabellen daarmee op. Zie blok U, punt U8. Punt afgesloten. |
| G2 | Bestaande ontsluiting van de brontabel (§9.2) | Vervallen op 15 september 2026 · we breiden de bestaande tabel Loonaangifte uren per medewerker niet meer uit, dus er is geen bestaande ontsluiting die moet worden herzien. De nieuwe brontabellen krijgen hun eigen afscherming (§9.2). |
| H1 | Afwijkende term variabele componenten (§6.1) | Besloten op 9 september 2026 · we hanteren variabele componenten. Het begrippenkader spreekt van "aanvullende of variabele componenten"; die volledige term is als veldnaam en als kolomkop onwerkbaar. |
| H2 | Mediane loonkloofpercentages (§5.5, hoofdstuk 11) | Besloten op 9 september 2026 · de vier mediane percentages zijn alsnog in het model opgenomen en worden vanaf fase 1 gevuld, zie blok K. DP2 hoeft ze niet opnieuw te beleggen. · **aangescherpt op 10 september 2026, zie blok M punt M22: fase 1 vult ze alleen per functiecategorie, de organisatiebrede varianten die de rapportage vraagt komen in fase 2** |
| H3 | Toelichting bij geslacht X of niet ingevuld (§3.8, §8.7) | Open · we tonen deze medewerkers dezelfde tabel als iedereen, zonder aparte melding. De vraag is of er een korte uitleg bij hoort dat de vergelijking bewust met beide groepen wordt getoond, of dat tekst hier juist ongewenste aandacht op de registratie vestigt. Voorleggen aan PM en team Content. |
| L10 | Inkomstenverhoudingnummer op de brontabel (§5.3, §5.4) | Afgehandeld op 10 september 2026 · geverifieerd in de Profit-repository. De tabel heeft naast het volgnummer dienstverband ook het veld **Inkomstenverhoudingnummer**. Laag 2 kan daar dus rechtstreeks op groeperen; een join naar de dienstverbandgegevens is niet nodig. Zie blok M, punt M15. |
| L11 | Aanname over inkomstenverhouding en dienstverband (§2, §5.3) | Afgehandeld op 10 september 2026 · de aanname **klopt in één richting**: een nieuwe inkomstenverhouding levert altijd ook een nieuw (sub)dienstverband op, dus de sleutel van laag 1 blijft ongewijzigd. Wat niet klopt is de omkering: meerdere dienstverbanden kunnen onder hetzelfde inkomstenverhoudingnummer vallen, als subdienstverbanden onder één kapstok. Zie blok M, punten M7 en M16, en blok O, punt O3. |
| N1 | Triggerregel bij wijziging van de functiecategorie-inrichting (§7.2) | Besloten op 10 september 2026 · een wijziging in de functiecategorie-inrichting schrijft een triggerregel weg voor **alle** werkgevers, op het laatste klaargezette tijdvak per periodetabel. Die wijziging hangt niet aan een werkgever of een tijdvak, dus een kleinere afbakening is er niet. Punt afgesloten. · Sinds blok R is dat het laatste **geaccordeerde** tijdvak. · **Aangevuld op 6 oktober 2026**: het is een trigger van soort *Stamgegevens* en herbouwt dus per werkgever het hele venster aan bronregels. Zie blok AI, punt AI4. |
| N2 | Prestatie van de dagelijkse run (§7.3, §7.4) | Besloten op 10 september 2026 · de run past binnen het tijdvenster van de dagovergang. Er komt geen begrenzing op het aantal rapportage-eenheden per run. Punt afgesloten. |
| N3 | Eerdere functieregels voor het dashboard (§5.9) | Besloten op 10 september 2026 · laag 2 krijgt **twee** gegevensverzamelingen. **Loontransparantie per inkomstenverhouding (actuele functie)** voor de KPI, het document en DP4, met een filter op rapportagejaar 0 én de actuele functie. **Loontransparantie per inkomstenverhouding (alle functies)** voor het dashboard, met alleen het filter op rapportagejaar 0. Ze verschillen uitsluitend in dat ene filter. Punt afgesloten. |
| L12 | Meertaligheid van de schermteksten (§8.7) | Open · de conceptteksten zijn alleen in het Nederlands opgesteld. Of het reguliere vertaalproces volstaat of er iets bijzonders speelt bij deze gevoelige teksten, hoort bij team Content. |
| L13 | Acceptatiecriteria | Open · dit document bevat geen toetsbare criteria waarmee is vast te stellen dat de bouw klaar is. Die horen in het FO zelf; te beleggen bij het opstellen daarvan. |
| J2 | Eenmanszaak met meerdere subheffingsnummers (§5.2) | **Afgesloten op 1 oktober 2026** · vervallen met blok AH. De terugval op de werkgeverscode bestaat niet meer: het RSIN komt uit de eerste negen posities van het loonheffingsnummer en is dus altijd gevuld. Subheffingsnummers van dezelfde eenmanszaak komen daarmee vanzelf op hetzelfde nummer uit, ook als ze in Profit als aparte werkgevers zijn ingericht. |
| O1 | Landafhankelijkheid van de bron (§1.1, §1.4, §9.6) | Besloten op 15 september 2026 · de scope van dit deelproject is **Nederland**. België valt buiten scope: de loongegevens lopen daar via het sociaal secretariaat en het is niet bekend hoe België invulling geeft aan de richtlijn. Een denkbare latere route staat in §9.6. De Caribbean vallen niet onder deze Europese regelgeving. De landtoets blijft, en komt er in de taak bij (§7.3). Punt afgesloten; zie blok S, punt S1. |
| R1 | Meerdere actuele dienstverbanden op de stamkaart (§8.5) | **Afgesloten op 23 september 2026** · wisselen tussen dienstverbanden is technisch niet mogelijk op de standaard stamkaart, dus de uitwerking met tabbladen vervalt. We tonen het **hoofddienstverband**, zonder melding op het scherm: de activering *Meerdere dienstverbanden* geldt maar voor een deel van de klanten en de functieomschrijving in de subtitel van tegel 1 maakt al zichtbaar welk dienstverband wordt getoond. De uitleg komt in de help. Zie blok AC, punt AC8. |
| R2 | Vrije velden van de functiecategorie op de stamkaart (§8.3) | Open · we tonen geen vrije velden van de functiecategorie, omdat de klant naar verwachting niet kan sturen wélke daarvan worden getoond. Die aanname is niet geverifieerd. Blijkt sturing wél mogelijk, dan is het tonen van geselecteerde vrije velden in het pagina-onderdeel *Functie* alsnog een optie. Zie actie 23. |
| AC-a | Lengte van de functiecategorie in de subtitel (§8.2) | Open · de subtitel van de tegels bestaat uit de functiecategorie of de functie, gevolgd door *laatste 12 maanden*. Bij een lange omschrijving kan die tekst afbreken in een smalle tegel. Te bevestigen bij de bouw; anders is een kortere periodeaanduiding nodig. |
| AC-b | Info-icoon op een aanraakscherm (§8.2, §8.7) | Open · de drie uitlegteksten bevatten alle drie bedragen; sinds blok AO hebben tegel 2 en 3 geen info-icoon meer. Op Pocket en op een tablet bestaat hover niet. Controleren of het info-icoon daar op tik opent; zo niet, dan zijn die bedragen op mobiel onbereikbaar en is een andere route nodig. |
| AC-c | Vorm van het filter op de actuele functie (§5.9) | Open · het filter vergelijkt het veld Functie op de regel met de actuele functie uit de stamgegevens van het dienstverband. Dat is geen vergelijking met een vaste waarde, dus er is een koppeling of een berekend veld voor nodig. Welke vorm dat wordt, hoort bij het technisch ontwerp. Let daarbij op subdienstverbanden: het filter moet de functie van het **kapstokdienstverband** volgen, net als de taak bij het samenstellen van de regel (§5.4). |
| AD-a | Verschil tussen Pocket en de stamkaart bij meerdere dienstverbanden (§8.5, §8.8) | Open · Pocket kan tussen dienstverbanden navigeren, de standaard stamkaart niet (punt R1). Een medewerker met twee dienstverbanden ziet in de app dus beide en op de stamkaart één. Inhoudelijk aanvaard — Pocket vult het recht voller in, niet beperkter — maar het raakt de help en de communicatie: de uitleg "je ziet alleen je hoofddienstverband" geldt niet voor Pocket. Voorleggen aan PM en team Content. |
| AD-b | Extra velden van Vraag aan HR in Pocket (§8.8) | Open en **blokkerend** · de pagina's *tonen* en *aanpassen* zijn pas te bouwen als DP4 heeft vastgesteld welke extra velden het type heeft, welke de medewerker zelf invult en welke alleen ter inzage zijn. Uit te vragen bij DP4, met een datum. |
| AD-c | Profielkeuze in Pocket (§8.1, §8.8) | Open · op de stamkaart start de actieknop de profielkeuzepagina (punt AD6). Of Pocket zo'n keuzepagina kent is niet bekend. Zo niet, dan moet worden bepaald hoe de medewerker daar bij het juiste profiel komt — en of hij in Pocket überhaupt meer dan één profiel te kiezen krijgt. Af te stemmen met team Pocket en DP4. |
| AD-d | Veldsoorten die Pocket aankan (§8.8) | Open · Pocket rendert de schermdefinitie die ook de InSite-webform voedt. Wat de app kan tonen is daarmee begrensd door dat model. Of alle velden die DP4 op het type zet in Pocket te tonen zijn, is niet geverifieerd. Te controleren zodra de velden bekend zijn (punt AD-b). |
| T9 | Populatiefilter voor uitzendkrachten (§3.2, §3.3, §5.3) | **Besloten op 22 september 2026** · overgenomen uit het begrippenkader: **soort inkomstenverhouding 11, 13, 15 of 17** — dezelfde vier als bij eigen medewerkers, want §3.7.3 maakt op dat punt geen onderscheid — en **aard arbeidsverhouding 11, 22 of 82** uit §3.7.2. De toevoeging bij code 11 dat die *alleen bij de inlener* meetelt, geldt voor de **rapportage** en niet voor de brontabel: de uitlener heeft die loongegevens wél en heeft ze nodig voor het recht op informatie (§3.3). Punt afgesloten; zie blok AA, punt AA1. · **Herzien op 13 oktober 2026**: de aard arbeidsverhouding bepaalt niet meer de populatie; de indeling volgt de verloningsvariant. Het filter op aard blijft, met de codes van beide populaties samen. Zie blok AN, punten AN1 en AN2. |
| Q1 | Functiecategorie op het uitvraagformulier gelijkwaardige beloning richting de inlener (hoofdstuk 11, raakvlak DP5) | Open · bespreekpunt voor PM, **uitwerking verhuisd naar DP5** (blok AA, punt AA4). Bij een terbeschikkingstelling geeft de inlener het pakket aan arbeidsvoorwaarden door aan de uitlener via het uitvraagformulier gelijkwaardige beloning. De functiecategorie staat daar nu niet op, terwijl de uitlener die nodig heeft om de uitzendkracht in de juiste vergelijkingsgroep te plaatsen. Zonder dat veld is bij plaatsing niet vastgelegd in welke categorie de functie valt en is dat achteraf niet meer te herleiden. De vraag aan PM is of het veld aan het formulier wordt toegevoegd, wie daarvan eigenaar is (AFAS, ABU/NBBU of de klant) en per wanneer. **Tijdkritisch:** de vastlegging moet staan vóór de gegevens over 2027 worden opgebouwd, anders mist het eerste rapportagejaar de indeling. Hier geregistreerd omdat dit ontwerp dezelfde functiecategorie-indeling gebruikt. Zie actie 21. |
| W1 | Lijstbegrippen voor uitzendkrachten (§5.3, §6.2) | **Afgesloten op 29 september 2026** · het cao-team heeft de set opgeleverd: **zeven** begrippen met Profit Id **6.782 tot en met 6.788**, per plaatsing, door AFAS meegeleverd en dichtgezet. Daarmee vervalt de blokkade die er sinds 22 september 2026 op dit deelproject lag (blok AA, punt AA2). Voor eigen medewerkers golden toen nog de bestaande lijstbegrippen van de loonaangifte; die leveren de acht grootheden per dienstverband. De set voor uitzendkrachten telt er zeven: *waarde niet in geld uitgekeerd loon* ontbreekt, omdat dat bedrag niet naar een plaatsing te herleiden is. De definitie volgt het kader uitzendkrachten van 3 maart 2026: bruto per opdracht is de som van de looncomponenten onder het reguliere tarief plus de reserveringen vakantiegeld en arbeidsvoorwaardenbedrag, zonder het werknemersdeel pensioen en de bijtelling auto; de variabele componenten zijn de componenten onder het bijzondere tarief minus vakantiebijslag en opname arbeidsvoorwaardenbedrag. Onbelaste componenten en componenten onder nultarief tellen niet mee. Punt afgesloten; zie blok AF en actie 26. · **Aangevuld op 7 oktober 2026**: die definitie stond alleen hier en niet in de hoofdstukken zelf. Ze is nu verwerkt in §5.3, §6.1 en §6.2, en daarbij bleek de gedeelde formule voor het bruto jaarloon niet te kloppen voor deze populatie. Zie blok AJ en punt AJ-a. · **Medewerkers krijgen op 7 oktober 2026 ook een eigen set**, Profit Id 6.821 t/m 6.827; zie blok AL en punt AL-a. Op diezelfde datum vervalt het dichtzetten: **beide** sets staan voortaan open voor eigen intellingen van de klant (blok AL, punten AL2 en AL4). |
| X6 | Moment en reikwijdte van de uitlevering (§9.5) | Open · voorstel uit het voortgangsoverleg van 22 september 2026: de functionaliteit wél uitleveren, met een duidelijke disclaimer dat het functionaliteit in ontwikkeling is, maar de standaard autorisatierollen voor ESS en MSS nog niet openzetten, zodat in eerste instantie alleen functioneel beheer meekijkt. Aanleiding is de onzekere wetgeving (§1.1) in combinatie met de aard van de gegevens: loongegevens wil je niet openzetten voordat vaststaat dat ze gezien mogen worden. Daar staat tegenover dat vroeg uitleveren klantfeedback oplevert die nog in Profit 9 kan worden verwerkt. **Nog niet besloten**; §9.5 gaat vooralsnog uit van generiek uitleveren onder de HR-conditie. Te bevestigen door PM. Zie actie 29. |
| AE-a | Omschrijving van de vrije rubriek (§5.3) | Open · de klant geeft de vrije rubriek een eigen invulling **en** een eigen omschrijving. Dat de rubriek openstaat is met AE6 besloten; waar de klant die omschrijving vastlegt en hoe het dashboard hem toont, is dat niet. Zonder die omschrijving staat er in het dashboard een bedrag zonder label. Zie actie 30. |
| AE-b | Verklarende bedragen op Loontransparantie bron extern (§5.3) | Open · die tabel krijgt de negen velden nu bewust niet (AE4). Ze dienen het dashboard en niet de rapportageverplichting van de inlener, en een veld waaraan de uitlener eigen intellingen heeft toegevoegd betekent bij de inlener iets anders. Te beleggen bij DP2, samen met de rest van die tabel (besluit 98). |
| AE-c | Zwangerschap en bevalling als afzonderlijk begrip (§5.3) | Open · in de brainstorm besproken als mogelijk tiende begrip, maar het bestaande lijstbegrip is leeg. Voorlopig buiten scope gehouden. Opnieuw te bezien als het begrip alsnog wordt gevuld. |
| AI-a | Stamgegevens buiten het venster en de soort rapportage *Rapportage* (§5.3, §7.3) | Open · een stamgegeven-trigger herbouwt de bronregels van het **venster**; daarbuiten houden ze de functie en de functiecategorie die golden toen ze voor het laatst zijn weggeschreven. Voor dit deelproject is dat geen probleem, want de medewerker ziet alleen het venster. Voor DP2 wél: een afgesloten kalenderjaar reikt verder terug dan het venster, dus zo'n jaar kan deels op de oude en deels op de nieuwe indeling staan. Dat moet daar een bewuste keuze worden — de indeling bevriezen op het moment van rapporteren, of het hele jaar herbouwen — en niet een gevolg van hoe dit deelproject zijn venster bepaalt. Te beleggen bij DP2. Zie actie 31. |
| AI-b | Prestatie van een stamgegeven-trigger bij een uitlener (§7.3, §7.4, hoofdstuk 10) | Open · de zwaarste run herbouwt voortaan voor alle werkgevers het hele venster aan bronregels, bij weekverloning drieënvijftig tijdvakken per plaatsing. Punt N2 stelde vast dat de run binnen het tijdvenster van de dagovergang past, maar dat was vóór deze verzwaring en zonder de uitzendkrachtpopulatie. Opnieuw te toetsen bij het technisch ontwerp, met een uitzendbureau met weekverloning als maatgevend geval. Zie actie 32. |
| AJ-a | **De gebouwde formule voor het bruto jaarloon van een uitzendkracht moet worden hersteld** (§6.1) | Open en **urgent** · de bouw is uitgegaan van één gedeelde formule, waarin het bruto jaarloon ontstaat door de variabele componenten van het totaalloon af te trekken. Dat werkt alleen als het loonbegrip het bijzondere deel ál bevat, en bij lijstbegrip 6.783 is dat niet zo (blok AJ, punt AJ1). De gebouwde routine trekt daardoor een bedrag af dat er nooit bij is opgeteld: het bruto jaarloon van **elke** uitzendkracht valt te laag uit, precies met de waarde van zijn variabele componenten. Het werkt door in het bruto uurloon, het totaal uurloon, de groepsgemiddelden, de medianen en alle loonverschilpercentages van de populatie *Ter beschikking gestelde arbeidskrachten*. Te melden bij de programmeur en te herstellen vóór de uitlevering; daarna de bestaande gegevens opnieuw laten opbouwen. Zie actie 33. |
| AK-a | **Controleren wat de bouw in het veld Loon LB/PH heeft gezet** (§5.3, §6.1) | Open en **urgent** · het veld heette *Loon LB/PH normaal tarief* en §6.2 schreef voor dat de twee velden samen LnLbPh vormen. Volgt de bouw die tekst, dan telt de routine beide velden op terwijl het eerste al het totaal bevat (blok AK, punt AK1), en telt het bijzondere tarief dubbel in het loon terwijl het er maar één keer af gaat. Het bruto jaarloon van **elke eigen medewerker** valt dan te **hoog** uit, met precies het bedrag onder bijzonder tarief. Dat is de spiegelbeeldige fout van punt AJ-a en raakt de grootste populatie. Eerst vaststellen wát er gebouwd is — het kan ook goed staan — en pas daarna bepalen of er hersteld moet worden. Zie actie 34. |
| AL-a | **Oplevering van de set lijstbegrippen voor medewerkers** (§5.3, §6.2) | Open en **blokkerend** · de set met Profit Id 6.821 t/m 6.827 is op 7 oktober 2026 besloten (blok AL) maar nog niet bevestigd opgeleverd door het cao-team. Zolang die er niet is, kan de brontabel voor medewerkers niet langs de nieuwe weg worden gevuld. Te bevestigen zijn: de zeven nummers, dat 6.822 zowel zonder als met het tarieffilter uitleesbaar is, dat alle zeven **per dienstverband** beschikbaar zijn (*sinds blok AN: per inkomstenverhouding*), en dat de klant er eigen intellingen aan kan toevoegen. Zie actie 35. |
| AL-b | Staat de set voor uitzendkrachten ook open? (§5.3) | **Afgesloten op 7 oktober 2026** · ja. De aanleiding is daar een andere dan bij medewerkers: klanten moeten in bepaalde situaties een **uitwijkmogelijkheid** hebben, omdat de looninrichting van een uitzendorganisatie zich niet altijd in de standaarddefinitie laat vangen. Daarmee staan beide sets open en herziet dit besluit 108. Zie blok AL, punt AL4. |
| AN-a | Soort inkomstenverhouding bij een UMC met afwijkende afspraken (§3.2) | Open · een UMC heeft mogelijk met de Belastingdienst afgesproken een andere soort inkomstenverhouding te gebruiken, vermoedelijk 35. Die medewerkers vallen dan buiten het filter. Uitzoeken of dat zo is en of het filter daarvoor moet worden verruimd. Zie actie 40. |
| AN-b | **De gebouwde indeling op type periodetabel aanpassen** (§3.3, §7.3) | Open en **blokkerend vanaf loonjaar 2027** · de bouw deelt in op het type periodetabel. Voor *Plaatsingen verwerken in periodeverloning* levert dat alleen regels in bron medewerkers op, en nooit het loon per plaatsing. De indeling moet worden aangepast naar blok AN; daarvoor komt een nieuwe POA. Daarbij ook nagaan of de filters op soort inkomstenverhouding, aard arbeidsverhouding en soort medewerker erin zitten, en of bron medewerkers per inkomstenverhouding wordt gevuld. Zie actie 41. |
| AN-c | Herkenbaarheid van het plaatsingsdienstverband (§5.3, hoofdstuk 11) | Open · de taak moet bij *Plaatsingen verwerken in periodeverloning* een berekening op een plaatsingsdienstverband kunnen herkennen en aan de plaatsing en de verkooprelatie kunnen koppelen. Af te stemmen met de ontwerper van RHR02179. Zie actie 42. |
| AN-d | Juridische status van gedetacheerden (§3.3) | Open, **niet blokkerend** · of een gedetacheerde met een gewone arbeidsovereenkomst als eigen personeel of als ter beschikking gestelde arbeidskracht telt, zeggen wet- en regelgeving niet. De gekozen indeling is de best uitlegbare op dit moment. Brengen de Kamerbehandeling of latere specificaties duidelijkheid, dan is de indeling bij te sturen zonder het datamodel te wijzigen. |
| AN-e | Uitleg bij twee sets cijfers voor één detacheerder (§8.1, §8.7) | Open · een detacheerder met *Plaatsingen verwerken in periodeverloning* ziet op de medewerker-stamkaart en op de plaatsing-stamkaart verschillende cijfers. Hoe dat in de help en in de info-iconen wordt uitgelegd, hoort bij team Content. Zie actie 43. · **Deels opgevangen op 19 oktober 2026**: de toelichting op de plaatsing-stamkaart noemt dat de vergelijking binnen dezelfde opdrachtgever plaatsvindt (blok AO, punt AO9). De uitleg in de help blijft nodig. |
| AN-f | Fictieve dienstbetrekkingen in de populatie medewerkers (§3.2) | **Afgesloten op 13 oktober 2026** · het filter op aard arbeidsverhouding blijft, op de codes uit het begrippenkader. Musicus, deelvisser, thuiswerker en andere fictieve dienstbetrekkingen vallen daarmee af. Alleen de indeling in populaties volgt de aard niet meer. Zie blok AN, punt AN1; actie 44 vervalt. |
| AN-g | Arbeidsverhoudingen buiten de filters en DP2 (§3.2, hoofdstuk 11) | Open · sinds AN13 staan arbeidsverhoudingen met een soort inkomstenverhouding, aard of soort medewerker die niet meetelt niet in de brontabellen. DP2 moet bevestigen dat de rapportage ze nergens voor nodig heeft, ook niet voor de drempel van de rapportageplicht. Is dat wel zo, dan moet DP2 ze uit de salarisgegevens halen of moet een filter worden verruimd, met een eenmalige vulling van de triggertabel. Zie actie 45. |
| AO-a | Toelichting van de sectie via een script (§8.1, §8.7) | Open · de vaste toelichting per stamkaart is nog niet als metagegeven in te checken en wordt met een SQL-script geleverd. Met de programmeur vaststellen op welke tabel, welk veld en welke records van de drie standaard stamkaarten de tekst landt, en hoe de vertaling verloopt (punt L12). Zie actie 46. |

Alle punten die als PM1 tot en met PM8 bij PM voorlagen, zijn op 3 september 2026 besloten. De uitkomsten staan hieronder in blok E.

Afgehandeld in blok A:

| Nr. | Onderwerp | Besluit |
| --- | --- | --- |
| A2 | Populatiefilter op soort inkomstenverhouding (§3.2) | Voor eigen medewerkers 11, 13, 15 en 17 |
| A5 | Populatiefilter op aard arbeidsverhouding (§3.3) | Voor eigen medewerkers 1, 18, 21, 23, 24 en 83 · **herzien op 13 oktober 2026**: één filter voor beide populaties met de codes 1, 11, 18, 21, 22, 23, 24, 82 en 83, dat niet de populatie bepaalt. Zie blok AN, punt AN1 |
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
| F5 | Aard arbeidsverhouding en soort inkomstenverhouding (§5.3) | Alleen op de standregel, als momentopname | Ook per periode in de brontabel; het zijn per tijdvak vastgelegde loonaangiftegegevens die binnen een jaar kunnen wijzigen · sinds blok AN bepaalt de aard niet meer de populatie |
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
| L4 | Peilmoment van het populatiefilter (§3.5) | Niet belegd; §5.3 en §5.4 noemden verschillende peilmomenten | Soort inkomstenverhouding en aard arbeidsverhouding toetsen we **per tijdvak**; alleen kwalificerende tijdvakken tellen mee. Loon en uren toetsen we over het venster als geheel. De ultimo-waarde op de regel is een kenmerk, niet de filterwaarde · sinds blok AN komt daar de **soort medewerker** bij, getoetst bij het vullen van de brontabellen · sinds AN13 worden alle drie de filters per tijdvak bij het vullen van de brontabellen getoetst |
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

Herzien in blok T, de laag 0-ronde, op 16 september 2026:

Aanleiding was een doorloop van laag 0. De sleutelopzet met een soort naast een waarde bleek lastig te lezen en te filteren, en de soort van de rapportageperiode was alleen af te leiden uit een jaartal 0. Daarnaast stonden er drie velden op die niet te bepalen of nog niet te onderbouwen zijn.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| T1 | Naam van laag 0 (§5.1, §5.2) | Alleen aangeduid als *rapportageperiode* | De tabel heet **Loontransparantie rapportage**, in lijn met de andere lagen. *Rapportageperiode* blijft het begrip voor één regel |
| T2 | Sleutel van laag 0 (§5.2); herziet J1 | Een samengestelde sleutel met soort rapportage-eenheid, rapportage-eenheid, rapportagejaar en volgnummer | Een **primaire sleutel Rapportage ID** (surrogaat) met daarnaast een **unieke sleutel** op RSIN, werkgever, soort rapportage, jaar en volgnummer. Laag 2 en 3 verwijzen alleen nog naar het Rapportage ID |
| T3 | Groeperingsvelden (§5.2); herziet J1 | Soort rapportage-eenheid plus één waardeveld waarvan de betekenis van het soort afhing | Twee aparte velden **RSIN** en **Werkgever**, waarvan er precies één is gevuld. Eenvoudiger te lezen en te filteren, en er staat nooit een werkgeverscode in een veld dat RSIN heet |
| T4 | Soort rapportageperiode (§5.2); herziet J8 | Vervallen; het rapportagejaar bepaalde de soort, met 0 voor het venster | Er komt **wél** een veld **Soort rapportage**: een codetabel met *Recht op informatie* en *Rapportage*. Een magische waarde 0 maakt de betekenis afhankelijk van een conventie die elke query moet kennen. Het soort zit ook in de unieke sleutel |
| T5 | Veld Jaar (§5.2) | Rapportagejaar, altijd gevuld, 0 bij het venster | **Leeg** bij soort Recht op informatie. Een voortschrijdend venster hoort bij geen enkel kalenderjaar |
| T6 | Begindatum en einddatum op laag 0 (§5.2, §5.9, §7.8) | Indicatieve datums voor het bereik waarover is gerekend | **Vervallen.** Ze zijn niet betrouwbaar te bepalen als een werkgever meerdere periodetabellen heeft, en de exacte grenzen staan al per arbeidsverhouding op laag 2 |
| T7 | Status rapportageperiode (§5.2, §5.7) | Fase 2-veld met in bewerking, vastgesteld, ingediend en gecorrigeerd | **Vervallen uit dit ontwerp.** Welke statussen de rapportage nodig heeft is hier niet te overzien; DP2 werkt dat uit |
| T8 | Rapportage-eenheid op laag 3 (§5.5); herziet I4 en J1 | Expliciet in de sleutel, zodat de tabel zelfstandig leesbaar is | **Vervallen.** De eenheid volgt uit het Rapportage ID; herhalen zou de gegevens op twee plekken zetten. Een weergave of dashboard koppelt naar laag 0 om het RSIN te tonen |

Herzien in blok U, de laag 2-, laag 3- en triggerronde, op 16 september 2026:

Aanleiding was een doorloop van laag 2 en laag 3, in het verlengde van blok T, en een technische toets op het vulmoment. De sleutels van beide lagen waren samengesteld en breed, terwijl laag 0 er net een surrogaatsleutel bij had gekregen. Op laag 2 stonden twee velden die er niet thuishoren. En het direct vullen van laag 1 bij het accorderen bleek in de praktijk op de batchservice te drukken.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| U1 | Primaire sleutel van laag 2 (§5.4) | Een samengestelde sleutel van zes velden | Een **GUID** als primaire sleutel, met daarnaast een **unieke sleutel** op Rapportage ID, medewerker, nummer inkomstenverhouding, verkooprelatie en functie. Dezelfde afweging als op laag 0, maar met een GUID in plaats van een teller: deze tabel wordt voor veel werkgevers tegelijk opgebouwd en runs mogen naast elkaar lopen |
| U2 | Werkgever op laag 2 (§5.4) | Sleutelonderdeel | **Vervallen**, ook als kenmerk. Het inkomstenverhoudingnummer wordt per medewerker uitgegeven, dus medewerker plus nummer is binnen een rapportageperiode al eenduidig. Welke werkgever erbij hoort volgt uit laag 0 en uit de bronregels op laag 1 |
| U3 | Periodetabel op laag 2 (§4.3, §5.4) | Kenmerk op de regel, om vast te leggen hoe de rapportageperiode is bepaald | **Vervallen.** De periodetabel zegt iets over een tijdvak en staat daarom op de bronregel. Op deze regel is hij bovendien niet altijd eenduidig: stapt een werkgever binnen het venster over, dan bevat één regel tijdvakken uit twee periodetabellen |
| U4 | Populatie (§5.4, §5.5) | Fase 2-veld op laag 2, met de waarden eigen medewerker en uitzendkracht | Codetabel **Populatie loontransparantie** met *Medewerkers* en *Ter beschikking gestelde arbeidskrachten*, vanaf **fase 1** gevuld. De wettelijke term is breder dan uitzendarbeid en komt terug in de rapportage. Het veld blijft niet leeg, omdat het op laag 3 sleutelonderdeel is |
| U5 | Primaire sleutel van laag 3 (§5.5) | Een samengestelde sleutel van vier velden | Een **GUID** als primaire sleutel, met een **unieke sleutel** op Rapportage ID, populatie, functiecategorie en verkooprelatie |
| U6 | Verkooprelatie op laag 3 (§5.5); scherpt R9 aan | Sleutelonderdeel, in fase 1 leeg en in fase 2 gevuld bij populatie uitzendkracht | Toegelicht op het niveau van de **soort rapportage**: het recht op informatie wordt gegroepeerd op verkooprelatie, de wettelijke rapportage niet. Op een regel met soort Rapportage blijft het veld dus leeg, ook bij populatie Ter beschikking gestelde arbeidskrachten |
| U7 | Vulmoment van laag 1 (§5.3, §7.1); herziet R4 en M2 | Direct bij het accorderen van de salarisverwerking | Het accorderen schrijft **alleen triggerregels** weg, voor het geaccordeerde tijdvak én voor elk tijdvak dat met terugwerkende kracht is geraakt. De taak vult laag 1 in de dagovergang. Drie redenen: werkgevers onder hetzelfde RSIN worden zo één keer bijgewerkt in plaats van per werkgever, een werkgever met meerdere periodetabellen valt in dezelfde run, en de taak zit verlonen, accorderen, loonstroken en loonaangifte niet in de weg op een batchservice die overdag al zwaar belast is |
| U8 | Eerste vulling (§7.7); herziet R7, M6, I1 en G11 | Geen conversie; de brontabellen lopen vanaf de eerstvolgende keer accorderen vol | De **conversie naar Profit 9 vult de triggertabel** voor alle verloonde werkgevers, periodetabellen en periodes in 2026. De eerstvolgende dagovergang bouwt daarmee de brontabel en de lagen erboven op. Het bezwaar uit R7 vervalt: de conversie rekent zelf niets uit en haalt de bedragen niet uit een tweede bron, ze zet alleen werkvoorraad klaar |
| U9 | Reikwijdte van de venstertoets (§7.3); scherpt M4 aan | Een triggerregel buiten het venster leidde tot niets en werd alleen opgeruimd | De **bronregel wordt altijd bijgewerkt**, ook buiten het venster. De venstertoets bepaalt alleen of de lagen erboven opnieuw worden samengesteld. Nodig omdat de brontabellen niet worden opgeschoond en DP2 een compleet kalenderjaar moet kunnen vaststellen (R14) |
| U10 | Omvang van de transactie (§7.8); scherpt I5 aan | Laag 2, dan laag 3, dan de rapportageperiode | Laag 1 hoort er nu ook bij en gaat vooraan. Een mislukte run laat dus ook de brontabel ongewijzigd; de berekende salarisgegevens worden alleen gelezen en kunnen nooit worden geraakt |

Herzien in blok R, het datamodel en het vulproces, op 15 september 2026:

Aanleiding was de vraag om één datamodel te hebben waarin de berekeningen voor zowel het recht op informatie als de rapportage kunnen worden opgeslagen, met daarin het onderscheid tussen medewerkers en uitzendkrachten. Uitzendkrachten pasten niet in het model dat op de loonaangifte was gebaseerd. Dat raakt hoofdstuk 1, 2, 4, 5, 6, 7, 9, 10 en 11.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| R1 | Bron van de bedragen (§5.3, §6.2); herziet I2 en G3 | De loonaangifterubrieken, vastgelegd in de bestaande tabel Loonaangifte uren per medewerker | De **berekende salarisgegevens**, ontsloten via **lijstbegrippen** die AFAS standaard meelevert. Voor uitzendkrachten is dit de enige begaanbare weg: de loonaangifte bevat alleen het totaal over alle plaatsingen heen, terwijl het recht op informatie per verkooprelatie moet worden afgebakend. We hanteren dezelfde route voor medewerkers, zodat er één werkwijze is |
| R2 | Opzet van laag 1 (§5.1, §5.3); herziet G3 | Eén bestaande tabel, uitgebreid met zeven rubrieken | **Drie eigen brontabellen**: *Loontransparantie bron medewerkers*, *Loontransparantie bron uitzendkrachten* en *Loontransparantie bron extern*. Uitzendkrachten vragen extra sleutels die het model voor gewone medewerkers onnodig complex zouden maken, en de bronnen zijn in de rapportage toch al fysiek gescheiden |
| R3 | Intellingen in de bedragen (§5.3, §6.2) | Niet belegd | Alleen intellingen die **per dienstverband** zijn berekend tellen mee. Intellingen op arbeidsvoorwaardenniveau, zoals een auto van de zaak en de pensioenpremie, vallen af omdat ze niet naar een plaatsing herleidbaar zijn. Bij uitzendkrachten vervalt daardoor ook de waarde niet in geld uitgekeerd loon (rubriek 1321) uit de formule voor de variabele componenten |
| R4 | Vulmoment van laag 1 (§7.1); herziet G8, M2 en F1 | Het klaarzetten van de loonaangifte | Het **accorderen van de salarisverwerking**. Dat is het moment waarop de berekende gegevens definitief zijn; wachten op het klaarzetten zou de cijfers laten achterlopen en zou voor uitzendkrachten helemaal niet werken |
| R5 | Eindpunt van het venster (§4.2); herziet B1 en G8 | Het laatste klaargezette aangiftetijdvak | Het **laatste geaccordeerde tijdvak**, per werkgever en periodetabel. Zo reikt het venster nooit verder dan de gegevens |
| R6 | Trigger bij intrekken (§7.2, §7.6); herziet G9 en M13 | Intrekken van een loonaangifte | **Terugdraaien van een geaccordeerde salarisverwerking** |
| R7 | Eerste vulling (§7.7); herziet M6, I1 en G11 | Eenmalig over 2026 in de conversie naar Profit 9 | **Geen conversie.** De brontabellen zijn nieuw en lopen vanaf de eerstvolgende keer accorderen vol, voor nieuwe én bestaande klanten gelijk. Een conversie zou de bedragen niet betrouwbaar kunnen reconstrueren: verwerkingen kunnen zijn verwijderd en een herberekening achteraf kan afwijken van wat destijds is uitbetaald |
| R8 | Functie in laag 1 (§4.5, §5.3, §5.4); scherpt M8 aan | De functie stond niet in de brontabel en werd door de taak per tijdvak afgeleid | De **functie en de functiecategorie staan op de bronregel**. De toekenning per aangiftetijdvak blijft ongewijzigd; alleen wordt hij nu bij het vullen vastgelegd in plaats van bij elke run opnieuw afgeleid. Bij een uitzendkracht komt de functie uit de **plaatsing** |
| R9 | Verkooprelatie in laag 2 en 3 (§5.4, §5.5) | Niet aanwezig | **Verkooprelatie** komt in de sleutel van beide lagen. Alleen gevuld bij populatie uitzendkracht. Zonder dat sleutelonderdeel zouden twee plaatsingen bij verschillende inleners op één regel samenvallen en zou het loon van de ene inlener in de vergelijking van de andere terechtkomen |
| R10 | Gegevensverzamelingen op laag 1 (§5.9); herziet J7 | Uitbreiding van de bestaande verzameling Loonaangifte uren per medewerker | Een **eigen verzameling** op *Loontransparantie bron medewerkers*, met medewerkerautorisatie. De verzamelingen op de brontabellen voor uitzendkrachten en extern horen bij DP3 respectievelijk DP2 |
| R11 | Afscherming van laag 1 (§9.2); sluit G2 | De bestaande ontsluiting moest worden herzien vóór uitlevering | **Vervalt.** Met eigen tabellen is er geen bestaande view of datamodeldefinitie die meelift; de afscherming wordt meteen goed ingericht |
| R12 | Landfilter in de taak (§7.3, §9.6); herziet O4 gedeeltelijk | Niet nodig, want de brontabel werd alleen door de Nederlandse loonaangifte gevuld en de gegevens filterden zichzelf | De taak krijgt een **expliciete landtoets** bij het selecteren van de arbeidsverhoudingen. Die redenering gaat niet meer op nu de brontabellen vanuit de salarisverwerking worden gevuld. De toets bij het tonen blijft daarnaast staan |
| R13 | Jaargrens (§4.4); herziet I2 gedeeltelijk | Geen probleem, want we gebruikten rechtstreeks de loonaangifterubrieken | Lijstbegrippen worden per kalenderjaar ingericht, dus het jaargrensprobleem zou terug kunnen komen. **Het doet zich niet voor**, omdat AFAS de lijstbegrippen standaard meelevert en de klant ze niet kan aanpassen |
| R14 | Opschonen van laag 1 (§5.6); vervangt de motivering bij G10 | Geen opschoning, want de bestaande tabel kende die ook niet | Nog steeds geen opschoning, maar nu op eigen gronden: er moet altijd een compleet afgesloten kalenderjaar aanwezig zijn voor DP2, en late correcties moeten verwerkt kunnen worden |
| R15 | Triggers bij een mislukte taak (§7.8) | Beschreven, maar niet als besluit vastgelegd | Bevestigd: de **triggerregels blijven staan** als de wachtrijtaak mislukt, zodat de eerstvolgende dagovergang de taak opnieuw uitvoert zonder handmatige tussenkomst |
| R16 | Lagen 2 en 3 (§5.4, §5.5) | — | **Verder ongewijzigd**, op de verkooprelatie uit R9 na. Sleutels, kenmerken, berekende waarden en de eenentwintig velden per geslacht blijven staan · **herzien op 16 september 2026, zie blok U**: beide lagen krijgen een GUID als primaire sleutel en op laag 2 vervallen Werkgever en Periodetabel. De berekende waarden en de eenentwintig velden per geslacht blijven ook nu ongewijzigd |

Besloten in blok S, de scope, de stamkaart en de KPI's, op 15 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| S1 | Scope van het deelproject (§1.4, §9.6); sluit O1 | Open vraag of België binnen scope valt | **Nederland.** België valt buiten scope: de loongegevens lopen daar via het sociaal secretariaat en het is niet bekend hoe België invulling geeft aan de richtlijn. Een denkbare latere route is de door het sociaal secretariaat teruggekoppelde berekende gegevens in dezelfde brontabellen te vullen, zodat België meelift op de KPI's. De Caribbean vallen niet onder deze Europese regelgeving |
| S2 | Grondslag van het loonverschil (§2, §6.5, §6.8, §8.2); herziet E2 (PM1), C4 en 41 | Het bruto jaarloon was de wettelijk voorgeschreven maat, het uurloon stond er aanvullend naast | **Het jaarloon blijkt niet de wettelijk voorgeschreven maat te zijn.** Daarmee vervalt de reden om het voorop te zetten en krijgt het **bruto uurloon** de voorkeur, omdat het corrigeert voor deeltijd en voor een dienstverband dat niet het hele venster liep. Het jaarloon blijft berekend en vastgelegd, en staat in de vergelijkingstabel en het dashboard. De begrippen *wettelijk loonverschil* en *aanvullend loonverschil* vervallen uit hoofdstuk 2 |
| S3 | Aantal KPI-tegels (§8.2); herziet E11 en 42 | Vier tegels: jaarloon, componenten jaarwaarde, uurloon, componenten uurwaarde | **Twee tegels**, beide op uurbasis: *Loonverschil uurloon functiecategorie* en *Loonverschil componenten uurwaarde functiecategorie*. Het blijft zo overzichtelijk voor de medewerker, en een KPI op jaarloon roept vooral vragen op omdat die geen rekening houdt met het parttimepercentage. Alle vier de percentages worden wél berekend en vastgelegd |
| S4 | Titels van de KPI's (§8.2) | Loonverschil uurloon, Loonverschil componenten uurwaarde | Met **functiecategorie** erachter, zodat een los gelezen tegel niet als een persoonlijk verschil wordt opgevat |
| S5 | Waar de KPI's staan (§8.1); scherpt D4 aan | Een tabblad Loontransparantie onder Salaris op de stamkaart medewerker | Een sectie Loontransparantie op **drie standaard stamkaarten**: medewerker ESS, medewerker MSS en kandidaat. Uitsluitend op de **standaard** stamkaart; niet op vrije stamkaarten van de klant |
| S6 | Opbouw van de pagina (§8.1) | KPI's bovenaan | De **omschrijving van de functiecategorie** als titel bovenaan, daaronder de **toelichting op de functiecategorie** als niet-bewerkbare tekst, en pas daarna de KPI's. Zonder die context is een percentage betekenisloos |
| S7 | Actieknop Vraag aan HR (§8.1) | Niet aanwezig | Een actieknop **Vraag aan HR** die de profielpagina voor Recht op informatie opstart, zodat de medewerker direct een vraag kan insturen (DP4) |
| S8 | Naam van de eerste kolom (§8.3); herziet K8 gedeeltelijk | Overal Jij | **Jij** op de ESS-stamkaart, **Medewerker** op de MSS- en de kandidaat-stamkaart. Daar kijkt een ander naar de gegevens, en "Jij" wijst dan naar de verkeerde persoon |
| S9 | Vrije velden op de stamkaart (§8.1) | Niet belegd | **Niet tonen.** Klanten kunnen vrije velden maken, maar naar verwachting kunnen ze niet sturen wélke worden getoond. Zonder die sturing verschijnt elk vrij veld automatisch naast iemands loongegevens. De aanname is niet geverifieerd; zie openstaand punt R2 |
| S10 | Meerdere actuele dienstverbanden (§8.5); heropent D2 en 28 | Alleen het hoofddienstverband, met een verwijzing naar het document of Vraag aan HR | **Open ontwerpvraagstuk** met drie richtingen op volgorde van voorkeur: een dropdown op dienstverband, herhaalde pagina-onderdelen, of de bestaande route via Vraag aan HR. De bestaande route blijft de voorlopige stand; zie openstaand punt R1 |

Herzien in blok V, de KPI-ronde, op 17 september 2026:

Aanleiding was de constatering dat twee percentages op zichzelf niet genoeg context geven: ze zeggen iets over de groep, maar niet waar de medewerker zelf staat en hoe groot die groep is. Dat raakt hoofdstuk 8 en §9.4.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| V1 | Aantal KPI-tegels (§8.2); herziet S3 | Twee tegels, beide een loonverschilpercentage op uurbasis | **Vier tegels**: *Loonverschil uurloon*, *Loonverschil componenten uurwaarde*, *Gemiddeld bruto jaarloon* en *Aantal inkomstenverhoudingen*. De eerste twee blijven inhoudelijk ongewijzigd; de twee nieuwe zijn grafieken en geen getallen |
| V2 | Titels van tegel 1 en 2 (§8.2, §8.7); herziet S4 | Met **functiecategorie** erachter, zodat een los gelezen tegel niet als een persoonlijk verschil wordt opgevat | **Zonder die toevoeging.** De sectie noemt de categorie als titel bovenaan (§8.1) en de vier tegels staan daar direct onder. Alles in de sectie gaat over die ene categorie, dus herhalen in elke tegeltitel voegt niets toe en maakt de titels lang en onderling moeilijk te onderscheiden |
| V3 | Gemiddeld bruto jaarloon (§8.2) | Niet aanwezig; het jaarloon stond alleen als bedrag in de vergelijkingstabel | Een **horizontale staafgrafiek** met op de verticale as Jij of Medewerker, Mannen en Vrouwen, en op de horizontale as het bruto jaarloon in euro's. De eigen balk komt uit laag 2, de twee gemiddelden uit laag 3. Het jaarloon en niet het uurloon, omdat het bedrag herkenbaar is van de jaaropgave; het is geen percentage, dus het bezwaar uit S2 speelt hier niet |
| V4 | Aantal inkomstenverhoudingen (§8.2) | Niet aanwezig | Een **taartdiagram** op het aantal arbeidsverhoudingen mannen en vrouwen uit laag 3. Geeft de groepsgrootte waar de twee percentages erboven zonder betekenisloos zijn. De tegel heette eerst *Samenstelling functiecategorie*; de titel noemt nu wat er wordt geteld. We tellen arbeidsverhoudingen in de zin van het begrippenkader, en dat is in Profit de **inkomstenverhouding** (§2, §3.1). De velden op laag 3 houden de wettelijke term aan, het scherm de Profit-term |
| V5 | Geslacht X en niet ingevuld in de taart (§3.8, §8.2) | Niet belegd | **Niet tonen.** De richtlijn splitst uit naar mannen en vrouwen, de tegel hoort bij de twee tegels erboven die over diezelfde groepen gaan, en een derde partje bestaat in de praktijk vaak uit één persoon. Gevolg: de taart telt niet op tot het veld Aantal arbeidsverhoudingen totaal |
| V6 | Aantallen per geslacht tonen (§9.4) | We tonen geen aantallen per geslacht | **We tonen ze wél**, in tegel 4. Zonder groepsgrootte is een loonverschilpercentage niet te duiden. Dat de aantallen in een kleine categorie naar een individuele collega wijzen, is dezelfde aanvaarde afweging als bij de gemiddelden (§9.3) |
| V7 | Grafiek bij de KPI's (§8.3); herziet E11 | Geen grafiek; een staafgrafiek zou dezelfde getallen een derde keer laten zien | De grafieken zitten **in de tegels** en niet onder de vergelijkingstabel. Het argument gold voor een grafiek naast de percentages; tegel 3 en 4 tonen andere gegevens dan die percentages. De tabel zelf blijft puur cijfers |
| V8 | Lege groep of ontbrekende eigen regel in de grafieken (§8.5, §8.6) | Alleen belegd voor de percentages en de kolommen | Tegel 3 laat de ontbrekende balk weg, tegel 4 toont één taartpunt van honderd procent. Beide blijven staan; ze tonen wat er is in plaats van niets |
| V9 | Begin- en einddatum in de KPI-uitleg (§8.2, §8.7) | De info-icoontekst vulde een begin- en einddatum in | **Vervallen.** De tegels lezen de tabel per functiecategorie en die heeft sinds T6 geen datums meer; binnen één categorie verschilt het venster bovendien per arbeidsverhouding. De eigen begin- en einddatum blijven op laag 2 staan en worden gebruikt bij de informatie die aan de medewerker wordt verstrekt |

Herzien in blok W, het loontijdvak en de periodetabellen, op 17 september 2026:

Aanleiding was dat de keuze uit blok R — van de klaargezette loonaangifte naar de geaccordeerde salarisverwerking, met eigen brontabellen — ook doorwerkt in de eenheid waarop de brontabellen zijn opgebouwd. Dat raakt hoofdstuk 1 tot en met 7 en hoofdstuk 10.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| W2 | Eenheid van de brontabellen (hele document); volgt uit R1 en R4 | Het **aangiftetijdvak**: het tijdvak van de loonaangifte | Het **loontijdvak**: het tijdvak waarover de salarisverwerking is uitgevoerd. De brontabellen worden uit de berekende salarisgegevens gevuld, dus het tijdvak volgt de salarisverwerking en niet de aangifte. De term is overal in de lopende tekst vervangen; in het besluitenlog blijft de oude term staan |
| W3 | Ondersteunde periodetabellen (§4.3); herziet L1 | Alleen **maand, vier weken en week**; de overige vijf buiten scope, met een melding op de stamkaart | **Alle acht.** De beperking hoorde bij het aangiftetijdvak, dat maar drie indelingen kent. Het loontijdvak volgt de periodetabel van de salarisverwerking, dus alle acht kunnen in de brontabel voorkomen. Uitsluiten zou betekenen dat een werkgever met bijvoorbeeld kwartaalverloning een lege sectie ziet terwijl zijn gegevens er wél staan. Het venster is voor elke indeling hetzelfde principe; alleen het aantal tijdvakken verschilt |
| W4 | Aantal tijdvakken in het venster (§4.3, §6.1); herziet L2 gedeeltelijk | Twaalf bij maand, dertien bij vier weken en week | Per periodetabel: jaar 1, halfjaar 2, kwartaal 4, maand 12, halve maand 24, vier weken 13, twee weken 26, week 52. Met een restperiode of een 53e week komt daar bij de week-, twee- en vierwekentabel één tijdvak bij |
| W5 | Hergroeperen bij weekverloning (§4.3); herziet B2 | De weken werden geherbundeld naar dertien perioden van vier weken | **Vervalt.** Het loontijdvak ís de week, dus het venster is simpelweg de laatste tweeënvijftig weken. Hergroeperen zou nu een bewerking toevoegen die de herleidbaarheid naar de salarisverwerking verstoort |
| W6 | Vensterbepaling in de berekening (§6.1) | Niet als eigen stap beschreven; hoofdstuk 6 begon bij de formules | Hoofdstuk 6 begint nu met het bepalen van het venster, per werkgever **en periodetabel**. De taak mag nergens een vast aantal tijdvakken aannemen; een fout hierin werkt door in laag 2 én laag 3 |
| W7 | Melding bij een niet-ondersteunde periodetabel (§8.6) | Viel onder de melding dat de arbeidsverhouding buiten de regeling valt | **Vervalt**, want er is geen niet-ondersteunde periodetabel meer |
| W8 | Lijstbegrippen per populatie (§5.3, §6.2, hoofdstuk 10); scherpt R1 aan | Eén ongedeelde set lijstbegrippen die AFAS meelevert | **Gesplitst.** Voor eigen medewerkers gebruiken we de **bestaande** lijstbegrippen van de loonaangifte; die zijn er al en vragen geen actie. Voor uitzendkrachten komt er een **eigen** set op plaatsingniveau: de loonaangifte kent de plaatsing niet, en de definitie wijkt inhoudelijk af. Dat is een actie voor het **cao-team**; zie openstaand punt W1. De twee sets hoeven **niet** gelijk te zijn, omdat de uitkomsten van medewerkers en uitzendkrachten nooit met elkaar worden vergeleken — populatie is sleutelonderdeel op laag 3. Binnen één populatie moet de definitie wél overal gelijk zijn |

Besloten in blok X, het voortgangsoverleg, op 22 september 2026:

In het wekelijkse voortgangsoverleg zijn de deelprojecten per onderdeel langsgelopen. Vier punten raken dit ontwerp inhoudelijk; twee andere komen er als raakvlak bij.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| X1 | Formatieverdeling (§2, §4.5) | Niet belegd; het ontwerp ging er impliciet van uit dat de functie van het dienstverband komt | **Uitgesloten**, nu expliciet met onderbouwing. We kijken altijd naar de functie van het **dienstverband**; formatieverdelingsregels tellen niet mee. Formatieverdeling is bedoeld voor kostentoerekening en niet voor beloning: werkt iemand in twee functies met verschillende salarissen, dan hoort daar de werkwijze van twee dienstverbanden bij, en is het salaris gelijk, dan verandert een kostenverdeling niets aan het loonniveau. Meetellen zou meerdere functies onder één inkomstenverhouding opleveren, waarbij niet te bepalen is welk deel van het loon bij welke functie hoort en zo'n verdeelde arbeidsverhouding niet meer te vergelijken is met een collega die zijn uren niet verdeelt. De klant kan hiervan afwijken; dit is het standaardadvies |
| X2 | Meerdere actuele dienstverbanden (§8.5); herziet S10 en scherpt besluit 28 aan | Drie richtingen op volgorde van voorkeur, met tabbladen bovenaan en het hoofddienstverband als terugvaloptie | **Omgedraaid.** Het **hoofddienstverband** is de scope voor Profit 9; de tabbladen per dienstverband zijn een uitbreiding als de planning het toelaat. De uitwerking van de tabbladen blijft in §8.5 staan, inclusief het uitgangspunt dat een tabwissel de hele sectie ververst. Het **rapport** toont wél alle dienstverbanden, dus de medewerker kan er via die route bij |
| X3 | Titel van tegel 4 (§8.2, §8.7, §9.4); herziet V4 gedeeltelijk | *Aantal inkomstenverhoudingen*, omdat de titel moest zeggen wat er wordt geteld | **Samenstelling functiecategorie.** De tegel is bedoeld om te laten zien hoe de groep is samengesteld waarmee de medewerker wordt vergeleken; de rekeneenheid is daarbij bijzaak. Dat het om inkomstenverhoudingen gaat en niet om personen, staat in het info-icoon. De velden op laag 3 houden hun naam |
| X4 | Rapport in plaats van document (§1.4, §5.9, hoofdstuk 11); herziet besluit 76 | Een leeg **document** Loontransparantie medewerker, gekoppeld aan een type document, meegeleverd in DP4 | Een **rapport** uit de workflow-editor. Sinds Profit 9 kan die rapporten genereren, en omdat er niets bewerkt hoeft te worden is dat de betere keuze: geen conversie van DOCX naar PDF — op AFAS Online merkbaar in de performance — en geen koppeling tussen de workflow en een type document, waardoor de gebruiker niet uit een lange lijst hoeft te kiezen. Een vrije toelichting kan via een memoveld dat op het rapport wordt opgenomen. Voorwaarde is de gegevensverzameling uit §5.9. Het zwaartepunt van deze wijziging ligt in DP4 |
| X5 | Pocket (§1.4, hoofdstuk 11) | Eén regel: Pocket en OutSite gebruiken dezelfde gegevens, uitwerking buiten deze beschrijving | **Concreet gemaakt.** De medewerker ziet zijn loontransparantiegegevens in Pocket naast loonstrook en jaaropgave en kan van daaruit een vraag aan HR insturen. Het insturen loopt over de bestaande generieke updateconnector; voor het tonen is een **dataconnector** nodig die per medewerker en dienstverband de KPI-gegevens ophaalt, alleen voor Pocket en niet open voor klanten. Die connector leest dezelfde regels als de stamkaart en moet dus hetzelfde filter op de actuele functie en dezelfde medewerkerautorisatie hanteren, zodat Pocket en de stamkaart nooit verschillende getallen tonen. Het bouwen valt buiten dit ontwerp; zie actie 27 |
| X7 | Jonas (hoofdstuk 11) | Niet belegd | Als **raakvlak** opgenomen en **buiten scope** van dit ontwerp gehouden. Onderzocht wordt of Jonas in begrijpelijke taal kan uitleggen waar de medewerker naar kijkt, en of er een tag *loontransparantie* in centraal bronbeheer komt waarmee de klant eigen documenten als context koppelt. Zie actie 28 |

Niet gewijzigd naar aanleiding van dit overleg: het **BI-dashboard** moet aansluiten op de KPI's van de stamkaart, maar dat is al afgedekt door de eis in hoofdstuk 11 dat het dashboard leest en niet opnieuw rekent. Het vastleggen van **functiecategorieën voor uitzendkrachten** loopt als actie 21 en raakt de tekst van dit ontwerp niet.

Besloten in blok Y, de ontsluiting van de brontabellen, op 22 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| Y1 | Gegevensverzameling op laag 1 (§1.4, §5.9); herziet R10 en J7 | Een eigen verzameling op *Loontransparantie bron medewerkers*, met medewerkerautorisatie bij het lezen | **Vervalt.** De brontabellen krijgen geen gegevensverzameling, ook niet voor uitzendkrachten en *bron extern*. Deze gegevens stellen we niet binnen Profit beschikbaar; binnen Profit is er daarmee geen enkele route naar de loongegevens per loontijdvak |
| Y2 | Route van het dashboard naar laag 1 (§5.9, §9.2, hoofdstuk 11) | Via de gegevensverzameling, met medewerkerautorisatie | Het **Power BI-dashboard leest de brontabellen rechtstreeks** uit. Die route staat alleen open voor applicatiebeheerders die BI-modellen mogen aanmaken; die groep kan vandaag al bij gegevensverzamelingen met salarisgegevens. De eindgebruiker kan geen BI-model aanmaken, dus dit levert **geen extra risico** op. Het dashboard was bovendien de enige afnemer van de vervallen verzameling, terwijl de afscherming ervan wél voor elke Profit-gebruiker moest kloppen |
| Y3 | Gegevensverzamelingen op laag 2 en 3 (§5.9) | Vier verzamelingen in totaal | **Drie**, ongewijzigd van opzet: *(actuele functie)* en *(alle functies)* op laag 2 en één op laag 3. De verzameling *(alle functies)* blijft staan; ze is niet alleen voor het dashboard bedoeld, maar voor elke weergave waarin de regels vóór en ná een functiewijziging nodig zijn |

Gecorrigeerd in blok Z, op 22 september 2026:

Bij het nalezen van laag 3 bleek dat §5.4 en §5.5 twee assen door elkaar haalden. De kolommen *Fase 1* en *Fase 2* gaan over de **soort rapportage** — Recht op informatie tegenover een afgesloten kalenderjaar — maar de rijen Populatie en Verkooprelatie waren ingevuld alsof ze over het **deelproject** gingen. Daardoor kwam DP3 in de fase 2-kolom terecht, terwijl een ter beschikking gestelde arbeidskracht juist soort Recht op informatie heeft.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| Z1 | Verkooprelatie op laag 3 (§5.5); corrigeert U6 | "In fase 1 altijd leeg"; gevuld stond in de fase 2-kolom | De verkooprelatie is gevuld bij populatie *Ter beschikking gestelde arbeidskrachten* **én** soort Recht op informatie, en is daarmee **niet fase-afhankelijk**. Juist het recht op informatie van een uitzendkracht — fase 1 dus — heeft het veld nodig, omdat de uitlener per inlener moet kunnen vergelijken. Dat het veld in de uitlevering van DP1 leeg blijft, komt doordat DP1 alleen regels met populatie Medewerkers vult: een scopegevolg en geen fase-eigenschap |
| Z2 | Populatie op laag 2 en 3 (§5.4, §5.5); corrigeert U4 | "In fase 1 altijd Medewerkers"; de tweede waarde stond in de fase 2-kolom | Ook hier is de fase niet bepalend. In de uitlevering van **dit deelproject** staat er altijd *Medewerkers*; DP3 voegt de tweede waarde toe, binnen dezelfde soort rapportage. De formulering "in fase 1" is overal vervangen door "in de uitlevering van dit deelproject" |
| Z3 | Vorm van de sleuteltabel op laag 3 (§5.5) | Twee kolommen *Fase 1* en *Fase 2* voor alle vier de sleutelonderdelen | Eén kolom *Invulling*. Rapportage ID en Functiecategorie zijn wél fase-afhankelijk en vermelden dat in hun eigen tekst; Populatie en Verkooprelatie zijn dat niet en zeggen dat er expliciet bij |

Aangevuld in blok AA, op 22 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AA1 | Individu in *Loontransparantie bron extern* (§2, §5.3) | Geen veld voor het individu; de sleutel bestond uit groepskenmerken plus het nummer van de inkomstenverhouding | Er komt een sleutelveld **Kenmerk arbeidskracht**. Zonder dat veld zijn de regels van verschillende personen niet te onderscheiden: het nummer van de inkomstenverhouding begint bij elke arbeidskracht opnieuw bij één, en de overige velden zijn groepskenmerken. Twee mannen in dezelfde functiecategorie zouden dan op één regel vallen, terwijl de gemiddelden, de medianen en de tellingen per arbeidsverhouding gaan. Het kenmerk moet **niet herleidbaar** zijn tot een persoon en **stabiel** over de tijdvakken heen, anders valt één arbeidsverhouding in laag 2 uiteen in losse regels per tijdvak. Hoe de uitlener het bepaalt en uitwisselt hoort bij DP2 |
| AA2 | Populatiefilter voor uitzendkrachten (§3.2, §3.3, §5.3); sluit T9 | Open punt: welke waarden meetellen lag nog niet vast | **Soort inkomstenverhouding 11, 13, 15 of 17** — dezelfde vier als bij eigen medewerkers, want §3.7.3 van het begrippenkader maakt op dat punt geen onderscheid — en **aard arbeidsverhouding 11** (uitzendkracht), **22** (WSW-detachering) of **82** (payrolling) uit §3.7.2. De toevoeging bij code 11 dat die *alleen bij de inlener* meetelt, slaat op de **rapportage** en niet op de brontabel: de uitlener beschikt over die loongegevens en heeft ze nodig voor het recht op informatie van zijn eigen uitzendkracht (§3.3) · **herzien op 13 oktober 2026 in blok AN**: de filters blijven, maar de aard bepaalt niet meer de populatie; de codes van beide populaties vormen samen één filter |
| AA3 | Vullen van *Loontransparantie bron uitzendkrachten* en van laag 2 en 3 voor die populatie (§1.4, §5.3, §5.4, §5.5, §7.4, hoofdstuk 10 en 11); herziet Z1 en Z2 | Ontwerpen in DP1, vullen in DP3 | **Alles in DP1.** Het datamodel en het berekenen van de gegevens zijn voor beide populaties hetzelfde werk: hetzelfde venster, dezelfde acht grootheden, dezelfde gemiddelden en medianen. Door het te splitsen zou de berekening twee keer worden geraakt en twee keer getest. De basis komt daarom in één keer, en DP3 houdt over wat echt anders is: de **uitwisseling tussen uitlener en inlener** |
| AA4 | Nieuw deelproject DP5 – Functiecategorie en flex (hoofdstuk 11); herplaatst Q1 | Functiegroepen-model, uitvraagformulier en plaatsinggegevens hoorden bij DP3 | Die drie onderwerpen vormen **DP5**. Ze gaan niet over uitwisseling maar over **inrichting**, en ze zijn nodig vóórdat de rapportage over 2027 wordt opgebouwd. DP5 komt daarom **tussen DP1 en DP2**; de volgorde wordt DP1 → DP5 → DP2 → DP3, met DP4 parallel |
| AA5 | Triggerregel bij een mutatie op de plaatsing (§7.2) | Niet uitgewerkt | **Geen triggerregel.** De plaatsing zelf verandert de loongegevens niet; die komen uit de salarisverwerking, en die schrijft al een triggerregel. Een wijziging in de functie of de functiecategorie op de plaatsing werkt door via dezelfde route als bij een eigen medewerker: de eerstvolgende verwerking neemt de nieuwe indeling mee. Een eigen triggerregel zou de zwaarste run onnodig vaak starten · **herzien op 6 oktober 2026 in blok AI, punt AI2**: de afwijkende functiecategorie op de plaatsing schrijft wél een triggerregel weg. Voor de overige plaatsingmutaties blijft dit besluit gelden |
| AA6 | Lijstbegrippen voor uitzendkrachten (§5.3, §6.2, punt W1) | Blokkerend voor DP3 | **Blokkerend voor dit deelproject**, omdat DP1 de brontabel nu zelf vult. De aanvraag bij het cao-team krijgt daarmee prioriteit P0. Het kader uitzendkrachten van 3 maart 2026 geeft de definitie al op hoofdlijn: bruto per opdracht is de som van de looncomponenten onder het reguliere tarief plus de reserveringen vakantiegeld en arbeidsvoorwaardenbedrag, zonder het werknemersdeel pensioen en de bijtelling auto; de variabele componenten zijn de componenten onder het bijzondere tarief minus vakantiebijslag en opname arbeidsvoorwaardenbedrag. Onbelaste componenten en componenten onder nultarief tellen niet mee |

Besloten in blok AB, na de conflictronde op de vorige blokken, op 23 september 2026:

Het nalopen van blok AA op tegenstrijdigheden leverde vijf punten op. Drie waren redactioneel en zijn zonder besluit hersteld: de scope van dit deelproject sloot nog uit wat punt AA3 juist insluit, besluit 95 verwees naar het verkeerde besluitnummer, en het detailbestand bij actie 26 noemde nog DP3 als blokkerend deelproject. De twee punten hieronder vroegen een keuze.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AB1 | Bruikbaarheid van de uitzendkrachtcijfers vóór DP5 (hoofdstuk 10); volgt uit AA3 en AA4 | Niet benoemd; AA3 en AA4 samen lieten een gat open | **Aanvaard dat de cijfers voor deze populatie pas na DP5 bruikbaar zijn.** Dit ontwerp vult de brontabel en de lagen erboven, maar de functiecategorie bij plaatsing wordt in DP5 vastgelegd; tot dat moment valt een uitzendkracht in geen vergelijkingsgroep (§3.7). De twee alternatieven — die vastlegging naar dit deelproject halen, of DP5 vóór DP1 plaatsen — vallen af. De keten wordt in de logische volgorde gebouwd: eerst de opslag en de berekening, dan de indeling die ze betekenis geeft. Voor 2026 is het venster voor deze populatie daarmee sowieso incompleet (§7.7) |
| AB2 | Wie de rapportage over uitzendkrachten ontwerpt (hoofdstuk 11); scherpt AA3 aan | Verdeeld: de rapportage door de inlener bij DP2, de gescheiden rapportage bij DP3 | **De rapportage is één onderdeel en hoort in haar geheel bij DP2.** Zowel de rapportage die de inlener maakt over ingeleende krachten als de scheiding tussen de populaties *Medewerkers* en *Ter beschikking gestelde arbeidskrachten* binnen de rapportage. Splitsen zou betekenen dat DP2 eerst een rapportage voor één populatie ontwerpt en DP3 die daarna verbouwt — hetzelfde patroon dat bij AA3 al reden was om het vullen niet te splitsen. DP3 houdt alleen de uitwisseling over |

Besloten in blok AC, de herziening van hoofdstuk 8 op 23 september 2026:

De vergelijkingsmatrix bleek voor de medewerker niet te begrijpen. In een ontwerpsessie is de sectie opnieuw opgebouwd rond één vraag: wat kan een medewerker hier zonder uitleg mee? Dat leverde elf besluiten op. Twee daarvan volgen uit technische beperkingen die tijdens de sessie zijn bevestigd.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AC1 | Het bruto jaarloon op de stamkaart (§2, §6.1, §6.5, §8.2) | Het loonniveau moest in twee eenheden tegelijk worden uitgedrukt: bruto jaarloon én bruto uurloon | **Er is geen juridische basis** die het bruto jaarloon bij het recht op informatie voorschrijft; de eerdere aanname berustte op een misverstand. Het jaarloon verdwijnt van het scherm en blijft alleen in het datamodel, het dashboard en het document *Loontransparantie medewerker*. De hele pagina staat daarmee op uurbasis |
| AC2 | De vergelijkingstabel (§6.4, §8.3) | Vijf regels maal drie kolommen onder de tegels: jaaruren, bruto jaarloon, bruto uurloon, jaar- en uurwaarde variabele componenten | **Vervalt.** Vijftien getallen waarvan de medewerker de helft niet kan plaatsen. Op uurbasis blijven er zes over, en die passen in één gestapelde balk (tegel 2). De plek onder de tegels wordt het pagina-onderdeel *Functie* |
| AC3 | Nieuw kerngetal: totaal uurloon (§2, §5.4, §6.1) | Bestond niet; *bruto uurloon* is in dit ontwerp alleen het basisloon | **Totaal uurloon** = bruto uurloon + uurwaarde variabele componenten. Het volledige loon per verloond uur, en het enige bedrag dat de medewerker als eigen kengetal ziet. Vastgelegd als optelling van twee al afgeronde bedragen, zodat scherm en opslag niet uiteen kunnen lopen |
| AC4 | Grondslag van het loonverschil op de stamkaart (§6.5, §8.2) | Twee percentages: één op het basisloon en één op de variabele componenten | **Eén percentage, op het totaal uurloon.** Twee percentages vragen dat de medewerker eerst het onderscheid begrijpt, en juist de variabele componenten zeggen hem weinig. Dit percentage komt niet terug in de wettelijke rapportage; dat is geen harde eis en weegt niet op tegen de duidelijkheid. Het onderscheid blijft zichtbaar als bedrag in de gestapelde balk |
| AC5 | Individueel loonverschil (§5.4, §6.4, §6.5, §8.2) | Vervallen bij de PM-terugkoppeling van 3 september 2026 (punt E5) | **Komt beperkt terug**, als één percentage op het totaal uurloon. Het bezwaar van toen gold een percentage op elke regel van de tabel; die tabel is er niet meer. Dit is de vraag die de medewerker zelf stelt zodra hij de groepscijfers ziet · **de grondslag is op 24 september 2026 gewijzigd, zie blok AD punt AD5** |
| AC6 | Rekenrichting van het individuele percentage (§6.5) | Voorstel: (eigen − gemiddelde) / gemiddelde, zodat een plus iets gunstigs betekent | **Omgedraaid naar (gemiddelde − eigen) / gemiddelde**, dezelfde richting als het groepsverschil. Vanuit de medewerker leest het voorstel logischer, maar dan tellen twee percentages op hetzelfde scherm tegengesteld op en wijkt dit getal af van de voorgeschreven rekenwijze — wat vooral in het dashboard vragen oproept |
| AC7 | Acht nieuwe berekende velden (§5.4, §5.5) | Alleen de bestaande maatstaven | **Totaal uurloon** en **Individueel loonverschil** op laag 2; **Gemiddeld totaal uurloon** en **Mediaan totaal uurloon** per geslacht, plus **Loonverschil totaal uurloon** en **Mediane loonverschil totaal uurloon** op laag 3. Vastleggen in plaats van live rekenen houdt de KPI eenvoudig en maakt de velden bruikbaar voor het BI-dashboard. Het zijn velden specifiek voor het recht op informatie en geen officiële rapportagegegevens |
| AC8 | Wisselen tussen dienstverbanden (§8.5, punt R1) | Tabbladen per dienstverband als uitbreiding, uitgewerkt in §8.5 | **Technisch niet mogelijk** op de standaard stamkaart. De uitwerking vervalt; we tonen het hoofddienstverband. De melding uit §8.7 vervalt ook: de activering *Meerdere dienstverbanden* geldt maar voor een deel van de klanten, en de functieomschrijving in de subtitel van tegel 1 maakt al zichtbaar welk dienstverband wordt getoond. De uitleg komt in de help |
| AC9 | Plaats van de functiecategorie (§8.1, §8.2, §8.3) | Als titel en toelichting **boven** de tegels | **Onder de tegels**, als pagina-onderdeel *Functie*. Op de standaard stamkaart staan de KPI's altijd bovenaan en kan er niets boven. De context wordt opgevangen in de **subtitel** van de tegels, die de functiecategorie bij naam noemt. Bij tegel 1 staat daar de **eigen functie**, want dat bedrag gaat over het dienstverband en niet over de categorie |
| AC10 | Hamburger op een Value-tegel (§8.2) | Overwogen om de onderliggende bedragen achter de hamburger te zetten | **Niet mogelijk**: een Value-tegel heeft geen onderliggende dataset om naar om te klappen. De bedragen staan in de uitleg achter het **info-icoon**, die daarmee per medewerker wordt samengesteld. Ook de hamburger op de grafiektegel toont alleen wat in de grafiek zit; verloonde uren en bruto jaarloon kunnen er niet bij |
| AC11 | Geslacht X of niet ingevuld (§3.8, §8.2, §8.6) | Alle tegels zichtbaar, alleen niet meegeteld in de gemiddelden | De tegel **Individueel verschil uurloon wordt niet getoond** voor deze medewerkers. Er is geen eigen geslachtsgroep en dus geen gemiddelde om tegen af te zetten · **vervallen op 24 september 2026: met het categoriegemiddelde als grondslag tellen zij gewoon mee en zien zij de tegel wél, zie blok AD punt AD5** |
| AC12 | Op welke drie stamkaarten de sectie komt (§1.4, §8.1); herziet S5 | Medewerker ESS, medewerker MSS en **kandidaat** | De kandidaat-stamkaart **vervalt** en wordt vervangen door de **plaatsing**-stamkaart. Een kandidaat heeft geen loongegevens en dus geen regel per inkomstenverhouding; een ter beschikking gestelde arbeidskracht heeft die wél, en de uitlener moet die persoon het recht op informatie bieden (§3.3). De plaatsing-stamkaart leest de regels met populatie *Ter beschikking gestelde arbeidskrachten*, waarin de vergelijkingsgroep mede door de verkooprelatie wordt bepaald (§5.5). Die cijfers zijn pas bruikbaar ná DP5 (punt AB1) |
| AC13 | Handmatig starten van de taak (§2, §7.3, §7.4, punt E1); beperkt M1 | De taak is "los te starten" en kan daarnaast handmatig worden uitgevoerd | **Er komt vooralsnog geen knop** om de taak handmatig te starten. Hij draait uitsluitend vanuit de dagovergang, op basis van de triggertabel. De klant wacht dus altijd tot de eerstvolgende nacht; dat is in de regel geen probleem, want de wettelijke reactietermijn is twee maanden. Het "los" uit M1 blijft gelden in de zin dat de taak **zelfstandig en herstartbaar** is en niet aan de accordeertaak hangt — niet in de zin dat een gebruiker hem kan aanroepen |
| AC14 | Filters op de gegevensverzamelingen van laag 2 (§5.9, §8.5) | Twee verzamelingen met één of twee filters; het filter op de actuele functie was alleen benoemd, niet uitgewerkt | **Drie filters en vier verzamelingen.** Er komt een **filter op populatie** bij, omdat beide populaties in dezelfde tabel staan en één persoon in allebei kan voorkomen; de populatie volgt uit de stamkaart, dus de presentatieverzameling krijgt twee varianten. Het filter op de **actuele functie** is uitgewerkt: het vergelijkt met de stamgegevens van het dienstverband en volgt bij subdienstverbanden het kapstokdienstverband (punt AC-c). En het is expliciet gemaakt dat de verzameling **niet** afbakent welke regel wordt getoond: de keuze voor het hoofddienstverband gebeurt bij het opbouwen van de tegels, zodat het rapport wél alle dienstverbanden kan tonen |
| AC15 | Bron van de weergave Functies in functiecategorie (§8.4, §9.4); herziet D7 | De **functiecategorie-inrichting**: alle functies die de werkgever aan de categorie heeft gekoppeld, ook die waarop niemand werkt | De **regels per inkomstenverhouding**, gekoppeld aan die inrichting. De lijst toont alleen functies die in het venster daadwerkelijk meetellen, met dezelfde afbakening als de vergelijkingscijfers: functiecategorie, populatie en — bij een uitzendkracht — verkooprelatie. Zo verdwijnen onbezette functies en oude inrichting uit beeld, die anders een grotere of andere vergelijkingsgroep voorspiegelen. Het privacyargument onder D7 — de lijst zou de omvang van de groep verraden — is achterhaald: sinds de tegel *Samenstelling functiecategorie* staat het aantal arbeidsverhoudingen per geslacht al op het scherm |

De schermteksten zijn in dezelfde sessie regel voor regel doorgenomen. De uitkomst staat in §8.7. Drie taalkeuzes zijn daar vastgelegd: overal de **je-vorm** in lopende tekst en de **ik-vorm** in koppen, **verloonde uren** als vaste term, en **extra's** met als uitleg "bijzondere beloningen en loon in natura".

Besloten in blok AD, bij het nalopen van de sectie op 24 september 2026:

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AD1 | Titel van tegel 1 (§8.2, §8.7) | *Mijn uurloon* | **Gemiddeld uurloon**. Het bedrag is een gemiddelde over twaalf maanden en geen actueel uurtarief; dat hoort in de titel te staan en niet pas in de uitleg · **herzien op 19 oktober 2026**: de titel wordt een vraag, het gemiddelde verhuist naar het bijschrift. Zie blok AO, punten AO1 en AO2 |
| AD2 | Titel van tegel 2 (§8.2, §8.7) | *Uurloon vergeleken* | **Gemiddeld uurloon binnen functiecategorie**. Maakt in de titel zelf duidelijk over welke groep het gaat. *Vergeleken* is er op 24 september weer uit gehaald: dat de staven naast elkaar staan zie je al, en de titel werd er alleen langer van |
| AD3 | Bijschrift onder tegel 1 (§8.2, §8.7); volgt uit AD1 | *Gemiddeld uurloon* | **Vervalt.** Na AD1 zou het de titel woordelijk herhalen. De tegel bestaat nu uit titel, subtitel en bedrag · **herzien op 19 oktober 2026**: het bijschrift wordt *gemiddeld per uur*. Zie blok AO, punt AO2 |
| AD4 | Plaats van het tabblad (§8.1) | Alleen vastgelegd dat het een sectie op de standaard stamkaart is | Het tabblad **Loontransparantie** komt op de **onderste plek** in de groep *Salaris*. De tabbladen erboven horen bij lopende zaken — declaratie, voorschot, loonstrook — en die wil je niet naar beneden duwen voor een pagina die een paar keer per jaar wordt geopend |
| AD5 | Grondslag van het individueel loonverschil (§2, §3.8, §5.4, §5.5, §6.3, §6.4, §6.5, §7.3, §8.2, §8.6, §8.7, §9.4); herziet AC5 en laat AC11 vervallen | Het gemiddelde totaal uurloon van het **eigen geslacht** binnen de functiecategorie | Het gemiddelde totaal uurloon van de **hele functiecategorie**, alle geslachten samen. Afzetten tegen het eigen geslacht draait de wettelijke norm om: de richtlijn gaat juist over gelijke beloning **ongeacht** geslacht, en dan is "wat mannen gemiddeld verdienen" of "wat vrouwen gemiddeld verdienen" de verkeerde maatstaf. Gevolgen: er komt een veld **Gemiddeld totaal uurloon categorie** op laag 3, medewerkers met geslacht X of zonder ingevuld geslacht zien de tegel nu **wél**, en de schermtekst noemt geen geslacht meer |
| AD6 | Wat de actieknop Vraag aan HR start (§8.1, hoofdstuk 11); herziet S7 | Direct het profiel **Recht op informatie** van het type dossieritem Vraag aan HR | De **profielkeuzepagina**, zodat de medewerker zelf kiest. Dat profiel levert dezelfde cijfers op als de pagina waar hij net vandaan komt, alleen in een rapport — terwijl wie hier klikt juist vaak een andere vraag heeft |
| AD7 | Naam van het nieuwe veld op laag 3 (§5.5, §6.3, §6.5); volgt uit AD5 | *Gemiddeld totaal uurloon totaal*, naar het voorbeeld van Aantal arbeidsverhoudingen totaal | **Gemiddeld totaal uurloon categorie**. In deze ene veldnaam betekent "totaal" twee verschillende dingen — basisloon plus variabele componenten, én alle geslachten samen — en dat leest als één begrip. *Categorie* maakt zichtbaar waarover het gemiddelde loopt. De vier velden per geslacht blijven ongewijzigd: tegel 2 en het loonverschil hebben ze nodig |
| AD8 | De Pocket-dataconnector (§1.3, §1.4, §8.8, hoofdstuk 11) | Buiten scope; in hoofdstuk 11 alleen benoemd als iets wat Pocket nodig heeft | **In scope van dit deelproject.** Er komt een interne dataconnector met vier modi: *Dienstverbanden*, *Eigen loongegevens*, *Vergelijkingscijfers* en *Functies in de functiecategorie*. Hij leest de voorberekende velden en rekent niet. Anders dan de bestaande Pocket-connectors krijgt hij een **dienstverband-parameter**, omdat Pocket tussen dienstverbanden kan navigeren. De medewerker blijft uit de ingelogde gebruiker komen, en het meegegeven dienstverband wordt getoetst tegen die medewerker |
| AD9 | De Pocket-pagina's voor Vraag aan HR (§1.4, §8.8, hoofdstuk 11) | Niet belegd | **In scope van dit deelproject.** Vraag aan HR is een technisch type dossieritem met extra velden; Pocket toont standaard alleen onderwerp, toelichting en bijlage. Wij leveren de pagina's *tonen* en *aanpassen*, team Pocket bouwt het insturen. **Blokkerend afhankelijk van DP4**, dat de extra velden vaststelt |

Besloten in blok AE, de dashboardronde van 28 september 2026:

Aanleiding was de vraag hoe het Power BI-dashboard een loonverschil deels kan verklaren, zodat een leidinggevende niet voor elk verschil aanvullende informatie hoeft op te vragen. Het raakt §5.3, §5.4, §5.9, §6.1 en §6.2.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AE1 | Verklarende bedragen in het datamodel (§5.3, §5.4, §5.9) | Niet aanwezig | **Negen velden van het type Bedrag**, op *Loontransparantie bron medewerkers*, *Loontransparantie bron uitzendkrachten* en *Loontransparantie per inkomstenverhouding*. Gevuld uit de lijstbegrippen met Profit Id 6.773 tot en met 6.781. Op laag 2 telt de taak ze op over dezelfde toegekende tijdvakken als de berekende waarden |
| AE2 | Lijstbegrippen per populatie (§5.3, §6.2); nuanceert blok R en blok W | Medewerkers en uitzendkrachten gebruiken verschillende lijstbegrippen, met een eigen definitie per populatie | Dat blijft gelden voor de **acht kerngrootheden**. De negen verklarende bedragen zijn **één gedeelde set**, beschikbaar per dienstverband én per plaatsing. Daarmee vraagt deze uitbreiding geen aparte set voor uitzendkrachten en is ze niet afhankelijk van actie 26 |
| AE3 | Plaats in de berekening (§6.1, §6.2) | Niet van toepassing | De bedragen komen in **geen enkele formule** voor: niet in het bruto jaarloon, niet in de variabele componenten, en niet in een gemiddelde, mediaan of loonverschilpercentage. Ze liggen al besloten in LnLbPh en LnTabBB, dus apart optellen zou hetzelfde loon twee keer laten meetellen. Ook de ondergrens op nul uit §6.1 geldt er niet voor |
| AE4 | Reikwijdte binnen het model (§5.3, §5.5) | Niet van toepassing | Alleen de twee **eigen** brontabellen en laag 2. *Loontransparantie bron extern* krijgt ze niet — die dient de rapportageverplichting van de inlener en niet het dashboard (punt AE-b) — en laag 3 evenmin, omdat die laag uitsluitend groepscijfers bevat en deze bedragen nooit worden gemiddeld |
| AE5 | Indeling van de verlof- en verminderingsbegrippen (§5.3) | Onbetaald verlof, kopen van uren en verkopen van uren vielen onder één brede categorie incidentele inkomstenvermindering | **Gesplitst in drie begrippen.** Die categorie is te grof: de drie verklaren elk iets anders en verkopen van uren werkt zelfs de andere kant op. **Ouderverlof** is juist samengevoegd tot één overkoepelend begrip voor (aanvullend) geboorteverlof en voor betaald en onbetaald ouderschapsverlof. Zwangerschap en bevalling blijft buiten scope omdat het bestaande begrip leeg is (punt AE-c) |
| AE6 | Inrichting van de lijstbegrippen (§5.3, §6.2); nuanceert blok R | AFAS levert de lijstbegrippen mee en de klant kan er niet aan sleutelen | Dat blijft gelden voor de acht kerngrootheden, want die vormen de grondslag van de vergelijking. AFAS onderhoudt de negen verklarende bedragen wél, maar ze **staan open** voor eigen intellingen van de klant — voor de hele set en niet alleen voor de vrije rubriek. Aanvaard gevolg: de inhoud kan per omgeving verschillen, en juist daarom blijven ze buiten elke vergelijking (AE3) |
| AE7 | Presentatie van de bedragen (§5.3, hoofdstuk 8) | Niet van toepassing | Het datamodel legt een **bedrag** vast; of het dashboard dat bedrag toont of alleen de indicatie dát een rubriek gevuld is, bepaalt het dashboard zelf. De vijf KPI-tegels op de stamkaart wijzigen niet: deze bedragen komen daar niet op |

Besloten in blok AF, bij de oplevering van de lijstbegrippen voor uitzendkrachten op 29 september 2026:

Het cao-team heeft de set opgeleverd waarop dit deelproject wachtte. Daarmee gaat punt W1 dicht en vervalt de laatste blokkerende afhankelijkheid. Het raakt §1.4, hoofdstuk 2, §5.3, §6.1 en §6.2; het datamodel, de formules en het vulproces wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AF1 | De set lijstbegrippen voor uitzendkrachten (§1.4, §5.3, §6.2) | Nog te maken door het cao-team; **blokkerend** voor dit deelproject (punt W1, actie 26) | **Opgeleverd.** Zeven begrippen met Profit Id **6.782 tot en met 6.788**, beschikbaar **per plaatsing**, door AFAS meegeleverd en dichtgezet zoals bij medewerkers. De brontabel voor uitzendkrachten kan daarmee langs dezelfde weg worden gevuld als die voor medewerkers, zonder nieuw vulmoment. Punt W1 en actie 26 zijn afgesloten |
| AF2 | Eén set of twee (§5.3, §6.2); onderbouwt blok R en blok W | De keuze voor twee sets lag vast, maar stond er als gevolg van een beperking: de loonaangifte kent de plaatsing niet | Twee sets zijn ook een **bewuste keuze**: ze houden de **looninrichting van beide populaties uit elkaar**. Medewerkers houden de bestaande lijstbegrippen van de loonaangifte; er komt voor hen geen nieuwe set. De twee hoeven niet gelijk te zijn omdat de populaties nooit met elkaar worden vergeleken; **binnen** één populatie is de definitie wél overal gelijk |
| AF3 | Omvang van de set (§5.3, §6.1, §6.2) | Acht grootheden, naar analogie van de set voor medewerkers | **Zeven en geen acht.** *WrdLn*, de waarde niet in geld uitgekeerd loon, ontbreekt: dat bedrag wordt op arbeidsvoorwaardenniveau berekend en is niet naar een plaatsing te herleiden, net als een auto van de zaak en de pensioenpremie. Dat bevestigt de uitzondering die §5.3 en §6.1 al vastlegden; de jaarwaarde variabele componenten van een uitzendkracht blijft de som van (LnTabBB − VakBsl − OpnAvwb) |

Besloten in blok AG, de sleutel van laag 2, op 1 oktober 2026:

Aanleiding was de constatering dat de functiecategorie binnen Flex op de **plaatsing** wordt vastgelegd en daar kan afwijken van de categorie die bij de functie hoort. Het model ging er impliciet van uit dat de functie de categorie bepaalt. Dat raakt §4.5, §5.1, §5.3, §5.4, §5.9, §6.3 en §7.3; de berekeningen zelf wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AG1 | Functiecategorie in de sleutel van laag 2 (§5.4); herziet U1 en M8 | Een unieke sleutel op vijf velden: Rapportage ID, medewerker, nummer inkomstenverhouding, verkooprelatie en functie. De functiecategorie was een kenmerk dat uit de functie volgde | **Zes velden**; de **functiecategorie** komt erbij. Heeft een uitzendkracht bij dezelfde inlener twee plaatsingen in dezelfde functie maar in verschillende functiecategorieën, dan vallen die zonder dit sleutelonderdeel op één regel samen — terwijl ze in twee vergelijkingsgroepen thuishoren (§6.3). Dat is dezelfde fout die de verkooprelatie tussen twee inleners voorkomt (R9). Er ontstaan nu **twee regels per inkomstenverhouding**, elk met de tijdvakken die aan die categorie zijn toegekend; het loon telt niet dubbel, want elk tijdvak hoort bij precies één plaatsing |
| AG2 | Herkomst van de functiecategorie (§4.5, §5.3) | "De functiecategorie hoort bij de functie", met de koppeling op de laatste dag van de rapportageperiode | Dat blijft gelden voor **eigen medewerkers**. Bij een **uitzendkracht** komt de categorie van de **plaatsing** en kan ze afwijken van de categorie die bij de functie hoort. Het veld Functiecategorie op *Loontransparantie bron uitzendkrachten* is daarom niet langer omschreven als de categorie waarin de functie valt, maar als de categorie uit de plaatsing |
| AG3 | Gevolg voor eigen medewerkers (§5.4) | Niet van toepassing | **Geen.** Bij een eigen medewerker hangt de categorie aan de functie, dus groeperen op functie levert vanzelf één categorie op en het extra sleutelonderdeel voegt geen regel toe. De uitbreiding raakt uitsluitend de populatie *Ter beschikking gestelde arbeidskrachten* |
| AG4 | Welke regel bij welke plaatsing hoort (§5.9) | Het filter op de actuele functie leverde per verkooprelatie één regel op | Dat is niet meer gegarandeerd: binnen één inlener kunnen er twee regels in dezelfde functie staan. Het filter zeeft ze niet uit elkaar; welke regel bij welke plaatsing hoort volgt uit de **functiecategorie van die plaatsing**. De verzameling bakent dus nog steeds niet af wélke regel wordt getoond (AC14) |

Besloten in blok AH, de rapportage-eenheid, op 1 oktober 2026:

Aanleiding was de constatering dat Profit het veld **Fiscaal nummer** op de organisatie bewaakt met een integriteitsregel: hetzelfde nummer mag bij maar één organisatie voorkomen. Die regel kunnen we niet wijzigen. Daarmee valt het veld af als groeperingssleutel, juist in het geval dat we willen samenvoegen: een concern met één RSIN dat in Profit onder meerdere organisaties hangt. Het raakt hoofdstuk 2, §5.2, §5.3, §5.5, §5.9, §6.3, §7.3, §7.4 en hoofdstuk 10 en 11; de berekeningen zelf wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AH1 | Herkomst van het RSIN (§5.2, §5.3); herziet J3 | Lezen uit het veld **Fiscaal nummer** op de organisatie, nadrukkelijk níét uit het loonheffingsnummer | De **eerste negen posities van het loonheffingsnummer**, met het subnummer achter de L weggelaten. De integriteitsregel maakt het Fiscaal nummer onbruikbaar: bij een concern met meerdere organisaties onder één RSIN kan hooguit één daarvan het nummer voeren. Het loonheffingsnummer is er altijd zodra er wordt verloond, dus het RSIN is voortaan altijd te bepalen |
| AH2 | Het veld Werkgever op laag 0 (§5.2, §5.9); herziet J1 en T3 | De werkgeverscode als er geen RSIN was; precies één van RSIN en Werkgever was gevuld | **Altijd leeg.** Eén RSIN kan meerdere werkgevers bevatten die juist één rapportage-eenheid moeten vormen; een werkgeverscode zou die eenheid weer uit elkaar trekken. Het veld blijft bestaan en blijft in de unieke sleutel staan, zodat die sleutel niet wijzigt als het ooit wél wordt gevuld. In de gegevensverzamelingen en de sortering laten we het weg |
| AH3 | Niveau waarop het RSIN wordt bepaald (§5.2, §6.3, §7.3, §7.4) | Per organisatie, en daarmee per werkgever | Per **werkgever én periodetabel**. Drie inrichtingen komen voor: één werkgever met een subnummer per periodetabel, twee werkgevers met hetzelfde RSIN gesplitst op periodetabel, en één werkgever met twee loonheffingsnummers waarvan het RSIN verschilt. De eerste twee vragen een bredere blik dan de werkgever, de derde een fijnere; alleen deze combinatie dekt beide. Ze staat ook op de bronregel, dus elke bronregel is eenduidig toe te wijzen. Gevolg: één werkgever kan over twee rapportage-eenheden verdeeld zijn, en stap 9 van de taak raakt dan beide |
| AH4 | Afdwingen van het Fiscaal nummer (§5.2, hoofdstuk 10 en 11); herziet J5 en J9 | We dwingen het niet af voor het recht op informatie; DP2 zou het wél als voorwaarde moeten stellen | **Niet meer aan de orde.** Het veld speelt geen rol meer, dus er is niets af te dwingen, aan te vullen of te signaleren — ook niet in DP2. Wat voor DP2 overblijft is de vraag of het loonheffingsnummer zelf bij de aanlevering moet worden meegegeven; dit ontwerp legt dat nummer niet vast |
| AH5 | BSN bij een eenmanszaak (§5.2); aanvaardt het bezwaar uit J3 | Reden om het loonheffingsnummer níét te gebruiken | **Aanvaard, zonder beperkende maatregel.** Bij een eenmanszaak zijn de eerste negen posities het BSN van de ondernemer, en een BSN is niet van een RSIN te onderscheiden. De drie bezwaren uit J3 staan nog overeind, maar er is geen alternatief: zonder groeperingssleutel is er geen vergelijkingsgroep en dus geen recht op informatie. Het RSIN blijft gewoon beschikbaar in de gegevensverzamelingen en waar van toepassing op het scherm; afschermen zou de herkomst van een vergelijkingsgroep onnavolgbaar maken |
| AH6 | Wijzigend loonheffingsnummer (§5.2, §5.8) | Niet belegd | **Niets regelen.** Wijzigt het nummer, dan valt de werkgever bij de eerstvolgende run onder een andere rapportage-eenheid; de taak bouwt alles toch volledig opnieuw op. De oude rapportageperiode blijft leeg achter en wordt niet opgeruimd. Het geval is zeldzaam genoeg om er geen routine voor te bouwen; §5.8 krijgt dus geen opruimregel |

Besloten in blok AI, de triggerronde na DP5, op 6 oktober 2026:

Aanleiding is de functionaliteit uit DP5. Dat deelproject legt de functiecategorie van een uitzendkracht op twee nieuwe plekken vast: op de **functie van de klantovereenkomst** en als **afwijkende functiecategorie op de plaatsing**. Blok AG verwerkte dat in de sleutel van laag 2, maar niet in het vulproces — er was geen gebeurtenis die een wijziging van die twee velden zou oppikken. Bij het nalopen bleek daarnaast dat een wijziging in de indeling niet alleen laag 2 en laag 3 raakt: functie en functiecategorie staan óók op laag 1, en die bronregels werden maar voor één tijdvak bijgewerkt. Het raakt §1.3, hoofdstuk 2, §5.3, §7.1 tot en met §7.4, §8.1 en hoofdstuk 10; de berekeningen in hoofdstuk 6 en de sleutels van laag 2 en laag 3 wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AI1 | Triggerregel bij de functiecategorie op de functie van de klantovereenkomst (§7.2); herziet AA5 | Geen triggerregel; de eerstvolgende verwerking zou de nieuwe indeling meenemen | **Wél een triggerregel.** Koppelt de inlener een functie aan een andere categorie, dan verandert de vergelijkingsgroep van elke plaatsing op die functie, zonder dat er iets in de salarisverwerking gebeurt — precies wat bij een eigen medewerker de functiewijziging doet. De functie hangt aan één verkooprelatie maar de triggertabel gaat per **werkgever**, dus we leiden de betrokken uitleners af uit de **plaatsingen op die functie** en schrijven per werkgever en periodetabel één regel weg op het laatste geaccordeerde tijdvak. Het alternatief — alle werkgevers, zoals bij de functiecategorie-inrichting — valt af: dat rekent de hele omgeving door voor een wijziging bij één inlener |
| AI2 | Triggerregel bij de afwijkende functiecategorie op de plaatsing (§7.2); herziet AA5 | Geen triggerregel bij een mutatie op de plaatsing | **Wél een triggerregel**, bij vullen, wijzigen én leegmaken. Leeghalen is net zo goed een wijziging: de plaatsing valt dan terug op de categorie van de functie. De plaatsing hangt aan één dienstverband en dus aan één werkgever; die krijgt per periodetabel één regel op het laatste geaccordeerde tijdvak. Het volume-argument onder AA5 houdt hier geen stand: dit is één veld op een bestaande plaatsing en geen plaatsingmutatie in het algemeen. Voor nieuwe plaatsingen, inlenerwissels en overige mutaties **blijft AA5 gelden** |
| AI3 | Triggerregel bij de functie van de plaatsing (§7.2); corrigeert AA5 | AA5 en §7.2 noemden "een gewijzigde functie op de plaatsing" als geval waarvoor géén triggerregel nodig is | **Niet van toepassing.** De functie op de plaatsing is na het aanmaken niet meer te wijzigen, dus er is geen gebeurtenis om op te triggeren. De oude formulering suggereerde een afweging waar er geen was; die is eruit gehaald |
| AI4 | Reikwijdte van het bijwerken van de bronregels (§5.3, §7.3); scherpt U9 aan | Stap 2 schreef per openstaande triggerregel de bronregels van **dat ene tijdvak** opnieuw weg | Bij een trigger op **stamgegevens** worden de bronregels van **alle tijdvakken binnen het venster** opnieuw weggeschreven. Laag 1 legt naast de berekende bedragen ook stamgegevens vast — functie, functiecategorie, geslacht, soort en aard inkomstenverhouding, plaatsing en verkooprelatie (§5.3) — en die wijzigen over het hele venster mee. Eén tijdvak bijwerken zou de nieuwe indeling op één bronregel zetten en de oude op de tijdvakken daarvoor, waarna laag 2 het loon over twee categorieën verdeelt die één vergelijkingsgroep vormen. De berekende bedragen komen daarbij ongewijzigd terug; dat kost rekentijd en levert dezelfde waarden op. Bij een trigger op **salarisgegevens** blijft het bij dat ene tijdvak. Geldt voor soort rapportage *Recht op informatie*; voor soort *Rapportage* is het een vraag voor DP2 (punt AI-a) |
| AI5 | Kenmerk Soort trigger op de triggertabel (§7.2, hoofdstuk 2, hoofdstuk 10); herziet M3 en M18 | De tabel bevatte alleen werkgever, periodetabel, jaar en periode; wát er was gewijzigd deed niet ter zake | Er komt één kenmerk bij: **Soort trigger**, met de waarden *Salarisgegevens* en *Stamgegevens*. Zonder dat kenmerk is AI4 niet uitvoerbaar: een stamgegeven-trigger staat op het laatste geaccordeerde tijdvak en is daar niet te onderscheiden van een gewone accordering. Het alternatief — de schrijvende processen een regel per tijdvak in het venster laten wegschrijven — valt af omdat de triggertabel dan met twaalf tot drieënvijftig regels per werkgever groeit, tegen het uitgangspunt in dat de werkvoorraad klein blijft (§7.4) |
| AI6 | Volgorde van de stappen in de taak (§7.3) | Stap 2 werkte de bronregels bij, stap 3 bepaalde daarna het venster | **Omgedraaid.** De vensterbepaling wordt stap 2 en het bijwerken van de bronregels stap 3, omdat dat bijwerken bij een stamgegeven-trigger moet weten welke tijdvakken in het venster vallen. Aan de vensterbepaling zelf en aan de stappen 4 tot en met 11 verandert niets |

Besloten in blok AJ, de loonbegrippen voor uitzendkrachten, op 7 oktober 2026:

Aanleiding was de vraag wat het afwijkende begrippenkader voor uitzendkrachten nu precies betekent voor de velden en de formules. Het antwoord bleek nergens in de hoofdstukken zelf te staan: §5.3, §6.1 en §6.2 meldden alleen dát de definities verschillen, en de enige plek met de inhoud was punt W1 in dit hoofdstuk. Daarbij kwam een inhoudelijke fout aan het licht: de gedeelde formule voor het bruto jaarloon werkt niet voor deze populatie. Het raakt §5.3, §6.1 en §6.2; de sleutels en het vulproces wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AJ1 | Inhoud van lijstbegrip 6.783 (§5.3, §6.2) | De begrippentabel in §6.2 zette 6.783 op de rij **LnLbPh**, wat het leest als dezelfde grootheid op plaatsingniveau | **Bevestigd op 7 oktober 2026:** 6.783 bevat **alleen de looncomponenten onder het reguliere tarief**. Het is dus géén LnLbPh: het deel onder bijzonder tarief zit er niet in, en dat komt uit het aparte begrip 6.784. Onbelaste componenten, componenten onder nultarief, het werknemersdeel pensioen en de bijtelling vervoermiddel zitten in geen van beide. De tabel in §6.2 heeft daarom aparte rijen per populatie gekregen in plaats van één rij met twee Profit Id's |
| AJ2 | Formule voor het bruto jaarloon (§6.1); volgt uit AJ1 | Eén gedeelde formule voor beide populaties: totaalloon minus de variabele componenten. §6.1 vermeldde expliciet dat de formule voor het bruto jaarloon niet wijzigt | Een **eigen formule voor uitzendkrachten**: som van ([Brutoloon] + OpgRchtVakBsl + OpbAvwb). Het brutoloon wordt daar **opgeteld en niet afgeleid**, omdat er geen totaalbedrag is om de variabele componenten vanaf te trekken. VakBsl en OpnAvwb staan er niet in: die vallen onder bijzonder tarief, zitten al in [Brutoloon bijzonder tarief] en gaan er bij de variabele componenten af. De formuletabel in §6.1 heeft een tweede kolom gekregen |
| AJ3 | Veldnamen in de brontabellen voor uitzendkrachten en extern (§5.3) | *Loon LB/PH normaal tarief* en *Loon LB/PH bijzonder tarief*, identiek aan de tabel voor medewerkers, met als enige toelichting "Per plaatsing" | **Loon regulier tarief** en **Loon bijzonder tarief**, met een toelichting die de definitie uitschrijft · **nader vastgesteld op 7 oktober 2026: Brutoloon en Brutoloon bijzonder tarief**, in de termen van het kader uitzendkrachten. De toevoeging *LB/PH* verwijst naar een rubriek uit de loonaangifte, en die kent de plaatsing niet. Dezelfde naam voeren suggereerde dat beide populaties hetzelfde gegeven vastleggen, en juist bij deze twee velden is dat niet zo. **Loontransparantie bron extern** krijgt dezelfde namen; de tabel bevat dezelfde grootheden en zou anders hetzelfde misverstand oproepen |
| AJ4 | Waar het verschil wordt beschreven (§5.3, §6.1, §6.2) | Alleen in punt W1 van dit hoofdstuk; de hoofdstukken zelf meldden alleen dát de definities verschillen. §6.2 stelde bovendien dat beide sets "hetzelfde gegeven" leveren | De definitie staat nu in de **hoofdtekst**: in §5.3 bij de velden, in §6.1 bij de formules en in §6.2 bij de lijstbegrippen. De zin over "hetzelfde gegeven" is vervangen: zes grootheden leveren dat wél, de twee loonvelden niet |
| AJ5 | Bijtelling vervoermiddel en pensioenpremie (§6.2) | "Die afbakening geldt voor beide populaties" | **Niet gelijk.** Bij een uitzendkracht vallen ze er volledig buiten, omdat het kader ze uitzondert. Bij een medewerker komt een bijtelling voor een auto van de zaak wél mee, via WrdLn in de variabele componenten: daar is het bedrag per dienstverband bekend en is er één werkgever om het aan toe te rekenen. De populaties worden nooit met elkaar vergeleken, dus dat verschil hoeft niet te worden gladgestreken |

Besloten in blok AK, het loon LB/PH bij medewerkers, op 7 oktober 2026:

Blok AJ bracht de loonbegrippen van de uitzendkrachten op orde. Bij het nalopen van de tegenhanger voor medewerkers bleek dat daar een vergelijkbare fout zat, met omgekeerd teken. Het ontwerp ging ervan uit dat de brontabel het loon in twee niet-overlappende helften vastlegt, normaal tarief en bijzonder tarief, en dat die samen LnLbPh vormen. Dat is in Profit niet zo. Geverifieerd in de repository: LnLbPh en LnTabBB hangen aan **hetzelfde lijstbegrip** (Profit Id 1287 + 1670), dat twee keer wordt uitgelezen — zonder filter levert het het **totale** loon LB/PH inclusief het bijzondere deel, met een filter op het tarief levert het alleen dat bijzondere deel. Een variant die alleen het normale tarief oplevert bestaat niet. Het raakt §5.3, §6.1 en §6.2.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AK1 | Inhoud van LnLbPh (§5.3, §6.2) | De brontabel legde twee niet-overlappende delen vast, en "samen vormen ze LnLbPh" | **LnLbPh is het totaal.** Het bijzondere tarief zit er al in; LnTabBB is daarvan een **deelverzameling** en geen bedrag ernaast. Het filter op het tarief bestaat alleen voor het bijzondere deel, niet voor het normale |
| AK2 | Veldnaam in *Loontransparantie bron medewerkers* (§5.3); volgt uit AK1 | *Loon LB/PH normaal tarief*, met als toelichting dat het samen met het bijzondere tarief LnLbPh vormt | **Loon LB/PH**, zonder de toevoeging *normaal tarief*. Gevuld uit lijstbegrip 1287 + 1670 is het veld het hele loon LB/PH; de oude naam beschreef iets wat er niet in zit en wat uit de bron ook niet te halen is. *Loon LB/PH bijzonder tarief* blijft ongewijzigd heten |
| AK3 | Overlap tussen de twee velden (§5.3, §6.2); herziet M-redenering | "Zo slaan we geen bedrag dubbel op" | **Het bijzondere bedrag staat in beide velden, en dat is aanvaard.** Het alternatief — het normale deel zelf uitrekenen als totaal min bijzonder — zet een bedrag in de brontabel dat geen enkel lijstbegrip levert en dat niet terug te voeren is op één verwerkte salarisregel (uitgangspunt 3). Gevolg en voorwaarde: de twee velden mogen **nooit bij elkaar worden opgeteld** |
| AK4 | Leesbaarheid van de formules (§6.1) | De formule noemde LnLbPh, wat geen veld in de brontabel was maar de som van twee velden | Na AK2 is **elke afkorting in de medewerkerskolom precies één veld**. §6.1 zegt dat nu expliciet, samen met de waarschuwing dat LnTabBB in LnLbPh zit en maar één keer mag worden afgetrokken |

Besloten in blok AL, een eigen set lijstbegrippen voor medewerkers, op 7 oktober 2026:

Tot nu toe vulde dit ontwerp de brontabel voor medewerkers uit de **bestaande lijstbegrippen van de loonaangifte**. Dat vroeg geen bouwwerk, maar het bond de loontransparantie aan de inrichting van de aangifte — en daar kan de klant niet aan sleutelen, met goede reden. Het gevolg was dat **correctie-looncomponenten** die in de aangifterubriek niet op de juiste plek landen, ook in de loontransparantie niet meetellen. Het raakt §1.4, hoofdstuk 2, §4.4, §5.3, §6.2 en hoofdstuk 10; de formules en het datamodel wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AL1 | Herkomst van de bedragen voor medewerkers (§5.3, §6.2); herziet AF2 | De **bestaande** lijstbegrippen van de loonaangifte: 3515, 1287 + 1670, 1317, 1318, 1321, 5068 en 5069 | Een **eigen set**, Profit Id **6.821 t/m 6.827**, per dienstverband. Zeven begrippen voor acht grootheden: 6.822 levert zowel LnLbPh als LnTabBB, zonder en met een filter op het tarief. Beide populaties hebben daarmee een eigen set, wat de redenering uit AF2 doortrekt |
| AL2 | Intellingen door de klant (§5.3, §6.2); herziet R13 en de kerngrootheden-helft van AE6 | De acht kerngrootheden stonden **dicht**: AFAS levert ze en de klant kan er niet aan sleutelen, want ze vormen de grondslag van de vergelijking | De set voor medewerkers **staat open** voor eigen intellingen. Dat is de reden dat hij er is: zonder die ruimte ontbreken correctie-looncomponenten die inhoudelijk wél bij het loon horen. **Volledigheid weegt zwaarder dan gegarandeerde uniformiteit.** Aanvaard omdat het vergelijken binnen één omgeving gebeurt — daar geldt een toegevoegde intelling voor iedereen — en omdat de klant aanvult en niet vervangt |
| AL3 | De jaargrens (§4.4); herziet R13 | Geen probleem, want AFAS levert de begrippen en de klant kan ze niet aanpassen, dus de definitie is in elk jaar dezelfde | Het probleem is **niet meer uitgesloten**. Voegt een klant in jaar twee een component toe die in jaar één niet meetelde, dan telt het venster over de jaargrens bedragen op die niet precies hetzelfde betekenen. We rekenen dat **niet glad**: het gaat om een aanvulling en niet om een andere grondslag, en het effect is dat het venster ná de wijziging iets vollediger is. Uitleg hoort bij de help |
| AL4 | De set voor uitzendkrachten (§5.3); herziet besluit 108 | Door AFAS meegeleverd en **dichtgezet** | **Staat ook open.** Dezelfde dag alsnog besloten, met een eigen aanleiding: klanten moeten in bepaalde situaties een **uitwijkmogelijkheid** hebben. De looninrichting van een uitzendorganisatie laat zich niet altijd in de standaarddefinitie vangen, en zonder die ruimte blijft zo'n klant met cijfers zitten die hij niet kan herstellen. Daarmee staat er in dit ontwerp geen lijstbegrip meer dicht, en sluit punt AL-b |
| AL5 | Gevolg voor het onderscheid met de verklarende bedragen (§5.3) | De kerngrootheden stonden dicht — grondslag van de vergelijking — en de negen verklarende bedragen open, want die geven alleen duiding | Dat onderscheid loopt **niet langer via open of dicht**; alles staat open. Het blijft wél bestaan, maar op de enige grond die overeind blijft: de verklarende bedragen komen in geen enkele formule voor omdat ze bedragen duiden die al in de kerngrootheden besloten liggen, en niet omdat hun inhoud minder vastligt (AE3) |

Besloten in blok AM, de rekenrichting van de percentages, op 7 oktober 2026:

Aanleiding is het gedrag van de tegels 4 en 5 op het scherm. Een positief loonverschil betekende dat vrouwen mínder verdienden, en een positief individueel verschil dat de medewerker mínder verdiende dan het gemiddelde van zijn functiecategorie. Dat leest voor de medewerker averechts: hij ziet een plus en leest die als iets gunstigs. §6.5 beschreef die richting niet als een vergissing maar als een afweging — consistentie met de rapportage woog daar zwaarder dan leesbaarheid. Die afweging valt nu de andere kant uit. Bij het nalopen van de schermteksten kwamen er drie losse punten bij: een ontbrekend bijschrift bij een uitkomst van nul, een opengelaten aanspreekvorm voor de MSS-stamkaart en een achtergebleven regel over tegel 4. Het raakt hoofdstuk 2, §5.4, §5.5, §5.9, §6.5, §6.6, §6.9, §7.3, §8.2, §8.6, §8.7, §8.8 en hoofdstuk 10 en 11; de velden, de sleutels, de grondslagen en het vulproces wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AM1 | Rekenrichting van de loonverschilpercentages (§2, §5.5, §6.5, §6.6); herziet de afweging onder het individuele loonverschil | Eén richting voor alle percentages: (gemiddelde mannen − gemiddelde vrouwen) / gemiddelde mannen, waarin een **plus** betekent dat vrouwen minder verdienen | Twee richtingen, bepaald door de **soort rapportage**. Bij *Recht op informatie* wisselt de teller van volgorde: (gemiddelde vrouwen − gemiddelde mannen) / gemiddelde mannen, waarin een **min** betekent dat vrouwen minder verdienen. Bij *Rapportage* blijft de wettelijke richting staan. De noemer, de grondslagen, de afrondingsregel en de regels bij een lege groep wijzigen niet |
| AM2 | Reikwijdte van de omkering (§5.5, §6.5, §6.6) | Niet aan de orde | **Alle elf percentages**: de vijf loonverschilpercentages en de vijf mediane varianten op laag 3, plus het individuele loonverschil op laag 2. Het alternatief — alleen de drie percentages die de medewerker ziet — valt af: dan tellen binnen één regel percentages met en zonder omkering door elkaar, en dat is op de regel zelf niet te zien. Nu is de richting een eigenschap van de **rij** en staat ze vast zodra de soort rapportage bekend is |
| AM3 | Richting van het individuele loonverschil (§2, §5.4, §6.5, §8.2, §8.7); herziet de keuze om dezelfde kant op te tellen als het groepsverschil | (gemiddeld totaal uurloon categorie − eigen totaal uurloon) / gemiddeld totaal uurloon categorie; een plus betekende **minder** verdienen | (eigen totaal uurloon − gemiddeld totaal uurloon categorie) / gemiddeld totaal uurloon categorie. Het teken gaat uit van de **eigen waarde**: een plus staat boven het categoriegemiddelde, een min eronder. Geslacht speelt er niet in mee — niet in de teller en niet in de noemer — dus de teksten bij tegel 4 noemen geen geslacht |
| AM4 | Onderbouwing van de afwijking (§6.5) | Consistentie met de voorgeschreven rekenwijze woog zwaarder dan leesbaarheid, vooral vanwege het dashboard | **Omgekeerd gewogen.** Het recht op informatie en de wettelijke rapportage zijn twee losse onderdelen die zelden naast elkaar worden gelegd, en de rapportagecijfers zelf wijzigen niet. Dat de medewerker begrijpt waar hij naar kijkt weegt zwaarder dan dat beide onderdelen hetzelfde teken dragen |
| AM5 | Eén soort rapportage per ontsluiting (§5.9, §8.8, hoofdstuk 10 en 11) | Het filter op soort rapportage stond er om dubbele regels te voorkomen | Het filter krijgt er een **tweede, hardere grond** bij: het houdt de twee rekenrichtingen uit elkaar. Het **Power BI-dashboard toont uitsluitend soort *Recht op informatie***, net als de meegeleverde verzamelingen, de weergaven daarop en de Pocket-connector. DP2 levert een **eigen ontsluiting** met een filter op soort Rapportage en hergebruikt de verzamelingen uit §5.9 niet. Daarmee kunnen twee percentages met dezelfde veldnaam nooit tegengesteld naast elkaar staan |
| AM6 | Herkomst van de formules (§6.9) | De tabel koppelde vier percentages aan een G-nummer; *Loonverschil totaal uurloon* en *Mediane loonverschil totaal uurloon* stonden er niet in | Een **G-nummer legt de formule vast, niet het teken**: grondslag, noemer en vergelijkingsgroep blijven identiek, alleen de leesrichting verschilt per soort. De twee ontbrekende percentages op het totaal uurloon zijn aan de tabel toegevoegd als eigen uitbreiding zonder nummer |
| AM7 | Grondslag van het individuele loonverschil in de lopende tekst van §6.5 | §6.5 schreef nog dat de medewerker wordt afgezet tegen "het gemiddelde van de **eigen** geslachtsgroep" | **Hersteld.** Dat was blijven staan na de wijziging van 24 september 2026 (punt AD5) en sprak de rest van het ontwerp tegen: de noemer is het gemiddelde van de **hele** functiecategorie, alle geslachten samen. Een losse correctie, geen nieuwe keuze |
| AM8 | Conversie van reeds berekende percentages (§7.7) | Niet aan de orde | **Geen conversie.** Deze wijziging landt vóór de eerste uitlevering van Profit 9, en de conversie vult de triggertabel over heel 2026 (besluit 86), dus de eerste dagovergang rekent alles met de nieuwe formule door. Er bestaat geen gegeven met het oude teken. Expliciet vastgelegd omdat de taak alleen rekent waarvoor een triggerregel openstaat (§7.3): zonder dat conversiemechanisme zou een werkgever zonder salarisverwerking op de oude waarden blijven staan |
| AM9 | Onderwerp van tegel 5 (§8.2, §8.7) | Niet benoemd; het bijschrift wisselde bij een positieve uitkomst van onderwerp naar de mannen | Het percentage van tegel 5 beschrijft de **vrouwen als groep** en niet de lezer: een man in een categorie waar vrouwen minder verdienen ziet een min, terwijl hij zelf meer verdient. Het bijschrift benoemt daarom altijd beide groepen en het percentage staat nooit zonder bijschrift op het scherm. De vrouwen blijven daarbij in **alle drie** de varianten het onderwerp — bij een plus staat er *Vrouwen verdienen gemiddeld meer dan mannen* en niet *Mannen verdienen gemiddeld minder dan vrouwen* — zodat het bijschrift in dezelfde volgorde leest als de teller van de formule (§6.5). Bij tegel 4 is het onderwerp juist de medewerker zelf en blijft geslacht eruit. De titel *Verschil uurloon mannen/vrouwen* blijft ongewijzigd; het bijschrift draagt de richting |
| AM10 | Bijschrift bij een uitkomst van nul (§8.2, §8.7) | Twee varianten per tegel: meer of minder | **Drie varianten per tegel.** Komt het percentage op 0,00 uit, dan is een bijschrift met *meer* of *minder* onjuist. Tegel 4 krijgt *evenveel als het gemiddelde*, tegel 5 krijgt *Mannen en vrouwen verdienen gemiddeld evenveel*. Zonder die derde variant zou er bij 0,00% in tegel 5 staan dat vrouwen minder verdienen. Bij tegel 4 staat dit los van de medewerker die als enige in zijn categorie zit; daar vervalt de tegel (§8.6) · **herzien op 19 oktober 2026**: de tegel blijft staan met een melding, zie blok AP, punt AP4 |
| AM11 | Aanspreekvorm van de schermteksten (§8.7); scherpt de taalkeuze uit blok AC aan | De je-vorm met de aantekening dat team Content bepaalt of de MSS- en plaatsing-stamkaart een eigen formulering krijgen | **Vastgelegd in plaats van opengelaten.** Op de **ESS**-stamkaart geldt de **je-vorm**, op de **MSS**- en de plaatsing-stamkaart de **de-medewerkervorm**: *je*, *jij* en *jouw* worden *de medewerker*. Dat raakt de meldingen, het bijschrift van tegel 4 en de info-teksten van tegel 1, 2 en 4. De teksten van tegel 3 en 5 gaan over een groep en blijven gelijk. Het volgt de splitsing die tegel 2 al kende met *Jij* tegenover *Medewerker*. Blok AC noteerde "overal de je-vorm"; dat gold voor de ESS-stamkaart |
| AM12 | Tegel 4 bij een lege geslachtsgroep (§8.6) | §8.6 liet tegel 4 én tegel 5 leeg als er geen mannen of geen vrouwen in de functiecategorie zijn | **Alleen tegel 5 blijft leeg.** Tegel 4 rekent sinds blok AD, punt AD5 tegen het gemiddelde van de héle functiecategorie, en dat bestaat ongeacht de samenstelling. De oude regel dateerde uit de tijd dat de tegel tegen het eigen geslacht rekende. Een losse correctie, net als AM7 |

Besloten in blok AN, de indeling in medewerkers en uitzendkrachten, op 13 oktober 2026:

Aanleiding is onderzoek ON-10, dat de aard arbeidsverhouding op AFAS Online naast de verloningsvariant heeft gelegd, en de nieuwe verloningsvariant *Plaatsingen verwerken in periodeverloning* uit RHR02179. De aard blijkt niet consequent te worden vastgelegd, en de bouw deelde al niet in op de aard maar op het type periodetabel. In de brainstorm van 13 oktober 2026 is gekozen voor de best uitlegbare regel, met de aantekening dat latere wet- en regelgeving tot bijsturing kan leiden. Het raakt hoofdstuk 2, §3.1, §3.2, §3.3, §3.5, §5.3, §5.4, §5.6, §5.9, §6.1, §6.2, §6.3, §6.7, §7.3, §7.7, §8.1, §8.6, §8.7, §8.8 en hoofdstuk 10 en 11; de sleutels, de formules en de lijstbegrippen wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AN1 | Aard arbeidsverhouding (§2, §3.2, §3.3, §5.3, §5.4); herziet A5, AA2 en T9 | Twee populatiefilters: aard 1, 18, 21, 23, 24 en 83 voor medewerkers, aard 11, 22 en 82 voor uitzendkrachten | De aard **bepaalt niet meer de populatie**. ON-10 laat zien dat ze daarvoor niet bruikbaar is: uitzendkrachten bij declaratieverwerking op aard 1 komen bij de medewerkers, en aard 11, 22 en 82 zonder loon per plaatsing komen in een brontabel die niet te vullen is. De aard **blijft wel een filter**, met de negen codes uit het begrippenkader samen — 1, 11, 18, 21, 22, 23, 24, 82 en 83 — voor beide populaties. Zo blijven fictieve dienstbetrekkingen buiten de dataset. Het veld staat op laag 1 en laag 2 |
| AN2 | Indeling in de brontabellen (§3.3, §5.3, §7.3) | Op aard arbeidsverhouding; de bouw deelde in op het type periodetabel | Op de **verloningsvariant**. Declaratieverwerking gaat **altijd** naar bron uitzendkrachten en nooit naar bron medewerkers. Periodeverwerking gaat naar bron medewerkers, ook als er plaatsingen administratief zijn vastgelegd. *Plaatsingen verwerken in periodeverloning* gaat naar **beide**. Het criterium is of de berekening aan een plaatsing hangt; daarmee kan er nooit een regel ontstaan in een tabel die niet te vullen is |
| AN3 | Bron medewerkers bij Plaatsingen verwerken in periodeverloning (§3.3, §5.3) | Niet aan de orde | Bron medewerkers bevat **altijd het totaal**, conform de set lijstbegrippen voor medewerkers. Die leveren hun waarde per inkomstenverhouding, en de plaatsingsdienstverbanden vallen onder dezelfde inkomstenverhouding als het hoofddienstverband. Naast het vaste loon zitten daar dus ook de projecttoeslagen van de plaatsingen in. Het alternatief — alleen het restloon na toerekening — valt af: de gedetacheerde wil zich in de eerste plaats vergelijken met de collega's in zijn eigen functiecategorie, op zijn volledige loon |
| AN4 | Bron uitzendkrachten bij Plaatsingen verwerken in periodeverloning (§3.3, §5.3) | Niet aan de orde | Per plaatsing het **toegerekende deel** van het vaste loon **plus de projecttoeslag**. De projecttoeslag laten we niet weg: die hoort bij wat de gedetacheerde voor zijn werk bij die inlener ontvangt. Het bedrag is een deel van het totaal in bron medewerkers; de twee worden **nooit opgeteld** |
| AN5 | Payrolling en detacheren op gewone periodeverwerking (§3.3) | Volgens het aard-filter bij de uitzendkrachten, maar daar niet te vullen; in de bouw stilzwijgend bij de medewerkers | **Bewust bij de medewerkers.** Er is wel een plaatsing maar geen loon per plaatsing. Detacheren voelt bovendien meer als eigen organisatie dan als uitzenden. Wie per inlener wil vergelijken, zet de nieuwe variant aan |
| AN6 | Filter op soort medewerker (§3.2, §3.5, §5.3, §7.3) | Niet aanwezig; het filter in ON-10 telde alleen de soorten die Profit verloont | Een **filter bij het vullen van de brontabellen**. Personeelslid, Ondernemer met salaris en Expat tellen mee. Stagiair met salaris valt af, omdat de stagevergoeding het gemiddelde van de functie drukt waarin de stagiair meeloopt. Nabetaling na uitdienst valt af, wit én groen, omdat eindafrekeningen en vaststellingsovereenkomsten niets zeggen over het loonniveau. De soort medewerker wordt **niet opgeslagen** in de brontabellen: wat erin staat, telt mee |
| AN7 | Filter op soort inkomstenverhouding (§3.2) | Soort 11, 13, 15 en 17, voor beide populaties | **Ongewijzigd en hard.** Het is het kenmerk waarmee uitkeringen en transitievergoedingen buiten de dataset blijven. Eén uitzondering wordt nog uitgezocht: een UMC met afwijkende afspraken (punt AN-a) |
| AN8 | Toerekening van het vaste loon aan de plaatsing (§3.3, hoofdstuk 10 en 11) | Niet beschreven | **Uitgangspunt.** Het cao-team levert een aanvullende looninrichting waarmee een deel van het vaste loon aan de plaatsing wordt toegerekend, met een rekencomponent die het salaris terugverdeelt naar het plaatsingsdienstverband. Zonder die toerekening bestaat het loon per plaatsing vrijwel alleen uit de projecttoeslag |
| AN9 | Eén persoon in twee populaties (§5.4, §5.9, §6.3, §6.7, §8.1, hoofdstuk 11) | Alleen mogelijk bij twee dienstverbanden met een verschillende aard | Ook bij **één inkomstenverhouding** in de nieuwe variant. Voor het recht op informatie is dat juist: elke vergelijking blijft binnen één populatie en één functiecategorie, en de stamkaart toont per populatie de eigen cijfers. Voor de **rapportage** mag de arbeidsverhouding niet twee keer meetellen; dat lost DP2 op |
| AN10 | Overgang naar de nieuwe variant in 2027 (§7.7) | Niet beschreven | **Geen conversie.** Bron medewerkers loopt zonder breuk door, omdat daar vóór en na de overstap het totaal staat. Bron uitzendkrachten loopt pas vanaf de overstap vol; dat aanvaarden we, net als bij AB1 |
| AN11 | Melding bij ontbrekende gegevens (§8.6, §8.7, §8.8) | Twee meldingen: één als er nog geen salarisverwerking is, één als de arbeidsverhouding buiten de regeling valt | **Eén generieke melding.** We maken geen onderscheid tussen "(nog) geen loongegevens" en "valt buiten de regeling". De reden zegt de medewerker niets, en een dienstverband dat op soort medewerker afvalt heeft bovendien geen bronregel, zodat het onderscheid alleen met een extra toets op de stamgegevens te maken zou zijn. De melding verwijst naar HR |
| AN12 | Niveau van bron medewerkers (§3.1, §5.3, §5.4, §6.1, §6.2, §7.3); verduidelijkt L10, L11 en AL1 | Een regel per dienstverband; laag 2 telde de dienstverbanden onder dezelfde inkomstenverhouding op | De lijstbegrippen voor medewerkers leveren hun waarde **per inkomstenverhouding**, dus de brontabel heeft één regel per inkomstenverhouding en tijdvak. Effectief is elk dienstverband een eigen inkomstenverhouding, behalve bij subdienstverbanden: die zijn daardoor **al in de brontabel gegroepeerd**, onder het kapstokdienstverband. Dat geldt ook voor de **negen verklarende bedragen**: die halen we bij medewerkers eveneens per inkomstenverhouding op. De sleutel wijzigt niet; laag 2 hoeft geen dienstverbanden meer op te tellen. Hetzelfde mechanisme neemt bij Plaatsingen verwerken in periodeverloning de plaatsingsdienstverbanden mee in het totaal (AN3) |
| AN13 | Plaats van de filters (§3.2, §3.5, §5.3, §7.3); herziet de plaats uit L4 en AN6 | Soort medewerker bij het vullen van de brontabellen (stap 3); soort inkomstenverhouding en aard bij het samenstellen van laag 2 (stap 6) | **Alle drie bij het vullen** (stap 3). In de brontabellen staat alleen wat meetelt. Doorslaggevend is dat het Power BI-dashboard laag 1 rechtstreeks leest en de filters anders zelf zou moeten nabouwen: een tweede waarheid naast de taak. De uitkomsten op laag 2 en 3 wijzigen niet, want ook in stap 6 werd per tijdvak getoetst. Kwalificeert een tijdvak bij het opnieuw wegschrijven niet meer, dan verwijdert stap 3 de bronregel. Aanvaard: een latere verruiming van een filter vraagt een eenmalige vulling van de triggertabel, en DP2 moet bevestigen dat het de afgevallen arbeidsverhoudingen niet nodig heeft (punt AN-g). Stap 6 houdt alleen de landtoets over; de toets op loon en uren over het venster (§3.4) blijft op laag 2 |

Besloten in blok AO, de teksten van de tegels, op 19 oktober 2026:

Aanleiding is een wijzigingsverzoek op de tegels uit §8.2 en de teksten uit §8.7, met een verduidelijking over het valutasymbool en de periode op dezelfde dag. De titels worden vragen, de uitleg achter de info-iconen ligt vast en de sectie krijgt een vaste toelichting. Het raakt §3.8, §5.9, §8.1, §8.2, §8.7, §8.8, §9.4 en hoofdstuk 12; de velden, de formules, het vulproces en de bijschriften van tegel 4 en 5 wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AO1 | Titels van de tegels (§3.8, §5.9, §8.2, §8.7, §9.4); herziet AD1 en de neutrale koppen uit blok AC | *Gemiddeld uurloon*, *Gemiddeld uurloon binnen functiecategorie*, *Samenstelling functiecategorie*, *Individueel verschil uurloon* en *Verschil uurloon mannen/vrouwen*, op elke stamkaart gelijk | De titel is de **vraag** die de tegel beantwoordt. Tegel 1: *Hoeveel verdien ik per uur?* op ESS, *Hoeveel verdient de medewerker per uur?* op MSS en plaatsing. Tegel 4: *Verdien ik meer of minder dan mijn collega's?* op ESS, *Verdient de medewerker meer of minder dan collega's?* op MSS en plaatsing. Tegel 2 en 3 houden hun titel; tegel 5 heet overal *Wat is het verschil tussen mannen en vrouwen?*. Het pagina-onderdeel en de weergave houden een neutrale kop |
| AO2 | Bijschrift onder tegel 1 (§8.2, §8.7); herziet AD3 | Geen bijschrift; de titel zei al dat het om een gemiddelde ging | **gemiddeld per uur.** De vraagtitel noemt geen gemiddelde meer, en zonder bijschrift leest het bedrag als het actuele uurtarief |
| AO3 | Valutasymbool (§8.2, §8.7, §8.8) | Currency, EUR, vast | Het symbool van de valuta in het veld *Valutasymbool* op de **werkgever** van het getoonde dienstverband (AfasHrCurrencyId); is dat leeg, dan dat van de **basisvaluta** van de omgeving. Geldt voor elk bedrag: tegel 1, tegel 2 en de uitleg bij tegel 1, 4 en 5. Er wordt niets omgerekend. De Pocket-connector levert het symbool mee |
| AO4 | Periodeaanduiding (§8.2, §8.7); bevestigt D1 | *laatste 12 maanden* op alle tegels; verzocht werd die tekst dynamisch te maken op basis van de begin- en einddatum | **Blijft ongewijzigd.** De gegevens gaan steeds over het afgelopen jaar; voor vier weken en week maken we geen eigen tekst. Ook tegel 1, die wel een eigen begin- en einddatum heeft, noemt geen eigen periode, en de uitleg achter het info-icoon noemt vast *12 maanden* |
| AO5 | Uitleg bij tegel 1 (§8.7) | De opbouw uit basisloon en extra's met het totaal en de verloonde uren | Vastgesteld, in twee vormen: het gemiddelde per uur over de afgelopen 12 maanden, de verloonde uren, het basissalaris per uur en de extra's per uur. Het totaal staat er niet meer in; dat is de waarde van de tegel zelf |
| AO6 | Info-icoon van tegel 2 en 3 (§8.2, §8.7); herziet de verwijzing in X3 | Een uitleg wat er naast elkaar staat en waar de verdeling over gaat | **Vervalt.** Legenda, hamburger en de aantallen in de donut tonen het al. Dat de donut arbeidsverhoudingen telt en geen personen, gaat naar de help |
| AO7 | Uitleg bij tegel 4 (§8.2, §8.7); herziet de varianten uit AM11 | Het verschil als bedrag met *meer* of *minder* en het percentage; bij nul viel het slot van de zin weg | Eigen uurloon, het categoriegemiddelde en het verschil als **bedrag en percentage, beide met teken**. Eén zin dekt plus, min en nul, dus er zijn geen varianten meer. Twee vormen: ESS en MSS/plaatsing |
| AO8 | Uitleg bij tegel 5 (§8.2, §8.7) | De twee gemiddelden, het verschil zonder teken en het percentage, met de zin *Het minteken betekent dat vrouwen minder verdienen* | Het gemiddelde van de vrouwen en van de mannen en het verschil als **bedrag en percentage, beide met teken** (vrouwen min mannen, §6.5). De verklarende zin over het minteken vervalt: bedrag en percentage wijzen dezelfde kant op. Eén vorm voor alle stamkaarten |
| AO9 | Toelichting van de sectie (§8.1, §8.7) | Niet aanwezig; alleen de toelichting van de werkgever bij de functiecategorie | Een **vaste tekst per stamkaart**: je-vorm op ESS, de-medewerkervorm op MSS, en op de plaatsing met *bij dezelfde opdrachtgever* en *De opdrachtgever heeft bepaald*. Staat naast de toelichting in het pagina-onderdeel *Functie*. Wordt met een **script** geleverd, omdat de tekst nog niet als metagegeven in te checken is (punt AO-a) |
| AO10 | Status van de teksten (§8.7) | Alle teksten waren een voorstel van het ontwerp, aan te scherpen door team Content | Titels, het bijschrift van tegel 1, de toelichting en de uitleg achter de info-iconen liggen **vast**. De meldingen en de bijschriften van tegel 4 en 5 blijven een voorstel · **aangevuld op 19 oktober 2026**: ook de meldingen liggen vast, zie blok AP |

Besloten in blok AP, de meldingen, op 19 oktober 2026:

Aanleiding is een tweede wijzigingsverzoek op §8.7, dezelfde dag als blok AO. De meldingen krijgen een vaste tekst per toestand, met de tegel waar ze staan. Het raakt §8.2, §8.6, §8.7, §8.8, §9.4 en §9.6; de velden, de formules en het vulproces wijzigen niet.

| Nr. | Onderwerp | Was | Is |
| --- | --- | --- | --- |
| AP1 | Meldingen (§8.7); vult AO10 aan | Een voorstel in de je-vorm, zonder vaste plek | Een vaste tekst per **state** — NoPayrollYet, NoJobCategory, RecentFunctionChange, NotApplicable en bij Available geen mannen, geen vrouwen, alleen en functie gewisseld — met de **tegel** waar hij staat en een je-vorm en een de-medewerkervorm. De Pocket-connector geeft dezelfde state terug als reden |
| AP2 | Melding bij geen loongegevens (§8.6, §8.7); bevestigt AN11 | *Er zijn (nog) geen loongegevens om te tonen. Heb je hier vragen over? Stel ze aan HR.* | *Er zijn (nog) geen **salarisgegevens** om te tonen. Heb je hier vragen over? Stel ze aan HR.* Op tegel 1; de tegels 2 tot en met 5 vervallen. De tekst belooft geen moment, zodat hij ook klopt voor een arbeidsverhouding buiten de regeling. Gelijk op alle stamkaarten. Een tussenvoorstel dat de eerste salarisuitbetaling noemde, valt daarom af |
| AP3 | Melding bij een recente functiewissel (§8.6, §8.7) | Eén melding bij de sectie | De melding staat op **tegel 1 en tegel 4**, de twee tegels die de eigen regel nodig hebben. De tegels 3 en 5 en de gemiddelden in tegel 2 tonen gewoon hun cijfers |
| AP4 | De enige in de functiecategorie (§8.2, §8.6, §8.7, §9.4); herziet de regel in §8.6 en AM10 | Tegel 4 vervalt | Tegel 4 **blijft staan**, zonder percentage en met de melding dat de functiecategorie te klein is om te vergelijken. De pagina blijft daarmee steeds gelijk opgebouwd; dat de medewerker alleen staat, bleek al uit tegel 3 |
| AP5 | Buiten Nederland (§8.6, §8.8, §9.6) | De stamkaart toont de sectie niet en Pocket toont de pagina niet | De stamkaart toont de sectie **nog steeds niet**. **Pocket** toont een melding dat de cijfers alleen gelden voor werk onder de Nederlandse wet; de connector geeft de reden NotApplicable terug. In de app navigeert de medewerker zelf naar de pagina en verwacht hij uitleg |
| AP6 | Functiewissel binnen het jaar (§8.7, §8.8) | Een melding op de stamkaart | **Alleen in Pocket.** Op de stamkaart is de functie al te zien in de subtitel van tegel 1 |
