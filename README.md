# SPADE -- Spanning Tree Progression of Density Normalized Events

SPADE is a visualization and analysis tool for high-dimensional flow cytometry data. SPADE is implemented as an R package and can be installed via R's packing facilities. Additionally a GUI is provided, as a [Cytoscape](http://www.cytoscape.org) plugin for setting-up and interactively visualizing the results of SPADE analyses. Please see the project homepage at [cytospade.org](http://www.cytospade.org) or the github wiki for the primary documentation. This README is primarily targeted at developers working on SPADE itself.

## Prerequisites
1. Latest version of [R](http://www.r-project.org/) and the following packages: igraph, flowCore

## Setup
The SPADE package has a C++ core that must be built before use. SPADE successfully builds on Linux, OSX and Windows (with Rtools), although Windows users will not be able to take advantage of the OpenMP parallelization used withing SPADE. SPADE can be installed from the command line via

    $ R CMD INSTALL <SPADE PATH>


### Building on Windows
You will need to install the [Rtools](http://www.murdoch-sutherland.com/Rtools) that matches your R distribution. After installation make sure that your `PATH` contains the neccessary Rtools binary directories, e.g.:

1. Open *Control Panel -> System*
1. Click on *Advanced Tab* and then on *Environment Variables*
1. Highlight *PATH* and click *Edit*
1. In the character string in *Variable Value*, make sure the following appears before the Windows default entries:

    c:\Rtools\bin;c:\Rtools\perl\bin;c:\Rtools\MinGW\bin;c:\Program Files\R\<your R version>\bin;


## Building Packages
Source packages can be built with

    $ R CMD build <SPADE PATH>

and binary packages with

    $ R CMD build --binary <SPADE PATH>

## Tips and Resources
* [R manual for writing extensions](http://cran.r-project.org/doc/manuals/R-exts.html)

## Citations
SPADE was developed in the Plevritis and Nolan Labs at Stanford University, and is described in the following publications:

* Peng Qiu, Erin F. Simonds, Sean C. Bendall, Kenneth D. Gibbs, Robert V. Bruggner, Michael D. Linderman, Karen Sachs, Garry P. Nolan, Sylvia K. Plevritis, "Phenotypically determined self-organization of flow cytometry data with spanning-tree progression analysis of density normalized events. *Under review*, 2011.
* Michael D. Linderman, Erin F. Simonds, Peng Qiu, Zach Bjornson, Nikesh Kotecha, Teresa H. Meng, Sylvia Plrevritis, Garry P. Nolan, "Algorithmically recoving the hematopoietic lineage from high-dimensional cytometry data using SPADE", *Congress of the Intl. Society for Advancement of Cytometry*, 2010.
