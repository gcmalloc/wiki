<h1>CM Solar thermal and PV potential</h1>

## Table of Contents

* [Introduction](#introduction)
* [Inputs and outputs](#inputs-and-outputs)
* [Method](#method)
* [Sample run](#sample-run)
  * [Test Run 1: default input values](#test-run-1-default-input-values)
  * [Test Run 2: modified input values](#test-run-2-modified-input-values)
* [References](#references)
* [How to cite](#how-to-cite)
* [Authors and reviewers](#authors-and-reviewers)
* [License](#license)
* [Acknowledgement](#acknowledgement)


## Introduction

It aims to compute the solar thermal and the photovoltaic energy potential and the financial feasibility of a selected area by considering:
- the installation of new Solar thermal / PV systems on a percentage of the available areas (the default area are the building footprint)
- assess the financial feasibility of new plants

[**`To Top`**](#table-of-contents)


## Inputs and outputs

The input parameters and layers as well as output layers and parameters are as follows.


**Input layers and parameters are:**

* raster file:
     * mean yearly solar irradiation [kWh m^{-2}] 
     * with the area available for the solar energy exploitation. The default raster use the building footprint raster file [m^{2}] 
* percentage of available area that can be covered with solar panels [%] 
* reference plant parameters:  
     * average installed peak power per plant [kW_p] 
     * system efficiency, value between 0 and 1 [-] 
     * the solar radiation at Standard Test Condition equal to 1 kW  m^{-2}
     * module efficiency at Standard Test Conditions [kW  m^{-2}]

**Output layers and parameters are:**

* the total cost of covering the selected area with PV panels [currency]
* the total yearly energy production [MWh/year]
* the Levelized Cost of Energy  [€/kWh]
* a raster file with the most suitable areas for PV energy production

[**`To Top`**](#table-of-contents)


## Method

Starting from the available area and the kind of PV technology the module computes the PV energy production under the following assumptions:
- optimal inclination of the PV system
- area of the PV modules equal to the percentage of the building footprint chosen by the user
- unique selected technology for all the installed PV systems
- default system efficiency equal to 0.75 

These assumptions have been done in order to consider a planning phase for a region and not the design of a specific PV systems.

The yearly energy output is  derived by considering the spatial distribution of yearly solar radiation on the building footprint. The PV energy production is computed for a single representative plant.
The most representative installed peak power for a PV system is an input of the module.
Consequently, the surface covered by a single plant and the total number of plants are computed.
 
Finally, the most suitable area is computed by considering the roofs with higher energy production. 
The energy production of each pixel considers to cover only a fraction of the roofs equal to f_roof. The integral of the energy production of the most suitable area is equal to the total energy production of the selected area.


[**`To Top`**](#table-of-contents)

## Test Run 1
Here, the calculation module is run for the Lombardy region in Italy (NUTS2).

* First, select Nuts2 and the chosen area.

![Fig. 1](../images/cm_solar_PV/default_values_01.png "Select a region")

* Follow the steps as shown in the figure below:
  * Click on the "Layers" button to open the "Layers" window:
  * Click on the "CALCULATION MODULE" tab.
  * Click on the "SOLAR PV POTENTIAL" button.

* Now, the "Solar PV Potential" opens and is ready to run. 


[**`To Top`**](#table-of-contents)


### Test Run 1: default input values

The default input values considers the possibility to install roof-mounted PV panels on buildings. These values rerers to a plant of 3 kWp. You may need to set values bellow or above default values considering additional local considerations and costs. Therefore, the user should adapt these values to find the best combination of thresholds for his or her case study.

To run the calculation module, follow the next steps:

* Assign a name to the run session (optional - here, we chose "Test Run 1") and set the input parameters (here, default values were used).

![Fig. 2](../images/cm_solar_PV/default_values_02.png "Test run 1 with default values")

* Wait until the process is finished.
* As output, indicators and diagrams are shown in the "RESULTS" window. The indicators show:
  * Total energy production,
  * Total setup costs,
  * Number of installed systems,
  * Levelized Cost of Energy


![Fig. 3](../images/cm_solar_PV/default_values_03.png "Test run 1 INDICATORS tab")


* Also a new layer is added to the canvas showing the buildings with higher energy potential. This layer is added to the list of layers under the "Calculation module" category. The run session name distinguishes the outputs of this run from other ones.
If you deselected the default layers and select TEST RUN 1 you can visualize the most suitable areas for PV plants installations.

![Fig. 4](../images/cm_solar_PV/default_values_03.png "Test run 1 Calculation module LAYERS")


[**`To Top`**](#table-of-contents)



### Test Run 2: modified input values

Depending on your experience and  local knowledge, you may increase or decrease the input values to obtain better results. You may decide to increase the building surface suitable for PV plants.

* Assign a name to the run session (optional - here, we chose "Test Run 2") and set the input parameters Percentage of buildings with solar panels equal to 50. It means that we are covering the 50% of the available building roofs. Notice that since each pixel can represent more than one building and we are not covering the whole roof with PV panels, the user can set also the Effective building roof utilization factor. The default values is set to 0.15. This means that only the 15% of the roof surface in a pixel is covered by PV panels.

* Wait until the process is finished.
* As output, indicators and diagrams are shown in the "RESULTS" window. The indicators show:
  * Total energy production,
  * Total setup costs,
  * Number of installed systems,
  * Levelized Cost of Energy



[**`To Top`**](#table-of-contents)


## References



## How to cite
Giulia Garegnani, in Hotmaps-Wiki, CM-Solar-PV-potential (April 2019)


## Authors and reviewers

This page is written by Giulia Garegnani\*.


\* [Urban and Regional Energy System Group - EURAC Bozen](http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx)

Institute of Renewable Energy
Drususallee/Viale Druso 1
I-39100 Bozen/Bolzano
Italy


## License

Copyright © 2016-2019: Giulia Garegnani

Creative Commons Attribution 4.0 International License

This work is licensed under a Creative Commons CC BY 4.0 International License.

SPDX-License-Identifier: CC-BY-4.0

License-Text: https://spdx.org/licenses/CC-BY-4.0.html


## Acknowledgement

We would like to convey our deepest appreciation to the Horizon 2020 [Hotmaps Project](https://www.hotmaps-project.eu) (Grant Agreement number 723677), which provided the funding to carry out the present investigation.



[**`To Top`**](#table-of-contents)







<!--- THIS IS A SUPER UNIQUE IDENTIFIER -->

View in another language:

 [German](../de/CM-Solar-thermal-and-PV-potential)<sup>\*</sup> 

<sup>\*</sup> machine translated