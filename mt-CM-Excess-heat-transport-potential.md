<h2> Werrej </h2><ul><li> <a href="#introduction">Introduzzjoni</a> </li><li> <a href="#inputs-and-outputs">Inputs u outputs</a> </li><li> <a href="#method">Metodu</a> </li><li> <a href="#sample-run">Ġirja tal-kampjun</a> </li><li> <a href="#authors-and-reviewers">Awturi u opinjonisti</a> </li><li> <a href="#license">Liċenzja</a> </li><li> <a href="#acknowledgement">Rikonoxximent</a> </li></ul><h2> Introduzzjoni </h2><p> L-użu ta 'sħana żejda għat-tisħin distrettwali. </p><h2> Inputs u outputs </h2><h3> Saffi u parametri ta 'l-input </h3><h4> Provduta mill-Toolbox </h4><ul><li> Żoni ta 'tisħin distrettwali (għal issa pprovduti direttament mill-potenzjal ta' tisħin distrettwali CM) </li><li> Dejta industrijali (b’default ipprovduta mill-kaxxa tal-għodda) </li></ul><h4> Provduta mill-utent </h4><ul><li> Min. Id-domanda tas-sħana f'ettari. Ara l- <a href="https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-potential-areas-user-defined-thresholds">potenzjal tad-DH CM</a> </li><li> Min. talba tas-sħana f'żona DH. Ara l- <a href="https://github.com/HotMaps/hotmaps_wiki/wiki/CM-District-heating-potential-areas-user-defined-thresholds">potenzjal tad-DH CM</a> </li><li> Fittex raġġ f'km </li><li> Ħajja tat-tagħmir fis-snin </li><li> Rata ta 'skont f'% </li><li> Fattur tal-kost </li><li> Spejjeż operattivi f '% </li><li> Valur tal-limitu għal-linji ta ’trasmissjoni f’kt / kWh </li></ul><h4> Parametri tal-Prestazzjoni </h4><ul><li> Riżoluzzjoni ta 'ħin (siegħa, jum, ġimgħa, xahar, sena) </li><li> Riżoluzzjoni spazjali f'km </li></ul><h3> Saffi u indikaturi tal-ħruġ </h3><ul><li> Linji ta ’trasmissjoni </li><li> Sħana eċċessiva totali fiż-żona magħżula fi GWh </li><li> Sħana eċċessiva konnessa fi GWh </li><li> Sħana żejda użata fil-GWh </li><li> In-nefqa tan-netwerk f '€ </li><li> Spejjeż annwali tan-netwerk f '€ / sena </li><li> Spejjeż livellati ta 'provvista tas-sħana f'kt / kWh </li><li> Grafika li turi potenzjal tad-DH, sħana żejda totali, sħana eċċessiva konnessa u sħana eċċessiva użata </li><li> Grafika li turi domanda ta 'sħana u eċċess ta' kull xahar </li><li> Grafika li turi domanda medja ta 'sħana u eċċess ta' kuljum </li></ul><h2> Metodu </h2><h3> Ħarsa ġenerali </h3><p> L-element ewlieni tal-modulu tas-sħana eċċessiva huwa l-mudell tas-sink tas-sors użat. Huwa jibni netwerk ta 'trażmissjoni ta' tul minimu u jikkalkula l-fluss għal kull siegħa tas-sena abbażi ta 'profili ta' tagħbija residenzjali ta 'tisħin b'riżoluzzjoni Nuts2 u profili ta' tagħbija tal-industrija b'riżoluzzjoni Nuts0. Ibbażati fuq medji ta ’flussi tal-quċċata matul is-sena jistgħu jiġu kkalkulati l-ispejjeż għal kull linja ta’ trasmissjoni u skambjatur tas-sħana fuq in-naħa tas-sors u tas-sink. </p><h3> Dettalji </h3><h4> Immudellar ta 'sorsi </h4><p> Abbażi tal-ID Nuts0 u s-settur industrijali, profil ta 'tagħbija li tissolva fis-siegħa tul kull sena huwa assenjat lil kull sors. </p><h4> Immudellar tal-bjar </h4><p> Ibbażat fuq il-modulu ta 'kalkolu tal-potenzjal ta' tisħin distrettwali b'mod ekwistanti jinħolqu punti ta 'dħul fiż-żoni koerenti. Jiddependi fuq l-ID Nuts2 tal-punti tad-dħul profil huwa assenjat. </p><h4> Tiftix f'raġġ fiss </h4><p> F’raġġ ta ’sett huwa kkontrollat liema sorsi huma fil-firxa ta’ xulxin, liema sinkijiet huma fil-firxa ta ’xulxin u liema sinkijiet huma fil-firxa għas-sorsi. Dan jista 'jkun irrappreżentat minn graff b'sorsi u bjar li jiffurmaw il-vertiċi u l-vertiċi fil-medda li jkunu konnessi minn tarf. </p><h4> Tnaqqis għal netwerk ta 'tul minimu </h4><p> Siġra ta 'tifrix minimu hija kkalkulata bid-distanza tat-truf bħala piżijiet. Dan jirriżulta fi graff li jżomm il-konnettività tiegħu waqt li jkollu tul minimu minimu ta ’trufijiet. Innota li l-punti ta 'dħul ta' żoni koerenti huma konnessi internament mingħajr ħlas peress li jiffurmaw in-netwerk ta 'distribuzzjoni tagħhom stess. </p><h4> Komputazzjoni tal-fluss </h4><p> Il-fluss massimu mis-sorsi għall-bjar huwa kkalkulat għal kull siegħa tas-sena. </p><h4> Determinazzjoni tal-ispejjeż </h4><p> Il-fluss tal-quċċata medja ta 'aktar minn 3 sigħat jiddetermina l-kapaċità meħtieġa għal-linji tat-trasmissjoni u l-iskambjaturi tas-sħana. L-ispejjeż tal-linji ta 'trasmissjoni jiddependu fuq it-tul u l-kapaċità, filwaqt li l-ispejjeż tal-iskambjaturi tas-sħana huma influwenzati biss mill-kapaċità. Min-naħa tas-sors hemm skambjatur tas-sħana tal-arja għall-likwidu b'pompa integrata għal-linja tat-trasmissjoni u fuq in-naħa tas-sink huwa assunt skambjatur tas-sħana likwidu għal likwidu. </p><h4> Varjazzjoni tan-netwerk </h4><p> Billi l-ispiża u l-fluss ta 'kull linja ta' trasmissjoni huma magħrufa l-linji bl-ogħla proporzjon ta 'spiża għal fluss jistgħu jitneħħew u l-fluss jiġi kkalkulat mill-ġdid sakemm tinkiseb spiża mixtieqa għal kull fluss. </p><h3> Implimentazzjoni </h3><h4> Tiftix f'raġġ fiss </h4><p> Għall-komputazzjoni tad-distanza bejn żewġ punti tintuża angolu żgħir ta 'approssimazzjoni tat-tul loxodrome. Filwaqt li hemm ukoll implimentazzjoni eżatta tad-distanza tal-ortodromu, l-eżattezza miżjuda m'għandha l-ebda benefiċċju reali minħabba d-distanzi żgħar l-aktar baxxi minn 20km u l-inċertezza tat-tul tal-linja ta 'trasmissjoni reali minħabba ħafna fatturi bħat-topoloġija. Jekk żewġ punti jinsabu fil-medda tar-raġġ, hija maħżuna fil-lista ta 'l-adeġenza. Il-ħolqien ta 'listi ta' dawk l-adeġenza jsir bejn sorsi u sorsi, bjar u bjar, u sorsi u bjar. Ir-raġuni għas-separazzjoni tinsab fil-flessibilità biex jiżdiedu ċerti rekwiżiti tat-temperatura għal sorsi jew bjar. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/search.svg"/><figcaption> <i><br/> Eżempju ta 'tfittxija f'raġġ fiss. Il-vertiċi ħomor jirrappreżentaw is-sorsi u l-bjar blu. In-numri jirrappreżentaw id-distanza bejn il-punti. It-tpinġija mhix fuq skala kbira.</i> </figcaption></figure><h4> Klassi NetworkGraph </h4><p> Ibbażat fuq il-librerija igraph, klassi NetworkGraph hija implimentata bil-funzjonalità kollha meħtieġa għall-modulu ta 'kalkolu. Filwaqt li l-igraph huwa dokumentat ħażin, joffri prestazzjoni ferm aħjar minn moduli python puri bħal NetworkX u appoġġ ta 'pjattaforma usa' lil hinn minn Linux b'differenza graff-tool. Il-klassi NetworkGraph tiddeskrivi netwerk wieħed biss fuq il-wiċċ iżda fih 3 graffs differenti. L-ewwelnett, il-graff li jiddeskrivi n-netwerk kif inhu definit mill-tliet listi ta 'l-adeġenza. It-tieni nett il-graff tal-korrispondenza jgħaqqad internament bjar tal-istess żona koerenti u l-aħħar il-graff tal-fluss massimu użat għall-komputazzjoni tal-fluss massimu. </p><h5> Grafika </h5><p> Fih biss is-sorsi reali u l-bjar bħala vertiċi. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/graph.svg"/><figcaption> <i><br/> Eżempju ta 'graff. Il-vertiċi ħomor jirrappreżentaw is-sorsi u l-bjar blu.</i> </figcaption></figure><h5> Grafika tal-korrispondenza </h5><p> Kull sink teħtieġ id-korrispondenza, li tindika, jekk tkun konnessa internament minn netwerk diġà eżistenti bħal f'żoni koerenti. Sinkijiet bl-istess id tal-korrispondenza huma konnessi ma 'vertiċi ġodda bi truf b'piż żero. Dan huwa kruċjali għall-komputazzjoni ta 'siġra ta' tifrix minimu u r-raġuni li għaliha qed jintuża l-graff tal-korrispondenza. Din il-karatteristika hija implimentata wkoll għal sorsi iżda mhux użata. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/correspondence_graph.svg"/><figcaption> <i><br/> Eżempju ta 'graff tal-korrispondenza. Il-vertiċi ħomor jirrappreżentaw is-sorsi u l-bjar blu. It-tliet bjar fuq il-lemin huma koerenti konnessi minn vertiċi akbar akbar</i> </figcaption></figure><h5> Grafika tal-fluss massimu </h5><p> Peress li l-igraph ma jappoġġjax sorsi multipli u jegħreq fil-funzjoni tal-fluss massimu tiegħu, hemm bżonn ta 'graff awżiljarju. Jintroduċi sors infinit u sink vertikali. Kull sors reali huwa konness mas-sors infinit u kull sink reali huwa konness mas-sink infinit minn tarf. Innota li jekk sink ikun imqabbad ma 'vertiċi ta' korrispondenza dan il-vertiċi jkun imqabbad minflok is-sink innifsu. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/max_flow_graph.svg"/><figcaption> <i><br/> Eżempju ta 'graff tal-fluss massimu.</i> </figcaption></figure><h5> Il-komputazzjoni minima ta 'siġar mifruxa </h5><p> Ibbażat fuq il-graff tal-korrispondenza huwa kkalkulat is-siġra tal-firxa minima. It-truf li jgħaqqdu l-bjar koerenti dejjem għandhom il-piż 0 sabiex dejjem jibqgħu parti mis-siġra tal-firxa minima. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/correspondence_graph_with_weigths.svg"/><figcaption> <i><br/> Eżempju ta 'grafika tal-korrispondenza mal-piżijiet ta' kull tarf u s-siġra minima li tifrex.</i> </figcaption></figure><h5> Il-komputazzjoni tal-fluss massimu </h5><p> Il-fluss mit-truf li jgħaqqad is-sorsi reali jew il-bjar mas-sors infinit jew sink rispettivament huwa limitat għall-kapaċità reali ta 'kull sors jew sink. Għal raġunijiet numeriċi il-kapaċitajiet huma normalizzati sabiex l-akbar kapaċità tkun 1. Il-fluss mis-sottogrupp tat-truf li jinsab fil-grafika tal-korrispondenza huwa limitat għal 1000 li għandhom, għall-finijiet intensi u kollha joffru fluss mhux ristrett. Imbagħad il-fluss massimu mis-sors infinit għall-sink infinit huwa kkalkulat u l-fluss issiġillat mill-ġdid għad-daqs oriġinali tiegħu. Peress li l-bjar koerenti mhumiex marbuta direttament mal-vertiċi tas-sink infinit iżda mill-vertiċi tal-korrispondenza, il-fluss minnu huwa limitat għat-total tal-bjar koerenti. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/max_flow_graph_with_capacities.svg"/><figcaption> <i><br/> Eżempju ta ’graff tal-fluss massimu u l-kapaċitajiet ta’ kull sors u sink. Il-grafika t-tajba turi l-fluss massimu permess minn kull tarf wara n-normalizzazzjoni. Innota li l-fluss massimu permess mit-truf bis-simbolu infinit huwa attwalment limitat għal 1000 fl-implimentazzjoni.</i> </figcaption></figure><p> L-implimentazzjoni tal-funzjoni tal-fluss massimu igraph tuża l-algoritmu Push-relabel. Dan it-tip ta 'algoritmu mhuwiex sensittiv għall-ispejjeż u jista' mhux dejjem isib l-iqsar mod kif tgħaddi l-fluss. Algoritmu sensittiv għall-ispejjeż mhux disponibbli fl-igraph u l-prestazzjoni tista ’tkun baxxa biex tkun tista’ ssolvi fluss ibbażat fis-siegħa matul is-sena. Iżda minħabba t-tnaqqis minn qabel għal siġra ta 'tifrix minimu il-każijiet li fihom tintgħażel soluzzjoni mhux ideali huma limitati ħafna u improbabbli. L-algoritmu Push-relabel għandu wkoll it-tendenza li jgħaddi l-fluss mill-inqas ammont ta 'trufijiet. L-implimentazzjoni tal-igraph tidher li hija deterministika fl-ordni tal-allokazzjoni tal-fluss jekk il-graffs huma tal-inqas awtomorfiżmu, li huwa importanti għall-kalkolu tal-fluss ibbażat fis-siegħa peress li kwalunkwe oxxillazzjoni tal-fluss introdott artifiċjalment bejn it-truf mhix mixtieqa. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/max_flow_graph_with_flows.svg"/><figcaption> <i><br/> Fluss maħdum bl-algoritmu tal-fluss massimu u l-iskala mill-ġdid għad-daqs oriġinali.</i> </figcaption></figure><h4> Sorsi tas-sħana </h4><p> Is-sorsi tas-sħana huma meħuda mid- <strong><a href="https://gitlab.com/hotmaps/industrial_sites/industrial_sites_Industrial_Database">database industrijali.</a></strong> Abbażi tas-sħana eċċessiva tagħhom, Nuts0 ID u s-settur industrijali għandhom profil ta ’tagħbija li jkopri kull siegħa tas-sena għal kull sit. Iż-żieda tad-dwana ta 'siti hija ppjanata. </p><h4> Bjar tas-sħana </h4><p> Il-bjar tas-sħana huma bbażati fuq żoni koerenti bi talba ta 'sħana magħrufa. Iż-żoni koerenti jiffurmaw maskra għal grilja li fuqha jitqiegħdu punti ekwidistanti bħala punti tad-dħul. Skond l-ID magħżul Nuts2, profil ta 'tisħin residenzjali huwa assenjat għall-bjar. Iż-żieda tad-dwana tal-punti tad-dħul u l-bjar hija ppjanata. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/coherent_aera_entry_points.svg"/><figcaption> <i><br/> Eżempju ta 'żona koerenti u l-punti ta' dħul iġġenerati tagħha.</i> </figcaption></figure><h4> Profili tat-Tagħbija </h4><p> Il-profili tat-tagħbija msemmija jikkonsistu minn 8760 punt li jirrappreżentaw it-tagħbija għal kull siegħa tal-365 ġurnata. Aktar informazzjoni dwar il <strong><a href="https://gitlab.com/hotmaps/load_profile">-profili tat</a></strong> - <strong><a href="https://gitlab.com/hotmaps/load_profile">tagħbija tista 'tinstab hawn.</a></strong> </p><h4> Komputazzjoni ta 'l-ispejjeż </h4><p> Peress li s-sistemi ta 'tisħin distrettwali għandhom kapaċità ta' sħana kbira, il-quċċata tal-fluss ma tfissirx li l-linji ta 'trażmissjoni għandhom bżonn li jagħtu spike qasir ta' sħana istantanjament. Għalhekk, il-kapaċitajiet meħtieġa tal-linji ta 'trasmissjoni u skambjaturi tas-sħana huma ddeterminati bit-tagħbija medja medja. Speċifikament, il-funzjoni ta 'konvoluzzjoni numpy tintuża biex timmedja l-fluss matul l-aħħar tliet sigħat billi taqbel b'funzjoni kostanti. Jiddependi fuq dan il-valur tintgħażel linja ta 'trasmissjoni mit-tabella li ġejja. </p><p> <em>Spejjeż speċifiċi tal-linji ta ’trażmissjoni wżati</em> </p><p> | Qawwa f'MW | Spejjeż f '€ / m | Temperatura fi ° Ċ | ------------- |: -------------: | -----: | | 0,2 | 195 | &lt;150 | | 0,3 | 206 | &lt;150 | | 0,6 | 220 | &lt;150 | | 1.2 | 240 | &lt;150 | | 1.9 | 261 | &lt;150 | | 3.6 | 288 | &lt;150 | | 6.1 | 323 | &lt;150 | | 9.8 | 357 | &lt;150 | | 20 | 426 | &lt;150 | | 45 | 564 | &lt;150 | | 75 | 701 | &lt;150 | | 125 | 839 | &lt;150 | | 190 | 976 | &lt;150 | | &gt; 190 | 976 | &lt;150 | </p><p> L-ispejjeż ta 'l-iskambjatur tas-sħana fuq in-naħa tas-sors li hija preżunta bħala l-arja mal-likwidu hija kkalkulata magħha </p><p> C <sub>HSource</sub> (P) = P <sub>quċċata</sub> * 15,000 € / MW. </p><p> L-ispejjeż tal-likwidu għall-iskambjatur tas-sħana likwidu fuq in-naħa tas-sink huma ddeterminati bi </p><p> <sub>HSink</sub> C (P) = P <sub>quċċata</sub> * 265,000 € / MW jekk P <sub>quċċata</sub> &lt;1MW jew </p><p> <sub>HSink</sub> C (P) = P <sub>quċċata</sub> * 100,000 € / MW ħaġa oħra. </p><p> L-ispejjeż tal-pompa jsegwu </p><p> <sub>Pompa</sub> C (P) = P <sub>quċċata</sub> * 240,000 € / MW jekk P <sub>quċċata</sub> &lt;1MW jew </p><p> <sub>Pompa</sub> C (P) = P <sub>quċċata</sub> * 90,000 € / MW ħaġa oħra. </p><h4> Tneħħija ta 'linji ta' trasmissjoni </h4><p> B'limitu ta 'spejjeż għal fluss għal-linji ta' trasmissjoni jistgħu jitneħħew jekk jaqbżuh biex itejbu l-proporzjon tal-fluss għall-ispejjeż. Wara t-tneħħija tat-trufijiet, il-fluss irid jiġi kkalkulat mill-ġdid peress li l-kontinwità tal-fluss fil-graff m'għadhiex garantita. Il-proporzjon tan-nefqa għall-fluss jista 'jiżdied ukoll għal truf oħra issa, u għalhekk dan il-proċess jiġi ripetut sakemm is-somma tal-flussi kollha ma tibdilx aktar. </p><h4> Deskrizzjoni tar-rutina kompluta </h4><p> L-ewwel is-sorsi tas-sħana u l-bjar huma mgħobbija bil-profili tat-tagħbija tagħhom. Imbagħad issir it-tfittxija bir-raġġ fiss, u n-Netwerk inizjalizza. Wara n-Netwerk huwa mnaqqas għas-siġra tal-firxa minima tiegħu u l-fluss massimu jinħadem għal kull siegħa tas-sena. Fuq il-bażi tal-fluss jiġu kkalkulati l-ispejjeż għal kull skambjatur tas-sħana, pompa u linja ta 'trasmissjoni. Jekk limitu tal-proporzjon tal-kost tal-fluss huwa definit il-proċedura tat-tneħħija tal-linja tat-trasmissjoni hija eżegwita. Fl-aħħar, l-ispiża totali u l-fluss totali tan-netwerk u t-tqassim tan-netwerk jintbagħtu lura. </p><h2> Ġirja tal-kampjun </h2><p> Kampjun immexxi f'Aalborg. </p><figure><img alt="" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/cm_excess_heat/aalborg.png"/><figcaption> <i>Kampjun immexxi f'Aalborg. L-aeras blu jirrappreżentaw it-tisħin distrettwali. Il-larinġ jindika s-sors tas-sħana u l-isfar jindika d-dħul għan-netwerk tat-tisħin distrettwali.</i> </figcaption></figure><p> L-ispejjeż totali huma 13.7 M € u l-fluss annwali totali huwa ta '185 GWh li jirriżulta f'0.74 ct / kWh għal perjodu ta' investiment ta '10 snin. </p><h2> Awturi u opinjonisti </h2><p> Din il-paġna hija miktuba minn Ali Aydemir * u David Schilling * </p><ul><li> [] Din il-paġna ġiet riveduta minn Tobias Fleiter *. </li></ul><p> * <a href="https://isi.fraunhofer.de/">Fraunhofer ISI</a> Fraunhofer ISI, Breslauer Str. 48, 76139 Karlsruhe </p><h2> Liċenzja </h2><p> Copyright © 2016-2018: Ali Aydemir, David Schilling </p><p> Creative Commons Attribuzzjoni 4.0 Liċenzja Internazzjonali Dan ix-xogħol huwa liċenzjat taħt Liċenzja Internazzjonali Creative Commons CC BY 4.0. </p><p> SPDX-Identifikatur tal-Liċenzja: CC-BY-4.0 </p><p> It-Test tal-Liċenzja: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Rikonoxximent </h2><p> Aħna nixtiequ nwasslu l-aktar profond apprezzament tagħna għall- <a href="https://www.hotmaps-project.eu">Proġett Hotmaps ta '</a> Orizzont 2020 (Ftehim ta' Għotja numru 723677), li pprovda l-finanzjament biex titwettaq l-investigazzjoni preżenti. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Excess-heat-transport-potential) (original) [Bulgarian](bg-CM-Excess-heat-transport-potential)<sup>\*</sup> [Croatian](hr-CM-Excess-heat-transport-potential)<sup>\*</sup> [Czech](cs-CM-Excess-heat-transport-potential)<sup>\*</sup> [Danish](da-CM-Excess-heat-transport-potential)<sup>\*</sup> [Dutch](nl-CM-Excess-heat-transport-potential)<sup>\*</sup> [Estonian](et-CM-Excess-heat-transport-potential)<sup>\*</sup> [Finnish](fi-CM-Excess-heat-transport-potential)<sup>\*</sup> [French](fr-CM-Excess-heat-transport-potential)<sup>\*</sup> [German](de-CM-Excess-heat-transport-potential)<sup>\*</sup> [Greek](el-CM-Excess-heat-transport-potential)<sup>\*</sup> [Hungarian](hu-CM-Excess-heat-transport-potential)<sup>\*</sup> [Irish](ga-CM-Excess-heat-transport-potential)<sup>\*</sup> [Italian](it-CM-Excess-heat-transport-potential)<sup>\*</sup> [Latvian](lv-CM-Excess-heat-transport-potential)<sup>\*</sup> [Lithuanian](lt-CM-Excess-heat-transport-potential)<sup>\*</sup>  [Polish](pl-CM-Excess-heat-transport-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Excess-heat-transport-potential)<sup>\*</sup> [Romanian](ro-CM-Excess-heat-transport-potential)<sup>\*</sup> [Slovak](sk-CM-Excess-heat-transport-potential)<sup>\*</sup> [Slovenian](sl-CM-Excess-heat-transport-potential)<sup>\*</sup> [Spanish](es-CM-Excess-heat-transport-potential)<sup>\*</sup> [Swedish](sv-CM-Excess-heat-transport-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated