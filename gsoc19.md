# GSoC 2019

This is a list of summer projects for OSS incubators and research 
projects affiliated with CROSS.

## [Popper](https://github.com/systemslab/popper)

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Gitlab Integration
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar)
| **Description** | So far, [Popper](https://github.com/systemslab/project) assumes pipelines are hosted on Github. The goal of this project is to add support to the CLI tool so it becomes possible to upload and retrieve pipelines to/from Gitlab instances.
| **Link**        | https://github.com/systemslab/popper/projects/9

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Automate Popper Compliance Verification
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar)
| **Description** | An experimentation pipeline is Popper compliant if it complies with all the criteria define in [this document](https://zenodo.org/record/1422203/files/paper.pdf?download=1). For this project, we will implement a process to automatically verify that a pipeline is Popper compliant.
| **Link**        | https://github.com/systemslab/popper/projects/10

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Stage-level Features
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), REST (familiar)
| **Description** | Currently, the smallest shareable unit in Popper is a complete pipeline. For this project, the goal is to break this down and to make it possible to have individual stages as the smallest shareable unit. This will make it possible to create a catalog of re-usable stages that can be individually maintained.
| **Link**        | https://github.com/systemslab/popper/projects/11

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Github Actions Integration
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | GUI development (strong), Javascript (strong)
| **Description** | The goal of this project is to generate a Github Actions (GA) workflow automatically for one or more Popper pipelines. This will make it possible to run Popper pipelines as GA transparently, without users having to write the GA workflow themselves.
| **Link**        | https://github.com/systemslab/popper/projects/12

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Popper Pipeline and Stages Viewer
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | GUI development (strong), Javascript (strong)
| **Description** | Create a javascript-based viewer of Popper pipelines that allows users to visually explore a pipeline and its contents. As part of this project, a stage catalog will also be implemented, that allows users to search for available stages on Github.
| **Link**        | https://github.com/systemslab/popper/projects/13


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


## [Skyhook: programmable storage for databases](http://www.skyhookdm.com)

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Database statistics collection on partitioned data
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | Skyhook [formats](https://github.com/uccross/skyhook-ceph/wiki/Data-format-(flatbuffers)) database table partitions as [Flatbuffers](https://google.github.io/flatbuffers/), and stores each partition into a [Ceph](https://ceph.com) object.  Ceph object classes mechanism allow users to define custom read/write methods for objects.  We have developed methods (C++) for data management including data processing and indexing. This project will develop object-class methods to compute data statistics (histograms) for each object and store them in a query-able format within each storage server’s local RocksDB, then write client code to accumulate all the object-local statistics into global statistics for a given database table.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend current processing methods with column-oriented processing via Arrow
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | Skyhook [formats](https://github.com/uccross/skyhook-ceph/wiki/Data-format-(flatbuffers)) database table partitions as [Flatbuffers](https://google.github.io/flatbuffers/), and stores each partition into a [Ceph](https://ceph.com) object. Ceph object classes mechanism allow users to define custom read/write methods for objects.  We have developed methods (C++) for data management including data processing and indexing. This project will develop object-class methods to transform on-disk Flatbuffer data (row oriented) into [Apache Arrow](https://arrow.apache.org) format (col-oriented) in memory, then work toward extending our row-oriented filters and aggregations to column oriented versions using the Arrow APIs.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | high

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend current aggregations to include sort/groupby for database partitions
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | Skyhook [formats](https://github.com/uccross/skyhook-ceph/wiki/Data-format-(flatbuffers)) database table partitions as [Flatbuffers](https://google.github.io/flatbuffers/), and stores each partition into a [Ceph](https://ceph.com) object. Ceph object classes mechanism allow users to define custom read/write methods for objects.  We have developed methods (C++) for data management including data processing and indexing. This project will develop object-class methods methods to sort/group query result sets.  This requires extending the current code (select/project/basic-aggregations - min/max/sum/count) to support groupby and/or orderby.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | medium
