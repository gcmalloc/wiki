<h2> Tartalomjegyzék </h2><ul><li> <a href="#introduction">Bevezetés</a> </li><li> <a href="#inputs-and-outputs">Bemenetek és kimenetek</a> </li><li> <a href="#method">Eljárás</a> </li><li> <a href="#sample-run">Mintafuttatás</a> <ul><li> <a href="#test-run-1-default-input-values">1. tesztfutás: alapértelmezett bemeneti értékek</a> </li><li> <a href="#test-run-2-modified-input-values">2. tesztfutás: módosított bemeneti értékek</a> </li></ul></li><li> <a href="#references">Irodalom</a> </li><li> <a href="#how-to-cite">Hogyan lehet idézni</a> </li><li> <a href="#authors-and-reviewers">Szerzők és áttekintők</a> </li><li> <a href="#license">Engedély</a> </li><li> <a href="#acknowledgement">Elismerés</a> </li></ul><h2> Bevezetés </h2><p> A távhőellátó modul egy disztribúciós modell, amely megpróbál költség-optimális megoldást találni a hőigény fedezésére az év minden órájában. </p><p><img alt="concept.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/concept.png"/></p><blockquote><p> Az itt leírt módszer első koncepcióként értendő, és eltérhet a tényleges megvalósítástól (ebből a szempontból a modell összetettségét, a bemeneteket és outputokat stb. Kell figyelembe venni). </p></blockquote><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Bemenetek és kimenetek </h2><h3> Fő bemenetek </h3><ol><li> A hálózat hőigénye (kiválasztott régió) </li><li> Hőgenerátorok beépített kapacitása / tárolása </li><li> Hőgenerátorok / tárolók műszaki (hatékonysági) és fincancal paraméterei (opex, capex, élettartam) </li><li> Profilok (hőigény, napsugárzás, hőmérséklet, villamosenergia-árak stb. Idősorai) </li><li> ... </li></ol><h3> Fő outputok </h3><ul><li> Hőtermelési költségek </li><li> Beruházási, üzemeltetési és üzemanyagköltségek </li><li> Hőtermelő keverék hőgenerátoronként </li><li> CO2-kibocsátás </li><li> Teljes terhelési idő, </li><li> stb.. </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Eljárás </h2><p> A modul egy lineáris programként valósul meg, és egyrészt tiszta disztribúciós modellként, másrészt beruházástervezésként felhasználható terhelési profil lefedésére. A célfüggvény megpróbálja megtalálni a hőszolgáltatás költségeitől és a villamosenergia-termelésből származó bevételek közötti különbség minimumát. </p><h3> A lineáris program egyenlettöredékei: </h3><p><img alt="lp_fragment.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/lp_fragment.png"/></p><h4> Az összes költség <code>c <sub>total</sub></code> hozam az alábbiak összegéből: </h4><h5> beruházási költségek <code>IC</code> (telepített kapacitások szorozva a konkrét beruházási költségek járadékaival) </h5><p><img alt="ic.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/ic.png"/></p><h5> naptári költségek <code>CC</code> : </h5><p><img alt="cc.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/cc.png"/></p><h5> az <code>OPEX</code> változó költségei: </h5><p><img alt="opex.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/opex.png"/></p><h5> A CHP és a hulladékégető művek földi költségei (durva becslés): </h5><p><img alt="ramp.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/ramp.png"/></p><h5> téli téli időszakban a csúcsteljesítmény feltételezett költségei (durva becslés): </h5><p><img alt="peak.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/peak.png"/></p><h4> Az összes bevétel <code>rev <sub>total</sub></code> hozamot :: </h4><h5> villamosenergia-értékesítés (például kapcsolt energiatermelő létesítményekből és hulladékégető művekből): </h5><p><img alt="rev.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/rev.png"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h4> Legenda </h4><p><img alt="legend.png" src="https://github.com/HotMaps/hotmaps_wiki/blob/master/Images/dh_supply/legend.png"/></p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Mintafuttatás </h2><p> <code>NOT IMPLEMENTED&gt;</code> </p> <p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 1. tesztfutás: alapértelmezett bemeneti értékek </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> 2. tesztfutás: módosított bemeneti értékek </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Irodalom </h2><h2> Hogyan lehet idézni </h2><h2> Szerzők és áttekintők </h2><p> Ezt az oldalt Jeton Hasani írta *. </p><ul><li> [] Ezt az oldalt Lukas Kranzl * vizsgálta felül. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Energiagazdaságtan Csoport - TU Wien</a> Energia Rendszerek és Elektromos Meghajtók Intézete Gusshausstrasse 27-29 / 370 1040 Wien </p><h2> Engedély </h2><p> Copyright © 2016-2018: Jeton Hasani Creative Commons Nevezd meg! 4.0 Nemzetközi licenc Ezt a munkát a Creative Commons CC BY 4.0 Nemzetközi Licenc védi. SPDX-licenc-azonosító: CC-BY-4.0 licenc-szöveg: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Elismerés </h2><p> Szeretnénk <a href="https://www.hotmaps-project.eu">kifejezni</a> legmélyebb elismerésünket a Horizont 2020 <a href="https://www.hotmaps-project.eu">Hotmaps projekthez</a> (támogatási megállapodás száma: 723677), amely finanszírozást nyújtott a jelen vizsgálat elvégzéséhez. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><p> <code><a href="https://github.com/HotMaps/hotmaps_wiki/wiki/CM_DH_supply/_edit">Review this page</a></code> </p>

This page was automatically translated. View in another language:

[English](en-CM-District-heating-supply-dispatch) (original) [Bulgarian](bg-CM-District-heating-supply-dispatch)<sup>\*</sup> [Croatian](hr-CM-District-heating-supply-dispatch)<sup>\*</sup> [Czech](cs-CM-District-heating-supply-dispatch)<sup>\*</sup> [Danish](da-CM-District-heating-supply-dispatch)<sup>\*</sup> [Dutch](nl-CM-District-heating-supply-dispatch)<sup>\*</sup> [Estonian](et-CM-District-heating-supply-dispatch)<sup>\*</sup> [Finnish](fi-CM-District-heating-supply-dispatch)<sup>\*</sup> [French](fr-CM-District-heating-supply-dispatch)<sup>\*</sup> [German](de-CM-District-heating-supply-dispatch)<sup>\*</sup> [Greek](el-CM-District-heating-supply-dispatch)<sup>\*</sup>  [Irish](ga-CM-District-heating-supply-dispatch)<sup>\*</sup> [Italian](it-CM-District-heating-supply-dispatch)<sup>\*</sup> [Latvian](lv-CM-District-heating-supply-dispatch)<sup>\*</sup> [Lithuanian](lt-CM-District-heating-supply-dispatch)<sup>\*</sup> [Maltese](mt-CM-District-heating-supply-dispatch)<sup>\*</sup> [Polish](pl-CM-District-heating-supply-dispatch)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-District-heating-supply-dispatch)<sup>\*</sup> [Romanian](ro-CM-District-heating-supply-dispatch)<sup>\*</sup> [Slovak](sk-CM-District-heating-supply-dispatch)<sup>\*</sup> [Slovenian](sl-CM-District-heating-supply-dispatch)<sup>\*</sup> [Spanish](es-CM-District-heating-supply-dispatch)<sup>\*</sup> [Swedish](sv-CM-District-heating-supply-dispatch)<sup>\*</sup>
<sup>\*</sup>: machine translated