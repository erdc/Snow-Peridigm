# Snow-Peridigm

This repository contains the input files for the [Peridigm](https://github.com/peridigm/peridigm/) simulations presented in the manuscript titled "Peridynamic Modeling of the Micromechanical Response of Snow Under High Strain Rates" by West et al. 

Simulation results were presented for three different regions of a snow microstructure, and we provide the input Genesis files for each region within a separate folder. An example YAML file is provided for a compression simulation with strain rate of 0.01 s<sup>-1</sup>. A user can change the strain rate by going to the `Prescribed Displacement Top` section of the YAML file and updating the multiplying factor in the `Value: "X*t"` line.

Please see the [Peridigm](https://github.com/peridigm/peridigm/) repository for additional information on how to install and use the model.
