<h2> Inhoudsopgave </h2><ul><li> <a href="#introduction">Invoering</a> </li><li> <a href="#inputs-and-outputs">Ingangen en uitgangen</a> </li><li> <a href="#method">Methode</a> </li><li> <a href="#GitHub-Repository-of-this-calculation-module">GitHub-repository van deze berekeningsmodule</a> </li><li> <a href="#sample-run">Voorbeeldrun</a> <ul><li> <a href="#test-run-1-default-input-values">Testrun 1: standaard invoerwaarden</a> </li><li> <a href="#test-run-2-modified-input-values">Testrun 2: gewijzigde invoerwaarden</a> </li></ul></li><li> <a href="#references">Referenties</a> </li><li> <a href="#how-to-cite">Hoe te citeren</a> </li><li> <a href="#authors-and-reviewers">Auteurs en recensenten</a> </li><li> <a href="#license">Licentie</a> </li><li> <a href="#acknowledgement">Erkenning</a> </li></ul><h2> Invoering </h2><p> De warmtevraag speelt een belangrijke rol bij het bepalen van potentiële stadsverwarming (DH) gebieden. De implementatie van stadsverwarming in gebieden met een lage warmtevraag is bijvoorbeeld niet economisch haalbaar. Anderzijds kan het definiëren van elk gebied met een hoge warmtevraagdichtheid als potentieel DH-gebied ook onnauwkeurig zijn. Een hoge warmtevraagdichtheid in een gebied kan te wijten zijn aan de aanwezigheid van enkele consumenten met een zeer hoge warmtevraag in dat gebied. Integendeel, een lage gemiddelde warmtevraagdichtheid kan een teken zijn van zones met een zeer lage warmtevraag in het geselecteerde gebied. Het doel van de DH-potentiaalmodule is om een redelijk evenwicht te bieden tussen de warmtevraagdichtheid in een gebied en de samenstellende zones. </p><p> De DH-potentiaalmodule bepaalt de DH-gebieden en hun bijbehorende DH-potentieel op basis van de warmtevraagdichtheden. De warmtevraagdichtheden worden verkregen uit de input GIS-laag, namelijk <strong><a href="https://gitlab.com/hotmaps/heat/heat_tot_curr_density">European Heat Density Map (EHDM)</a></strong> , die werd ontwikkeld in de loop van het <strong><a href="https://www.hotmaps-project.eu">Hotmaps-project</a></strong> . De EHDM is in rasterformaat en heeft een resolutie van één hectare en Coordinate Reference System (CRS) van " <em><em>ETRS89 / LAEA Europe - EPSG 3035</em></em> ". De cellen in EHDM tonen de verwarmingsdichtheden in <em><strong>MWh / ha</strong></em> . </p><p> Als output worden één GIS-laag, drie indicatoren en twee diagrammen gepresenteerd. Deze uitgangen worden gedetailleerd uitgelegd in het gedeelte <a href="#sample-run">Voorbeeldrun</a> . De outputlaag toont de potentiële DH-gebieden. Door op elk gebied op de kaart te klikken, verschijnt er een venster en wordt het DH-potentieel dat overeenkomt met dat gebied getoond. Binnen het indicator- / grafiekvenster worden relevante indicatoren en grafieken met betrekking tot DH-potentieel binnen de geselecteerde zone en potentialen in subzones geïllustreerd. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Ingangen en uitgangen </h2><p> De invoerparameters en -lagen evenals uitvoerlagen en parameters zijn als volgt. </p><p> <strong>Invoerlagen en parameters zijn:</strong> </p><ul><li> Hittedichtheidskaart (wordt standaard geleverd door de toolbox) <ul><li> in rasterformaat (* .tif) </li><li> met een resolutie van 1 hectare </li><li> vraagdichtheden in <em><strong>MWh / ha</strong></em> </li></ul></li><li> Minimale warmtevraag per hectare [ <em><strong>MWh / ha</strong></em> ]: een waarde tussen <em><em>0</em></em> en <em><em>1000</em></em> </li><li> Minimale warmtevraag in een DH-gebied [ <em><strong>GWh / jaar</strong></em> ]: een waarde tussen <em><em>0</em></em> en <em><em>500</em></em> </li></ul><p> <strong>Uitvoerlagen en parameters zijn:</strong> </p><ul><li> DH-gebieden </li><li> DH-potentieel in elk DH-gebied </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Methode </h2><p> Het potentieel voor DH in een specifieke regio kan worden bepaald door de totale warmtevraag en de ruimtelijke toewijzing. In de Hotmaps-toolbox wordt de warmtevraag in EHDM weergegeven in de vorm van een rasterkaart. Elke selectie of gesneden uit EHDM bestaat uit een of meer cellen van één hectare. Om potentiële DH-gebieden goed te definiëren, moet zowel de warmtevraag in elke cel als ook in een gebied een bepaald niveau bereiken. Om te beginnen stelt de Hotmaps-toolbox standaardwaarden voor deze twee parameters voor. Afhankelijk van de verdeling van de warmtevraag en ook de lokale overweging, kan de Hotmaps-gebruiker deze waarden wijzigen. </p><p> De bepaling van DH-gebieden gebeurt in twee stappen: </p><p> In de eerste stap worden alle cellen met een warmtevraag onder de invoerparameter voor de minimale warmtevraag in hectare gefilterd. Door deze cellen van de kaart te verwijderen, verkrijgen we groepen cellen die aan elkaar zijn gekoppeld. Elke set van deze verbonden cellen vormt kleine zones die hier worden aangeduid als "coherente gebieden". In de tweede stappen wordt de totale warmtevraag in elk coherent gebied berekend. Als de totale warmtevraag voor elk coherent gebied hoger is dan de invoerparameter voor de "minimale warmtevraag in een DH-gebied", wordt deze beschouwd als potentieel DH-gebied. </p><p> Ten slotte wordt voor de DH-gebieden het potentieel berekend en gepresenteerd in de vorm van een GIS-laag, die te zien is in de toolbox. </p><p> Deze code gebruikt het concept van verbonden componenten uit de beeldverwerkingsbibliotheek van Scipy om de potentiële stadsverwarmingsgebieden te detecteren. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> GitHub-repository van deze berekeningsmodule </h2><p> <a href="https://github.com/HotMaps/dh_potential/tree/develop">Hier</a> krijg je de allernieuwste ontwikkeling voor deze berekeningsmodule. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Voorbeeldrun </h2><p> Hier wordt de berekeningsmodule uitgevoerd voor de case study van Aalborg in Denemarken. </p><ul><li> Gebruik eerst de balk "Ga naar plaats" om naar Aalborg te navigeren en selecteer de stad. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/1.png" title="Navigeer naar een locatie"/></p><ul><li> Volg de stappen zoals weergegeven in de onderstaande afbeelding: <ul><li> Klik op de knop "Lagen" om het venster "Lagen" te openen: </li><li> Klik op het tabblad "BEREKENINGSMODULE". </li><li> Klik op de knop "VERWARMINGSPOTENTIEEL". </li></ul></li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/2.png" title="Tabblad berekeningsmodule"/></p><ul><li> Nu wordt het "DISTRICT HEATING POTENTIAL" geopend en is het klaar voor gebruik. </li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/3.png" title="NDISTRICT VERWARMING POTENTIEEL"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testrun 1: standaard invoerwaarden </h3><p> De standaard invoerwaarden tonen de algemene omstandigheden waaronder een gebied kan worden beschouwd als een potentieel DH-gebied. Deze waarden moeten alleen als startpunt worden beschouwd. Mogelijk moet u waarden hieronder of boven standaardwaarden instellen, rekening houdend met aanvullende lokale overwegingen. Daarom moet de gebruiker deze waarden aanpassen om de beste combinatie van drempels voor zijn of haar case study te vinden. </p><p> Volg de volgende stappen om de berekeningsmodule uit te voeren: </p><ul><li> Wijs een naam toe aan de run-sessie (optioneel - hier hebben we "Test Run 1" gekozen) en de invoerparameters ingesteld (hier werden standaardwaarden gebruikt). </li></ul><p><img alt="Fig. 4-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-0.png" title="Geef de run-sessie een naam"/></p><ul><li> Wacht tot het proces is voltooid. </li><li> Als output worden indicatoren en diagrammen getoond in het venster "RESULTATEN". De indicatoren tonen: <ul><li> de totale warmtevraag in <em><em>GWh</em></em> binnen de geselecteerde zone, </li><li> totaal DH-potentieel in <em><em>GWh</em></em> binnen de geselecteerde zone, </li><li> het aandeel van het DH-potentieel van de totale vraag, dat wordt verkregen door het DH-potentieel te delen door de totale warmtevraag in de regio. </li></ul></li></ul><p><img alt="Fig. 4-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-1.png" title="INDICATOREN tabblad"/></p><p> Bovendien worden ook twee diagrammen gegenereerd. De eerste toont het DH-potentieel in elk DH-gebied. De bijbehorende labels zijn ook op de kaart te vinden. Het tweede diagram illustreert het totale DH-potentieel in vergelijking met de totale warmtevraag in het geselecteerde gebied. </p><p><img alt="Fig. 4-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-2.png" title="GRAFIEK tab"/></p><ul><li> Er wordt ook een nieuwe laag toegevoegd aan het canvas met DH-gebieden. Deze laag wordt toegevoegd aan de lijst met lagen onder de categorie "Berekeningsmodule". De naam van de run-sessie onderscheidt de uitvoer van deze run van andere. </li></ul><p><img alt="Fig. 4-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-3.png" title="Berekening module lagen"/></p><p> Volg deze stappen om een indruk te krijgen van de invoerwaarden en mogelijke DH-gebieden. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testrun 2: gewijzigde invoerwaarden </h3><p> Afhankelijk van uw ervaring en lokale kennis, kunt u de invoerwaarden verhogen of verlagen om betere resultaten te verkrijgen. In het geval van Aalborg, bijvoorbeeld, weet u misschien dat de warmtevraag in buitenstedelijke gebieden relatief dicht bij het centrale deel van de stad ligt en dat DH-systeem ook in die gebieden haalbaar is. Daarom kunt u besluiten om de minimale warmtevraag te verminderen in cellen die deel uitmaken van een DH-gebied; om echter voldoende warmtevraag te garanderen, kunt u de minimale warmtevraag in een DH-zone verhogen. Hier voert u de berekeningsmodules opnieuw uit met nieuwe invoerparameters. </p><ul><li> Wijs een naam toe aan de run-sessie (optioneel - hier hebben we "Testrun 2" gekozen) en de invoerparameters ingesteld ( <em><em>250 MWh / ha</em></em> voor min. Warmtevraag in hectare en <em><em>35 GWh / jaar</em></em> voor de minimale vraag in DH-gebied) . </li></ul><p><img alt="Fig. 5-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-0.png" title="Geef de run-sessie een naam"/></p><ul><li> Wacht tot het proces is voltooid. </li><li> Als output worden indicatoren en diagrammen getoond in het venster "RESULTATEN". De indicatoren tonen: <ul><li> de totale warmtevraag in <em><em>GWh</em></em> binnen de geselecteerde zone, </li><li> totaal DH-potentieel in <em><em>GWh</em></em> binnen de geselecteerde zone, </li><li> het aandeel van het DH-potentieel van de totale vraag, dat wordt verkregen door het DH-potentieel te delen door de totale warmtevraag in de regio. </li></ul></li></ul><p><img alt="Fig. 5-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-1.png" title="INDICATOREN tabblad"/></p><p> Bovendien worden ook twee diagrammen gegenereerd. De eerste toont het DH-potentieel in elk DH-gebied. De bijbehorende labels zijn ook op de kaart te vinden. Het tweede diagram illustreert het totale DH-potentieel in vergelijking met de totale warmtevraag in het geselecteerde gebied. </p><p><img alt="Fig. 5-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-2.png" title="GRAFIEK tab"/></p><ul><li> Er wordt ook een nieuwe laag toegevoegd aan het canvas met DH-gebieden. Deze laag wordt toegevoegd aan de lijst met lagen onder de categorie "Berekeningsmodule". De naam van de run-sessie onderscheidt de uitvoer van deze run van andere. </li></ul><p><img alt="Fig. 5-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-3.png" title="Berekening module lagen"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Referenties </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Hoe te citeren </h2><p> Mostafa Fallahnejad, in Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-potentials (april 2019) </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Auteurs en recensenten </h2><p> Deze pagina is geschreven door Mostafa Fallahnejad *. </p><ul><li> [] Deze pagina is beoordeeld door Lukas Kranzl *. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Energy Economics Group - TU Wien</a> </p><p> Instituut voor energiesystemen en elektrische aandrijvingen </p><p> Gusshausstrasse 27-29 / 370 </p><p> 1040 Wien </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Licentie </h2><p> Copyright © 2016-2019: Mostafa Fallahnejad </p><p> Creative Commons Naamsvermelding 4.0 Internationale licentie </p><p> Dit werk is in licentie gegeven onder een Creative Commons CC BY 4.0 International License. </p><p> SPDX-licentie-ID: CC-BY-4.0 </p><p> Licentietekst: https://spdx.org/licenses/CC-BY-4.0.html </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Erkenning </h2><p> We willen onze diepe waardering overbrengen aan het Horizon 2020 <a href="https://www.hotmaps-project.eu">Hotmaps-project</a> (subsidieovereenkomst nummer 723677), dat de financiering heeft verstrekt voor het uitvoeren van dit onderzoek. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-potential-areas-user-defined-thresholds) (original) [Bulgarian](bg-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Croatian](hr-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Czech](cs-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Danish](da-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>  [Estonian](et-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Finnish](fi-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [French](fr-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [German](de-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Greek](el-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Hungarian](hu-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Irish](ga-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Italian](it-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Latvian](lv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Lithuanian](lt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Maltese](mt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Polish](pl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Romanian](ro-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovak](sk-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovenian](sl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Spanish](es-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Swedish](sv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>
<sup>\*</sup>: machine translated