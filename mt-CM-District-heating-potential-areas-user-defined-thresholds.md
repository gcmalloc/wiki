<h2> Werrej </h2><ul><li> <a href="#introduction">Introduzzjoni</a> </li><li> <a href="#inputs-and-outputs">Inputs u outputs</a> </li><li> <a href="#method">Metodu</a> </li><li> <a href="#GitHub-Repository-of-this-calculation-module">Repożitorju GitHub ta 'dan il-modulu ta' kalkolu</a> </li><li> <a href="#sample-run">Ġirja tal-kampjun</a> <ul><li> <a href="#test-run-1-default-input-values">Ġirja tat-Test 1: valuri ta 'input default</a> </li><li> <a href="#test-run-2-modified-input-values">Ġirja tat-Test 2: valuri ta ’input modifikati</a> </li></ul></li><li> <a href="#references">Referenzi</a> </li><li> <a href="#how-to-cite">Kif tiċċita</a> </li><li> <a href="#authors-and-reviewers">Awturi u opinjonisti</a> </li><li> <a href="#license">Liċenzja</a> </li><li> <a href="#acknowledgement">Rikonoxximent</a> </li></ul><h2> Introduzzjoni </h2><p> Id-domanda għas-sħana għandha rwol importanti fid-determinazzjoni ta 'żoni potenzjali ta' tisħin distrettwali (DH). Pereżempju, l-implimentazzjoni ta 'tisħin distrettwali f'żoni li għandhom domanda ta' sħana baxxa mhix ekonomikament vijabbli. Min-naħa l-oħra, id-definizzjoni ta 'kwalunkwe żona b'densità għolja ta' domanda ta 'sħana bħala żona potenzjali ta' DH tista 'wkoll tkun mhux eżatta. Densità għolja fid-domanda tas-sħana f'żona tista 'tkun minħabba l-preżenza ta' ftit konsumaturi b'talba għolja ħafna ta 'sħana f'dik iż-żona. Għall-kuntrarju, densità baxxa ta 'domanda ta' sħana medja tista 'tkun sinjal ta' żoni li għandhom domanda ta 'sħana baxxa ħafna fiż-żona magħżula. L-għan tal-modulu potenzjali tad-DH huwa li jipprovdi bilanċ raġonevoli bejn id-densità tad-domanda tas-sħana f'żona u ż-żoni kostitwenti tagħha. </p><p> Il-modulu tal-potenzjal DH jiddetermina ż-żoni DH u l-potenzjal DH korrispondenti tagħhom ibbażat fuq id-densitajiet tad-domanda tas-sħana. Id-densitajiet tad-domanda tas-sħana jinkisbu mis-saff tal-GIS tal-input, jiġifieri l <strong><a href="https://gitlab.com/hotmaps/heat/heat_tot_curr_density">-Mappa Ewropea tad-Densità tas-Sħana (EHDM)</a></strong> , li ġiet żviluppata waqt il- <strong><a href="https://www.hotmaps-project.eu">proġett</a></strong> tal- <strong><a href="https://www.hotmaps-project.eu">Hotmaps</a></strong> . L-EHDM huwa f'format raster u għandu riżoluzzjoni ta 'ettaru u Sistema ta' Referenza tal-Koordinati (CRS) ta '" <em><em>ETRS89 / LAEA Europe - EPSG 3035</em></em> ". Iċ-ċelloli fl-EHDM juru d-densitajiet tat-tisħin <em><strong>f'MWh / ha</strong></em> . </p><p> Bħala produzzjoni, saff wieħed ta 'SIG, tliet indikaturi u żewġ dijagrammi huma ppreżentati. Dawn il-prodotti huma spjegati fid-dettall fit-taqsima tal- <a href="#sample-run">Eżekuzzjoni tal-Kampjun</a> . Is-saff tal-produzzjoni juri ż-żoni potenzjali tad-DH. Billi tikklikkja fuq kull żona fuq il-mappa, tieqa titfaċċa u l-potenzjal tad-DH li jikkorrispondi għal dik iż-żona jintwera. Fit-tieqa tal-indikatur / graff, huma indikati indikaturi u tabelli rilevanti dwar il-potenzjal tad-DH fiż-żona magħżula u l-potenzjal fis-sub-żoni. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Inputs u outputs </h2><p> Il-parametri u s-saffi tal-input kif ukoll is-saffi u l-parametri tal-ħruġ huma kif ġej. </p><p> <strong>Saffi u parametri ta 'dħul huma:</strong> </p><ul><li> Mappa tad-densità tas-sħana (awtomatikament hija pprovduta mill-kaxxa tal-għodda) <ul><li> f'format raster (* .tif) </li><li> b'riżoluzzjoni ta '1 ettaru </li><li> densitajiet tad-domanda <em><strong>f'MWh / ha</strong></em> </li></ul></li><li> Id-domanda minima tas-sħana f'kull ettaru [ <em><strong>MWh / ha</strong></em> ]: valur bejn <em><em>0</em></em> u <em><em>1000</em></em> </li><li> Id-domanda minima tas-sħana f'żona DH [ <em><strong>GWh / sena</strong></em> ]: valur bejn <em><em>0</em></em> u <em><em>500</em></em> </li></ul><p> <strong>Saffi u parametri tal-ħruġ huma:</strong> </p><ul><li> Żoni DH </li><li> Potenzjal DH f'kull żona DH </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Metodu </h2><p> Il-potenzjal għal DH f'reġjun speċifiku jista 'jiġi definit mid-domanda ġenerali tas-sħana u l-allokazzjoni spazjali tagħha. Fil-kaxxa tal-għodda tal-Hotmaps, id-domanda għat-tisħin tidher fl-EHDM fil-forma ta 'mappa raster. Kwalunkwe għażla jew qatgħa mill-EHDM tikkostitwixxi minn ċellula ta 'ettaru wieħed jew aktar. Sabiex jiġu definiti sew iż-żoni potenzjali tad-DH, kemm id-domanda tas-sħana f'kull ċellola kif ukoll f'żona għandha tilħaq ċertu livell. Għall-punt tat-tluq, il-kaxxa tal-għodda tal-Hotmaps tissuġġerixxi valuri awtomatiċi għal dawn iż-żewġ parametri. Madankollu, skont id-distribuzzjoni tad-domanda tas-sħana u wkoll il-konsiderazzjoni lokali, l-utent tal-Hotmaps jista 'jimmodifika dawn il-valuri. </p><p> Id-determinazzjoni taż-żoni tad-DH issir f'żewġ stadji: </p><p> Fl-ewwel pass, iċ-ċelloli kollha bit-talba għat-tisħin taħt il-parametru tal-input għad-domanda minima ta 'tisħin f'ektaru huma ffiltrati. Billi telimina dawn iċ-ċelloli mill-mappa, aħna nibdew gruppi ta 'ċelloli li huma mwaħħlin ma' xulxin. Kull sett ta 'dawn iċ-ċelloli mehmuża jikkostitwixxu żoni żgħar li hawn, huma msejħa bħala "żoni koerenti". Fit-tieni stadji, id-domanda tas-sħana totali f'kull qasam koerenti hija kkalkulata. Għal kull żona koerenti, jekk id-domanda għas-sħana totali hija ogħla mill-parametru tal-input għall- "talba tas-sħana minima f'żona DH", allura, tkun ikkunsidrata bħala żona DH potenzjali. </p><p> Fl-aħħarnett, għaż-żoni DH, il-potenzjal huwa kkalkulat u ppreżentat f'forma ta 'saff GIS, li jista' jidher fil-kaxxa tal-għodda. </p><p> Dan il-kodiċi juża l-kunċett ta 'komponenti konnessi mil-librerija tal-ipproċessar tal-immaġini ta' Scipy sabiex jidentifika ż-żoni potenzjali ta 'tisħin distrettwali. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Repożitorju GitHub ta 'dan il-modulu ta' kalkolu </h2><p> <a href="https://github.com/HotMaps/dh_potential/tree/develop">Hawnhekk</a> ikollok l-iżvilupp ta 'l-iktar fsada għal dan il-modulu ta' kalkolu. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Ġirja tal-kampjun </h2><p> Hawnhekk, il-modulu tal-kalkolu huwa mmexxi għall-istudju tal-każ ta 'Aalborg fid-Danimarka. </p><ul><li> L-ewwel, uża l-bar "Go To Place" biex tinnaviga lejn Aalborg u agħżel il-belt. </li></ul><p><img alt="Fig. 1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/1.png" title="Innaviga lejn post"/></p><ul><li> Segwi l-passi kif muri fil-figura hawn taħt: <ul><li> Ikklikkja fuq il-buttuna "Saffi" biex tiftaħ it-tieqa "Saffi": </li><li> Ikklikkja fuq it-tab "MODULU TA 'KALKOLAZZJONI". </li><li> Ikklikkja fuq il-buttuna "POTENZJAL TISĦAN TAD-DISTRITT". </li></ul></li></ul><p><img alt="Fig. 2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/2.png" title="Tab tal-modulu tal-kalkolu"/></p><ul><li> Issa, il- "POTENZJAL TISĦAN DISTRITT" jiftaħ u huwa lest biex jibda jaħdem. </li></ul><p><img alt="Fig. 3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/3.png" title="POTENZJAL TAS-SAĦĦA TA 'NDISTRICT"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Ġirja tat-Test 1: valuri ta 'input default </h3><p> Il-valuri tal-input default juru l-kundizzjonijiet ġenerali li fihom żona tista 'titqies bħala żona DH potenzjali. Dawn il-valuri għandhom jitqiesu bħala punt tat-tluq biss. Jista 'jkollok bżonn issettja valuri taħt jew hawn fuq valuri ta' default billi tqis konsiderazzjonijiet lokali addizzjonali. Għalhekk, l-utent għandu jadatta dawn il-valuri biex isib l-aħjar kombinazzjoni ta 'limiti għall-istudju tal-każ tiegħu jew tagħha. </p><p> Biex tmexxi l-modulu tal-kalkolu, segwi l-passi li ġejjin: </p><ul><li> Assenja isem lis-sessjoni tal-ġirja (mhux obbligatorju - hawnhekk, għażilna "Test Test 1") u waqqfu l-parametri tal-input (hawnhekk, intużaw valuri awtomatiċi). </li></ul><p><img alt="Fig. 4-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-0.png" title="Semmi s-sessjoni mmexxija"/></p><ul><li> Stenna sakemm jintemm il-proċess. </li><li> Bħala produzzjoni, indikaturi u dijagrammi huma murija fit-tieqa "RIŻULTATI". L-indikaturi juru: <ul><li> it-talba totali tas-sħana fi <em><em>GWh</em></em> fiż-żona magħżula, </li><li> potenzjal totali tad-DH <em><em>f'GWh</em></em> fiż-żona magħżula, </li><li> is-sehem tal-potenzjal tad-DH mid-domanda totali, li tinkiseb permezz tad-diviżjoni tal-potenzjal tad-DH skont id-domanda totali tas-sħana fir-reġjun. </li></ul></li></ul><p><img alt="Fig. 4-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-1.png" title="Tab INDIKATURI"/></p><p> Barra minn hekk, żewġ dijagrammi huma ġġenerati wkoll. L-ewwel wieħed juri l-potenzjal tad-DH f'kull żona DH. It-tikketti korrispondenti jinsabu wkoll fuq il-mappa. It-tieni dijagramma turi l-potenzjal totali tad-DH bi tqabbil mad-domanda totali tas-sħana fiż-żona magħżula. </p><p><img alt="Fig. 4-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-2.png" title="Tab GRAFIKA"/></p><ul><li> Saff ġdid jiżdied ukoll mal-kanvas li turi żoni DH. Dan is-saff huwa miżjud mal-lista tas-saffi fil-kategorija "Modulu tal-Kalkolu". L-isem tas-sessjoni tal-ġirja jiddistingwi l-output ta 'din il-ġirja minn dawk oħrajn. </li></ul><p><img alt="Fig. 4-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/4-3.png" title="Saffi tal-moduli ta 'kalkolu"/></p><p> Wara dawn il-passi, ikollok impressjoni dwar il-valuri tal-input u ż-żoni potenzjali tad-DH. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Ġirja tat-Test 2: valuri ta ’input modifikati </h3><p> Jiddependi fuq l-esperjenza u l-għarfien lokali tiegħek, tista 'żżid jew tnaqqas il-valuri tal-input biex tikseb riżultati aħjar. Fil-każ ta 'Aalborg, pereżempju, tista' tkun taf li d-domanda tas-sħana f'żoni ta 'barra tal-belt hija relattivament viċin il-parti ċentrali tal-belt u s-sistema DH hija fattibbli wkoll f'dawk iż-żoni. Għalhekk, tista 'tiddeċiedi li tnaqqas id-domanda minima tas-sħana f'ċelloli li huma parti minn żona DH; madankollu, biex tiggarantixxi domanda tas-sħana biżżejjed, tista 'żżid id-domanda minima tas-sħana f'żona DH. Hawn terġa 'tmexxi l-moduli ta' kalkolu b'parametri ta 'input ġodda. </p><ul><li> Assenja isem lis-sessjoni tal-ġirja (mhux obbligatorju - hawn, għażilna "Test Run 2") u stabbilixxew il-parametri tal-input ( <em><em>250 MWh / ha</em></em> għal domanda minima tas-sħana f'ektar u <em><em>35 GWh / sena</em></em> għad-domanda minima fiż-żona DH) . </li></ul><p><img alt="Fig. 5-0" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-0.png" title="Semmi s-sessjoni mmexxija"/></p><ul><li> Stenna sakemm jintemm il-proċess. </li><li> Bħala produzzjoni, indikaturi u dijagrammi huma murija fit-tieqa "RIŻULTATI". L-indikaturi juru: <ul><li> it-talba totali tas-sħana fi <em><em>GWh</em></em> fiż-żona magħżula, </li><li> potenzjal totali tad-DH <em><em>f'GWh</em></em> fiż-żona magħżula, </li><li> is-sehem tal-potenzjal tad-DH mid-domanda totali, li tinkiseb permezz tad-diviżjoni tal-potenzjal tad-DH skont id-domanda totali tas-sħana fir-reġjun. </li></ul></li></ul><p><img alt="Fig. 5-1" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-1.png" title="Tab INDIKATURI"/></p><p> Barra minn hekk, żewġ dijagrammi huma ġġenerati wkoll. L-ewwel wieħed juri l-potenzjal tad-DH f'kull żona DH. It-tikketti korrispondenti jinsabu wkoll fuq il-mappa. It-tieni dijagramma turi l-potenzjal totali tad-DH bi tqabbil mad-domanda totali tas-sħana fiż-żona magħżula. </p><p><img alt="Fig. 5-2" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-2.png" title="Tab GRAFIKA"/></p><ul><li> Saff ġdid jiżdied ukoll mal-kanvas li turi żoni DH. Dan is-saff huwa miżjud mal-lista tas-saffi fil-kategorija "Modulu tal-Kalkolu". L-isem tas-sessjoni mmexxija jiddistingwi l-output ta 'din il-ġirja minn dawk oħrajn. </li></ul><p><img alt="Fig. 5-3" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_dh_potential/5-3.png" title="Saffi tal-moduli ta 'kalkolu"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Referenzi </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Kif tiċċita </h2><p> Mostafa Fallahnejad, fil-Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-potentials (April 2019) </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Awturi u opinjonisti </h2><p> Din il-paġna hija miktuba minn Mostafa Fallahnejad *. </p><ul><li> [] Din il-paġna ġiet riveduta minn Lukas Kranzl *. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Grupp tal-Ekonomija tal-Enerġija - TU Wien</a> </p><p> Istitut ta ’Sistemi ta’ Enerġija u Sewqan Elettriku </p><p> Gusshausstrasse 27-29 / 370 </p><p> 1040 Wien </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Liċenzja </h2><p> Copyright © 2016-2019: Mostafa Fallahnejad </p><p> Creative Commons Attribuzzjoni 4.0 Liċenzja Internazzjonali </p><p> Dan ix-xogħol huwa liċenzjat taħt Liċenzja Internazzjonali ta ’Creative Commons CC BY 4.0. </p><p> SPDX-Identifikatur tal-Liċenzja: CC-BY-4.0 </p><p> It-Test tal-Liċenzja: https://spdx.org/licenses/CC-BY-4.0.html </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Rikonoxximent </h2><p> Aħna nixtiequ nwasslu l-aktar profond apprezzament tagħna għall- <a href="https://www.hotmaps-project.eu">Proġett Hotmaps ta '</a> Orizzont 2020 (Ftehim ta' Għotja numru 723677), li pprovda l-finanzjament biex titwettaq l-investigazzjoni preżenti. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-potential-areas-user-defined-thresholds) (original) [Bulgarian](bg-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Croatian](hr-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Czech](cs-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Danish](da-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Dutch](nl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Estonian](et-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Finnish](fi-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [French](fr-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [German](de-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Greek](el-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Hungarian](hu-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Irish](ga-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Italian](it-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Latvian](lv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Lithuanian](lt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>  [Polish](pl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Romanian](ro-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovak](sk-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Slovenian](sl-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Spanish](es-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup> [Swedish](sv-CM-District-heating-potential-areas-user-defined-thresholds)<sup>\*</sup>
<sup>\*</sup>: machine translated