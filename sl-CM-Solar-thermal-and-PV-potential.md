<h2> Kazalo vsebine </h2><ul><li> <a href="#introduction">Uvod</a> </li><li> <a href="#inputs-and-outputs">Vhodi in izhodi</a> </li><li> <a href="#method">Metoda</a> </li><li> <a href="#sample-run">Vzorec teče</a> <ul><li> <a href="#test-run-1-default-input-values">Test Run 1: privzete vhodne vrednosti</a> </li><li> <a href="#test-run-2-modified-input-values">Preskusna izvedba 2: spremenjene vhodne vrednosti</a> </li></ul></li><li> <a href="#references">Reference</a> </li><li> <a href="#how-to-cite">Kako navajati</a> </li><li> <a href="#authors-and-reviewers">Avtorji in recenzenti</a> </li><li> <a href="#license">Licenca</a> </li><li> <a href="#acknowledgement">Zahvala</a> </li></ul><h2> Uvod </h2><p> Njegov cilj je izračunati fotonapetostni energetski potencial in finančno izvedljivost izbranega območja z upoštevanjem: </p><ul><li> namestitev novih PV sistemov na odstotek stavbnega odtisa </li><li> finančna izvedljivost novih obratov </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Vhodi in izhodi </h2><p> Vhodni parametri in plasti ter izhodni sloji in parametri so naslednji. </p><p> <strong>Vhodne plasti in parametri so:</strong> </p><ul><li> rastrska datoteka: <ul><li> povprečno letno obsevanje sonca [kWh m ^ {- 2}] </li><li> odtis stavbe, izračunan iz vhodne rastrske datoteke [-] </li></ul></li><li> del stavb s sončnimi paneli} [-] </li><li> referenčni parametri obrata: <ul><li> povprečna instalirana največja moč na napravo [kW_p] </li><li> učinkovitost sistema [-] </li><li> sončno sevanje pri standardnem preskusnem stanju enako 1 kW m ^ {- 2} </li><li> Učinkovitost modula pri standardnih preskusnih pogojih [kW m ^ {- 2}] </li><li> učinkovit faktor izkoriščenosti strešne zgradbe </li></ul></li></ul><p> <strong>Izhodni sloji in parametri so:</strong> </p><ul><li> skupni stroški pokrivanja izbranega območja s PV ploščami [valuta] </li><li> skupna letna proizvodnja energije [MWh / leto] </li><li> izravnani stroški energije [valuta / kWh] </li><li> rastrska datoteka z najprimernejšimi strehami za proizvodnjo PV energije </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metoda </h2><p> Izhajajoč iz razpoložljive površine in vrste PV tehnologije modul izračuna proizvodnjo PV energije pod naslednjimi predpostavkami: </p><ul><li> optimalen naklon PV sistema </li><li> površina PV modulov, ki je enaka odstotku odtisa zgradbe, ki ga izbere uporabnik </li><li> edinstvena izbrana tehnologija za vse nameščene PV sisteme </li><li> privzeta učinkovitost sistema enaka 0,75 </li></ul><p> Te predpostavke so bile storjene z namenom upoštevanja faze načrtovanja za regijo in ne oblikovanja posebnih PV sistemov. </p><p> Letna proizvodnja energije se izračuna z upoštevanjem prostorske porazdelitve letnega sončnega sevanja na odtisu stavbe. Proizvodnja PV energije se izračuna za eno samo reprezentativno napravo. Najbolj reprezentativna nameščena največja moč za PV sistem je vhod modula. Posledično se izračuna površina, ki jo zajema posamezna rastlina, in skupno število rastlin. </p><p> Nazadnje je najprimernejše območje izračunano z upoštevanjem streh z večjo proizvodnjo energije. Proizvodnja energije vsakega piksla zajema le del strehe, ki je enak f_roof. Sestavni del proizvodnje energije najprimernejšega območja je enak skupni proizvodnji energije izbranega območja. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Preskusna izvedba 1 </h2><p> Tu se obračunski modul izvaja za regijo Lombardija v Italiji (NUTS2). </p><ul><li> Najprej izberite Nuts2 in izbrano območje. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_01.png" title="Izberite regijo"/></p><ul><li><p> Sledite korakom, kot je prikazano na spodnji sliki: </p><ul><li> Kliknite gumb "Sloji", da odprete okno "Sloji": </li><li> Kliknite kartico "MODUL IZRAČUNA". </li><li> Kliknite na gumb "SOLAR PV POTENTIAL". </li></ul></li><li><p> Zdaj se odpre "Solar PV Potencial" in je pripravljen za zagon. </p></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Test Run 1: privzete vhodne vrednosti </h3><p> Privzete vhodne vrednosti upoštevajo možnost namestitve strešnih PV plošč na stavbe. Te vrednosti so povezane s obratom s 3 kWp. Morda boste morali nastaviti vrednosti pod ali nad privzetimi vrednostmi ob upoštevanju dodatnih lokalnih pomislekov in stroškov. Zato bi moral uporabnik te vrednosti prilagoditi tako, da najde najboljšo kombinacijo pragov za svojo študijo primera. </p><p> Če želite zagnati modul za izračun, sledite naslednjim korakom: </p><ul><li> Seji teči dodelite ime (neobvezno - tukaj smo izbrali "Test Run 1") in nastavili vhodne parametre (tukaj so bile uporabljene privzete vrednosti). </li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_02.png" title="Preskusna izvedba 1 s privzetimi vrednostmi"/></p><ul><li> Počakajte, da se postopek konča. </li><li> Kot izhodni podatki se v oknu "REZULTATI" prikažejo kazalniki in diagrami. Kazalniki kažejo: <ul><li> Skupna proizvodnja energije, </li><li> Skupni stroški namestitve, </li><li> Število nameščenih sistemov, </li><li> Izravnani stroški energije </li></ul></li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Preskusna izvedba 1 zavihek INDIKATORJI"/></p><ul><li> Na platno je dodana tudi nova plast, ki prikazuje zgradbe z večjim energijskim potencialom. Ta plast je dodana na seznam plasti v kategoriji "Izračunski modul". Ime seje izvajanja razlikuje izhode te izvedbe od drugih. Če prekličete izbiro privzetih slojev in izberete TEST RUN 1, si lahko prikažete najprimernejša območja za PV naprave. </li></ul><p><img alt="Fig. 4" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Preskusna izvedba 1 Računski modul PROSTORI"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Preskusna izvedba 2: spremenjene vhodne vrednosti </h3><p> Glede na vaše izkušnje in lokalno znanje lahko vhodne vrednosti povečate ali zmanjšate, da dosežete boljše rezultate. Lahko se odločite za povečanje površine stavbe, primerne za PV rastline. </p><ul><li><p> Določite ime seje izvajanja (neobvezno - tukaj smo izbrali "Test Run 2") in vhodne parametre Odstotek stavb s sončnimi paneli je enak 50. To pomeni, da pokrivamo 50% razpoložljivih strešnih zgradb. Upoštevajte, da lahko vsak piksel predstavlja več zgradb in ne pokrivamo celotne strehe s PV ploščami, lahko uporabnik nastavi tudi faktor izkoristka strešne zgradbe. Privzete vrednosti so nastavljene na 0,15. To pomeni, da je PV folij pokritih le 15% strešne površine v sliki. </p></li><li><p> Počakajte, da se postopek konča. </p></li><li><p> Kot izhodni podatki se v oknu "REZULTATI" prikažejo kazalniki in diagrami. Kazalniki kažejo: </p><ul><li> Skupna proizvodnja energije, </li><li> Skupni stroški namestitve, </li><li> Število nameščenih sistemov, </li><li> Izravnani stroški energije </li></ul></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Reference </h2><h2> Kako navajati </h2><p> Giulia Garegnani, v Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-Solar-PV-potential (april 2019) </p><h2> Avtorji in recenzenti </h2><p> To stran je napisal Giulia Garegnani *. </p><p> * <a href="http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx">Skupina za mestni in regionalni energetski sistem - EURAC Bozen</a> </p><p> Inštitut za obnovljivo energijo Drususallee / Viale Druso 1 I-39100 Bozen / Bolzano Italija </p><h2> Licenca </h2><p> Copyright © 2016–2019: Giulia Garegnani </p><p> Mednarodna licenca Creative Commons Attribution 4.0 </p><p> To delo je licencirano pod mednarodno licenco Creative Commons CC BY 4.0. </p><p> SPDX-identifikator licence: CC-BY-4.0 </p><p> Besedilo licence: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Zahvala </h2><p> Želeli bi izraziti našo globoko zahvalo <a href="https://www.hotmaps-project.eu">projektu Hotmaps</a> Obzorje 2020 (sporazum o dodelitvi sredstev 723677), ki je zagotovil sredstva za izvedbo te preiskave. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Solar-thermal-and-PV-potential) (original) [Bulgarian](bg-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Croatian](hr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Czech](cs-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Danish](da-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Dutch](nl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Estonian](et-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Finnish](fi-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [French](fr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [German](de-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Greek](el-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Hungarian](hu-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Irish](ga-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Italian](it-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Latvian](lv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Lithuanian](lt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Maltese](mt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Polish](pl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Romanian](ro-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovak](sk-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>  [Spanish](es-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Swedish](sv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated