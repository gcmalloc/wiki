<h2> Sisällysluettelo </h2><ul><li> <a href="#introduction">esittely</a> </li><li> <a href="#inputs-and-outputs">Tulot ja lähdöt</a> </li><li> <a href="#method">Menetelmä</a> </li><li> <a href="#sample-run">Näyte ajo</a> <ul><li> <a href="#test-run-1-default-input-values">Testiajo 1: oletusarvot</a> </li><li> <a href="#test-run-2-modified-input-values">Testiajo 2: muunnetut tuloarvot</a> </li></ul></li><li> <a href="#references">Viitteet</a> </li><li> <a href="#how-to-cite">Kuinka lainata</a> </li><li> <a href="#authors-and-reviewers">Tekijät ja arvioijat</a> </li><li> <a href="#license">lisenssi</a> </li><li> <a href="#acknowledgement">tunnustus</a> </li></ul><h2> esittely </h2><p> Sen tavoitteena on laskea matala geoterminen potentiaali <a href="https://grass.osgeo.org/grass76/manuals/addons/r.green.gshp.theoretical.html">r.green.gshp.theoretical</a> perusteella <a href="https://www.sciencedirect.com/science/article/pii/S0360544216303358">G.pot metodologian mukaisesti</a> . Tässä moduulissa lähtö on teoreettinen maksimienergia, joka voidaan muuntaa ihanteellisessa tapauksessa ottamatta huomioon taloudellisia ja alueellisia rajoituksia. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Tulot ja lähdöt </h2><p> Tuloparametrit ja -kerrokset samoin kuin lähtötasot ja -parametrit ovat seuraavat. </p><p> <strong>Syöttökerrokset ja parametrit ovat:</strong> </p><ul><li> Vektori syvyyskeskeisellä maan lämmönjohtavuudella [W m-1 K-1] </li><li> Arvo lämmityskauden [0-365] päivän kanssa </li><li> Rasteri, jonka alkuperäinen maanlämpötila on T0 [° C] </li><li> Arvo syvyyskeskeisellä maan lämpökapasiteetilla [MJ m-3 K-1] </li><li> Arvo syvyyskeskeisellä maan lämpökapasiteetilla [MJ m <sup>-3</sup> K <sup>-1</sup> ] </li></ul><p> Edistyneet tulot ovat: </p><ul><li> Reiän säde [m] </li><li> Reiän lämpöresistanssi [m KW <sup>-1</sup> ] </li><li> Reiän pituus [m] </li><li> Putken säde [m] </li><li> Putkien lukumäärä porakaivossa </li><li> Reiän täytteen lämmönjohtavuus (geoterminen laasti) [W m-1 K-1] </li><li> Nesteen minimi- tai maksimilämpötila [° C] </li><li> Laitoksen simuloitu käyttöikä [vuotta] </li></ul><p> <strong>Lähtökerrokset ja parametrit ovat:</strong> </p><ul><li> rasterikartta geotermisen potentiaalin kanssa [W] </li><li> rasterikartta geotermisen energian potentiaalilla [MWh] </li></ul><p> <a href="https://gitlab.com/hotmaps/potential/potential_geothermal_raster">Perusteellisempi syöttörasteri</a> löytyy <a href="https://gitlab.com/hotmaps/potential/potential_geothermal_raster">Hotmaps-arkistosta</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Menetelmä </h2><p> Menetelmä energiapotentiaalin määrittelemiseksi perustuu <a href="https://www.sciencedirect.com/science/article/pii/S0360544216303358">G.pot-arvoon</a> . Matalan geotermisen energian potentiaali lasketaan <a href="https://www.sciencedirect.com/science/article/pii/S0360544216303358">Casasso et al: n</a> ehdottaman empiirisen suhteen avulla <a href="https://www.sciencedirect.com/science/article/pii/S0360544216303358">. (2016)</a> . </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Koeajo 1 </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testiajo 1: oletusarvot </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h3> Testiajo 2: muunnetut tuloarvot </h3><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Viitteet </h2><h2> Kuinka lainata </h2><h2> Tekijät ja arvioijat </h2><p> Tämän sivun ovat kirjoittaneet Pietro Zambelli * ja Giulia Garegnani *. </p><p> * <a href="http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx">Kaupunkien ja alueiden energiajärjestelmäryhmä - EURAC Bozen</a> </p><p> Uusiutuvan energian instituutti Drususallee / Viale Druso 1 I-39100 Bozen / Bolzano Italia </p><h2> lisenssi </h2><p> Tekijänoikeudet © 2016-2019: Giulia Garegnani </p><p> Creative Commons Attribution 4.0 - kansainvälinen lisenssi </p><p> Tämä teos on lisensoitu Creative Commons CC BY 4.0 International -lisenssillä. </p><p> SPDX-lisenssitunniste: CC-BY-4.0 </p><p> Lisenssiteksti: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> tunnustus </h2><p> Haluamme ilmaista syvimmän arvion Horizon 2020 <a href="https://www.hotmaps-project.eu">Hotmaps -hankkeelle</a> (avustussopimus nro 723677), joka rahoitti tämän tutkimuksen toteuttamista. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-CM-Shallow-geothermal-potential) (original) [Bulgarian](bg-CM-Shallow-geothermal-potential)<sup>\*</sup> [Croatian](hr-CM-Shallow-geothermal-potential)<sup>\*</sup> [Czech](cs-CM-Shallow-geothermal-potential)<sup>\*</sup> [Danish](da-CM-Shallow-geothermal-potential)<sup>\*</sup> [Dutch](nl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Estonian](et-CM-Shallow-geothermal-potential)<sup>\*</sup>  [French](fr-CM-Shallow-geothermal-potential)<sup>\*</sup> [German](de-CM-Shallow-geothermal-potential)<sup>\*</sup> [Greek](el-CM-Shallow-geothermal-potential)<sup>\*</sup> [Hungarian](hu-CM-Shallow-geothermal-potential)<sup>\*</sup> [Irish](ga-CM-Shallow-geothermal-potential)<sup>\*</sup> [Italian](it-CM-Shallow-geothermal-potential)<sup>\*</sup> [Latvian](lv-CM-Shallow-geothermal-potential)<sup>\*</sup> [Lithuanian](lt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Maltese](mt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Polish](pl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Romanian](ro-CM-Shallow-geothermal-potential)<sup>\*</sup> [Slovak](sk-CM-Shallow-geothermal-potential)<sup>\*</sup> [Slovenian](sl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Spanish](es-CM-Shallow-geothermal-potential)<sup>\*</sup> [Swedish](sv-CM-Shallow-geothermal-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated