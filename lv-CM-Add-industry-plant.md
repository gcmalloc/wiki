<h2> Satura rādītājs </h2><ul><li> <a href="#introduction">Ievads</a> </li><li> <a href="#inputs-and-outputs">Ieejas un izejas</a> </li><li> <a href="#method">Metode</a> </li><li> <a href="#sample-run">Izlases skrējiens</a> </li><li> <a href="#authors-and-reviewers">Autori un recenzenti</a> </li><li> <a href="#license">Licence</a> </li><li> <a href="#acknowledgement">Apstiprinājums</a> </li></ul><h2> Ievads </h2><p> Šis modulis nodrošina iespēju HotMaps rīklodziņā pievienot papildu nozares vietnes ar to apkures un dzesēšanas pieprasījumu un lieko siltuma potenciālu. Ir iespējams pievienot papildu energoietilpīgas, kā arī mazāk energoietilpīgas nozares. Lietotājs nepieciešamos datus ievada atsevišķā Excel rīkā, kas pēc tam ģenerē datu lapu, kuru augšupielādēt HotMaps rīklodziņā. </p><h2> Ieejas un izejas (kā lietot) </h2><h3> Lietotāja datu ievade Excel rīkā </h3><p> Lūdzu, lejupielādējiet nodrošināto Excel rīku šeit: xxx </p><h4> Pievienojiet vispārīgu informāciju </h4><p> Lūdzu, dodieties uz cilni: <figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/General_information.PNG"/></figure></p><p> Pirmajā solī, lūdzu, ievadiet visu nepieciešamo vispārīgo informāciju par vietām, kurās jāaprēķina siltuma un dzesēšanas pieprasījums un liekā siltuma potenciāls. Ir iespējams pievienot līdz 10 rūpniecības objektiem. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/General_information_Box.PNG"/></figure><h4> Izvēlieties aprēķina iespēju </h4><p> Otrajā posmā ir 3 iespējas, kā novērtēt siltuma un dzesēšanas pieprasījumu un lieko siltuma potenciālu. Lūdzu, ņemiet vērā, ka dažādiem uzņēmumiem ir iespējams pārslēgties no trim iespējām, bet ne pašā uzņēmumā. </p><p> Attiecībā uz pārmērīgu siltuma temperatūru ir jāpiemin, ka zemas temperatūras karstumu (&lt;100 ° C) var ievadīt Excel rīkā, bet tas vēl nav novērtēts HotMaps rīklodziņā. Ja jāapsver karstums ar zemu temperatūru, ir nepieciešams izmantot siltumsūkni. Tāpēc lietotājs var iekļaut siltumsūkņa elektroenerģijas pieprasījumu galīgajā enerģijas pieprasījumā pēc elektroenerģijas un paaugstināt ģenerētā siltuma pārpalikuma temperatūru diapazonā no 100-200 ° C. </p><p> xxx Img soļi xxx </p><h5> 1. variants: manuāla ievadīšana </h5><p> Lūdzu, dodieties uz cilni: <figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/Option1.PNG"/></figure></p><p> Lūdzu, izvēlieties šo opciju, ja izvēlētajam uzņēmumam ir pieejami dati par siltuma / dzesēšanas pieprasījumu un lieko siltuma potenciālu un temperatūras sadalījumu, un tos var aizpildīt manuāli. </p><h5> 2. variants: Augu izvēle </h5><p> Lūdzu, dodieties uz cilni: <figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/Option2.PNG"/></figure></p><p> Lūdzu, izvēlieties šo opciju, ja izvēlētajam uzņēmumam nav pieejama informācija par siltuma / dzesēšanas pieprasījumu un lieko siltuma potenciālu. Balstoties uz augu specifisku datu bāzi, vairākiem augiem un produktiem / procesiem var izvēlēties tipisku siltuma / dzesēšanas pieprasījumu un lieko siltuma potenciālu ar temperatūras sadalījumu. Pēc nepieciešamās ievades produkta specifisko datu konvertēšanai ir jāievada vērtība kā aprēķina bāze (piemēram, ražošana, platība utt.). Papildinformāciju par aprēķina metodi skatīt [Metode]. </p><h5> 3. risinājums: nozares izvēle </h5><p> Lūdzu, dodieties uz cilni: <figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/Option3.PNG"/></figure></p><p> Lūdzu, izvēlieties šo opciju, ja jūsu iekārtas tips nav pieejams 2. variantā. Pamatojoties uz nozares specifiskajiem siltuma datiem, tiek aprēķināts tipiskais siltuma / dzesēšanas pieprasījums un liekā siltuma potenciāls. Pēc nepieciešamības jāievada siltuma pieprasījums pēc kurināmā (GWh / gadā). Papildinformāciju par aprēķina metodi skatīt [Metode]. </p><h3> Datu augšupielāde HotMaps rīklodziņā </h3><p> Lūdzu, dodieties uz cilni: <figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/Data_Import.PNG"/></figure></p><p> Lūdzu, ņemiet vērā: pašlaik CSV failu augšupielāde vēl nav ieviesta HotMaps rīklodziņā. Drīzumā parādīsies vairāk informācijas. </p><h2> Metode </h2><p> Ja iekārtas siltuma / dzesēšanas vajadzība un liekā siltuma potenciāls nav zināms, lietotājam tiek piedāvātas divas uz indikatoriem balstītas metodes siltuma pieprasījuma un liekā siltuma potenciāla aprēķināšanai. </p><p> Jāpiemin, ka šīs vērtības ir tikai aptuvenas aptuvenās vērtības tipiskām iekārtām (2. opcija) vai nozaru līmenī (3. opcija) un neaizstāj rūpīgu siltuma pieprasījuma un liekā siltuma detalizētu analīzi un mērījumus. </p><h3> 2. variants: Augu izvēle </h3><p> Dati par augu specifisko siltumu tiek ņemti no datu bāzes Prognoze. (Pieeja no apakšas uz augšu vai no augšas uz leju?) Daudziem dažādiem energoietilpīgiem un mazāk energoietilpīgiem iekārtu procesiem siltuma / dzesēšanas pieprasījums un liekā siltuma potenciāls tiek iegūts no konkrētā kurināmā un elektrības gala enerģijas pieprasījuma. Ir svarīgi atzīmēt, ka bāzes datu bāzes dēļ šī metode attiecas tikai uz procesa siltumu un procesa dzesēšanu; telpas apkure un karstais ūdens šeit nav iekļauti. Atkarībā no auga veida tiek aprēķināti dažādi izejmateriāli (piemēram, ražošanas apjoms tonnās vai platība m2). </p><p> Siltuma un dzesēšanas pieprasījuma aprēķināšanai ir jāpieņem konversijas efektivitāte no galīgās enerģijas uz siltumu un dzesēšanu. Tā kā lielākā daļa siltuma lietojumu ir balstīti uz tvaiku, tiek pieņemts, ka efektivitāte ir 90% (Was ist mit Electricity?). Dzesēšanas iekārtām tiek pieņemts, ka energoefektivitātes koeficients (EER) ir xxx (von Tobi noch auszufüllen). </p><p> Visa 2. opcijai izmantotā datu bāze ir pieejama šeit: Repository_Link </p><h3> 3. risinājums: nozares izvēle </h3><p> 3. risinājums sniedz plašu siltuma pieprasījuma un siltuma pārpalikuma novērtējumu apstrādes rūpniecības nozarēs (saskaņā ar NACE 2008). </p><h4> Pārmērīga siltuma potenciāla aprēķināšana nozaru līmenī </h4><p> Lai aprēķinātu dažādu sektoru liekā siltuma potenciālu, tiek izmantoti siltuma pārpalikuma koeficienti saskaņā ar Brückner 2016 (sk. Attēlu xxx). Siltuma pārpalikuma koeficients tiek definēts kā izdalītais siltums, kas saražots uz vienu degvielas patēriņu. Brückner 2016 pieejamie dati, lai noteiktu siltuma pārpalikuma potenciālu apstrādes rūpniecībā, ir iegūti no emisiju apsekojuma, ko reizi četros gados veic valsts līmenī Vācijā. Saskaņā ar Emisijas deklarācijas rīkojumu (1. BImSchG) visiem augu operatoriem, kuri ir pakļauti apstiprināšanai, ik pēc četriem gadiem jāiesniedz deklarācija par emisijām. Novērtēti dati par 2008. gadu uzņēmuma līmenī, kas sastāv no izplūdes gāzu apjoma plūsmām un to temperatūras līmeņa. Kopā ar pieejamo informāciju par augu degvielas patēriņa veidu un kvantitāti, liekā siltuma koeficientu iekārtai aprēķina kā: </p><p> Pārmērīgs siltuma koeficients = Pārmērīgs siltuma / degvielas patēriņš </p><p> Visbeidzot, siltuma pārpalikuma koeficients tiek aprēķināts ne tikai uzņēmuma, bet arī nozares līmenī. Sīkāku informāciju skatīt Brückner 2016. </p><p> Saskaņā ar Brückner 2016 lieko siltuma faktoru skaitā ir siltuma pārpalikums, kas rodas no procesa siltuma, kā arī telpas siltuma veidošanās un karstā ūdens. Tas ir saistīts ar faktu, ka tiek analizēta tikai izplūdes gāzu apjoma plūsma, kas iziet no rūpnīcas, nesadalot kurināmā patēriņu telpas apsildē, karstā ūdenī un procesa siltumā. </p><h4> Siltuma pieprasījuma aprēķins nozaru līmenī </h4><p> darāms </p><p> Visa 3. opcijai izmantotā datu bāze ir pieejama šeit: Repository_Link </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_add_industry_plant/Factors.PNG"/><figcaption> <i><br/> Muss noch übersetzt werden.</i> </figcaption></figure><h2> Autori un recenzenti </h2><p> Šīs lapas autori ir Ali Ajdemirs * un Lisa Neusel * </p><ul><li> [] Šo lapu pārskatīja Tobiass Fleiters *. </li></ul><p> * <a href="https://isi.fraunhofer.de/">Fraunhofer ISI</a> Fraunhofer ISI, Breslauer Str. 48, 76139 Karlsrūe </p><h2> Licence </h2><p> Autortiesības © 2016-2018: Ali Aydemir, Lisa Neusel </p><p> Creative Commons Attribution 4.0 starptautiskā licence Šis darbs ir licencēts ar Creative Commons CC BY 4.0 starptautisko licenci. </p><p> SPDX-licences identifikators: CC-BY-4.0 </p><p> Licences teksts: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Apstiprinājums </h2><p> Mēs vēlamies izteikt visdziļāko atzinību Horizon 2020 <a href="https://www.hotmaps-project.eu">karsto karšu projektam</a> (dotācijas līguma numurs 723677), kas sniedza finansējumu šīs izmeklēšanas veikšanai. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><p> `` </p>

