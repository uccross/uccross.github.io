<img src="HiRes-Vector.png" alt="Logo of the Center for Research in Open Source Software" valign="middle" />

# Open Source Project Ideas

<img src="OSRE2021image.jpg" alt="Light bulb with digital business interface" valign="middle" />

This list of projects are meant for student and other up-and-coming developers interested in contributing to any of the CROSS supported projects. The list below notes the CROSS project and ideas associated to each that were submitted by a CROSS mentor. If you are interested in any of these projects, please [read this](https://uccross.github.io/getinvolved) on how to get involved. If you have any questions, please visit our Gitter channel: [![Join the chat at 
https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

CROSS will be applying for Google Summer of Code 2021; we also support student work through our [Summer Undergraduate Research Program in Open Source Projects at UCSC](https://cross.ucsc.edu/programs/summerprogram2020.html). More on both of these Summer 2021 programs will be available in late February.

Table of contents:

- [LiveHD](#livehd)
  * [Tree-sitter Pyrope](#tree-sitter-pyrope)
  * [Mockturtle](#mockturtle)
  * [Query Shell](#query-shell)
  * [Lgraph and LNAST check pass](#lgraph-and-lnast-check-pass)
  * [Terminal record replay](#terminal-record-replay)
  * [OS X Alpine Linux Support](#os-x-alpine-linux-support)
  * [Random CHISEL Verilog Pyrope generator](#random-chisel-verilog-pyrope-generator)
  * [unbitwidth](#unbitwidth)
  * [gRPC Client](#grpc-client)
  * [LNAST Opt](#lnast-opt)

- [Open Source Autonomous Vehicle Controller](#open-source-autonomous-vehicle-controller)
  * [Vehicle/Craft sensor driver development](#vehicle-craft-sensor-driver-development)
  * [IMU calibration algorithm development](#imu-calibration-algorithm-development)
  * [State estimation/sensor fusion algorithm development](#state-estimation-sensor-fusion-algorithm-development)
  * [Vehicle dynamic model development](#vehicle-dynamic-model-development)
  
- [Eusocial Storage Devices](#eusocial-storage-devices)
  * [Evaluating user-space networking stacks on SmartNICs](#evaluating-user-space-networking-stacks-on-smartnics)
  * [Demonstrating a composable storage system accelerated by memory-semantic technologies](#demonstrating-a-composable-storage-system-accelerated-bymemory-semantic-technologies)


- [SkyhookDM](#-skyhookdm--http---wwwskyhookdmcom-)
  * [Ingest data via Python convert to pyarrow tables horizonally partition and write to SkyhookDM](#ingest-data-via-python-convert-to-pyarrow-tables-horizonally-partition-and-write-to-skyhookdm)
  * [Compaction of formatted database partitions within objects](#compaction-of-formatted-database-partitions-within-objects)
  * [Port wiki to ReadTheDocs or other documentation platform](#port-wiki-to-readthedocs-or-other-documentation-platform)
  * [Database statistics collection on partitioned data](#database-statistics-collection-on-partitioned-data)
  * [Add support for a relevant subset of operations on List data types](#add-support-for-a-relevant-subset-of-operations-on-list-data-types)
- [SkyhookDM/HDF5](#-skyhookdm--http---wwwskyhookdmcom---hdf5--https---portalhdfgrouporg-display-knowledge-what-is-hdf5-)
  * [HDF5 - Apache Arrow Integration](#hdf5---apache-arrow-integration)
  * [HDF5 - Ceph RADOS Integration](#hdf5---ceph-rados-integration)
  * [Column-storage in HDF5](#column-storage-in-hdf5)
  * [Sparse data storage in HDF5](#sparse-data-storage-in-hdf5)
  * [Metadata search in HDF5 with Database Solutions](#metadata-search-in-hdf5-with-database-solutions)
- [SkyhookDM/Proactive Data Containers (PDC)](#-skyhookdm--http---wwwskyhookdmcom---proactive-data-containers--https---sdmlblgov-pdc-abouthtml---pdc-)
  * [PDC - Ceph RADOS Integration](#pdc---ceph-rados-integration)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

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
| Link | 	https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#tree-sitter-pyrope |

Using https://github.com/tekinengin/tree-sitter-pyrope as a starting point, complete the Pyrope grammar
to correctly parse the Pyrope grammar (https://masc.soe.ucsc.edu/pyrope.html), interface with LiveHD
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
| Link | 	https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#mockturtle |

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
| Link | 	https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#query-shell-not-lgshell-to-query-graphs |

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
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#lgraph-and-lnast-check-pass |

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


### Terminal record replay

|   |   |
|---|---|
| Title | Terminal record/replay |
| Description | Record terminal commands and have the capacity to replay for testing and performance |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#term-recordreplay-for-benchmarkingtesting |

Use automatic asciinema generation. Compare the test speed and summarize the
performance difference from "a user" point of view. The results should allow to
track performance changes. These are integration tests that should be used for
overall performance and correctness. The same tests can be used as "demo" to
explain how to use the flow.

Maybe expand tmt_test and main_test to be a more stand-alone testing setup.


### OS X Alpine Linux Support

|   |   |
|---|---|
| Title | OS X, Alpine Linux Support |
| Description | LiveHD has issues with non-linux setups like OS X and Alpine Linux |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#os-x-alpine-linux-support |

LiveHD compiles (it did) with OS X, but there are some issues with the mmap
infrastructure inside mmap_lib. The code functionality should be able to run
(the mmap_remap does not exist in OS X, but a more costly alternative is
implemented for OS X, just not tested
and it seems faulty).

There are different set of issues with the alpine Linux distribution. Alpine
Linux does not use libc, and there are some failures. It would be good to fix
them all.

### Random CHISEL Verilog Pyrope generator

|   |   |
|---|---|
| Title | Random CHISEL/Verilog/Pyrope generator |
| Description | Create a random program generator that generates the same program for multiple languages |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#random-chiselverilogpyrope-generator |

Create a python/ruby/C++ program that generates pseudo-random programs in
several languages (CHISEL/Verilog/Pyrope). The idea is that the same program
can be implemented in multiple ways but all should have the same result
(simulation and LEC).

### unbitwidth

|   |   |
|---|---|
| Title | unbitwidth |
| Description | Not all the variables need bitwidth information. Find the small subset |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#unbitwidth-local-and-global-bitwidth |

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

### gRPC Client

|   |   |
|---|---|
| Title | gRPC Client |
| Description | Allow LiveHD to submit gRPC (bazel) jobs to distributed computing |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#grpc-client |

Leverage the gRPC client in liveHD to allow the submission of work to remote servers.

Once we can submit gRPC from inside LiveHD, we should have to re-structure the
pass API to have a gRPC call for each of the main steps.

### LNAST Opt

|   |   |
|---|---|
| Title | LNAST Opt |
| Description | Perform copy propagation, constant folding, and dce at LNAST level |
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/cross.md#lnast-opt |

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

## [SkyhookDM](http://www.skyhookdm.com)

[SkyhookDM]The Skyhook Data Management project extends object storage with data 
management functionality for tabular data. SkyhookDM enables storing and query 
database tables in Ceph distributed object storage, and supports multiple data 
formats including [Google Flatbuffers](https://google.github.io/flatbuffers/) 
and [Apache Arrow](https://arrow.apache.org).  SkyhookDM partitions and formats 
data as objects, and we utilize Ceph's object class extension mechanism 'cls' 
to develop data management methods that can be executed directly within storage.  
Methods include offloading processing to storage (e.g., SELECT, PROJECT) as well 
as physical design methods including indexing and data layouts.
Please see current project ideas listed below.
[SkyhookDM on Github](https://github.com/uccross/skyhookdm-ceph-cls).

-------------------

### Ingest data via Python, convert to pyarrow tables, horizonally partition and write to SkyhookDM

  - **Topics**: `PyArrow`, `Data partitioning`, `data loading`
  - **Skills**: C++, Python, Flatbuffers
  - **Difficulty**: Medium
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>

This project will create a Python client to read raw input data 
in CSV and JSON form (no nested data), convert to 
[PyArrow tables](https://arrow.apache.org/docs/python/), 
partition pyarrow tables horizontally (creating an individual Arrow 
table for each partition) and write each partition to SkyhookDM as 
an independent object, formatted with our 
[Flatbuffer metadata wrapper](https://github.com/uccross/skyhookdm-ceph-cls/blob/master/src/cls/fb_meta.fbs).  
Partitioning should be done with 
[JumpConsistentHash](https://arxiv.org/pdf/1406.2294.pdf) 
on the specified key columns, and will augment to our 
[Python client writer](https://github.com/uccross/skyhookdm-pythonclient) 
that currently performs vertical (column) based partitioning. 
[Github issue](https://github.com/uccross/skyhookdm-pythonclient/issues/16).


-------

### Compaction of formatted database partitions within objects

  - **Topics**: `Arrow`, `Data partitioning`, `compaction`
  - **Skills**: C++
  - **Difficulty**: High
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>

This project will develop object class methods that will merge (or conversely split) 
formatted data partitions within an object.  Self-contained partitions are written 
(appended) to objects and over time objects may contain a sequence of independent 
formatted data structures e.g., a sequence of 
[Arrow](https://arrow.apache.org/) 
tables each representing a sub-partition.  A compaction request will invoke this 
method that will iterate over the data structures, combining (or splitting) them 
into a single larger data structure representing the complete data partition.
In essence, this methods will perform a read-modify-write 
operation on an object's local data. 
[Github issue](https://github.com/uccross/skyhookdm-ceph/issues/33).

-------

### Port wiki to ReadTheDocs or other documentation platform

  - **Topics**: `Documentation`, `wiki`, `markdown`
  - **Skills**: Markdown, documentation, html
  - **Difficulty**: Easy
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>

SkyhookDM's documentation is [currently written](https://github.com/uccross/skyhookdm-ceph/wiki)
as Github Wiki pages. We would like to move it to another platform such as 
[ReadTheDocs](https://readthedocs.org), 
to reorganize it and rewrite some sections as part of this effort. 
[Github issue](https://github.com/uccross/skyhookdm-ceph-cls/issues/42).

-------

### Database statistics collection on partitioned data

  - **Topics**: `Statistics`, `histograms`, `data partitioning`
  - **Skills**: C++
  - **Difficulty**: Medium
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>
This project will develop object-class methods to compute data statistics 
stored as histogram for each object and store them in a query-able format within 
each storage server’s local RocksDB, then accumulate all 
the object-local statistics into global statistics for a given database table.
[Github issue](https://github.com/uccross/skyhookdm-ceph/issues/77).

-------

### Add support for a relevant subset of operations on List data types

  - **Topics**: `Array data`, `Arrow`, `Awkward Array`
  - **Skills**: C++
  - **Difficulty**: Hard
  * **Mentor**: [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre) <mailto:jlefevre@ucsc.edu>
  
Array data is currently stored as 
[lists within Arrow tables](https://arrow.apache.org/docs/cpp/api/datatype.html#classarrow_1_1_list_type) 
inside SkyhookDM.  This project will investigate and implement a small subset 
of operations on list data types that can be offloaded ("pushed down") into 
storage for query processing. Common list manipulations that perform data 
reduction such as filters or summary/agg methods (min, max, first, in) will 
be most useful to apply withing storage, since these will reduce network IO 
transferred back to the client from the storage layer.
We can look to [awkward array](https://github.com/scikit-hep/awkward-array) 
for reference of common operations on scientific array data.
[Github issue](https://github.com/uccross/skyhookdm-ceph-cls/issues/38).

-------

## [SkyhookDM](http://www.skyhookdm.com)/[HDF5](https://portal.hdfgroup.org/display/knowledge/What+is+HDF5)

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

## [SkyhookDM](http://www.skyhookdm.com)/[Proactive Data Containers](https://sdm.lbl.gov/pdc/about.html) (PDC)

[Proactive Data Containers](https://sdm.lbl.gov/pdc/about.html) (PDC) are containers within a locus of storage (memory, NVRAM, disk, etc.) that store science data in an object-oriented manner.  Managing data as objects enables powerful optimization opportunities for data movement and 
transformations, and storage mechanisms that take advantage of the deep storage hierarchy and enable automated performance tuning

-------------------

### PDC - Ceph RADOS Integration

  * **Topics**: `PDC`, `Ceph`, `object storage`
  * **Skills**: C, PDC, Ceph / RADOS
  * **Difficulty**: Medium
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

The [Ceph](https://ceph.io) distributed storage system provides object, block, and file system layer interfaces.
PDC has plugabble storage mechanisms and the [RADOS](https://ceph.io/geen-categorie/the-rados-distributed-object-store/) object storage layer
within Ceph is an ideal target for storing PDC objects.  This project would extend PDC to store its objects in RADOS pools.

