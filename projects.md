<img src="HiRes-Vector.png" alt="Logo of the Center for Research in Open Source Software" valign="middle" />

# Open Source Project Ideas

<img src="OSRE2021image.jpg" alt="Light bulb with digital business interface" valign="middle" />

This list of projects are meant for student and other up-and-coming developers interested in contributing to participating Universiy of California-based open source projects. The list below notes the UC-based open source project and ideas associated to each that were submitted by a Open Source Research Experience (OSRE) mentor. If you have any questions, please visit our Gitter channel: [![Join the chat at
https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

*UC-affiliated mentors interested in OSRE'22 can add project ideas to this page. See instructions on our [READ ME](https://github.com/uccross/uccross.github.io/blob/master/README.md) file. If you have questions about being a mentor, go to the [Mentor Info Page](https://cross.ucsc.edu/2022-osre/osre2022mentor.html)*

The Open Source Research Experience Program (https://cross.ucsc.edu/2022-osre/index.html) will be accepting student project application in February/March 2022. We will have exact deadlines published by January 2022. Connected to that CROSS will be applying to be a mentor organization under the Google Summer of Code for 2022 and hope to be part of that program again. The project ideas below can be utilized in applying for either of these programs.

Table of Contents:

<!--ts-->
* [Open Source Project Ideas](#open-source-project-ideas)
   * [LiveHD](#livehd)
      * [Tree sitter Pyrope](#tree-sitter-pyrope)
      * [Mockturtle](#mockturtle)
      * [Query Shell](#query-shell)
      * [Lgraph and LNAST check pass](#lgraph-and-lnast-check-pass)
      * [unbitwidth](#unbitwidth)
      * [LNAST Opt](#lnast-opt)
   * [Eusocial Storage Devices](#eusocial-storage-devices)
      * [Evaluating user space networking stacks on SmartNICs](#evaluating-user-space-networking-stacks-on-smartnics)
      * [Dynamic function injection for RocksDB](#dynamic-function-injection-for-rocksdb)
      * [Demonstrating a composable storage system accelerated by memory semantic technologies](#demonstrating-a-composable-storage-system-accelerated-by-memory-semantic-technologies)
   * [Open Source Autonomous Vehicle Controller](#open-source-autonomous-vehicle-controller)
      * [Vehicle/Craft sensor driver development](#vehiclecraft-sensor-driver-development)
      * [IMU calibration algorithm development](#imu-calibration-algorithm-development)
      * [Path finding algorithm using OpenCV](#path-finding-algorithm-using-opencv)
      * [State estimation/sensor fusion algorithm development](#state-estimationsensor-fusion-algorithm-development)
      * [Vehicle dynamic model development](#vehicle-dynamic-model-development)
   * [SkyhookDM](#skyhookdm)
      * [Add Ability to create and save views from Datasets](#add-ability-to-create-and-save-views-from-datasets)
      * [Ability to Push back query execution to the Client in case of overloaded OSDs](#ability-to-push-back-query-execution-to-the-client-in-case-of-overloaded-osds)
      * [Port wiki to ReadTheDocs or other documentation platform](#port-wiki-to-readthedocs-or-other-documentation-platform)
      * [Integrating Delta Lake on top of SkyhookDM](#integrating-delta-lake-on-top-of-skyhookdm)
      * [Write Helm charts for easy deployment of the SkyhookDM, Dask , ServiceX stack on Kubernetes](#write-helm-charts-for-easy-deployment-of-the-skyhookdm-dask--servicex-stack-on-kubernetes)
      * [Facilitate continuous benchmarking/regression testing for the critical components of SkyhookDM](#facilitate-continuous-benchmarkingregression-testing-for-the-critical-components-of-skyhookdm)
   * [HDF5](#hdf5)
      * [HDF5 - Apache Arrow Integration](#hdf5---apache-arrow-integration)
      * [HDF5 - Ceph RADOS Integration](#hdf5---ceph-rados-integration)
      * [Column-storage in HDF5](#column-storage-in-hdf5)
      * [Sparse data storage in HDF5](#sparse-data-storage-in-hdf5)
      * [Metadata search in HDF5 with Database Solutions](#metadata-search-in-hdf5-with-database-solutions)
   * [Proactive Data Containers (PDC)](#proactive-data-containers-pdc)
      * [Python interface to an object-centric data management system](#python-interface-to-an-object-centric-data-management-system)
   * [CephFS](#cephfs)
      * [CephFS namespace traversal offloading](#cephfs-namespace-traversal-offloading)
   * [Popper](#popper)
      * [Popper / Drone workflow translation](#popper--drone-workflow-translation)
   * [OpenROAD - A Complete, Autonomous RTL-GDSII Flow for VLSI Designs](#openroad---a-complete-autonomous-rtl-gdsii-flow-for-vlsi-designs)
      * [Static RAM Generator](#static-ram-generator)
      * [VLSI Power Planning and Analysis](#vlsi-power-planning-and-analysis)
      * [Enhance project website](#enhance-project-website)
      * [Demos and Tutorials](#demos-and-tutorials)
      * [Comprehensive flow testing](#comprehensive-flow-testing)
      * [Enhance GUI features](#enhance-gui-features)
      * [Automate OpenDB code Generation](#automate-opendb-code-generation)
      * [Implement an NLP based AI bot](#implement-an-nlp-based-ai-bot)
   * [Apache AsterixDB](#apache-asterixdb)
      * [Geospatial Data Science on AsterixDB](#geospatial-data-science-on-asterixdb)
         * [The goals of this project are:](#the-goals-of-this-project-are)
         * [Machine Learning Integration](#machine-learning-integration)
   * [FasTensor](#fastensor)
      * [Continuous Integration](#continuous-integration)
   * [Polyphorm / PolyPhy](#polyphorm--polyphy)
      * [Develop website for PolyPhy](#develop-website-for-polyphy)
      * [Design visual experience for PolyPhy's website and presentations](#design-visual-experience-for-polyphys-website-and-presentations)
      * [Write PolyPhy's technical story and content](#write-polyphys-technical-story-and-content)
      * [Video tutorials and presentation for PolyPhy](#video-tutorials-and-presentation-for-polyphy)
      * [Implement heterogeneous data I/O ops](#implement-heterogeneous-data-io-ops)
      * [Setup CI/CD for PolyPhy](#setup-cicd-for-polyphy)
      * [Refine PolyPhy's UI and develop new functional elements](#refine-polyphys-ui-and-develop-new-functional-elements)
      * [Create new data visualization regimes](#create-new-data-visualization-regimes)
      * [Discrete graph extraction from simulated scalar fields](#discrete-graph-extraction-from-simulated-scalar-fields)

<!-- Added by: runner, at: Fri Dec 10 21:09:25 UTC 2021 -->

<!--te-->

## LiveHD

Projects for [LiveHD](https://github.com/masc-ucsc/livehd). Lead Mentors: Jose Renau <mailto:renau@ucsc.edu> and Sheng-Hong Wang <mailto:swang203@ucsc.edu>

### Tree sitter Pyrope

|   |   |
|---|---|
| Title | Tree-sitter Pyrope  |
| Description | Work on a tree-sitter grammar for Pyrope |
| Mentor(s) | Jose Renau|
| Skills | C++17, Parsing |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#tree-sitter-pyrope)

Using [https://github.com/tekinengin/tree-sitter-pyrope](https://github.com/tekinengin/tree-sitter-pyrope) as a starting point, complete the Pyrope grammar
to correctly parse the [Pyrope grammar](https://masc.soe.ucsc.edu/pyrope.html), interface with LiveHD
and third party tools.

Main features:

* Pyrope tree-sitter grammar
* tree-sitter to LNAST generation (Comparable to https://github.com/masc-ucsc/livehd/tree/master/inou/pyrope)
* Atom and neovim integration
* Atom go definition, highlight, and attribute
* Atom capacity to query LNAST/Lgraph generated grammar for bit-width. The incremental grammar passed to LNAST, passed to Lgraph,
  and incremental bit-width inference.
* neovim highlight, indent, fold support
* Integrate with atom-hide as extra language

In addition to the packages, there should be an iterator that use the incremental builder to support incremental changes.


### Mockturtle

|   |   |
|---|---|
| Title | Mockturtle |
| Description | Perform synthesis for graph in LiveHD using Mockturtle |
| Mentor(s) | Jose Renau|
| Skills | C++17, synthesis |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#mockturtle)

There are some issues with Mockturtle integration (new cells) and it is not using the latest Mockturtle library versions.
The goal is to use Mockturtle (https://github.com/lsils/mockturtle) with LiveHD. The main characteristics:

* Use mockturtle to tmap to LUTs
* Use mockturtle to synthesize (optimize) logic
* Enable cut-rewrite as an option
* Enable hierarchy cross optimization (hier:true option)
* Use the graph labeling to find cluster to optimize
* Re-timing
* Map to LUTs only gates and non-wide arithmetic. E.g: 32bit add is not mapped to LUTS, but a 2-bit add is mapped.
* List of resources to not map:
    * Large ALUs. Large ALUs should have an OpenWare block (hardcoded in FPGAs and advanced adder options in ASIC)
    * Multipliers and dividers
    * Barrell shifters with not trivial shifts (1-2 bits) selectable at run-time
    * memories, luts

### Query Shell

|   |   |
|---|---|
| Title | Query Shell |
| Description | Create a console app that interacts with LiveHD to query parameters about designs |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#query-shell-not-lgshell-to-query-graphs)

* Based on replxx (like lgshell)
* Query bits, ports...  like
    * https://github.com/rubund/netlist-analyzer
    * https://www.jameswhanlon.com/querying-logical-paths-in-a-verilog-design.html
* It would be cool if subsections (selected) parts can be visualized with something like https://github.com/nturley/netlistsvg
* The shell may be expanded to support simulation in the future
* Wavedrom/Duh dumps

Wavedrom and duh allows to dump bitfield information for structures. It would be interesting to explore to dump tables and bit
fields for Lgraph IOs, and structs/fields inside the module. It may be a way to integrate with the documentation generation.

Example of queries: show path, show driver/sink of, do topo traversal,....

As an interesting extension would be to have some simple embedded language (TCL or ChaiScript or ???) to control queries more
easily and allow to build functions/libraries.

### Lgraph and LNAST check pass

|   |   |
|---|---|
| Title | Lgraph and LNAST check pass |
| Description | Create a pass that check the integrity/correctness of Lgraph and LNAST |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#lgraph-and-lnast-check-pass)

Create a pass that checks that the Lgraph (and/or LNAST) is semantically
correct. The LNAST already has quite a few tests (pass.semantic), but it can be
further expanded. Some checks:

* No combinational loops
* No mismatch in bit widths
* No disconnected nodes
* Check for inefficient splits (do not split buses that can be combined)
* Transformations stages should not drop names if same net is preserved
* No writes in LNAST that are never read
* All the edges are possible. E.g: no pin 'C' in Sum_op


### unbitwidth

|   |   |
|---|---|
| Title | unbitwidth |
| Description | Not all the variables need bitwidth information. Find the small subset |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#unbitwidth-local-and-global-bitwidth)

This pass is needed to create less verbose CHISEL and Pyrope code generation.

The LGraph can have bitwidth information for each dpin. This is needed for
Verilog code generation, but not needed for Pyrope or CHISEL.  CHISEL can
perform local bitwidth inference and Pyrope can perform global bitwidth
inference.

A new pass should remove redundant bitwidth information. The information is
redundant because the pass/bitwidth can regenerate it if there is enough
details. The goal is to create a pass/unbitwidth that removes either local or
global bitwidth. The information left should be enough for the bitwidth pass to
regenerate it.

* Local bitwidth: It is possible to leave the bitwidth information in many
places and it will have the same results, but for CHISEL the inputs should be
sized. The storage (memories/flops) should have bitwidth when can not be
inferred from the inputs.

* Global bitwidth: Pyrope bitwidth inference goes across the call hierarchy.
This means that a module could have no bitwidth information at all. We start
from the leave nodes. If all the bits can be inferred given the inputs, the
module should have no bitwidth. In that case the bitwidth can be inferred from
outside.

### LNAST Opt

|   |   |
|---|---|
| Title | LNAST Opt |
| Description | Perform copy propagation, constant folding, and dce at LNAST level |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| [Link](https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#lnast-opt)

In LiveHD, LGraph has the cprop pass that performs constant folding, copy
propagation, strength reduction... and many other optimizations.


It may be useful to have a copy propagation, constant folding, and dead code
elimination in LNAST. There are several reasons:

* Doing code simplification early (LNAST is the earliest) reduces workload/steps in successive passes.
* The simulation saves checkpoints, a LNAST Opt without dead code elimination would be useful to create the intermediate values for debugging.

## Eusocial Storage Devices

As storage devices get faster, data management tasks rob the host of CPU cycles and main memory bandwidth. The [Eusocial project](https://cross.ucsc.edu/projects/eusocialpage.html) aims to create a new interface to storage devices that can leverage existing and new CPU and main memory resources to take over data management tasks like availability, recovery, and migrations. The project refers to these storage devices as “eusocial” because we are inspired by eusocial insects like ants, termites, and bees, which as individuals are primitive but collectively accomplish amazing things.

### Evaluating user space networking stacks on SmartNICs

 - **Skills:** C, Bash, performance evaluation tools (Linux perf, SystemTap, etc.)
 - **Difficulty:** Easy
 - **Mentor:** Jianshen Liu <mailto:jliu120@ucsc.edu>

The BlueField DPU as an example of SmartNICs is available nowadays. However, the performance of the kernel networking stack on this device is known to involve expensive overhead. The alternatives are to use some user-space solutions such as DPDK (for TCP and RDMA) and libvma (for RDMA). Therefore, it would be interesting to evaluate the performance differences between the kernel and these user-space alternatives, especially focusing on characterizing the benefits for SmartNICs.
 - References: Tork, Maroun, Lina Maudlej, and Mark Silberstein. "Lynx: A SmartNIC-driven accelerator-centric architecture for network servers." Proceedings of the Twenty-Fifth International Conference on Architectural Support for Programming Languages and Operating Systems. 2020.

### Dynamic function injection for RocksDB

 - **Skills:** C/C++, Java
 - **Difficulty:** Challenging
 - **Mentor:** Jianshen Liu <mailto:jliu120@ucsc.edu>

Recent research reveals that the compaction process in RocksDB can be altered to optimize future data access by changing the data layout in compaction levels. The benefit of this approach can be extended to different data layout optimization based on application access patterns and requirements. In this project, we want to create an interface that would allow users to dynamically inject layout optimization functions to RockDB, using containerization technologies such as Webassembly.
 - Reference: Saxena, Hemant, et al. "Real-Time LSM-Trees for HTAP Workloads." arXiv preprint arXiv:2101.06801 (2021).


### Demonstrating a composable storage system accelerated by memory semantic technologies

 - **Skills:** C/C++, Bash, Python, System architecture, Network fabrics
 - **Difficulty:** Challenging
 - **Mentor:** Jianshen Liu <mailto:jliu120@ucsc.edu>

Since the last decade, the slowing down in the performance improvement of general-purpose processors is driving the system architecture to be increasingly heterogeneous. We have seen the kinds of domain-specific accelerator hardware (e.g., FPAG, SmartNIC, TPU, GPU) are growing to take over many different jobs from the general-purpose processors. On the other hand, the network and storage device performance have been tremendously improved with a trajectory much outweighed than that of processors. With this trend, a natural thought to continuously scale the storage system performance economically is to efficiently utilize and share different sources from different nodes over the network. There already exist different resource sharing protocols like CCIX, CXL, and GEN-Z. Among these GEN-Z is the most interesting because, unlike RDMA, it enables remote memory accessing without exposing details to applications (i.e., not application changes). Therefore, it would be interesting to see how/whether these technologies can help improve the performance of storage systems, and to what extent. This project would require building a demo system that uses some of these technologies (especially GEN-Z) and run selected applications/workloads to better understand the benefits.
 - References: Gen-Z: An Open Memory Fabric for Future Data Processing Needs: https://www.youtube.com/watch?v=JLb9nojNS8E, Pekon Gupta, SMART Modular; Gen-Z subsystem for Linux, https://github.com/linux-genz


## Open Source Autonomous Vehicle Controller


The OSAVC is a vehicle-agnostic open source hardware and software project.  This project is designed to provide a real-time hardware controller adaptable to any vehicle type, suitable for aerial, terrestrial, marine, or extraterrestrial vehicles. It allows control researchers to develop state estimation algorithms, sensor calibration algorithms, and vehicle control models in a modular fashion such that once the hardware set has been developed switching algorithms requires only modifying one C function and recompiling.

Lead mentor: Aaron Hunter <mailto:aamuhunt@ucsc.edu>

Projects for the OSAVC:


### Vehicle/Craft sensor driver development
 - **Topics**: Driver code to integrate sensor to a microcontroller
 - **Skills**: C, I2C, SPI, UART interfaces
 - **Difficulty** Easy
 - **Mentor** Aaron Hunter


Help develop a sensor library for use in autonomnous vehicles.  Possible sensors include range finders, ping sensors, IMUs, GPS receivers, RC receivers, barometers, air speed sensors, etc. Code will be written in C using state machine methodology and non-blocking algorithms. Test the drivers on a Microchip microncontroller.

### IMU calibration algorithm development
 - **Topics**: Least Squares, DCM,
 - **Skills**: C/Python, Matlab/Simulink, numerical optimzation algorithms
 - **Difficulty** Medium
 - **Mentor** Aaron Hunter


The IMU is a sensor comprising nine separate sensors in a single package, including acceleromeeters, gyroscopes, and magnetometer. Using a model for sensor errors, develop calibration algorithms that characterize these errors and provide optimal estimates of the true sensor reading.  Provide an algorithm in C or Python to implement this efficiently on a microcontroller or single board computer (e.g., Raspberry Pi).

### Path finding algorithm using OpenCV
 - **Topics**: Computer vision, blob detection
 - **Skills**: C/Python, OpenCV
 - **Difficulty** Medium
 - **Mentor** Aaron Hunter


Use OpenCV to identify a track for an autonomous vehicle to follow.  For example, a closed circuit course for an autonomous race car might be demarcated by different colored cones indicating the left and right boundaries of the track.  Use OpenCV to find and track the location of these cones as the car navigates the course. Implement initially on a laptop using video frames.  Ideally, transfer the algorithm to a Raspberry Pi and test on a real track.


### State estimation/sensor fusion algorithm development
 - **Topics**: Kalman filtering, Mahoney
 - **Skills**: C/Python, Matlab/Simulink, numerical optimzation algorithms
 - **Difficulty** Challenging
 - **Mentor** Aaron Hunter


Implement an optimal state estimation algorithm from a model.  This model can be derived from a Kalman filter or some other state estimation filter (e.g., Mahoney filter).  THe model takes sensor readings as input and provides an estimate of the state of a vehicle. Finally, convert the model to standard C using the Simulink code generation or implement in Python (for use on a single board computer, e.g., Raspberry Pi)

### Vehicle dynamic model development
 - **Topics**: Dynamic modeling, control theory
 - **Skills**: C, Matlab/Simulink
 - **Difficulty** Challenging
 - **Mentor** Aaron Hunter


Help develop the library of models for autonomous vehicles. Develop a dynamic model of a vehicle based on standard vehicle types, e.g., differential-drive vehicle, surface vehicle (boat), quadcopter, etc.  Models to be developed in Matlab and ported to standard C.

## SkyhookDM

[SkyhookDM](http://www.skyhookdm.com)

The Skyhook Data Management project extends object storage with data
management functionality for tabular data. SkyhookDM enables storing and query
database tables in Ceph distributed object storage.  SkyhookDM is an
[Apache Arrow](https://arrow.apache.org) native
storage system that utilizes the Arrow Dataset API to store and query data,
and our Ceph extensions support server-side data processing. For example,
pushing down SELECT, PROJECT and other functionality into storage to reduce
data returned to the client.

-------------------

### Add Ability to create and save views from Datasets

  - **Topics**: `Arrow`, `Database views`, `virtual datasets`
  - **Skills**: C++
  - **Difficulty**: Medium
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>, [Ivo Jimenez](https://ivotron.me/) [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)

Problem - Workloads may repeat the same or similar queries over time. This causes repetition of IO and compute operations, wasting resources.  
Saving previous computation in the form of materialized views can provide benefit for future
workload processing.
Solution - Add a method to the Dataset API to create views from queries and save the view as an object in a separate pool with some object key that can be generated from the query that created it.

Reference:
https://docs.dremio.com/working-with-datasets/virtual-datasets.html

-------

### Ability to Push back query execution to the Client in case of overloaded OSDs

  - **Topics**: `Arrow`, `query opererators`, `push down computation`
  - **Skills**: C++
  - **Difficulty**: High
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>, [Ivo Jimenez](https://ivotron.me/) [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)

Problem - Currently, SkyhookDM v0.1.0 just allows pushing down Compute operations such as selection and projection into the Storage layer (i.e the Ceph Object Storage Devices). With a large number of clients trying to push down computation into the OSDs at a time, the CPU and Memory pressure of the OSDs may quickly increase causing run-time side effects such as blocked and slow OSD operations.  
Solution - We can modify the Dataset API by adding a method to check the resource utilization on the Storage side periodically and if the CPU and Memory usage passes a user-defined threshold or some other metrice, the Datasets API silently shifts to client side query execution for a while and then tries to push down again.  This method could also be applied dynamically at the OSD, allowing the OSD to reject certain operations, returning metadata concerning which operations have not yet been applied.

Reference:
https://github.com/uccross/skyhookdm-ceph/blob/skyhook-luminous/src/cls/tabular/cls_tabular.h#L1104


-------

### Port wiki to ReadTheDocs or other documentation platform

  - **Topics**: `Documentation`, `wiki`, `markdown`
  - **Skills**: Markdown, documentation, html
  - **Difficulty**: Easy
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>, [Ivo Jimenez](https://ivotron.me/) [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)

SkyhookDM's documentation is [currently written](https://github.com/uccross/skyhookdm-ceph/wiki)
as Github Wiki pages. We would like to move it to another platform such as
[ReadTheDocs](https://readthedocs.org),
to reorganize it and rewrite some sections as part of this effort.
[Github issue](https://github.com/uccross/skyhookdm-ceph-cls/issues/42).

-------

### Integrating Delta Lake on top of SkyhookDM

  - **Topics**: `data lakes`, `lake house`, `distributed query processing`
  - **Skills**: C++
  - **Difficulty**: Medium
  * **Mentor**: [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)

[Delta Lake](https://delta.io/) is a new architecture for querying big data lakes through Spark, providing transactions.
An important benefit of this integration will be to provide an SQL interface for SkyhookDM functionality, through Spark SQL.
This project will further build upon our current work connecting Spark to SkyhookDM through the Arrow Dataset API.
This would allow us to run some of the TPC-DS queries (popular set of SQL queries for benchmarking databases) on SkyhookDM easily.

Reference: [Delta Lake paper] (https://databricks.com/jp/wp-content/uploads/2020/08/p975-armbrust.pdf)

-------


### Write Helm charts for easy deployment of the SkyhookDM, Dask , ServiceX stack on Kubernetes

  - **Topics**: `helm charts lakes`, `deployment`, `Dask`, `Kubernetes`
  - **Skills**: C++
  - **Difficulty**: Medium
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>, [Ivo Jimenez](https://ivotron.me/) [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)

Problem - In the IRIS-HEP DOMA project, SkyhookDM will be used to act as a lake house where data will be ingested from ServiceX. The Data stored in SkyhookDM will be processed by Coffea through several Dask workers. The deployment of this 3 layered end-to-end system is quite cumbersome and inefficient if done manually. Most importantly, it's a blockage to someone who would like to test out the entire system very quickly.

Solution - We can write Helm charts to easily deploy this end-to-end system on Kubernetes with just a few Helm commands. The goal is to deploy ServiceX, SkyhookDM, and Dask workers and ensure they can communicate with one another. We can expose the system to the end-users via a Jupyter notebook with some getting started code/guide.

Reference:
https://www.youtube.com/watch?v=Zzwq9FmZdsU&t=2s
https://arxiv.org/pdf/2103.01871.pdf


-------
### Facilitate continuous benchmarking/regression testing for the critical components of SkyhookDM

  - **Topics**: `helm charts lakes`, `deployment`, `Dask`, `Kubernetes`
  - **Skills**: C++
  - **Difficulty**: Medium
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>, [Ivo Jimenez](https://ivotron.me/) [Jayjeet Chakraboorty](https://iris-hep.org/fellows/JayjeetChakraborty.html)


Problem - SkyhookDM,  which is a computational storage system built by embedding Apache Arrow is a performance critical distributed storage system. Often small changes in the performance critical parts of the source code can cause significant performance changes. It is very important to properly track these performance changes in order to allow the project to evolve more performant and prevent silent degradation in performance over time.

Solution - We can use the Google benchmark framework to create benchmarks (very similar to unit tests) for all the performance critical parts of the source code. These benchmarks would be run on CI via Github workflows and would allow us to track the performance changes caused by every commit/pull request. We can also create a nice little web dashboard to visualize the performance results uploaded from the CI. But maybe this is another project on it’s own.

Reference :
https://arxiv.org/pdf/1812.03149.pdf


-------


## HDF5

[HDF5](https://portal.hdfgroup.org/display/knowledge/What+is+HDF5) is a unique technology suite that makes possible the management of extremely large and complex data collections.

The HDF5 technology suite includes:
* A versatile data model that can represent very complex data objects and a wide variety of metadata.
* A completely portable file format with no limit on the number or size of data objects in the collection.
* A software library that runs on a range of computational platforms, from laptops to massively parallel systems, and implements a high-level API with C, C++, Fortran 90, and Java interfaces.
* A rich set of integrated performance features that allow for access time and storage space optimizations.
* Tools and applications for managing, manipulating, viewing, and analyzing the data in the collection.



-------------------

### HDF5 - Apache Arrow Integration

  * **Topics**: `VOL connector`, `streaming data`, `column store`
  * **Skills**: C, HDF5, Apache Arrow
  * **Difficulty**: Medium
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

[Apache Arrow](https://arrow.apache.org) creates in-memory column stores that can be used to manage streamed data.
Accessing this data through the HDF5 API would allow applications to take advantage of transient, column-oriented
data streams, such as realtime data from high-speed scientific instruments and cameras.  Bridging the gap between
science applications and analytics tools that use HDF5 and Apache Arrow data streams could bring new kinds of tools
and data together.  This project will create a standalone HDF5 [VOL connector](https://portal.hdfgroup.org/display/HDF5/Virtual+Object+Layer)
that allows applications to make HDF5 calls to access Apache Arrow data.

-------

### HDF5 - Ceph RADOS Integration

  * **Topics**: `VOL connector`, `Ceph`, `object storage`
  * **Skills**: C, HDF5, Ceph / RADOS
  * **Difficulty**: Medium
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

The [Ceph](https://ceph.io) distributed storage system provides object, block, and file system layer interfaces.
A prototype HDF5 [VOL connector](https://portal.hdfgroup.org/display/HDF5/Virtual+Object+Layer) has been developed
to access the [RADOS](https://ceph.io/geen-categorie/the-rados-distributed-object-store/) object storage layer, enabling
HDF5 objects (datasets, groups, etc) to be directly stored as RADOS objects.  This project would expand the capabilities
of this VOL connector, enabling HDF5 applications to store data directly in RADOS pools.

-------

### Column-storage in HDF5

  * **Topics**: `HDF5`, `column-store`
  * **Skills**: C, HDF5
  * **Difficulty**: High
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

[Column-oriented storage](https://en.wikipedia.org/wiki/Column-oriented_DBMS) provides efficient access to fields within
records, across many rows.  Adding this storage method to HDF5 would dramatically improve performance for applications that
primarily access subsets of the fields in an HDF5 dataset.

-------

### Sparse data storage in HDF5

  * **Topics**: `HDF5`, `sparse data`
  * **Skills**: C, HDF5
  * **Difficulty**: High
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

[Sparse matrices](https://en.wikipedia.org/wiki/Sparse_matrix) have applications in many fields within science and mathematics.
Storing and accesssing them in HDF5 is inefficient though, as HDF5 is currently optimized for storing dense arrays.
Adding efficient storage of sparse data in HDF5 would dramatically improve performance for applications that wish to store and
access sparse data.  This could extend beyond sparse matrices proper, and include any form of sparsely populated array or table.

-------

### Metadata search in HDF5 with Database Solutions

  * **Topics**: `HDF5`, `search`, `index`, `database`
  * **Skills**: HDF5, Database Integration
  * **Difficulty**: Medium
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

[Relational databases](https://en.wikipedia.org/wiki/Relational_database) excel at many tasks, one of which is content queries.
HDF5 does not currently have good methods for indexing and searching available to user applications, although protoyping work
has been performed in a [git branch](https://bitbucket.hdfgroup.org/projects/HDFFV/repos/hdf5/branches?base=feature%2Findexing).
Instead of adding index and query operations directly to HDF5, this project would instead connect a database package, such as
[RocksDB](https://rocksdb.org) or [VoltDB](https://www.voltdb.com), with HDF5 and perform query and index operations in the
database and array-oriented I/O with HDF5.

## Proactive Data Containers (PDC)

[Proactive Data Containers](https://sdm.lbl.gov/pdc/about.html) (PDC) are containers within a locus of storage (memory, NVRAM, disk, etc.) that store science data in an object-oriented manner.  Managing data as objects enables powerful optimization opportunities for data movement and
transformations, and storage mechanisms that take advantage of the deep storage hierarchy and enable automated performance tuning

-------------------

### Python interface to an object-centric data management system

  * **Topics**: `Python`, `object-centric data management`, `PDC`
  * **Skills**: Python, C, PDC
  * **Difficulty**: Medium
  * **Mentor**: Suren Byna <mailto:sbyna@lbl.gov>, Houjun Tang <mailto:htang4@lbl.gov>

[Proactive Data Containers (PDC)](https://sdm.lbl.gov/pdc/about.html) is an object-centric data management system for scientific data on high performance computing systems. It manages objects and their associated metadata within a locus of storage (memory, NVRAM, disk, etc.). Managing data as objects enables powerful optimization opportunities for data movement and transformations, and storage mechanisms that take advantage of the deep storage hierarchy and enable automated performance tuning. Currently PDC has a C interface. Providing a python interface would make it easier for more Python applications to utilize it.


## CephFS
[CephFS](https://docs.ceph.com/en/latest/cephfs/) is a distributed file system on top of [Ceph](https://ceph.io). It is implemented as a distributed metadata service (MDS) that uses dynamic subtree balancing to trade parallelism for locality during a continually changing workloads. Clients that mount a CephFS file system connect to the MDS and acquire capabilities as they traverse the file namespace. Capabilities not only convey metadata but can also implement strong consistency semantics by granting and revoking the ability of clients to cache data locally.

### CephFS namespace traversal offloading

  * **Topics**: `Ceph`, `filesystems`, `metadata`, `programmable storage`
  * **Skills**: C++, Ceph / MDS
  * **Difficulty**: Medium
  * **Mentor**: [Carlos Maltzahn](https://people.ucsc.edu/carlosm) <mailto:carlosm@ucsc.edu>

The frequency of metadata service (MDS) requests relative to the amount of data accessed can severely affect the performance of distributed file systems like CephFS, especially for workloads that randomly access a large number of small files as is commonly the case for machine learning workloads: they purposefully randomize access for training and evaluation to prevent overfitting. The datasets of these workloads are read-only and therefore do not require strong coherence mechanisms that metadata services provide by default.

The key idea of this project is to reduce the frequency of MDS requests by offloading namespace traversal, i.e. the need to open a directory, list its entries, open each subdirectory, etc. Each of these operations usually require a separate MDS request. Offloading namespace traversal refers to a client’s ability to request the metadata (and associated read-only capabilities) of an entire subtree with one request, thereby offloading the traversal work for tree discovery to the MDS.

Once the basic functionality is implemented, this project can be expanded to address optimization opportunities, e.g. describing regular tree structures as a closed form expression in the tree’s root, shortcutting tree discovery.

## Popper

[Popper](https://getpopper.io) is a container-native task automation engine that runs on distinct container engines, orchestration frameworks and CI services. Write simple YAML files, run everywhere.

### Popper / Drone workflow translation

  * **Topics**: `Popper`, `drone.io`, `workflow`, `reproducibility`, `containers`, `cloud native`
  * **Skills**: YAML, Python, Docker
  * **Difficulty**: Easy
  * **Mentor**: [Carlos Maltzahn](https://people.ucsc.edu/carlosm) <mailto:carlosm@ucsc.edu>

[Drone](https://github.com/drone) is a Container-Native, Continuous Delivery Platform with a similar functionality as Popper. In some areas Drone is more mature than Popper, but Popper is easier to debug. Both specify workflows in easy-to-read YAML files. The goal of this project is to be able to easily switch between Popper and Drone, e.g. to debug Drone workflows with Popper. This can be accomplished by implementing a translator that converts a Popper workflow into a Drone workflow and vice versa.

## OpenROAD - A Complete, Autonomous RTL-GDSII Flow for VLSI Designs
[OpenROAD](https://theopenroadproject.org) is a DARPA supported initiative through the IDEA program, that delivers an open sourced ecosystem of a complete and autonomous VLSI design flow from from RTL-GDSII, that fosters innovation and easy access of design kits and software access for VLSI designers.

OpenROAD's flow reduces cost and uncertainty barriers of commercial tools and enables a collaborative and democratized approach to learning and sharing of leading edge VLSI design and software methodologies. The OpenROAD flow aims at a rapid (less than 24 hour) design  turnaround time  with minimal human intervention. This is made possible through key innovations like the usage of distributed processing using Cloud resources, an adaptive ML based auto-tuning capability that allows the flow to self-adjust key design parameters for rapid convergence to good results.

OpenROAD is the key enabler of successful Chip initiatives like the Google-sponsored [Efabless](efabless.com) that has made possible more than 140 successful tapeouts across a world wide and broad user community. The OpenROAD project repository is https://github.com/The-OpenROAD-Project/OpenROAD.

### Static RAM Generator

  * **Topics**: `Memory Compilers`, `OpenRAM`, `Programmable RAM`
  * **Skills**: python, basic knowledge of memory design, VLSI technology, PDK, Verilog
  * **Difficulty**: Medium
  * **Mentor**: Mehdi Saligane <mailto:mehdi@umich.edu>, Matt Liberty <mailto:mliberty@eng.ucsd.edu>

Design of  static RAMs in VLSI designs for good performance and area is generally time-consuming. Memory compilers significantly reduce design time for complex analog and mixed-signal designs by allowing designers to explore, verify and configure multiple variants and hence select a design that is optimal for area and performance. This project requires the support of memory compilers to [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) based on popular PDKS. See link for details:[OpenRAM](https://openram.soe.ucsc.edu)

### VLSI Power Planning and Analysis

  * **Topics**: `Power Planning for VLSI`, `IR Drop Analysis`, `Power grid Creation and Analysis`
  * **Skills**: C++, tcl, VLSI Layout
  * **Difficulty**: Medium
  * **Mentor**: Mehdi Saligane <mailto:mehdi@umich.edu>, Ming-Hung  <mailto:minghung@umich.edu>

Take the existing power planning (pdngen.tcl) module of openroad and recode the functionality in C++ ensuring that all of the unit tests on the existing code pass correctly. Work with a senior member of the team at ARM. Ensure that designs created are of good quality for power routing and overall power consumption.

###  Enhance project website

  * **Topics**: `Web Development`, `Dynamic updates`, `AI bot`
  * **Skills**: Web development experience
  * **Difficulty**: Easy
  * **Mentor**: Vitor Bandeira <mailto:vvbandeira@eng.ucsd.edu>, Indira Iyer Almeida <mailto:dralabeing@openroad.tools>

The [OpenROAD](https://theopenroadproject.org/) project serves a wide user community by providing free access and learning of open sourced VLSI design tools and a knowledge base. The project website needs to be updated to enhance information access, useful resources and links with analytics to provide useful information for enhanced user engagement.

###  Demos and Tutorials

  * **Topics**: `Demo Development`, `Documentation`, `VLSI design basics`
  * **Skills**:  Knowledge of EDA tools, basics of VLSI design flow, tcl, shell scripts, Documentation, Markdown
  * **Difficulty**: Medium
  * **Mentor**: Indira Iyer Almeida <mailto:dralabeing@openroad.tools>, Vitor Bandeira <mailto:vvbandeira@eng.ucsd.edu>

For [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts), develop demos showing:
The basic usage of OpenROAD features and flow
GUI visualizations
Different options and how they impact the results
Different design styles and particular challenges

### Comprehensive flow testing

  * **Topics**: `Demo Development`, `Documentation`, `VLSI design basics`
  * **Skills**:  Knowledge of EDA tools, basics of VLSI design, tcl, shell scripts, Verilog, Layout
  * **Difficulty**: Medium
  * **Mentor**: Tom Spyrou <mailto:aspyrou@eng.ucsd.edu>, Indira Iyer Almeida <mailto:dralabeing@openroad.tools>

Add open sourced designs to existing test suite for the OpenROAD flow to expand coverage and technology capabilities. This includes design specification, configuration and creation of all necessary files for regression testing. Souruggested sources : ICCAS benchmarks, opencores, LSOracle for synthesis flow option.

### Enhance GUI features

  * **Topics**: `GUI`, `Visualization`, `User Interfaces`
  * **Skills**:  C++, Qt
  * **Difficulty**: Medium
  * **Mentor**: Matt Liberty <mailto:<mailto:mliberty@eng.ucsd.edu>>, Vitor Bandeira <mailto:vvbandeira@eng.ucsd.edu>

For [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD), develop and enhance visualizations for EDA data and algorithms in the OpenROAD GUI. Allow deeper understanding of the tool results for users and tool internals for developers.

### Automate OpenDB code Generation

  * **Topics**: `Database`, `EDA`
  * **Skills**:  C++, Python, JSON, Jinja templating
  * **Difficulty**: Medium
  * **Mentor**: Matt Liberty <mailto:mliberty@eng.ucsd.edu>, Tom Spyrou <mailto:aspyrou@eng.ucsd.edu>

For [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD)- Automatic code generation for the OpenDB database which allows improvements to the data model with much less hand coding.  Allow the generation of storage, serialization, and callback code from a custom schema description format.

### Implement an NLP based AI bot

  * **Topics**: `AI`, `ML`, `Analytics`
  * **Skills**:   Python. ML libraries (e.g., Tensorflow, PyTorch)
  * **Difficulty**: Medium
  * **Mentor**: Vitor Bandeira <mailto:vvbandeira@eng.ucsd.edu>, Indira Iyer Almeida <mailto:dralabeing@openroad.tools>

The [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD) project and several of it's repositories see a good amount of useful discussion in it’s issues and slack channels. Implement an AI analytics bot that picks relevant discussions and classifies/records them into useful documentation and actionable issues.

## Apache AsterixDB

AsterixDB is an open source parallel big-data management system [http://asterixdb.apache.org/]. AsterixDB is a well-established Apache project that has been active in research for more than 10 years. It provides a flexible data model that supports modern NoSQL applications with a powerful query processor that can scale to billions of records and terabytes of data. Users can interact with AsterixDB through a power and easy to use declarative query language, SQL++, which provides a rich set of data types including timestamps, time intervals, text, and geospatial, in addition to traditional numerical and Boolean data types.

### Geospatial Data Science on AsterixDB

- *Topics*: Data science, SQL++, documentation
- *Skills*: SQL, Writing, Spreadsheets
- *Difficulty*: Medium
- *Mentors*: [Ahmed Eldawy](mailto:eldawy@ucr.edu), [Akil Sevim](mailto:asevi006@ucr.edu)

Build a data science project using AsterixDB that analyzes geospatial data among other dimensions. Use [Chicago Crimes](https://star.cs.ucr.edu/?Chicago%20Crimes#center=41.8313,-87.6830&zoom=11) as the main dataset and combine with other datasets including [points of interests](https://star.cs.ucr.edu/?osm21/pois#center=41.8313,-87.6830&zoom=11) [ZIP Code boundaries](https://star.cs.ucr.edu/?TIGER2018/ZCTA5#center=41.8313,-87.6830&zoom=11). During this project, we will answer interesting questions about the data and visualize the results such as:

- What is the most common crime type in a specific date or over the weekends?
- Where do most of the arrests happen?
- How are the crime rates change over time for different regions?

#### The goals of this project are:

- Understand how to build a scalable data science project using AsterixDB.
- Translate common questions to SQL queries and run them on large data.
- Learn how to visualize the results of queries and present them.
- Write detailed documentation about the process of building a data science application in AsterixDB.
- Improve the documentation of AsterixDB while working in the project to improve the experience for future users.

#### Machine Learning Integration
As a bonus task, and depending on the progress of the project, we can explore the integration of machine learning with AsterixDB through Python UDFs. We will utilize the AsterixDB Python integration through [user-defined functions](https://asterixdb.apache.org/docs/0.9.7/udf.html) to connect AsterixDB backend with [scikit-learn](https://scikit-learn.org/stable/index.html) to build some unsupervised and supervised models for the data. For example, we can cluster the crimes based on their location and other attributes to find interesting patterns or hotspots.

## FasTensor
[FasTensor](https://sdm.lbl.gov/fastensor/) is a parallel execution engine for user-defined functions on multidimensional arrays.  The user-defined functions follow the stencil metaphor used for scientific computing and is effective for expressing a wide range of computations for data analyses, including common aggregation operations from database management systems and advanced machine learning pipelines.  FasTensor execution engine exploits the structural-locality in the multidimensional arrays to automate data management operations such as file I/O, data partitioning, communication, parallel execution, and so on.

### Continuous Integration

  * **Topics**: `Data Management`, `Analytics`
  * **Skills**:   C++, github
  * **Difficulty**: Easy
  * **Mentor**: [John Wu](mailto:kwu@lbl.gov), [Bin Dong](mailto:dbin@lbl.gov), [Suren Byna](mailto:sbyna@lbl.gov)
 
- Develop a test suite for the public API of FasTensor
- Automate execution of the test suite
- Document the continuous integration process
- Develop performance testing suite

## Polyphorm / PolyPhy

[Polyphorm](https://github.com/CreativeCodingLab/Polyphorm) is an agent-based system for reconstructing and visualizing *optimal transport networks* defined over sparse data. Rooted in astronomy and inspired by nature, we have used Polyphorm to reconstruct the Cosmic web structure, but also to discover network-like patterns in natural language data. You can find more details about our research [here](https://elek.pub/research.html). Under the hood, Polyphorm uses a richer 3D scalar field representation of the reconstructed network, instead of a discrete representation like a graph or a mesh.

**PolyPhy** will be a Python-centric redesigned version of Polyphorm, currently in the beginning of its development cycle. PolyPhy will be a multi-platform toolkit meant for a wide audience across different disciplines: astronomers, neuroscientists, data scientists and even artists and designers. All of the offered projects focus on PolyPhy, with a variety of topics including design, coding, and even research. Ultimately, PolyPhy will become a tool for discovering connections between different disciplines by creating quantitatively comparable structural analytics.

### Develop website for PolyPhy

- **Topics:** `Web Development` `Dynamic Updates` `UX`
- **Skills:** web development experience, good communicator, (HTML/CSS), (Javascript)
- **Difficulty:** Moderate
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Develop a clean and welcoming website for the project. The organization needs to reflect the needs of PolyPhy users, but also provide a convenient entry point for interested project contributors. No excessive pop-ups or webjunk.

Specific tasks:
- Work with mentors on understanding the context of the project.
- Port the contents of the [repository page](https://github.com/CreativeCodingLab/Polyphorm) to a dedicated website.
- Design the structure of the website according to best OS practices.
- Work with the visual designer (see below) in creating a coherent and organic presentation.
- Interactively link important metrics from the project dev environment as well as documentation.

### Design visual experience for PolyPhy's website and presentations

- **Topics:** `Design` `Art` `UX`
- **Skills:** vector and bitmap drawing, sense for spatial symmetry and framing, (interactive content creation), (animation)
- **Difficulty:** Moderate
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Develop visual content for the project using its main themes: nature-inspired computation, biomimetics, interconnected structures. Aid in designing visual structure of the website as well as other public-facing artifacts.

Specific tasks:
- Work with mentors on understanding the context of the project.
- Design imagery and other graphical elements to visually (re-)present PolyPhy.
- Work with the technical writer (see below) in designing a coherent story.
- Work with the web developer (see above) in creating a coherent and organic presentation.

### Write PolyPhy's technical story and content

- **Topics:** `Writing` `Documentation` `Storytelling`
- **Skills:** experienced writing structured text over 10 pages, well read, (technical or scientific education)
- **Difficulty:** Moderate-Challenging
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Integral to PolyPhy's presentation is a story that the users and the project contributors can relate to. The objective is to develop the verbal part of that story, as well as major portions of technical documentation that matches it. The difficulty of the project is scalable.

Specific tasks:
- Work with mentors on understanding the context of the project.
- Write different pages of the project website.
- Work with mentors to improve project's written community practices (diversity, communication).
- Write and edit narrative and explanatory parts of PolyPhy's documentation.
- Work with the visual designer (see above) in designing a coherent story.

### Video tutorials and presentation for PolyPhy

- **Topics:** `Video Presentation` `Tutorials` `Didactics`
- **Skills:** video editing, creating educational content, communication, (native or fluent in another language)
- **Difficulty:** Easy-Moderate
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Create a public face for PolyPhy that reflects its history, context, and teaches its functionality to users in different degrees of familiarity.

Specific tasks:
- Work with mentors on understanding the context and history of the project.
- Interview diverse project contributors.
- Create a video documenting PolyPhy's history, with roots in astronomy, complex systems, fractals.
- Create a set of tutorial videos for starting and intermediate PolyPhy users.
- Create an accessible template for future tutorials.

### Implement heterogeneous data I/O ops

- **Topics:** `I/O Operations` `File Conversion` `Numerics` `Testing`
- **Skills:** Python, experience working with scientific or statistical data, good debugging skills
- **Difficulty:** Moderate-Challenging
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu), [Anisha Goel](mailto:anishagoel14@gmail.com)

By default, PolyPhy operates with an unordered set of points as an input and scalar fields (float ndarrays) as an output, but others are applicable as well. Design and implement interfaces to load and export different data formats (CSV, OBJ, HDF5, FITS...) and modalities (points, meshes, density fields). The difficulty of the project can be scaled based on contributor's interest.

Specific tasks:
- Research which modalities are used by members of the target communities.
- Implement modular loaders for the inputs and an interface to PolyPhy core.
- Implement exporters for simulation datasets and visualization captures.
- Write testing code for the above.
- Integrate external packages as necessary.

### Setup CI/CD for PolyPhy

- **Topics:** `Continuous Integration` `Continuous Deployment` `DevOps`
- **Skills:** experience with CI/CD, GitHub, Python package deployment
- **Difficulty:** Moderate
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu), [Anisha Goel](mailto:anishagoel14@gmail.com)

The objective is to setup a CI/CD pipeline that automates the build testing and deployment of the software. The resulting process needs to be robust to contributor errors and work in the distributed conditions of a diverse contributor base.

Specific tasks:
- Automate continuous building, testing, merging and deployment for PolyPhy in GitHub.
- Publish the CI/CD metrics and build assets to the project webpage.
- Work with other contributors in educating them about the best practices of using the developed CI/CD pipeline.
- Add support for automated packaging using common management systems (pip, Anaconda).

### Refine PolyPhy's UI and develop new functional elements

- **Topics:** `UI/UX` `Visual Experience`
- **Skills:** Python programming, UI/UX development experience, (knowledge of graphics)
- **Difficulty:** Moderate
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

The key feature of PolyPhy is its interactivity. By interacting with the underlying simulation model, the user can adjust its parameters in real time and respond to its behavior. For instance, an astrophysics expert can load a dataset of 100k galaxies and reconstruct the large-scale structure of the intergalactic medium. A responsive UI combined with real-time visualization allows them to judge the fidelity of the reconstruction and make necessary changes.

Specific tasks:
- Implement a platform-agnostic UI to house PolyPhy's main rendering context as well as secondary analytics.
- Work with the visualization developer (see below) to integrate the rendering functionality.
- Optimize to UI's performance.
- Test the implementation on different OS platforms.

### Create new data visualization regimes

- **Topics:** `Interactive Visualization` `Data Analytics` `3D Rendering`
- **Skills:** basic graphics theory and math, Python, GPU programming, (previous experience visualizing novel datasets)
- **Difficulty:** Challenging
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Data visualization is one of the core components of PolyPhy, as it provides a real-time overview of the underlying MCPM simulation. Through the feedback provided by the visualization, PolyPhy users can adjust the simulation model and make new findings about the dataset. Various operations over the reconstructed data (e.g. spatial searching) as well as important statistical summaries also benefit from clear visual presentation.

Specific tasks:
- Develop novel ways of visualizing scientific data in PolyPhy.
- Work with diverse data modalities - point clouds, graphs, scalar and vector fields.
- Add support for visualizing metadata, such as annotations and labels.
- Create UI elements for plotting statistical summaries computed in real-time.

### Discrete graph extraction from simulated scalar fields

- **Topics:** `Graph Theory` `Data Science`
- **Skills:** good understanding of discrete math and graph theory, Python, (GPU programming)
- **Difficulty:** Challenging
- **Mentors:** [Oskar Elek](mailto:oelek@ucsc.edu)

Develop a custom method for graph extraction from scalar field data produced by PolyPhy. Because PolyPhy typically produces network-like structures, representing these structures as weighted discrete graphs is very useful for efficiently navigating the data. The most important property of this abstracted representation is that it preserves the topology of the base scalar field by navigating the 1D ridges of the scalar field.

Specific tasks:
- Become familiar with different algorithms for graph growing and skeleton extraction.
- Implement the most suitable method in PolyPhy, interpreting the source scalar field as a throughput (transport) network. The weights of the resulting graph need to reflect the source throughputs between the respective node locations.
- Implement common graph operations, e.g. hierarchical clustering and reduction, shortest path between two nodes, range queries.
- Optimize the runtime of the implemented methods.
- Work with the visualization developer (see above) to visualize the resulting graphs.

## DirtViz

DirtViz is a project to visualize data collected from
sensors deployed in sensor networks. We have deployed a number of
sensors measuring qualities like soil moisture, temperature, current
and voltage in outdoor settings. This project involves extending (or
replacing) our existing plotting scripts to create a fully-feledged
dataviz tool tailored to the types of data collected from embedded
systems sensor networks.

### Visualize Sensor Data

  * **Topics**: `Data Visualization`, `Analytics`
  * **Skills**:  javascript,  python, bash, webservers, git, embedded systems
  * **Difficulty**: Easy/Moderate
  * **Mentor**: [Colleen Josephson](mailto:cjosephson@ucsc.edu)

- Develop set of visualization tools (ideally web based) that easily allows users to zoom in on date ranges, change axes, etc.
- Document the tool thoroughly for future maintenance
- If interested, we are also interested in investigating correlations between different data streams
- ????
- PROFIT!!