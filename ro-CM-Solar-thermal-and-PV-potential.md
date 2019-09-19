<h2> Cuprins </h2><ul><li> <a href="#introduction">Introducere</a> </li><li> <a href="#inputs-and-outputs">Intrări și ieșiri</a> </li><li> <a href="#method">Metodă</a> </li><li> <a href="#sample-run">Proba de rulare</a> <ul><li> <a href="#test-run-1-default-input-values">Test Run 1: valori implicite de intrare</a> </li><li> <a href="#test-run-2-modified-input-values">Test Run 2: valori de intrare modificate</a> </li></ul></li><li> <a href="#references">Referințe</a> </li><li> <a href="#how-to-cite">Cum să cităm</a> </li><li> <a href="#authors-and-reviewers">Autori și recenzori</a> </li><li> <a href="#license">Licență</a> </li><li> <a href="#acknowledgement">Confirmare</a> </li></ul><h2> Introducere </h2><p> Acesta își propune să calculeze potențialul de energie fotovoltaică și fezabilitatea financiară a unei zone selectate, luând în considerare: </p><ul><li> instalarea de noi sisteme fotovoltaice pe un procent de amprentă de construcție </li><li> fezabilitatea financiară a instalațiilor noi </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Intrări și ieșiri </h2><p> Parametrii și straturile de intrare, precum și straturile și parametrii de ieșire sunt după cum urmează. </p><p> <strong>Straturile și parametrii de intrare sunt:</strong> </p><ul><li> fișier raster: <ul><li> medie iradiere solară anuală [kWh m ^ {- 2}] </li><li> construirea amprentei calculate din fișierul raster de intrare [-] </li></ul></li><li> fracție a clădirilor cu panouri solare} [-] </li><li> parametrii instalației de referință: <ul><li> puterea medie de vârf instalată pe instalație [kW_p] </li><li> eficiența sistemului [-] </li><li> radiația solară la starea de testare standard egală cu 1 kW m ^ {- 2} </li><li> eficiența modulului în condiții de testare standard [kW m ^ {- 2}] </li><li> Factorul eficient de utilizare a acoperișului pentru clădiri </li></ul></li></ul><p> <strong>Straturile de ieșire și parametrii sunt:</strong> </p><ul><li> costul total al acoperirii zonei selectate cu panouri fotovoltaice [valută] </li><li> producția anuală totală de energie [MWh / an] </li><li> Costul nivelat al energiei [valută / kWh] </li><li> un fișier raster cu cele mai potrivite acoperișuri pentru producerea de energie fotovoltaică </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metodă </h2><p> Pornind de la zona disponibilă și tipul de tehnologie fotovoltaică, modulul calculează producția de energie fotovoltaică în conformitate cu următoarele ipoteze: </p><ul><li> înclinație optimă a sistemului fotovoltaic </li><li> aria modulelor fotovoltaice egală cu procentul amprentei clădirii ales de utilizator </li><li> tehnologie unică selectată pentru toate sistemele fotovoltaice instalate </li><li> eficiența implicită a sistemului egal cu 0,75 </li></ul><p> Aceste ipoteze au fost făcute pentru a lua în considerare o fază de planificare pentru o regiune și nu proiectarea unui sistem fotovoltaic specific. </p><p> Producția anuală de energie este obținută luând în considerare distribuția spațială a radiației solare anuale pe amprenta clădirii. Producția de energie fotovoltaică este calculată pentru o singură centrală reprezentativă. Cea mai reprezentativă putere de vârf instalată pentru un sistem fotovoltaic este o intrare a modulului. În consecință, suprafața acoperită de o singură plantă și numărul total de plante sunt calculate. </p><p> În cele din urmă, zona cea mai potrivită este calculată luând în considerare acoperișurile cu o producție de energie mai mare. Producția de energie a fiecărui pixel consideră că acoperă doar o fracțiune din acoperișuri egală cu f_roof. Integrala producției de energie a celei mai potrivite zone este egală cu producția totală de energie a zonei selectate. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Testul 1 </h2><p> Aici, modulul de calcul este rulat pentru regiunea Lombardiei din Italia (NUTS2). </p><ul><li> Mai întâi, selectați Nuts2 și zona aleasă. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_01.png" title="Selectați o regiune"/></p><ul><li><p> Urmați pașii după cum se arată în figura de mai jos: </p><ul><li> Faceți clic pe butonul "Straturi" pentru a deschide fereastra "Straturi": </li><li> Faceți clic pe fila „MODUL DE CALCULARE”. </li><li> Faceți clic pe butonul "SOLAR PV POTENȚIAL". </li></ul></li><li><p> Acum, se deschide „Solar PV Potential” și este gata să funcționeze. </p></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Test Run 1: valori implicite de intrare </h3><p> Valorile implicite de intrare au în vedere posibilitatea de a instala panouri fotovoltaice montate pe acoperiș pe clădiri. Aceste valori se referă la o instalație de 3 kWp. S-ar putea să fie necesar să setați valori mai jos sau mai mari de valori implicite, luând în considerare costuri și costuri locale suplimentare. Prin urmare, utilizatorul ar trebui să adapteze aceste valori pentru a găsi cea mai bună combinație de praguri pentru studiul său de caz. </p><p> Pentru a rula modulul de calcul, urmați următorii pași: </p><ul><li> Alocați un nume sesiunii de rulare (opțional - aici, am ales „Test Run 1”) și am stabilit parametrii de intrare (aici s-au folosit valorile implicite). </li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_02.png" title="Executați testul 1 cu valori implicite"/></p><ul><li> Așteptați până când procesul este terminat. </li><li> Ca ieșire, indicatorii și diagramele sunt afișate în fereastra „REZULTATE”. Indicatorii arată: <ul><li> Producția totală de energie, </li><li> Costuri totale de configurare, </li><li> Număr de sisteme instalate, </li><li> Costuri nivelate ale energiei </li></ul></li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Execuție test 1 fila INDICATORI"/></p><ul><li> De asemenea, un nou strat este adăugat pe pânză care prezintă clădirile cu potențial energetic mai mare. Acest strat este adăugat la lista de straturi din categoria „Modulul de calcul”. Numele sesiunii de rulare distinge rezultatele acestei rulări de alte. Dacă ați deselectat straturile implicite și selectați TEST RUN 1 puteți vizualiza cele mai potrivite zone pentru instalațiile de instalații fotovoltaice. </li></ul><p><img alt="Fig. 4" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Execuție de test 1 Modul de calcul CĂPĂRI"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Test Run 2: valori de intrare modificate </h3><p> În funcție de experiența dvs. și de cunoștințele locale, puteți crește sau micșora valorile de intrare pentru a obține rezultate mai bune. Puteți decide să măriți suprafața clădirii potrivită pentru instalațiile fotovoltaice. </p><ul><li><p> Alocați un nume sesiunii de rulare (opțional - aici, am ales „Test Run 2”) și am stabilit parametrii de intrare Procentul clădirilor cu panouri solare egal cu 50. Înseamnă că acoperim 50% din acoperișurile disponibile ale clădirii. Observați că, deoarece fiecare pixel poate reprezenta mai mult de o clădire și nu acoperim întregul acoperiș cu panouri fotovoltaice, utilizatorul poate seta și factorul eficient de utilizare a acoperișului clădirii. Valorile implicite sunt setate la 0,15. Aceasta înseamnă că doar 15% din suprafața acoperișului într-un pixel este acoperită de panouri fotovoltaice. </p></li><li><p> Așteptați până când procesul este terminat. </p></li><li><p> Ca ieșire, indicatorii și diagramele sunt afișate în fereastra „REZULTATE”. Indicatorii arată: </p><ul><li> Producția totală de energie, </li><li> Costuri totale de configurare, </li><li> Număr de sisteme instalate, </li><li> Costuri nivelate ale energiei </li></ul></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Referințe </h2><h2> Cum să cităm </h2><p> Giulia Garegnani, în Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-Solar-PV-potential (aprilie 2019) </p><h2> Autori și recenzori </h2><p> Această pagină este scrisă de Giulia Garegnani *. </p><p> * <a href="http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx">Grupul de sisteme energetice urbane și regionale - EURAC Bozen</a> </p><p> Institutul de energie regenerabilă Drususallee / Viale Druso 1 I-39100 Bozen / Bolzano Italia </p><h2> Licență </h2><p> Copyright © 2016-2019: Giulia Garegnani </p><p> Licență internațională Creative Commons Attribution 4.0 </p><p> Această lucrare este licențiată în baza unei licențe internaționale Creative Commons CC BY 4.0. </p><p> SPDX-Identificator de licență: CC-BY-4.0 </p><p> Licență-text: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Confirmare </h2><p> Am dori să transmitem aprecierile noastre cele mai profunde <a href="https://www.hotmaps-project.eu">proiectului de hărți hot-uri</a> Orizont 2020 (Acordul de finanțare nr. 723677), care a furnizat finanțarea pentru realizarea prezentei anchete. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Solar-thermal-and-PV-potential) (original) [Bulgarian](bg-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Croatian](hr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Czech](cs-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Danish](da-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Dutch](nl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Estonian](et-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Finnish](fi-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [French](fr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [German](de-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Greek](el-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Hungarian](hu-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Irish](ga-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Italian](it-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Latvian](lv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Lithuanian](lt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Maltese](mt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Polish](pl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>  [Slovak](sk-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovenian](sl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Spanish](es-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Swedish](sv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated