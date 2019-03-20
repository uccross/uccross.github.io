# GSoC 2019

This is a list of summer projects for OSS incubators and research 
projects affiliated with CROSS. If you have any questions, please visit our Gitter channel: [![Join the chat at https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## [Popper](https://github.com/systemslab/popper)

Popper is a workflow execution engine based on [Github 
actions](https://github.com/features/actions) (GHA). Popper workflows 
are defined in a [HCL](https://github.com/hashicorp/hcl) syntax and 
behave like GHA workflows.

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Popper 2.0
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Github Actions and HCL (familiar), Docker (familiar)
| **Description** | The goal of this project is to add new features to the workflow execution engine, which is based on Github actions (GHA). Please look at the project link to see a list of associated issues.
| **Link**        | https://github.com/systemslab/popper/projects/12

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Popper Kubernetes Operator
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), Docker (familiar), Go (Strong), Kubernetes (familiar)
| **Description** | The goal of this project is to create a Kubernetes operator for running Popper workflows.
| **Link**        | https://github.com/blkswanio/popper-operator/projects/1

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Actions Library
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), Docker (familiar)
| **Description** | The goal of this project is to create a catalog of re-usable actions used in the creation of experimentation pipelines. For example: a Zenodo action that downloads a dataset to be consumed by a later stage in a pipeline; a Spack action that installs the software stack required for an exploration. This has a list of endless possibilities.
| **Link**        | https://github.com/systemslab/popper/projects/11

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Example Workflows
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), Docker (familiar)
| **Description** | The goal of this project is to create example workflows that showcase the distinct actions available for experimenters. This pipelines are relevant in multiple domains such as Genomics, Weather Prediction, Computational (Neuro/Math/etc) Science, among many other domains.
| **Link**        | https://github.com/systemslab/popper/projects/7

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Popper Pipeline and Stages Viewer
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | GUI development (strong), Javascript (strong)
| **Description** | Create a javascript-based viewer of Popper pipelines that allows users to visually explore a pipeline and its contents (similar to [Github's built-in](https://github.com/actions/gcloud/blob/master/.github/main.workflow) workflow editor). As part of this project, a stage catalog will also be implemented, that allows users to search for available stages on Github.
| **Link**        | https://github.com/systemslab/popper/projects/13

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend CI capabilities of CLI tool
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), Continuous integration (familiar)
| **Description** | Improve continuous integration aspects of the CLI tool. Currently, the `popper` command provides basic CI functionality via its `popper run` command, that allows experiment pipelines to be automatically executed on multiple CI services.
| **Link**        | https://github.com/systemslab/popper/projects/5

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Add Support for Popper Workflows in REANA
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)
| **Skills**      | Python (strong), Bash (familiar), Docker (familiar), Go (familiar), Kubernetes (familiar)
| **Description** | [REANA](https://reana.io) is a platform for running reproducible analysis. REANA currently supports CWL and Yadage workflows. The goal of this project is to add support for Popper workflows by creating a new reana workflow engine.
| **Link**        | https://gitter.im/falsifiable-us/popper

## LGraph
LGraph (https://github.com/masc-ucsc/lgraph) is the open source infrastructure for Synthesis and Simulation being developed by UCSC. The LGraph goal is to have a common LLVM-like format for synthesis and simulation with a focus on being very fast (Live) and compatible across languages.

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph and FIRRTL Bidirectional Bridge
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | FIRRTL (https://github.com/freechipsproject/firrtl) is the also open source infrastructure as "a platform for writing circuit-level transformations.". Both FIRRTL and LGraph share many common goals.  Creating a bridge between them allows to leverage features only existing in each one. There are many differences, for example LGraph has ABC synthesis integration and FIRRTL has CHISEL support.  The goal of this project is to implement at C++17 import/export for LGraph that handles FIRRTL.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph LLVM Code Generation
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | LGraph can output Verilog through a Yosys bridge. There is a work-in-progress custom Verilog and Pyrope output for LGraph. The goal of this project is to create an LLVM direct output bridge from LGraph to perform fast hardware simulations.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph AWS Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++/Verilog
| **Description** | The goal of this project is to setup a flow in AWS F1 instances to use LGraph for synthesis. LGraph can read Verilog and synthesize with ABC designs for Xilinx FPGAs. The end goal is to create an open source alternative to the Vivado flow used by AWS F1 instances. Since the open source tools are still not ready to handle place and route in AWS F1, for this project, the place and route will use Vivado, but the tools will be hidden behind LGraph.  Future projects could target to replace these missing pieces while having a working system.
| **Difficulty**        | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph FPGA NextPnr Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | Nextpnr is the new Open-source FPGA flow that targets Lattice and potentially Xilinx devices. The goal is to interface between LGraph and nextpnr. Creating a bidirectional bridge. The goal is to allow to leverage the incremental synthesis in LGraph, and target FPGAS like Lattice ECP5 and iCE40.
| **Difficulty**        | medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | LGraph ASIC RePlace Placement Integration
| **Mentor(s)**   | Jose Renau (https://users.soe.ucsc.edu/~renau/)
| **Skills**      | C++
| **Description** | RePlAce (https://github.com/abk-openroad/RePlAce) is a recently released placement tool from UCSD. The goal is to integrate LGraph with RePlAce.
| **Difficulty**        | high


## [Skyhook: programmable storage for databases](http://www.skyhookdm.com)
Skyhook extends object storage in the cloud with data management functionality. Skyhook [formats](https://github.com/uccross/skyhook-ceph/wiki/Data-format-(flatbuffers)) database table partitions as [Flatbuffers](https://google.github.io/flatbuffers/), and stores each partition as an object in [Ceph](https://ceph.com) distributed storage. Ceph object classes mechanism allow users to define custom read/write methods for objects.  We have developed methods (C++) for data management including data processing and indexing.

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Database statistics collection on partitioned data
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | This project will develop object-class methods to compute data statistics (histograms) for each object and store them in a query-able format within each storage server’s local RocksDB, then write client code to accumulate all the object-local statistics into global statistics for a given database table.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend current processing methods with column-oriented processing via Arrow
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | This project will develop object-class methods to transform on-disk Flatbuffer data (row oriented) into [Apache Arrow](https://arrow.apache.org) format (col-oriented) in memory, then work toward extending our row-oriented filters and aggregations to column oriented versions using the Arrow APIs.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | high

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend current aggregations to include sort/groupby for database partitions
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | We have developed methods (C++) for data management including data processing and indexing. This project will develop object-class methods methods to sort/group query result sets.  This requires extending the current code (select/project/basic-aggregations - min/max/sum/count) to support groupby and/or orderby.
| **Link**        | https://github.com/uccross/skyhook-ceph
| **Difficulty**  | medium

## [Tracery and Chancery](https://github.com/galaxykate/tracery)

Two little-languages and libraries for doing text expansion (used in 10,000 twitterbots, plus games and art projects) and state-based chatbots 

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Language and tutorial support for Tracery
| **Mentor(s)**   | [Kate Compton](http://www.galaxykate.com)
| **Skills**      | Javascript (low), Markdown (good), Language fluency and understanding of some non-English culture
| **Description** | In my [guide to supporting opensource art tools](https://github.com/galaxykate/OSSTA-Zine), I argued that art tools need contributors with different languages and cultures to translate the tools to enable access.  This project seeks someone with expert fluency in a non-English language to write javascript "modifiers" functions for Tracery, custom to that language. In English Tracery, these are things like pluralizing words or adding "a/an" to a word). I would like to enable this support for some non-English language, as well as get culturally-relevant Tracery/twitterbot tutorials written in that language.
| **Link**        | https://tracery.io

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Pathfinding for Chancery
| **Mentor(s)**   | [Kate Compton](http://www.galaxykate.com)
| **Skills**      | Javascript (high), graph analysis, pathfinding and traversal
| **Description** | Chancery is a state-based chatbot language (think Twine, but for the Alexa). Users write state machines that represent conversations or games. This project will build a pathfinding algorithm than can calculate which state exits or states cannot be reached (e.g., requiring 5 gems to move from one state to another, but only 4 gems can be collected). If interested, this project could also include building a visualization of that connectivity map.
| **Link**        | https://tracery.io/chancery

## [CAvSAT](https://github.com/uccross/cavsat)

A comprehensive and scalable query answering system over inconsistent databases.

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | CAvSAT (Consistent Answering via Satisfiability)
| **Mentor(s)**   | [Akhil Dixit](https://users.soe.ucsc.edu/~akadixit/), [Phokion G. Kolaitis](https://users.soe.ucsc.edu/~kolaitis/)
| **Skills**      | Java, SQL
| **Description** | Inconsistent relational databases are the ones that violate one or more integrity constraints defined over their schema. We are developing CAvSAT, which aims to be a scalable and comprehensive system for consistent query answering. In general, computing consistent answers over inconsistent databases is an intractable problem. However, for certain classes of queries and integrity constraints, there is an efficient algorithm to compute consistent answers. The goal of this project is two-fold. First is to get familiar with the literature and implement this algorithm. Second, the student will conduct experiments with both synthetic and real-world databases, to compare the performance of this algorithm with other methods.
| **Link**        | https://github.com/uccross/cavsat
| **References**  | https://dl.acm.org/citation.cfm?id=2371212, https://dl.acm.org/citation.cfm?id=303983, https://dl.acm.org/citation.cfm?id=3068334
| **Difficulty**  | Medium
