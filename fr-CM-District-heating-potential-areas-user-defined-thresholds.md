<h2> Table des matières </h2><ul><li> <a href="#introduction">introduction</a> </li><li> <a href="#inputs-and-outputs">Entrées et sorties</a> </li><li> <a href="#method">Méthode</a> </li><li> <a href="#GitHub-Repository-of-this-calculation-module">Dépôt GitHub de ce module de calcul</a> </li><li> <a href="#sample-run">Échantillon échantillon</a> <ul><li> <a href="#test-run-1-default-input-values">Test Run 1: valeurs d'entrée par défaut</a> </li><li> <a href="#test-run-2-modified-input-values">Essai 2: valeurs d'entrée modifiées</a> </li></ul></li><li> <a href="#references">Références</a> </li><li> <a href="#how-to-cite">Comment citer</a> </li><li> <a href="#authors-and-reviewers">Auteurs et relecteurs</a> </li><li> <a href="#license">Licence</a> </li><li> <a href="#acknowledgement">Reconnaissance</a> </li></ul><h2> introduction </h2><p> La demande de chaleur joue un rôle important dans la détermination des zones potentielles de chauffage urbain. Par exemple, la mise en œuvre du chauffage urbain dans les zones à faible demande de chaleur n’est pas économiquement viable. D'autre part, définir toute zone avec une forte densité de demande de chaleur en tant que zone DH potentielle peut également être imprécis. Une forte densité de demande de chaleur dans une zone pourrait être due à la présence de quelques consommateurs avec une demande de chaleur très élevée dans cette zone. Au contraire, une faible densité moyenne de demande de chaleur pourrait être un signe de zones avec une demande de chaleur très faible dans la zone sélectionnée. Le module de potentiel DH a pour objectif de fournir un équilibre raisonnable entre la densité de la demande de chaleur dans une zone et ses zones constitutives. </p><p> Le module de potentiel DH détermine les zones DH et leur potentiel DH correspondant en fonction de la densité de la demande de chaleur. Les densités de demande de chaleur sont obtenues à partir de la couche SIG d'entrée, à savoir <strong><a href="https://gitlab.com/hotmaps/heat/heat_tot_curr_density">la carte de densité de chaleur européenne (EHDM)</a></strong> , développée au cours du <strong><a href="https://www.hotmaps-project.eu">projet Hotmaps</a></strong> . Le modèle EHDM est au format raster et présente une résolution d'un hectare et un système de référence de référence (CRS) de " <em><em>ETRS89 / LAEA Europe - EPSG 3035</em></em> ". Les cellules dans EHDM montrent les densités de chauffage en <em><strong>MWh / ha</strong></em> . </p><p> En sortie, une couche SIG, trois indicateurs et deux diagrammes sont présentés. Ces sorties sont expliquées en détail dans la section <a href="#sample-run">Exemple d’exécution</a> . La couche de sortie montre les zones DH potentielles. En cliquant sur chaque zone de la carte, une fenêtre s’ouvre et le potentiel DH correspondant à cette zone s’affiche. Dans la fenêtre des indicateurs / graphiques, des indicateurs et des graphiques pertinents concernant le potentiel de DH dans la zone sélectionnée et les potentiels dans les sous-zones sont illustrés. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Entrées et sorties </h2><p> Les paramètres d'entrée et les couches ainsi que les couches de sortie et les paramètres sont les suivants. </p><p> <strong>Les couches et paramètres d'entrée sont:</strong> </p><ul><li> Carte de densité thermique (fournie par défaut par la boîte à outils) <ul><li> au format raster (* .tif) </li><li> avec une résolution de 1 hectare </li><li> densités de la demande en <em><strong>MWh / ha</strong></em> </li></ul></li><li> Demande calorifique minimale par hectare [ <em><strong>MWh / ha</strong></em> ]: valeur comprise entre <em><em>0</em></em> et <em><em>1000</em></em> </li><li> Demande calorifique minimale dans une zone DH [ <em><strong>GWh / an</strong></em> ]: valeur comprise entre <em><em>0</em></em> et <em><em>500</em></em> </li></ul><p> <strong>Les couches et paramètres de sortie sont:</strong> </p><ul><li> Zones DH </li><li> Potentiel DH dans chaque zone DH </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Méthode </h2><p> Le potentiel de DH dans une région spécifique peut être défini par la demande de chaleur globale et son allocation spatiale. Dans la boîte à outils Hotmaps, la demande de chauffage est affichée dans EHDM sous la forme d'une carte raster. Toute sélection ou coupe dans EHDM est constituée d'une ou plusieurs cellules d'un hectare. Afin de définir correctement les zones DH potentielles, la demande de chaleur dans chaque cellule ainsi que dans une zone doit atteindre un certain niveau. Pour point de départ, la boîte à outils Hotmaps propose des valeurs par défaut pour ces deux paramètres. Toutefois, en fonction de la répartition de la demande de chaleur et des considérations locales, l'utilisateur Hotmaps peut modifier ces valeurs. </p><p> La détermination des zones DH se fait en deux étapes: </p><p> Lors de la première étape, toutes les cellules dont la demande de chauffage est inférieure au paramètre d'entrée pour la demande de chauffage minimale en hectare sont filtrées. En éliminant ces cellules de la carte, nous obtenons des groupes de cellules attachées les unes aux autres. Chaque ensemble de ces cellules attachées constitue de petites zones qui, ici, sont appelées «zones cohérentes». Dans la deuxième étape, la demande totale de chaleur dans chaque zone cohérente est calculée. Pour chaque zone cohérente, si la demande de chaleur totale est supérieure au paramètre d'entrée pour la "demande de chaleur minimale dans une zone DH", elle est alors considérée comme une surface DH potentielle. </p><p> Enfin, pour les zones DH, le potentiel est calculé et présenté sous forme de couche SIG, visible dans la boîte à outils. </p><p> Ce code utilise le concept de composants connectés de la bibliothèque de traitement d'images de Scipy afin de détecter les zones potentielles de chauffage urbain. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Dépôt GitHub de ce module de calcul </h2><p> <a href="https://github.com/HotMaps/dh_potential/tree/develop">Ici,</a> vous obtenez le développement de pointe pour ce module de calcul. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Échantillon échantillon </h2><p> Ici, le module de calcul est exécuté pour l’étude de cas d’Aalborg au Danemark. </p><ul><li> Tout d'abord, utilisez la barre "Aller à l'endroit" pour naviguer jusqu'à Aalborg et sélectionnez la ville. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/1.png" title="Naviguer vers un lieu"/></p><ul><li> Suivez les étapes indiquées dans la figure ci-dessous: <ul><li> Cliquez sur le bouton "Couches" pour ouvrir la fenêtre "Couches": </li><li> Cliquez sur l'onglet "MODULE DE CALCUL". </li><li> Cliquez sur le bouton "POTENTIEL DE CHAUFFAGE DU DISTRICT". </li></ul></li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/2.png" title="Onglet du module de calcul"/></p><ul><li> Maintenant, le "POTENTIEL DE CHAUFFAGE DU DISTRICT" s'ouvre et est prêt à fonctionner. </li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/3.png" title="POTENTIEL DE CHAUFFAGE NDISTRICT"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Test Run 1: valeurs d'entrée par défaut </h3><p> Les valeurs d'entrée par défaut indiquent les conditions générales dans lesquelles une zone peut être considérée comme une zone DH potentielle. Ces valeurs ne doivent être considérées que comme point de départ. Vous devrez peut-être définir des valeurs ci-dessous ou supérieures aux valeurs par défaut en tenant compte de considérations locales supplémentaires. Par conséquent, l'utilisateur doit adapter ces valeurs pour trouver la meilleure combinaison de seuils pour son étude de cas. </p><p> Pour exécuter le module de calcul, suivez les étapes suivantes: </p><ul><li> Attribuez un nom à la session d'exécution (facultatif - ici, nous avons choisi "Test d'exécution 1") et définissons les paramètres d'entrée (ici, les valeurs par défaut ont été utilisées). </li></ul><p><img alt="Fig. 4-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-0.png" title="Nommez la session d'exécution"/></p><ul><li> Attendez que le processus soit terminé. </li><li> En sortie, les indicateurs et les diagrammes sont affichés dans la fenêtre "RESULTATS". Les indicateurs montrent: <ul><li> la demande totale de chaleur en <em><em>GWh</em></em> dans la zone sélectionnée, </li><li> potentiel total de DH en <em><em>GWh</em></em> dans la zone sélectionnée, </li><li> la part du potentiel DH de la demande totale, qui est obtenue par division du potentiel DH par la demande totale de chaleur dans la région. </li></ul></li></ul><p><img alt="Fig. 4-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-1.png" title="Onglet INDICATEURS"/></p><p> De plus, deux diagrammes sont également générés. La première montre le potentiel DH dans chaque zone DH. Les étiquettes correspondantes se trouvent également sur la carte. Le deuxième diagramme illustre le potentiel total de DH par rapport à la demande totale de chaleur dans la zone sélectionnée. </p><p><img alt="Fig. 4-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-2.png" title="Onglet GRAPHIQUE"/></p><ul><li> De plus, un nouveau calque est ajouté au canevas indiquant les zones DH. Cette couche est ajoutée à la liste des couches de la catégorie "Module de calcul". Le nom de session d'exécution distingue les sorties de cette exécution des autres. </li></ul><p><img alt="Fig. 4-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-3.png" title="Couches de module de calcul"/></p><p> En suivant ces étapes, vous aurez une impression sur les valeurs d’entrée et les zones DH potentielles. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Essai 2: valeurs d'entrée modifiées </h3><p> En fonction de votre expérience et de vos connaissances locales, vous pouvez augmenter ou diminuer les valeurs d'entrée pour obtenir de meilleurs résultats. Dans le cas d'Aalborg, par exemple, vous savez peut-être que la demande de chaleur dans les quartiers périphériques est relativement proche du centre-ville et que le système DH est également réalisable dans ces zones. Par conséquent, vous pouvez décider de réduire la demande de chaleur minimale dans les cellules faisant partie d'une zone DH. Cependant, pour garantir une demande de chaleur suffisante, vous pouvez augmenter la demande de chaleur minimale dans une zone de stockage DH. Ici, vous réexécutez les modules de calcul avec de nouveaux paramètres d'entrée. </p><ul><li> Attribuez un nom à la session d'analyse (facultatif - ici, nous avons choisi "Essai 2") et définissons les paramètres d'entrée ( <em><em>250 MWh / ha</em></em> pour une demande de chaleur minimale en hectare et <em><em>35 GWh / an</em></em> pour une demande minimale en zone DH). . </li></ul><p><img alt="Fig. 5-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-0.png" title="Nommez la session d'exécution"/></p><ul><li> Attendez que le processus soit terminé. </li><li> En sortie, les indicateurs et les diagrammes sont affichés dans la fenêtre "RESULTATS". Les indicateurs montrent: <ul><li> la demande totale de chaleur en <em><em>GWh</em></em> dans la zone sélectionnée, </li><li> potentiel total de DH en <em><em>GWh</em></em> dans la zone sélectionnée, </li><li> la part du potentiel DH de la demande totale, qui est obtenue par division du potentiel DH par la demande totale de chaleur dans la région. </li></ul></li></ul><p><img alt="Fig. 5-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-1.png" title="Onglet INDICATEURS"/></p><p> De plus, deux diagrammes sont également générés. La première montre le potentiel DH dans chaque zone DH. Les étiquettes correspondantes se trouvent également sur la carte. Le deuxième diagramme illustre le potentiel total de DH par rapport à la demande totale de chaleur dans la zone sélectionnée. </p><p><img alt="Fig. 5-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-2.png" title="Onglet GRAPHIQUE"/></p><ul><li> De plus, un nouveau calque est ajouté au canevas indiquant les zones DH. Cette couche est ajoutée à la liste des couches de la catégorie "Module de calcul". Le nom de session d'exécution distingue les sorties de cette exécution des autres. </li></ul><p><img alt="Fig. 5-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-3.png" title="Couches de module de calcul"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Références </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Comment citer </h2><p> Mostafa Fallahnejad, dans Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-potentials (avril 2019) </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Auteurs et relecteurs </h2><p> Cette page est écrite par Mostafa Fallahnejad *. </p><ul><li> [] Cette page a été révisée par Lukas Kranzl *. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Energy Economics Group - TU Wien</a> </p><p> Institut des systèmes énergétiques et des entraînements électriques </p><p> Gusshausstrasse 27-29 / 370 </p><p> 1040 Wien </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Licence </h2><p> Droits d'auteur © 2016-2019: Mostafa Fallahnejad </p><p> Licence internationale Creative Commons Attribution 4.0 </p><p> Ce travail est sous licence Creative Commons CC BY 4.0 International. </p><p> Identificateur de licence SPDX: CC-BY-4.0 </p><p> Licence-Text: https://spdx.org/licenses/CC-BY-4.0.html </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Reconnaissance </h2><p> Nous souhaitons exprimer notre profonde gratitude au projet Horizon 2020 <a href="https://www.hotmaps-project.eu">Hotmaps</a> (accord de subvention n ° 723677), qui a fourni le financement nécessaire à la réalisation de la présente enquête. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-potential-areas-user-defined-thresholds) (original) [Bulgarian](bg-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Croatian](hr-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Czech](cs-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Danish](da-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Dutch](nl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Estonian](et-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Finnish](fi-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>  [German](de-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Greek](el-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Hungarian](hu-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Irish](ga-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Italian](it-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Latvian](lv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Lithuanian](lt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Maltese](mt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Polish](pl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Romanian](ro-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovak](sk-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovenian](sl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Spanish](es-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Swedish](sv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>
<sup>\*</sup>: machine translated