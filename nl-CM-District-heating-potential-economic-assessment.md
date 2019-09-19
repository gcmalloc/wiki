<h2> Inhoudsopgave </h2><ul><li> <a href="#introduction">Invoering</a> </li><li> <a href="#inputs-and-outputs">Ingangen en uitgangen</a> </li><li> <a href="#method">Methode</a> </li><li> <a href="#GitHub-Repository-of-this-calculation-module">GitHub-repository van deze berekeningsmodule</a> </li><li> <a href="#sample-run">Voorbeeldrun</a> <ul><li> <a href="#test-run-1-default-input-values">Testrun 1: standaard invoerwaarden</a> </li><li> <a href="#test-run-2-modified-input-values">Testrun 2: gewijzigde invoerwaarden</a> </li></ul></li><li> <a href="#references">Referenties</a> </li><li> <a href="#how-to-cite">Hoe te citeren</a> </li><li> <a href="#authors-and-reviewers">Auteurs en recensenten</a> </li><li> <a href="#license">Licentie</a> </li><li> <a href="#acknowledgement">Erkenning</a> </li></ul><h2> Invoering </h2><p> Deze berekeningsmodule gebruikt de <a href="https://gitlab.com/hotmaps/heat/heat_tot_curr_density">Europese warmtedichtheidskaart (EHDM)</a> en een <a href="https://gitlab.com/hotmaps/gfa_tot_curr_density">Europese bruto vloeroppervlaktekaart (EGFAM)</a> , die beide werden ontwikkeld in de loop van het <a href="https://www.hotmaps-project.eu/">Hotmaps-project</a> , om een op GIS gebaseerde methode voor te stellen voor het bepalen van potentiële DH-gebieden met specifieke focus op de kosten van stadsverwarming (DH). De DH-gebieden worden bepaald door gevoeligheidsanalyses op de EHDM uit te voeren met inachtneming van een vooraf bepaalde bovengrens van de gemiddelde distributiekosten. De aanpak maakt het bovendien mogelijk om de lengte en diameter van transmissielijnen en de bijbehorende kosten te schatten. De uitgangen zijn GIS-lagen die gebieden illustreren die economisch levensvatbaar zijn voor de constructie van DH, evenals de kostenminimum transmissielijnen die deze gebieden met elkaar verbinden. De berekeningsmodule kan worden gebruikt om de impact van parameters zoals het plafond van de netkosten en het marktaandeel op het potentieel en op uitbreiding en uitbreiding van de DH-systemen te bestuderen. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Ingangen en uitgangen </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Methode </h2><p> Hier wordt een korte uitleg van de methodologie gegeven. Voor een meer volledige uitleg van de methodologie en formuleringen, gelieve de <a href="https://www.sciencedirect.com/science/article/pii/S1876610218304740">paper te raadplegen die</a> is gepubliceerd over deze berekeningsmodule [ <a href="#References">1</a> ]. </p><p> Het doel van de berekeningsmodule is om regio's te vinden waarin het DH-systeem kan worden gebouwd zonder een door de gebruiker gedefinieerd gemiddeld specifiek kostenplafond in <em><em>EUR / MWh</em></em> te overschrijden. Dit gebeurt onder de volgende veronderstellingen: </p><ul><li> Het economische DH-gebied met de grootste warmtevraag wordt beschouwd als de enige beschikbare warmtebron. Het produceert de warmte voor zichzelf en alle andere economische coherente gebieden. </li><li> tussen twee DH-gebieden kan warmte in één richting stromen, </li><li> de jaarlijkse DH-vraag wordt geacht constant te blijven na het laatste jaar van de investeringsperiode </li><li> marktaandeel of energiebesparing heeft dezelfde percentages binnen cellen van een DH-gebied en ook binnen verschillende DH-gebieden. </li></ul><p> De bepaling van economische DH-gebieden gebeurt in drie stappen. </p><p> <strong>STAP 1: Berekening van distributiekosten op basis van warmtevraag en plotverhouding met behulp van EHDM en EGFAM</strong> </p><p> <strong>STAP 2: Bepaling van potentiële DH-gebieden</strong> </p><p> <strong>STAP 3: Bepaling van economische DH-gebieden en transmissielijncapaciteiten en configuratie vereist om deze gebieden met elkaar te verbinden.</strong> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> GitHub-repository van deze berekeningsmodule </h2><p> <a href="https://github.com/HotMaps/dh_economic_assessment/tree/develop">Hier</a> krijg je de allernieuwste ontwikkeling voor deze berekeningsmodule. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Voorbeeldrun </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testrun 1: standaard invoerwaarden </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testrun 2: gewijzigde invoerwaarden </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Referenties </h2><p> [1]. Fallahnejad M, Hartner M, Kranzl L, Fritz S. Impact van investerings- en distributie-investeringskosten van stadsverwarmingssystemen op het potentieel voor stadsverwarming. Energy Procedia 2018; 149: 141–50. doi: 10.1016 / j.egypro.2018.08.178. </p><h2> Hoe te citeren </h2><p> Mostafa Fallahnejad, in Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-grid-costs (april 2019) </p><h2> Auteurs en recensenten </h2><p> Deze pagina is geschreven door Mostafa Fallahnejad *. </p><ul><li> [] Deze pagina is beoordeeld door Lukas Kranzl *. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Energy Economics Group - TU Wien</a> Institute of Energy Systems and Electrical Drives Gusshausstrasse 27-29 / 370 1040 Wien </p><h2> Licentie </h2><p> Copyright © 2016-2019: Mostafa Fallahnejad </p><p> Creative Commons Attribution 4.0 International License Dit werk is in licentie gegeven onder een Creative Commons CC BY 4.0 International License. </p><p> SPDX-licentie-ID: CC-BY-4.0 </p><p> Licentietekst: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Erkenning </h2><p> We willen onze diepe waardering overbrengen aan het Horizon 2020 <a href="https://www.hotmaps-project.eu">Hotmaps-project</a> (subsidieovereenkomst nummer 723677), dat de financiering heeft verstrekt voor het uitvoeren van dit onderzoek. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-potential-economic-assessment) (original) [Bulgarian](bg-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Croatian](hr-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Czech](cs-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Danish](da-CM-District-heating-potential-economic-assessment)<sup>\*</sup>  [Estonian](et-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Finnish](fi-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [French](fr-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [German](de-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Greek](el-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Hungarian](hu-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Irish](ga-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Italian](it-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Latvian](lv-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Lithuanian](lt-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Maltese](mt-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Polish](pl-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Romanian](ro-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Slovak](sk-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Slovenian](sl-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Spanish](es-CM-District-heating-potential-economic-assessment)<sup>\*</sup> [Swedish](sv-CM-District-heating-potential-economic-assessment)<sup>\*</sup>
<sup>\*</sup>: machine translated