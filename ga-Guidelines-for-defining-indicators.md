<h2> Clár ábhair </h2><ul><li> <a href="#Indicators">Táscairí</a> <ul><li> <a href="#Simple-indicator">Táscaire simplí</a> </li><li> <a href="#Cross-indicator">Trastháscaire</a> </li></ul></li><li> <a href="#Indicator-result">Toradh táscairí</a> </li><li> <a href="#references">Tagairtí</a> </li><li> <a href="#how-to-cite">Conas a lua</a> </li><li> <a href="#authors-and-reviewers">Údair agus léirmheastóirí</a> </li><li> <a href="#license">Ceadúnas</a> </li><li> <a href="#acknowledgement">Admháil</a> </li></ul><h2> Táscairí </h2><p> Míníonn an cháipéisíocht seo conas bainistiú a dhéanamh ar tháscairí ar an mbosca uirlisí Hotmaps. Is éard atá i dtáscaire luach a thaispeántar ar an mbosca uirlisí Hotmaps sa taobh cliant. Is cuid de shraith an táscaire. Is luach é an táscaire, i gcás réigiún spásúil ar leith, le haonad. Tá táscaire mar chuid de fhoclóir ciseal. Tá réad darb ainm “táscairí” i réad ciseal. Bainfear úsáid as an tábla seo chun na táscairí go léir ar mhaith leat a fheiceáil don tsraith a liostú. </p><pre> <code>layers = { 'heat_tot_curr_density_tif':{ 'tablename':'heat_tot_curr_density_tif', 'from_indicator_name':'stat_heat_tot_curr_density_tif', 'schema_scalelvl': 'stat', 'schema_hectare': 'geo', 'crs': '3035', 'geo_column': 'geometry', 'table_type':'raster', 'data_lvl':['NUTS 0','NUTS 1','NUTS 2','NUTS 3','LAU 2','Hectare'], 'data_aggregated':True, 'scalelvl_column':'', 'indicators':[ {'table_column': 'sum', 'unit': 'MWh','indicator_id':'consumption'}, {'table_column': 'count', 'unit': 'cells','indicator_id':'count_cell'}, { 'reference_indicator_id_1': 'consumption', 'reference_tablename_indicator_id_1': 'heat_tot_curr_density_tif', 'operator': '/', 'reference_indicator_id_2': 'count_cell', 'reference_tablename_indicator_id_2': 'pop_tot_curr_density_tif', 'unit':'MWh/person', 'indicator_id': 'heat_tot_curr_density_tif_per_pop_tot_curr_density_tif' } ] } }</code> </pre><ul><li> 'ainm boird' </li></ul><p> Ainm an tábla SS. (Díolúine: 'heat_tot_curr_density_tif') </p><ul><li> 'from_indicator_name' </li></ul><p> Ainm foghabhálach chun táscairí a roghnú. <strong>Ní mór a bheith uathúil.</strong> (Díolúine: 'stat_heat_tot_curr_density_tif') </p><ul><li> 'data_aggregated' </li></ul><p> An bhfuil na sonraí comhiomlánaithe nó ná bíodh (Luachanna: Fíor nó Bréagach) </p><ul><li> 'scalelvl_column' </li></ul><p> Ainm colún leibhéal scála murab ionann agus ceann réamhshocraithe (Díolúine: 'cód') </p><ul><li> 'data_lvl' </li></ul><p> Leibhéil atá ar fáil do na sonraí sa bhunachar sonraí </p><ul><li> 'schema_scalelvl' </li></ul><p> Suíomh scéimre an tábla do leibhéal na gcnónna. (Díolúine: 'geo', 'stat', 'poiblí') </p><ul><li> 'schema_hectare' </li></ul><p> Suíomh scéimre an tábla don leibhéal heicteáir. (Díolúine: 'geo', 'stat', 'poiblí') </p><ul><li> 'crs' </li></ul><p> Teilgean na geoiméadrachta (Díolúine: '3035', '4326', '4258') </p><ul><li> 'geo_column' </li></ul><p> Ainm an cholúin céimseata sa bhunachar sonraí (Eiseamláir: 'geom', 'geoiméadracht') </p><ul><li> 'table_type' </li></ul><p> Cineál an chiseal sa bhunachar sonraí (Luachanna: 'veicteoir' nó 'raster'). </p><p> <em><strong>Tábhachtach:</strong></em> Más raster é, is é an colún atá ar fáil <strong>comhaireamh, suim, meán, stddev, min agus max</strong> </p><ul><li> 'Táscairí' </li></ul><p> Tá 2 chineál táscaire ann (Táscairí simplí &amp; Trastháscairí). </p><h3> Táscaire simplí </h3><p> Is éard atá i dtáscaire simplí ná réad le 3 pharaiméadar. </p><pre> <code>{ 'table_column': 'count', 'unit': 'cells', 'indicator_id':'count_cell' }</code> </pre><ul><li> 'table_column' </li></ul><p> Is é seo an colún tábla a roghnaítear sa tábla. (Díolúine: 'comhaireamh') </p><p><img alt="díchódú boird" src="/api/assets/table_image.png"/></p><ul><li> 'aonad' </li></ul><p> Is é seo aonad an táscaire. (Díolúine: 'cealla', 'MWh') </p><ul><li> 'indicator_id' </li></ul><p> Is é seo aitheantóir táscaire an táscaire (Cosúil le ID). <strong>Caithfidh an</strong> t-ainm seo <strong>a bheith uathúil</strong> sa réimse táscairí. </p><h3> Trastháscaire </h3><p> Is éard is trastháscaire ann ná réad le 7 bparaiméadar. Is é sprioc an táscaire seo calca a dhéanamh idir táscairí simplí agus trastháscaire. </p><pre> <code>{ 'reference_indicator_id_1': 'consumption', 'reference_tablename_indicator_id_1':'heat_tot_curr_density_tif', 'operator': '/', 'reference_indicator_id_2':'count_cell', 'reference_tablename_indicator_id_2':'pop_tot_curr_density_tif', 'unit':'MWh/person', 'indicator_id':'heat_tot_curr_density_tif_per_pop_tot_curr_density_tif' }</code> </pre><ul><li> 'reference_indicator_id_1' </li></ul><p> Comhfhreagraíonn sé don aitheantóir de tháscaire simplí. <strong>Ní mór an</strong> t-ainm seo <strong>a shainiú</strong> san eagar táscairí. Is é an luach uimhir 1 é. </p><ul><li> 'reference_tablename_indicator_id_1' </li></ul><p> Tagairt an tsloinnte ciseal a thagraíonn don luach uimhir 1. (Díolúine: 'heat_tot_curr_density_tif') </p><ul><li> 'oibreoir' </li></ul><p> Riail chailc a bheith i bhfeidhm ar an 2 luach (Luachanna: '/' nó '*' nó '+' nó '-') </p><ul><li> 'reference_indicator_id_1' </li></ul><p> Comhfhreagraíonn sé don aitheantóir de tháscaire simplí. <strong>Ní mór an</strong> t-ainm seo <strong>a shainiú</strong> san eagar táscairí. Is é an luach uimhir 2 é. </p><ul><li> 'reference_tablename_indicator_id_2' </li></ul><p> Tagairt an tsloinnte ciseal a thagraíonn don luach uimhir 2. (Díolúine: 'pop_tot_curr_density_tif') </p><ul><li> 'aonad' </li></ul><p> Is é seo aonad an táscaire. (Díolúine: 'cealla', 'MWh') </p><ul><li> 'ainm' </li></ul><p> Is é seo ainm an táscaire (Cosúil le ID). <strong>Caithfidh an</strong> t-ainm seo <strong>a bheith uathúil</strong> sa réimse táscairí. </p><h5> Nóta: Don eiseamláir seo, déantar an ríomh. </h5><pre> <code>reference_indicator_id_1.reference_indicator_id_1 / reference_indicator_id_1.reference_indicator_id_1 = heat_tot_curr_density_tif.consumption / pop_tot_curr_density_tif.count_cell</code> </pre><h2> Toradh táscairí </h2><p> Seo a leanas toradh na dtáscairí: </p><pre> <code>{ "values": [ { "unit": "MWh", "name": "heat_tot_curr_density_tif_consumption", "value": "4112030.46" }, { "unit": "cells", "name": "heat_tot_curr_density_tif_count_cell", "value": "46764" }, { "unit": "MWh/person", "name": "heat_tot_curr_density_tif_per_pop_tot_curr_density_tif", "value": "38.0092476775893146" } ], "name": "heat_tot_curr_density_tif" }</code> </pre><h2> Tagairtí </h2><h2> Conas a lua </h2><p> Mostafa Fallahnejad, i Hotmaps-Wiki, https://github.com/HotMaps/hotmaps_wiki/wiki/Guidelines-for-defining-indicators (Aibreán 2019) </p><h2> Údair agus léirmheastóirí </h2><p> Is é Mostafa Fallahnejad * a scríobh an leathanach seo. </p><ul><li> [] Rinne Lukas Kranzl * athbhreithniú ar an leathanach seo. </li></ul><p> * <a href="https://eeg.tuwien.ac.at/">Grúpa Eacnamaíochta Fuinnimh - TU Wien</a> </p><p> Institiúid na gCóras Fuinnimh agus Tiomántán Leictreach </p><p> Gusshausstrasse 27-29 / 370 </p><p> 1040 Wien </p><h2> Ceadúnas </h2><p> Cóipcheart © 2016-2019: Mostafa Fallahnejad </p><p> Ceadúnas Idirnáisiúnta Creative Commons Attribution 4.0 </p><p> Tá an obair seo ceadúnaithe faoi Cheadúnas Idirnáisiúnta Creative Commons CC BY 4.0. </p><p> SPDX-Ceadúnas-Aitheantóir: CC-BY-4.0 </p><p> Téacs-Cheadúnas: https://spdx.org/licenses/CC-BY-4.0.html </p><h2> Admháil </h2><p> Ba mhaith linn ár mbuíochas mór a chur in iúl don <a href="https://www.hotmaps-project.eu">Tionscadal Hotmaps</a> Horizon 2020 (Comhaontú Deontais uimhir 723677), a chuir an maoiniú ar fáil chun an t-imscrúdú reatha a dhéanamh. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p>

