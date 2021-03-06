<h1>Database behind the Hotmaps toolbox</h1>

## Table of Contents

- [Introduction](#introduction)
- [How to export a dataset](#how-to-export-a-dataset)
- [References](#references)
- [How to cite](#how-to-cite)
- [Authors and reviewers](#authors-and-reviewers)
- [Acknowledgement](#acknowledgement)

## Introduction

The database built for Hotmaps is a spatial Data Warehouse made available to the platform for visualization and computation purposes.

There are different kinds of data:

- raster datasets (at hectare level)
- vector datasets (NUTS/LAU regions, points of interest, ...)
- non-spatial datasets (mostly NUTS/LAU related and linked to existing vector layers)

The datasets can be accessed via a geospatial server (GeoServer) which provides different services (WMS/WFS/...) that allows anyone to display, include or use those datasets.

The datasets can be found on the [Gitlab repository](https://gitlab.com/hotmaps)

## Query

Please note that aggregations when selecting NUTS or LAU regions are pre-computed and therefore faster than aggregations of hectare selections which are computed on-the-fly.

## Technologies

The technologies used for the database are:

- PostgreSQL version 9.6
- PostGIS version 2.3
- GeoServer version 2.11.2

[**`To Top`**](#table-of-contents)

## References

- Simon Pezzutto, Stefano Zambotti, Silvia Croce, Pietro Zambelli, Giulia Garegnani, Chiara Scaramuzzino, Ramón Pascual Pascuas, Alyona Zubaryeva, Franziska Haas, Dagmar Exner (EURAC), Andreas Mueller (e-think), Michael Hartner (TUW), Tobias Fleiter, Anna-Lena Klingler, Matthias Kühnbach, Pia Manz, Simon Marwitz, Matthias Rehfeldt, Jan Steinbach, Eftim Popovski (Fraunhofer ISI) Reviewed by Lukas Kranzl, Sara Fritz (TUW) Hotmaps Project, **D2.3 WP2 Report – Open Data Set for the EU28, 2018** 
  [www.hotmaps-project.eu](http://www.hotmaps-project.eu/wp-content/uploads/2018/05/D2.3-Hotmaps_FINAL-VERSION_for-upload.pdf)

[**`To Top`**](#table-of-contents)

## How to cite

[**`To Top`**](#table-of-contents)

## Authors and reviewers

Authors:

- Daniel Hunacek
- Lucien Zuber

Reviewers:

[**`To Top`**](#table-of-contents)

## Acknowledgement

We would like to convey our deepest appreciation to the Horizon 2020 [Hotmaps Project](https://www.hotmaps-project.eu) (Grant Agreement number 723677), which provided the funding to carry out the present investigation

[**`To Top`**](#table-of-contents)





<!--- THIS IS A SUPER UNIQUE IDENTIFIER -->

View in another language:

 [German](../de/Database-behind-the-Hotmaps-toolbox)<sup>\*</sup> 

<sup>\*</sup> machine translated
