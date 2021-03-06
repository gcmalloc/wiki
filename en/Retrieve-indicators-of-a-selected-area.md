<h1>Retrieve indicators of a selected area</h1>

## Table of Contents
1. [Introduction](#introduction)
1. [Indicators for raster layers](#indicators-for-raster-layers)
   * [Buildings](#buildings)
   * [Population](#population)
   * [Renewable Energy Source Potentials](#res-potentials)
1. [Indicators for vector layers](#indicators-for-vector-layers)
   * [Industry](#industry)
   * [Renewable Energy Source Potentials](#res--potentials)
   * [Electricity](#electricity)
1. [Example](#example)
1. [How to cite](#how-to-cite)
1. [Authors and reviewers](#authors-and-reviewers)
1. [License](#license)
## Indroduction 

Depending on the layers and region you selected indicators for your configuration are shown in a sidebar at the right of your screen 

![results.png][results]

[**`To Top`**](#table-of-contents)

In the following we look at the indicators that are displayed for raster and vector layers.

## Indicators for raster layers 

The indicators on raster layers are different from vector layers. With different we mean in terms of aggregation and disaggregation. This different behaviour comes from the territorial resolutions. 

Raster Layers have generally a much higher resolution whereas vector layers have only attributes at points or polygons. 

That mean on the one hand for example that if you select a vector layer which is defined by NUTS3 polygons and you want for example to select a LAU region then the NUTS3 value will not be disaggregated to LAU level, instead the NUTS3 indicator where this LAU region is located will be shown in the results side bar. 

On the other hand, raster layers are aggregated and disaggregated "arbitrarily"* 

*by the containing cells within the region you selected (naturally within the limit of the raster resolution itself)

### Buildings

**Heat Density Map**

![hdm.png][hdm]

**Extra Feature**

When you select the heat denisity layer and the Population Layer at the same time an extra indicator is shown (see picture below)

![hdm2.png][hdm2]

### In General:
When one of the bulding layers and the population layer is selected at the same time, an extra indicator will be shown as described before

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Cooling Density Map**

![cdm.png][cdm]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Building Volumes**

![bvol.png][bvol]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Gross floor area**

![gfa.png][gfa]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

### Population

![pop.png][pop]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

### Climate
**Temperature**

![temp.png][temp]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Cooling Degree Days**

![cdd.png][cdd]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Heating Degree Days**

![hdd.png][hdd]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Solar Radiation**

![rad.png][rad]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Wind Speed**

![wind.png][wind]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

### RES Potentials

**Solar Radiation On Building Footprint**

![srobf.png][srobf]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Wind Potential at 50m**

![wp.png][wp]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>

**Forest Residues**

![forest.png][forest]

<code><ins>**[To Chapter](#indicators-for-raster-layers)**</ins></code>
[**`To Top`**](#table-of-contents)

## Indicators for vector layers 

### Industry
**Industrial Site Emissions**
![ise.png][ise]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Industrial Site Excess Heat**
![iseh.png][iseh]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Industrial Site Company Name**
![isec.png][isec]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Industrial Site Subsector**
![ises.png][ises]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

### RES- Potentials

**Waste Water Treatment Plants Power**

![wwp.png][wwp]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Waste Water Treatment Plants Capacity**

![wwc.png][wwc]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Argicultural Residues**

![ar.png][ar]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Lifestock Effluents**

![le.png][le]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Municipal Solid Waste**

![sw.png][sw]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

**Geothermal Potential Heat Conductivity**

![geothermal.png][geothermal]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>

### Electricity

**Electricity C02 Emissions**

![electricity.png][electricity]

<code><ins>**[To Chapter](#indicators-for-vector-layers)**</ins></code>
[**`To Top`**](#table-of-contents)

## Example 
In the picture below you can see how it looks when all layers are visualized (here is Austria as NUTS0 selected)

![all_map.png][all_map]

Although this maps looks pretty messy, the indicators are straight forward illustrated. See below all indicators that are described in the result sidebar when you select all layers for Austria (NUTS0)

![all_results.png][all_results]

[**`To Top`**](#table-of-contents)

## How to cite

Jeton Hasani, in Hotmaps-Wiki, Retrieve-indicators-of-a-selected-area (April 2019)


## Authors and reviewers
<code>[Review this page !](CM-Access/_edit)</code>

This page is written by Jeton Hasani\*.
- [ ] This page was reviewed by <code>....</code>\.


\* [Energy Economics Group - TU Wien](https://eeg.tuwien.ac.at/)
Institute of Energy Systems and Electrical Drives
Gusshausstrasse 27-29/370
1040 Wien

## License
Copyright © Hotmaps
Creative Commons Attribution 4.0 International License
This work is licensed under a Creative Commons CC BY 4.0 International License.
SPDX-License-Identifier: CC-BY-4.0
License-Text: https://spdx.org/licenses/CC-BY-4.0.html


## Acknowledgement
We would like to convey our deepest appreciation to the Horizon 2020 [Hotmaps Project](https://www.hotmaps-project.eu) (Grant Agreement number 723677), which provided the funding to carry out the present investigation.

[**`To Top`**](#table-of-contents)
<code>[Review this page](Indicator-Section/_edit)</code>

[//]: # (Here are all the files to the links)

[results]: ../images/general_tool_functionalities_and_structure/results.png

[all_results]: ../images/general_tool_functionalities_and_structure/all_results.png

[all_map]: ../images/general_tool_functionalities_and_structure/all_map.png
[hdm2]: ../images/general_tool_functionalities_and_structure/hdm2.png
[hdm]: ../images/general_tool_functionalities_and_structure/hdm.png
[cdm]: ../images/general_tool_functionalities_and_structure/cdm.png
[gfa]: ../images/general_tool_functionalities_and_structure/gfa.png
[bvol]: ../images/general_tool_functionalities_and_structure/bvol.png
[temp]: ../images/general_tool_functionalities_and_structure/temp.png
[pop]: ../images/general_tool_functionalities_and_structure/pop.png
[cdd]: ../images/general_tool_functionalities_and_structure/cdd.png
[hdd]: ../images/general_tool_functionalities_and_structure/hdd.png
[rad]: ../images/general_tool_functionalities_and_structure/rad.png
[wind]: ../images/general_tool_functionalities_and_structure/wind.png
[temp]: ../images/general_tool_functionalities_and_structure/temp.png
[forest]: ../images/general_tool_functionalities_and_structure/forest.png
[wp]: ../images/general_tool_functionalities_and_structure/wp.png
[srobf]: ../images/general_tool_functionalities_and_structure/srobf.png
[ise]: ../images/general_tool_functionalities_and_structure/ise.png
[iseh]: ../images/general_tool_functionalities_and_structure/iseh.png
[isec]: ../images/general_tool_functionalities_and_structure/isec.png
[ises]: ../images/general_tool_functionalities_and_structure/ises.png
[wwp]: ../images/general_tool_functionalities_and_structure/wwp.png
[wwc]: ../images/general_tool_functionalities_and_structure/wwc.png
[ar]: ../images/general_tool_functionalities_and_structure/ar.png
[le]: ../images/general_tool_functionalities_and_structure/le.png
[geothermal]: ../images/general_tool_functionalities_and_structure/geothermal.png
[sw]: ../images/general_tool_functionalities_and_structure/sw.png
[electricity]: ../images/general_tool_functionalities_and_structure/electricity.png


<!--- THIS IS A SUPER UNIQUE IDENTIFIER -->

View in another language:

 [German](../de/Retrieve-indicators-of-a-selected-area)<sup>\*</sup> 

<sup>\*</sup> machine translated
