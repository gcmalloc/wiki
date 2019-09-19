<h2> Turinys </h2><ul><li> <a href="#introduction">Įvadas</a> </li><li> <a href="#inputs-and-outputs">Įėjimai ir išėjimai</a> </li><li> <a href="#method">Metodas</a> </li><li> <a href="#sample-run">Mėginio paleidimas</a> <ul><li> <a href="#test-run-1-default-input-values">1 bandymo eiga: numatytosios įvesties vertės</a> </li><li> <a href="#test-run-2-modified-input-values">2 testas: modifikuotos įvesties vertės</a> </li></ul></li><li> <a href="#references">Nuorodos</a> </li><li> <a href="#how-to-cite">Kaip cituoti</a> </li><li> <a href="#authors-and-reviewers">Autoriai ir recenzentai</a> </li><li> <a href="#license">Licencija</a> </li><li> <a href="#acknowledgement">Pripažinimas</a> </li></ul><h2> Įvadas </h2><p> Ja siekiama apskaičiuoti fotoelektros energijos potencialą ir pasirinktos srities finansinį pagrįstumą atsižvelgiant į: </p><ul><li> naujų PV sistemų įrengimas procentais nuo pastato pėdsakų </li><li> naujų gamyklų finansinis pagrįstumas </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Įėjimai ir išėjimai </h2><p> Įvesties parametrai ir sluoksniai, taip pat išvesties sluoksniai ir parametrai yra šie. </p><p> <strong>Įvesties sluoksniai ir parametrai yra šie:</strong> </p><ul><li> rastrinis failas: <ul><li> vidutinis metinis saulės spinduliavimas [kWh m ^ {- 2}] </li><li> pastato pėdsakas, apskaičiuotas iš įvesties rastrinio failo [-] </li></ul></li><li> dalis pastatų su saulės baterijomis} [-] </li><li> pamatiniai augalų parametrai: <ul><li> vidutinė įrengta didžiausia įrenginio galia [kW_p] </li><li> sistemos efektyvumas [-] </li><li> saulės spinduliuotė standartinėmis bandymo sąlygomis lygi 1 kW m ^ {- 2} </li><li> modulio efektyvumas standartinėmis bandymo sąlygomis [kW m ^ {- 2}] </li><li> efektyvus pastato stogo panaudojimo koeficientas </li></ul></li></ul><p> <strong>Išvesties sluoksniai ir parametrai yra šie:</strong> </p><ul><li> visos pasirinktos srities padengimo PV plokštėmis išlaidos [valiuta] </li><li> bendra metinė energijos gamyba [MWh / per metus] </li><li> suvienodintos energijos sąnaudos [valiuta / kWh] </li><li> rastrinis failas su tinkamiausiais stogais PV energijai gaminti </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metodas </h2><p> Pradėjęs nuo turimos srities ir PV technologijos rūšies, modulis apskaičiuoja PV energijos pagaminimą pagal šias prielaidas: </p><ul><li> optimalus PV sistemos polinkis </li><li> PV modulių plotas lygus vartotojo pasirinktam pastato pėdsako procentui </li><li> unikali pasirinkta technologija visoms įdiegtoms PV sistemoms </li><li> numatytasis sistemos efektyvumas lygus 0,75 </li></ul><p> Šios prielaidos buvo padarytos siekiant apsvarstyti regiono planavimo etapą, o ne konkrečios PV sistemos projektavimą. </p><p> Metinė energijos išeiga apskaičiuojama atsižvelgiant į metinį saulės spinduliuotės pasiskirstymą pagal pastato pėdsaką. PV energijos gamyba apskaičiuojama vienam tipiškam augalui. Labiausiai reprezentatyvi didžiausia PV sistemos įdiegta didžiausia galia yra modulio įvestis. Taigi apskaičiuojamas vieno augalo padengtas paviršius ir bendras augalų skaičius. </p><p> Galiausiai apskaičiuojamas tinkamiausias plotas atsižvelgiant į didesnės energijos gamybos stogus. Manoma, kad kiekvieno pikselio energijos gamyba apima tik dalį stogo, lygaus f_roof. Tinkamiausios srities energijos gamybos integralas yra lygus visai pasirinktos srities energijos gamybai. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> 1 bandomasis bėgimas </h2><p> Čia skaičiavimo modulis vykdomas Lombardijos regionui Italijoje (NUTS2). </p><ul><li> Pirmiausia pasirinkite „Nuts2“ ir pasirinktą sritį. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_01.png" title="Pasirinkite regioną"/></p><ul><li><p> Atlikite veiksmus, kaip parodyta paveikslėlyje žemiau: </p><ul><li> Spustelėkite mygtuką „Sluoksniai“, kad atidarytumėte langą „Sluoksniai“: </li><li> Spustelėkite skirtuką „APSKAIČIAVIMO MODULIS“. </li><li> Spustelėkite mygtuką „SOLAR PV POTENTIAL“. </li></ul></li><li><p> Dabar atidaromas „Saulės saulės energijos potencialas“ ir jis yra paruoštas vykdyti. </p></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 1 bandymo eiga: numatytosios įvesties vertės </h3><p> Numatytomis įvesties vertėmis atsižvelgiama į galimybę ant pastatų montuoti ant stogo montuojamas PV plokštes. Šios vertės nurodomos 3 kWp jėgainei. Jums gali reikėti nustatyti žemiau nurodytas arba didesnes reikšmes nei numatytosios vertės, atsižvelgiant į papildomus vietinius aspektus ir išlaidas. Todėl vartotojas turėtų pritaikyti šias vertes, kad surastų geriausią slenksčių derinį savo atvejo tyrimui. </p><p> Norėdami paleisti skaičiavimo modulį, atlikite šiuos veiksmus: </p><ul><li> Priskirkite vykdymo sesijos pavadinimą (pasirenkama - čia pasirinkome „Test Run 1“) ir nustatykite įvesties parametrus (čia buvo naudojamos numatytosios vertės). </li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_02.png" title="1 bandymo eiga su numatytosiomis vertėmis"/></p><ul><li> Palaukite, kol procesas bus baigtas. </li><li> Kaip išvestis, rodikliai ir diagramos rodomi lange „REZULTATAI“. Rodikliai rodo: <ul><li> Bendra energijos gamyba, </li><li> Bendros sąrankos išlaidos, </li><li> Įdiegtų sistemų skaičius, </li><li> Išlygintos energijos sąnaudos </li></ul></li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="1 bandomasis rodiklis skirtukas"/></p><ul><li> Taip pat ant drobės pridedamas naujas sluoksnis, parodantis didesnio energijos potencialo pastatus. Šis sluoksnis pridedamas prie sluoksnių sąrašo, esančio kategorijoje „Skaičiavimo modulis“. Vykdymo seanso pavadinimas išskiria šio vykdymo rezultatus iš kitų. Jei atžymėjote numatytuosius sluoksnius ir pasirinkote TEST VYKDYTI 1, galite vizualizuoti tinkamiausias PV augalų instaliacijos sritis. </li></ul><p><img alt="Fig. 4" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="1 bandomasis skaičiavimo modulis Sluoksniai"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 2 testas: modifikuotos įvesties vertės </h3><p> Atsižvelgiant į patirtį ir vietines žinias, galite padidinti arba sumažinti įvesties vertes, kad gautumėte geresnių rezultatų. Galite nuspręsti padidinti PV augalams tinkamą pastato paviršių. </p><ul><li><p> Priskirkite vykdomosios sesijos pavadinimą (pasirenkama - čia pasirinkome „2 bandomąjį bėgimą“) ir nustatykite įvesties parametrus Pastatų su saulės baterijomis procentinė dalis yra lygi 50. Tai reiškia, kad padengiame 50% turimų pastatų stogų. Atminkite, kad kiekvienas taškas gali atstovauti daugiau nei vienam pastatui ir mes nedengiame viso stogo PV plokštėmis, todėl vartotojas gali nustatyti ir efektyvų pastato stogo naudojimo koeficientą. Numatytosios vertės yra 0,15. Tai reiškia, kad tik 15% stogo paviršiaus taške yra padengta PV plokštėmis. </p></li><li><p> Palaukite, kol procesas bus baigtas. </p></li><li><p> Kaip išvestis, rodikliai ir diagramos rodomi lange „REZULTATAI“. Rodikliai rodo: </p><ul><li> Bendra energijos gamyba, </li><li> Bendros sąrankos išlaidos, </li><li> Įdiegtų sistemų skaičius, </li><li> Išlygintos energijos sąnaudos </li></ul></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Nuorodos </h2><h2> Kaip cituoti </h2><p> Giulia Garegnani, „Hotmaps-Wiki“, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-Solar-PV-potential (2019 m. Balandžio mėn.) </p><h2> Autoriai ir recenzentai </h2><p> Šį puslapį parašė Giulia Garegnani *. </p><p> * <a href="http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx">Miestų ir regionų energetikos sistemos grupė - EURAC Bozen</a> </p><p> Atsinaujinančios energijos institutas „Drususallee“ / „Viale Druso 1 I-39100 Bozen“ / Bolzano, Italija </p><h2> Licencija </h2><p> Autorinės teisės © 2016-2019: Giulia Garegnani </p><p> Tarptautinė „Creative Commons Attribution 4.0“ licencija </p><p> Šis darbas yra licencijuotas pagal „Creative Commons CC BY 4.0“ tarptautinę licenciją. </p><p> SPDX licencijos identifikatorius: CC-BY-4.0 </p><p> Licencijos tekstas: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Pripažinimas </h2><p> Norėtume išreikšti savo <a href="https://www.hotmaps-project.eu">nuoširdumą</a> „Horizon 2020“ <a href="https://www.hotmaps-project.eu">karštųjų žemėlapių projektui</a> (dotacijos sutarties numeris 723677), kuris skyrė lėšų šiam tyrimui atlikti. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Solar-thermal-and-PV-potential) (original) [Bulgarian](bg-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Croatian](hr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Czech](cs-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Danish](da-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Dutch](nl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Estonian](et-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Finnish](fi-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [French](fr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [German](de-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Greek](el-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Hungarian](hu-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Irish](ga-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Italian](it-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Latvian](lv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>  [Maltese](mt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Polish](pl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Romanian](ro-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovak](sk-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovenian](sl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Spanish](es-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Swedish](sv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated