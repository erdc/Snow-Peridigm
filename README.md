# Snow-Peridigm

This repository contains input files for the [Peridigm](https://github.com/peridigm/peridigm/) simulations presented in the CSRT publication titled ["Peridynamic Modeling of the Micromechanical Response of Snow Under High Strain Rates"](https://www.sciencedirect.com/science/article/pii/S0165232X23002860) by West et al., as well as the simulations presented in the manuscript titled "The Importance of Snow Microstructure: An Analysis of Snow Compressive Strength Under High Strain" by Hodgdon et al. The files related to each manuscript are separated into folders with the corresponding titles. Note that all of the geometry files in the "Peridynamic Modeling of the Micromechanical Response of Snow Under High Strain Rates" folder are the same as the "Medium" grain size samples in "The Importance of Snow Microstructure: An Analysis of Snow Compressive Strength Under High Strain". We point the reader to those files in order to avoid reproducing them.

Each simulation folder contains files for several different snow microstructures. We provide a zipped folder for each sample that includes the input geometry file for that microstructure, as well as the micro CT images used to create that geometry file. The geometry files consist of a txt file (`"material_points.txt`) containing the (x, y, z) coordinates of each material point and its volume, as well as separate txt files for each node set (`node_set1.txt`, `node_set2.txt`, etc. depending on the number of microstructure components). These node sets are used to define which points are included in each boundary condition set. Please reference the following script provided with Peridigm: https://github.com/peridigm/peridigm/blob/master/scripts/text_to_genesis.py. This script takes the different txt files and converts them to a Genesis file format, which Peridigm can take as input. Genesis files can be quite large, so we have decided to provide the much smaller txt files that can then be used to create the Genesis files.

An example YAML file is provided for a simulation with strain rate of 0.1 s<sup>-1</sup>. A user can change the strain rate by going to the `Prescribed Displacement Top` section and updating the multiplying factor in the `Value: "-6.000e-04*t"` line. The user can change the input Genesis file by updating the path in the `Input Mesh File: "Material_Points.g"` line to whichever microstructure they want to simulate.