This page was automatically translated. View in another language:

[English](en-CM-Add-industry-plant) (original) [Bulgarian](bg-CM-Add-industry-plant)<sup>\*</sup> [Croatian](hr-CM-Add-industry-plant)<sup>\*</sup> [Czech](cs-CM-Add-industry-plant)<sup>\*</sup> [Danish](da-CM-Add-industry-plant)<sup>\*</sup> [Dutch](nl-CM-Add-industry-plant)<sup>\*</sup> [Estonian](et-CM-Add-industry-plant)<sup>\*</sup> [Finnish](fi-CM-Add-industry-plant)<sup>\*</sup> [French](fr-CM-Add-industry-plant)<sup>\*</sup> [German](de-CM-Add-industry-plant)<sup>\*</sup> [Greek](el-CM-Add-industry-plant)<sup>\*</sup> [Hungarian](hu-CM-Add-industry-plant)<sup>\*</sup> [Irish](ga-CM-Add-industry-plant)<sup>\*</sup> [Italian](it-CM-Add-industry-plant)<sup>\*</sup>  [Lithuanian](lt-CM-Add-industry-plant)<sup>\*</sup> [Maltese](mt-CM-Add-industry-plant)<sup>\*</sup> [Polish](pl-CM-Add-industry-plant)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Add-industry-plant)<sup>\*</sup> [Romanian](ro-CM-Add-industry-plant)<sup>\*</sup> [Slovak](sk-CM-Add-industry-plant)<sup>\*</sup> [Slovenian](sl-CM-Add-industry-plant)<sup>\*</sup> [Spanish](es-CM-Add-industry-plant)<sup>\*</sup> [Swedish](sv-CM-Add-industry-plant)<sup>\*</sup>
<sup>\*</sup>: machine translated