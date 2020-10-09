[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![toolset: JKQ](https://img.shields.io/badge/toolset-JKQ-blue)](https://github.com/iic-jku/jkq)


# JKQ - An open-source toolset for design automation for quantum computing

The *JKQ toolset* by the [Institute for Integrated Circuits](http://iic.jku.at/eda/research/quantum/) 
at the [Johannes Kepler University Linz](https://jku.at) covers different
areas of design automation for quantum computing, namely simulation, compiling/mapping, and verification.

- [JKQ DDSIM](https://github.com/iic-jku/ddsim) is the decision diagram-based simulator for quantum circuits.
- [JKQ QMAP](https://github.com/iic-jku/qmap) provides heuristic and exact mapping/compilation methods to satisfy coupling constraints.
- [JKQ QCEC](https://github.com/iic-jku/qcec) checks circuits for equivalence with different strategies.
- [JKQ DDVis](http://github.com/iic-jku/ddvis) visualizes how decision diagrams are used in simulation and verification.
  - You can find an online instance of this tool at http://iic.jku.at/eda/research/quantum_dd/tool/
- [Quantum Circuits](https://github.com/iic-jku/quantum_circuits) is a collection of quantum circuits we use as benchmarks in our research.

We further develop libraries used across our tools:

- [JKQ DD Package](https://github.com/iic-jku/dd_package) is the fundamental library handling decision diagrams in our tools.
- [JKQ QFR](https://github.com/iic-jku/qfr) builds on the JKQ DD Package and handles input/output of various formats.

You can find additional information on the [website of the institute](http://iic.jku.at/eda/research/quantum/).

## Unifying Interface

The tools mentioned have to be compiled before they can be used.
To simplify that usage, we provide a unifying interface `jkq` that handles the downloading and building steps.

### Usage

The `jkq` script provides an interface to the underlying tools, such that the user does not have to manually handle
the download and installation. 

```commandline
$ git clone https://github.com/iic-jku/jkq.git && cd jkq
$ ./jkq help                                              
JKQ -- Johannes Kepler Quantum
Usage:
  jkq command arguments...

Commands:
help
  display this help
build
  build the JKQ tools

simulate [arguments...]
  run the simulate with the provided arguments (try --help)
mapper [arguments...]
  run the mapper with the provided arguments (try --help)
equivalencecheck [arguments...]
  run the equivalence checker with the provided arguments (try --help)

The commands may be abbreviated if the abbreviation is unambiguous.
```

### Requirements

Using the `jkq` script has the following requirements:

- [bash](https://www.gnu.org/software/bash/)
- [git](https://git-scm.com/)
- [cmake](https://cmake.org/)
- [boost](https://www.boost.org/) (having the [program_options](https://www.boost.org/doc/libs/1_74_0/doc/html/program_options.html) suffices)

## References

The JKQ toolset was introduced in *JKQ: JKU Tools for Quantum Computing* 
by Robert Wille, Stefan Hillmich, and Lukas Burgholzer in *International Conference on Computer Aided Design (ICCAD)*, 2020.

If you use our tools in your research, we will be thankful if you refer to it by citing the appropriate publication 
as indicated in the repositories of the individual tools.