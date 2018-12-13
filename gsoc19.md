# GSoC 2019

This is a list of summer projects for OSS incubators and research 
projects affiliated with CROSS.

## [Popper](https://github.com/systemslab/popper)

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Automate Popper Compliance
| **Mentor(s)**   | Ivo Jimenez
| **Skills**      | Python (strong), Bash (familiar)
| **Description** | An experimentation pipeline is Popper compliant if it complies with all the criteria define in [this document](https://zenodo.org/record/1422203/files/paper.pdf?download=1). For this project, we will implement a process to automatically verify that a pipeline is Popper compliant.
| **Link**        | https://github.com/systemlabs/popper/projects/4


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Popper Pipeline Viewer
| **Mentor(s)**   | Ivo Jimenez
| **Skills**      | GUI development (strong), Javascript (strong)
| **Description** | Create a javascript-based viewer of Popper pipelines.
| **Link**        | https://github.com/systemlabs/popper/projects/4

## LGraph
|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph and FIRRTL Bidirectional Bridge
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | Description: LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages.  FIRRTL (https://github.com/freechipsproject/firrtl) is the also open source infrastructure as "a platform for writing circuit-level transformations.". Both FIRRTL and LGraph share many common goals.  Creating a bridge between them allows to leverage features only existing in each one. There are many differences, for example LGraph has ABC synthesis integration and FIRRTL has CHISEL support.  The goal of this project is to implement at C++17 import/export for LGraph that handles FIRRTL.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph LLVM Code Generation
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | Description: Description: LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages. LGraph can output Verilog through a Yosys bridge. There is a work-in-progress custom Verilog and Pyrope output for LGraph. The goal of this project is to create an LLVM direct output bridge from LGraph to perform fast hardware simulations.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph AWS Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++/Verilog
| **Description** | Description: LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages. The goal of this project is to setup a flow in AWS F1 instances to use LGraph for synthesis. LGraph can read Verilog and synthesize with ABC designs for Xilinx FPGAs. The end goal is to create an open source alternative to the Vivado flow used by AWS F1 instances. Since the open source tools are still not ready to handle place and route in AWS F1, for this project, the place and route will use Vivado, but the tools will be hidden behind LGraph.  Future projects could target to replace these missing pieces while having a working system.
| **Difficulty**        | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph FPGA NextPnr Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | Description: Description: LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages. Nextpnr is the new Open-source FPGA flow that targets Lattice and potentially Xilinx devices. The goal is to interface between LGraph and nextpnr. Creating a bidirectional bridge. The goal is to allow to leverage the incremental synthesis in LGraph, and target FPGAS like Lattice ECP5 and iCE40.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph ASIC RePlace Placement Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | Description: LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages. RePlAce (https://github.com/abk-openroad/RePlAce) is a recently released placement tool from UCSD. The goal is to integrate LGraph with RePlAce.
| **Difficulty**        | high

