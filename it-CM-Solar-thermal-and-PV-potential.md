<h2> Sommario </h2><ul><li> <a href="#introduction">introduzione</a> </li><li> <a href="#inputs-and-outputs">Ingressi e uscite</a> </li><li> <a href="#method">Metodo</a> </li><li> <a href="#sample-run">Esecuzione del campione</a> <ul><li> <a href="#test-run-1-default-input-values">Esecuzione test 1: valori di input predefiniti</a> </li><li> <a href="#test-run-2-modified-input-values">Esecuzione test 2: valori di input modificati</a> </li></ul></li><li> <a href="#references">Riferimenti</a> </li><li> <a href="#how-to-cite">Come citare</a> </li><li> <a href="#authors-and-reviewers">Autori e recensori</a> </li><li> <a href="#license">Licenza</a> </li><li> <a href="#acknowledgement">Riconoscimento</a> </li></ul><h2> introduzione </h2><p> Mira a calcolare il potenziale di energia fotovoltaica e la fattibilità finanziaria di un'area selezionata considerando: </p><ul><li> l'installazione di nuovi sistemi fotovoltaici su una percentuale dell'impronta dell'edificio </li><li> la fattibilità finanziaria di nuovi impianti </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Ingressi e uscite </h2><p> I parametri e i livelli di input, nonché i livelli e i parametri di output sono i seguenti. </p><p> <strong>I livelli e i parametri di input sono:</strong> </p><ul><li> file raster: <ul><li> irraggiamento solare annuale medio [kWh m ^ {- 2}] </li><li> impronta di costruzione calcolata dal file raster di input [-] </li></ul></li><li> frazione di edifici con pannelli solari} [-] </li><li> parametri dell'impianto di riferimento: <ul><li> potenza di picco media installata per impianto [kW_p] </li><li> efficienza del sistema [-] </li><li> la radiazione solare in condizioni di prova standard pari a 1 kW m ^ {- 2} </li><li> efficienza del modulo in condizioni di prova standard [kW m ^ {- 2}] </li><li> efficace fattore di utilizzo del tetto dell'edificio </li></ul></li></ul><p> <strong>I livelli e i parametri di output sono:</strong> </p><ul><li> il costo totale della copertura dell'area selezionata con pannelli fotovoltaici [valuta] </li><li> la produzione totale annua di energia [MWh / anno] </li><li> il costo livellato dell'energia [valuta / kWh] </li><li> un file raster con i tetti più adatti per la produzione di energia fotovoltaica </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metodo </h2><p> Partendo dall'area disponibile e dal tipo di tecnologia fotovoltaica, il modulo calcola la produzione di energia fotovoltaica con i seguenti presupposti: </p><ul><li> inclinazione ottimale del sistema fotovoltaico </li><li> area dei moduli fotovoltaici pari alla percentuale dell'impronta dell'edificio scelta dall'utente </li><li> tecnologia unica selezionata per tutti i sistemi fotovoltaici installati </li><li> efficienza di sistema predefinita pari a 0,75 </li></ul><p> Queste ipotesi sono state fatte al fine di considerare una fase di pianificazione per una regione e non la progettazione di uno specifico sistema fotovoltaico. </p><p> La produzione annua di energia viene derivata considerando la distribuzione spaziale della radiazione solare annuale sull'impronta dell'edificio. La produzione di energia fotovoltaica viene calcolata per un singolo impianto rappresentativo. La potenza di picco installata più rappresentativa per un impianto fotovoltaico è un input del modulo. Di conseguenza, vengono calcolate la superficie coperta da una singola pianta e il numero totale di piante. </p><p> Infine, l'area più adatta viene calcolata considerando i tetti con maggiore produzione di energia. La produzione di energia di ciascun pixel considera di coprire solo una frazione dei tetti pari a f_roof. L'integrale della produzione di energia dell'area più adatta è uguale alla produzione totale di energia dell'area selezionata. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Prova di funzionamento 1 </h2><p> Qui, il modulo di calcolo viene eseguito per la regione Lombardia in Italia (NUTS2). </p><ul><li> Innanzitutto, seleziona Nuts2 e l'area selezionata. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_01.png" title="Seleziona una regione"/></p><ul><li><p> Seguire i passaggi come mostrato nella figura seguente: </p><ul><li> Fai clic sul pulsante "Livelli" per aprire la finestra "Livelli": </li><li> Fare clic sulla scheda "MODULO DI CALCOLO". </li><li> Fare clic sul pulsante "SOLAR PV POTENTIAL". </li></ul></li><li><p> Ora si apre il "Potenziale fotovoltaico solare" ed è pronto per essere eseguito. </p></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Esecuzione test 1: valori di input predefiniti </h3><p> I valori di input predefiniti considerano la possibilità di installare pannelli fotovoltaici montati sul tetto su edifici. Questi valori si riferiscono a un impianto di 3 kWp. Potrebbe essere necessario impostare valori inferiori o superiori ai valori predefiniti considerando ulteriori considerazioni e costi locali. Pertanto, l'utente deve adattare questi valori per trovare la migliore combinazione di soglie per il proprio caso di studio. </p><p> Per eseguire il modulo di calcolo, attenersi alla seguente procedura: </p><ul><li> Assegnare un nome alla sessione di esecuzione (facoltativo - qui, abbiamo scelto "Test Run 1") e impostare i parametri di input (qui sono stati utilizzati i valori predefiniti). </li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_02.png" title="Esecuzione di prova 1 con valori predefiniti"/></p><ul><li> Attendere il completamento del processo. </li><li> Come output, indicatori e diagrammi sono mostrati nella finestra "RISULTATI". Gli indicatori mostrano: <ul><li> Produzione totale di energia, </li><li> Totale costi di installazione, </li><li> Numero di sistemi installati, </li><li> Costo livellato dell'energia </li></ul></li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Scheda INDICATORI della corsa di prova 1"/></p><ul><li> Inoltre viene aggiunto un nuovo livello alla tela che mostra gli edifici con un potenziale energetico più elevato. Questo livello viene aggiunto all'elenco dei livelli nella categoria "Modulo di calcolo". Il nome della sessione di esecuzione distingue gli output di questa corsa dagli altri. Se si deselezionano i livelli predefiniti e si seleziona TEST RUN 1, è possibile visualizzare le aree più adatte per le installazioni di impianti fotovoltaici. </li></ul><p><img alt="Fig. 4" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_solar_PV/default_values_03.png" title="Prova di funzionamento 1 STRATO modulo di calcolo"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Esecuzione test 2: valori di input modificati </h3><p> A seconda dell'esperienza e delle conoscenze locali, è possibile aumentare o diminuire i valori di input per ottenere risultati migliori. È possibile decidere di aumentare la superficie dell'edificio adatta agli impianti fotovoltaici. </p><ul><li><p> Assegna un nome alla sessione di esecuzione (facoltativo: qui abbiamo scelto "Prova di esecuzione 2") e imposta i parametri di input Percentuale di edifici con pannelli solari pari a 50. Significa che stiamo coprendo il 50% dei tetti degli edifici disponibili. Si noti che poiché ogni pixel può rappresentare più di un edificio e non stiamo coprendo l'intero tetto con pannelli fotovoltaici, l'utente può impostare anche il fattore di utilizzo del tetto dell'edificio efficace. I valori predefiniti sono impostati su 0,15. Ciò significa che solo il 15% della superficie del tetto in un pixel è coperto da pannelli fotovoltaici. </p></li><li><p> Attendere il completamento del processo. </p></li><li><p> Come output, indicatori e diagrammi sono mostrati nella finestra "RISULTATI". Gli indicatori mostrano: </p><ul><li> Produzione totale di energia, </li><li> Totale costi di installazione, </li><li> Numero di sistemi installati, </li><li> Costo livellato dell'energia </li></ul></li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Riferimenti </h2><h2> Come citare </h2><p> Giulia Garegnani, in Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-Solar-PV-potential (aprile 2019) </p><h2> Autori e recensori </h2><p> Questa pagina è stata scritta da Giulia Garegnani *. </p><p> * <a href="http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx">Gruppo del sistema energetico urbano e regionale - EURAC Bolzano</a> </p><p> Institute of Renewable Drususallee / Viale Druso 1 I-39100 Bozen / Bolzano Italy </p><h2> Licenza </h2><p> Copyright © 2016-2019: Giulia Garegnani </p><p> Licenza internazionale Creative Commons Attribution 4.0 </p><p> Quest'opera è sotto licenza Creative Commons CC BY 4.0 International License. </p><p> Identificatore di licenza SPDX: CC-BY-4.0 </p><p> Testo della licenza: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Riconoscimento </h2><p> Vorremmo esprimere il nostro più profondo apprezzamento al <a href="https://www.hotmaps-project.eu">progetto Hotmaps di</a> Orizzonte 2020 ( <a href="https://www.hotmaps-project.eu">convenzione di</a> sovvenzione numero 723677), che ha fornito i finanziamenti per lo svolgimento della presente indagine. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Solar-thermal-and-PV-potential) (original) [Bulgarian](bg-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Croatian](hr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Czech](cs-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Danish](da-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Dutch](nl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Estonian](et-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Finnish](fi-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [French](fr-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [German](de-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Greek](el-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Hungarian](hu-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Irish](ga-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>  [Latvian](lv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Lithuanian](lt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Maltese](mt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Polish](pl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Romanian](ro-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovak](sk-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Slovenian](sl-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Spanish](es-CM-Solar-thermal-and-PV-potential)<sup>\*</sup> [Swedish](sv-CM-Solar-thermal-and-PV-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated