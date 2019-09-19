<h2> Turinys </h2><ul><li> <a href="#introduction">Įvadas</a> </li><li> <a href="#inputs-and-outputs">Įėjimai ir išėjimai</a> </li><li> <a href="#method">Metodas</a> </li><li> <a href="#GitHub-Repository-of-this-calculation-module">Šio skaičiavimo modulio „GitHub“ saugykla</a> </li><li> <a href="#sample-run">Mėginio paleidimas</a> <ul><li> <a href="#test-run-1-default-input-values">1 bandymo eiga: numatytosios įvesties vertės</a> </li><li> <a href="#test-run-2-modified-input-values">2 testas: modifikuotos įvesties vertės</a> </li></ul></li><li> <a href="#references">Nuorodos</a> </li><li> <a href="#how-to-cite">Kaip cituoti</a> </li><li> <a href="#authors-and-reviewers">Autoriai ir recenzentai</a> </li><li> <a href="#license">Licencija</a> </li><li> <a href="#acknowledgement">Pripažinimas</a> </li></ul><h2> Įvadas </h2><p> Šis skaičiavimo modulis naudoja <a href="https://gitlab.com/hotmaps/heat/heat_tot_curr_density">Europos šilumos tankio žemėlapį (EHDM)</a> ir <a href="https://gitlab.com/hotmaps/gfa_tot_curr_density">Europos bendrojo ploto žemėlapį (EGFAM)</a> , kurie abu buvo sukurti įgyvendinant „ <a href="https://www.hotmaps-project.eu/">Hotmaps“ projektą</a> , kad pasiūlytų GIS pagrįstą metodą, skirtą nustatyti potencialias DH sritis, kuriose pagrindinis dėmesys skiriamas. dėl centralizuoto šildymo (DH) tinklo sąnaudų. DH plotai nustatomi atliekant EHDM jautrumo analizę, atsižvelgiant į iš anksto nustatytą vidutinių paskirstymo išlaidų viršutinę ribą. Šis metodas papildomai leidžia įvertinti perdavimo linijų ilgį ir skersmenį bei su jomis susijusias išlaidas. Išvestys yra GIS sluoksniai, iliustruojantys teritorijas, kurios yra ekonomiškai perspektyvios DH statybai, taip pat sąnaudų reikalaujančios perdavimo linijos, jungiančios šiuos regionus viena su kita. Skaičiavimo modulis gali būti naudojamas norint ištirti parametrų, tokių kaip viršutinė tinklo sąnaudų riba ir rinkos dalis, įtaką potencialui ir CŠ sistemų išplėtimui. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Įėjimai ir išėjimai </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metodas </h2><p> Čia pateikiamas trumpas metodikos paaiškinimas. Išsamesnį paaiškinimą metodikos ir formulių, prašome į <a href="https://www.sciencedirect.com/science/article/pii/S1876610218304740">popieriaus</a> paskelbė apie šį skaičiavimo moduliu [ <a href="#References">1</a> ]. </p><p> Skaičiavimo modulio tikslas yra surasti regionus, kuriuose gali būti pastatyta DH sistema, neviršijant vartotojo nustatytų vidutinių konkrečių išlaidų viršutinės ribos ( <em><em>EUR / MWh)</em></em> . Tai daroma laikantis šių prielaidų: </p><ul><li> Vienintelis galimas šilumos šaltinis yra ekonominis DH rajonas, kuriame reikalingas didžiausias šilumos poreikis. Ji gamina šilumą sau ir visoms kitoms ekonomiškai suderintoms sritims. </li><li> tarp dviejų DH sričių šiluma gali tekėti viena kryptimi, </li><li> laikoma, kad metinis DH poreikis išlieka pastovus po paskutiniųjų investavimo metų </li><li> rinkos dalis arba energijos taupymas yra vienodi procentai DH zonos ląstelėse ir skirtingose DH srityse. </li></ul><p> Ekonominės DH zonos nustatomos trimis etapais. </p><p> <strong>1 ŽINGSNIS: Paskirstymo tinklo sąnaudų apskaičiavimas pagal šilumos poreikį ir sklypo santykį naudojant EHDM ir EGFAM</strong> </p><p> <strong>2 ŽINGSNIS: Galimų DH plotų nustatymas</strong> </p><p> <strong>3 ŽINGSNIS. DH zonų ir perdavimo linijos pajėgumų bei konfigūracijos, reikalingos šioms sritims sujungti tarpusavyje, nustatymas.</strong> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Šio skaičiavimo modulio „GitHub“ saugykla </h2><p> <a href="https://github.com/HotMaps/dh_economic_assessment/tree/develop">Čia</a> galite sužinoti apie šio skaičiavimo modulio pranašumą. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Mėginio paleidimas </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 1 bandymo eiga: numatytosios įvesties vertės </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 2 testas: modifikuotos įvesties vertės </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Nuorodos </h2><p> [1]. Fallahnejad M, Hartner M, Kranzl L, Fritz S. Centralizuoto šildymo sistemų paskirstymo ir perdavimo sąnaudų poveikis centralizuoto šilumos tiekimo potencialui. „Energy Procedia 2018“; 149: 141–50. doi: 10.1016 / j.egypro.2018.08.178. </p><h2> Kaip cituoti </h2><p> „Mostafa Fallahnejad“, „Hotmaps-Wiki“, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-grid-costs (2019 m. Balandžio mėn.) </p><h2> Autoriai ir recenzentai </h2><p> Šį puslapį parašė Mostafa Fallahnejad *. </p><ul><li> [] Šį puslapį peržiūrėjo Lukas Kranzl *. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Energijos ekonomikos grupė - TU Wien</a> Energetikos sistemų ir elektrinių pavarų institutas Gusshausstrasse 27-29 / 370 1040 Wien </p><h2> Licencija </h2><p> Autorinės teisės © 2016-2019: „Mostafa Fallahnejad“ </p><p> „Creative Commons“ priskyrimas 4.0 tarptautinei licencijai Šis kūrinys licencijuotas pagal „Creative Commons CC BY 4.0“ tarptautinę licenciją. </p><p> SPDX licencijos identifikatorius: CC-BY-4.0 </p><p> Licencijos tekstas: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Pripažinimas </h2><p> Norėtume išreikšti savo <a href="https://www.hotmaps-project.eu">nuoširdumą</a> „Horizon 2020“ <a href="https://www.hotmaps-project.eu">karštųjų žemėlapių projektui</a> (dotacijos sutarties numeris 723677), kuris skyrė lėšų šiam tyrimui atlikti. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-potential-economic-assessment) (original) [Bulgarian](bg-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Croatian](hr-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Czech](cs-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Danish](da-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Dutch](nl-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Estonian](et-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Finnish](fi-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [French](fr-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [German](de-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Greek](el-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Hungarian](hu-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Irish](ga-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Italian](it-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Latvian](lv-CM-District-heating-potential-economic-assessment)<sup>\*</sup>  [Maltese](mt-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Polish](pl-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Romanian](ro-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Slovak](sk-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Slovenian](sl-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Spanish](es-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Swedish](sv-CM-District-heating-potential-economic-assessment)<sup>\*</sup>
<sup>\*</sup>: machine translated