This page was automatically translated. View in another language:

[English](en-Guidelines-for-defining-indicators) (original) [Bulgarian](bg-Guidelines-for-defining-indicators)<sup>\*</sup> [Croatian](hr-Guidelines-for-defining-indicators)<sup>\*</sup> [Czech](cs-Guidelines-for-defining-indicators)<sup>\*</sup> [Danish](da-Guidelines-for-defining-indicators)<sup>\*</sup> [Dutch](nl-Guidelines-for-defining-indicators)<sup>\*</sup> [Estonian](et-Guidelines-for-defining-indicators)<sup>\*</sup> [Finnish](fi-Guidelines-for-defining-indicators)<sup>\*</sup> [French](fr-Guidelines-for-defining-indicators)<sup>\*</sup> [German](de-Guidelines-for-defining-indicators)<sup>\*</sup> [Greek](el-Guidelines-for-defining-indicators)<sup>\*</sup> [Hungarian](hu-Guidelines-for-defining-indicators)<sup>\*</sup>  [Italian](it-Guidelines-for-defining-indicators)<sup>\*</sup> [Latvian](lv-Guidelines-for-defining-indicators)<sup>\*</sup> [Lithuanian](lt-Guidelines-for-defining-indicators)<sup>\*</sup> [Maltese](mt-Guidelines-for-defining-indicators)<sup>\*</sup> [Polish](pl-Guidelines-for-defining-indicators)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-Guidelines-for-defining-indicators)<sup>\*</sup> [Romanian](ro-Guidelines-for-defining-indicators)<sup>\*</sup> [Slovak](sk-Guidelines-for-defining-indicators)<sup>\*</sup> [Slovenian](sl-Guidelines-for-defining-indicators)<sup>\*</sup> [Spanish](es-Guidelines-for-defining-indicators)<sup>\*</sup> [Swedish](sv-Guidelines-for-defining-indicators)<sup>\*</sup>
<sup>\*</sup>: machine translated