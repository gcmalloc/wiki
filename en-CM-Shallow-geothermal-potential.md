﻿## Table of Contents

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

It aims to compute the shallow geothermal potential based on [r.green.gshp.theoretical](en-https://grass.osgeo.org/grass76/manuals/addons/r.green.gshp.theoretical.html) according to the [G.pot methodology](https://www.sciencedirect.com/science/article/pii/S0360544216303358). 
In this module the output is the theoretical maximum energy that can be converted in the ideal case without considering the financial and spatial constraints. 


<code><ins>**[To Top](#table-of-contents)**</ins></code>


## Inputs and outputs

The input parameters and layers as well as output layers and parameters are as follows.


**Input layers and parameters are:**

* Vector with depth-averaged ground thermal conductivity [W m-1 K-1]
* Value with the Heating Season [0-365] days
* Raster with the initial ground temperature T0 [°C]
* Value with depth-averaged ground thermal capacity [MJ m-3 K-1]
* Value with depth-averaged ground thermal capacity [MJ m<sup>-3</sup> K<sup>-1</sup>]

The advanced input are:
* Borehole radius [m]
* Borehole thermal resistance [m K W<sup>-1</sup>]
* Borehole length [m]
* Pipe radius [m]
* Number of pipes in the borehole
* Thermal conductivity of the borehole filling (geothermal grout) [W m-1 K-1]
* Minimum or maximum fluid temperature [°C]
* Simulated lifetime of the plant [years]

**Output layers and parameters are:**

* a raster map with the geothermal power potential [W]
* a raster map with the geothermal energy potential [MWh]

A deeper explanation of the default input raster is available in the [Hotmaps repository](en-https://gitlab.com/hotmaps/potential/potential_geothermal_raster)

<code><ins>**[To Top](#table-of-contents)**</ins></code>


## Method
The method to define the energy potential is based on the [G.pot](en-https://www.sciencedirect.com/science/article/pii/S0360544216303358). The potential of shallow geothermal energy is computed by means of and empirical relationship proposed by [Casasso et al. (2016)](https://www.sciencedirect.com/science/article/pii/S0360544216303358).

<code><ins>**[To Top](#table-of-contents)**</ins></code>

## Test Run 1
<code><ins>**[To Top](#table-of-contents)**</ins></code>


### Test Run 1: default input values


<code><ins>**[To Top](#table-of-contents)**</ins></code>



### Test Run 2: modified input values

<code><ins>**[To Top](#table-of-contents)**</ins></code>


## References



## How to cite


## Authors and reviewers

This page is written by Pietro Zambelli\* and Giulia Garegnani\*.


\* [Urban and Regional Energy System Group - EURAC Bozen](en-http://www.eurac.edu/en/research/technologies/renewableenergy/researchfields/Pages/Energy-strategies-and-planning.aspx)

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

We would like to convey our deepest appreciation to the Horizon 2020 [Hotmaps Project](en-https://www.hotmaps-project.eu) (Grant Agreement number 723677), which provided the funding to carry out the present investigation.



<code><ins>**[To Top](#table-of-contents)**</ins></code>






View in another language:

 [Bulgarian](bg-CM-Shallow-geothermal-potential)<sup>\*</sup> [Croatian](hr-CM-Shallow-geothermal-potential)<sup>\*</sup> [Czech](cs-CM-Shallow-geothermal-potential)<sup>\*</sup> [Danish](da-CM-Shallow-geothermal-potential)<sup>\*</sup> [Dutch](nl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Estonian](et-CM-Shallow-geothermal-potential)<sup>\*</sup> [Finnish](fi-CM-Shallow-geothermal-potential)<sup>\*</sup> [French](fr-CM-Shallow-geothermal-potential)<sup>\*</sup> [German](de-CM-Shallow-geothermal-potential)<sup>\*</sup> [Greek](el-CM-Shallow-geothermal-potential)<sup>\*</sup> [Hungarian](hu-CM-Shallow-geothermal-potential)<sup>\*</sup> [Irish](ga-CM-Shallow-geothermal-potential)<sup>\*</sup> [Italian](it-CM-Shallow-geothermal-potential)<sup>\*</sup> [Latvian](lv-CM-Shallow-geothermal-potential)<sup>\*</sup> [Lithuanian](lt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Maltese](mt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Polish](pl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-CM-Shallow-geothermal-potential)<sup>\*</sup> [Romanian](ro-CM-Shallow-geothermal-potential)<sup>\*</sup> [Slovak](sk-CM-Shallow-geothermal-potential)<sup>\*</sup> [Slovenian](sl-CM-Shallow-geothermal-potential)<sup>\*</sup> [Spanish](es-CM-Shallow-geothermal-potential)<sup>\*</sup> [Swedish](sv-CM-Shallow-geothermal-potential)<sup>\*</sup>
<sup>\*</sup>: machine translated