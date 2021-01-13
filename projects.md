<img src="HiRes-Vector.png" alt="Logo of the Center for Research in Open Source Software" valign="middle" />

# Open Source Project Ideas

<img src="woman-draw-a-light-bulb-in-white-board-3758105.jpg" alt="Woman draw a light bulb in white board" valign="middle" />

This is a list of projects and ideas associated to each. Each of this can be developed into class, senior, or summer projects. 
If you are interested in any of these projects, please [read this](https://uccross.github.io/getinvolved) on how to get involved. If you have any questions, please visit our Gitter channel: [![Join the chat at 
https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

ANNOUNCING - [Summer Undergraduate Research Program in Open Source Projects at UCSC](https://cross.ucsc.edu/programs/summerprogram2020.html). 

Table of contents:

  - [LiveHD](#livehd)
- [CAvSAT](#-cavsat--https---githubcom-uccross-cavsat-)
- [SkyhookDM](#-skyhookdm--http---wwwskyhookdmcom-)
  * [Ingest data via Python, convert to pyarrow tables, horizonally partition and write to SkyhookDM](#ingest-data-via-python--convert-to-pyarrow-tables--horizonally-partition-and-write-to-skyhookdm)
  * [Compaction of formatted database partitions within objects](#compaction-of-formatted-database-partitions-within-objects)
  * [Port wiki to ReadTheDocs or other documentation platform](#port-wiki-to-readthedocs-or-other-documentation-platform)
  * [Database statistics collection on partitioned data](#database-statistics-collection-on-partitioned-data)
  * [Add support for a relevant subset of operations on List data types](#add-support-for-a-relevant-subset-of-operations-on-list-data-types)
- [SkyhookDM/HDF5](#-skyhookdm--http---wwwskyhookdmcom---hdf5--https---portalhdfgrouporg-display-knowledge-what-is-hdf5-)
  * [HDF5 - Apache Arrow Integration](#hdf5---apache-arrow-integration)
  * [HDF5 - Ceph/RADOS Integration](#hdf5---ceph-rados-integration)
  * [Column-storage in HDF5](#column-storage-in-hdf5)
  * [Sparse data storage in HDF5](#sparse-data-storage-in-hdf5)
  * [Metadata search in HDF5 with Database Solutions](#metadata-search-in-hdf5-with-database-solutions)
- [SkyhookDM/Proactive Data Containers (PDC)](#-skyhookdm--http---wwwskyhookdmcom---proactive-data-containers--https---sdmlblgov-pdc-abouthtml---pdc-)
  * [PDC - Ceph/RADOS Integration](#pdc---ceph-rados-integration)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## LiveHD

Projects for [LiveHD](https://github.com/masc-ucsc/livehd).

|   |   |
|---|---|
| Title | Floorplaner for LiveHD  |
| Description | Implement some state-of-the-art floorplaner with hierarchy and regularity for LiveHD. The goal is to typically target 10-1000 blocks. | 
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | 	https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#floorplaner |

|   |   |
|---|---|
| Title | LNAST Syntax Check Pass  |
| Description |LiveHD pass to check that the LNAST tree structure is valid. | 
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://masc.soe.ucsc.edu/lnast-doc/#introduction |

|   |   |
|---|---|
| Title | CHISEL/FIRRTL Checks  |
| Description | Create tests and sample CHISEL tests to test the FIRRTL passes in LiveHD | 
| Mentor(s) | Jose Renau|
| Skills | CHISEL, scala, C++17 |
| Difficulty | Medium |
| Link | 	https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#firrtl-2-lnast-hunter-coffman |

|   |   |
|---|---|
| Title | Mockturtle Synthesis  |
| Description | Add more blocks to the Mockturtle pass, testing cases, parallize calls | 
| Mentor(s) | Jose Renau|
| Skills | C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#parallel-and-hierarchical-synthesis-with-mockturtle |

|   |   |
|---|---|
| Title | Tree-sitter Pyrope Grammar  |
| Description | Build a tree-sitter Pyrope grammar | 
| Mentor(s) | Jose Renau |
| Skills | javascript, C |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#tree-sitter-pyrope |

|   |   |
|---|---|
| Title | Pyrope Language Server (vim/atom interface) |
| Description | Language Server is the new standard for editors feedback. The goal is to implement a language server for Pyrope | 
| Mentor(s) | Jose Renau |
| Skills | javascript, C++17 |
| Difficulty | Medium |
| Link | https://langserver.org/ |

|   |   |
|---|---|
| Title | Graph partition/coloring  |
| Description | Traverse Lgraph and interface with kahypar to partition graphs | 
| Mentor(s) | Jose Renau |
| Skills | javascript, C++17 |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#lgraph-partitiondecompositioncoloring,  https://github.com/SebastianSchlag/kahypar |

|   |   |
|---|---|
| Title | Competitive Analysis vivado, altera, ABC, mockturtle  |
| Description | Create a test suite and scripts to benchmark synthesis results | 
| Mentor(s) | Jose Renau |
| Skills | javascript, TCL |
| Difficulty | Medium |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#synthesis-asicfpga-competitive-analysis |

|   |   |
|---|---|
| Title | Useful LGraph Passes  |
| Description | Create several typical useful netlist checks like detect combinational loops, cross-clock checks, LGraph consistency checks | 
| Mentor(s) | Jose Renau |
| Skills | C++17 |
| Difficulty | Low |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#useful-lgraph-passes |

|   |   |
|---|---|
| Title | Performance Regression Infrastructure |
| Description | Website and reporting system using prometheous.io to monitor performance | 
| Mentor(s) | Jose Renau |
| Skills | javascript |
| Difficulty | Low |
| Link | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#performance-monitoring-infrastructure |

## [CAvSAT](https://github.com/uccross/cavsat)

Inconsistent relational databases are the ones that violate one or more integrity constraints defined over their schema. We are developing CAvSAT, which aims to be a scalable and comprehensive system for query answering over inconsistent databases.

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | CAvSAT (Consistent Answers via Satisfiability Solving)
| **Mentors**   | [Akhil Dixit](https://users.soe.ucsc.edu/~akadixit/), [Phokion G. Kolaitis](https://users.soe.ucsc.edu/~kolaitis/)
| **Skills**      | Java and SQL (required), Node.js and React (optional)
| **Description** | In general, computing consistent answers over inconsistent databases is an intractable problem. However, for certain classes of SQL queries and integrity constraints, there is an efficient algorithm to compute consistent answers. The first task of this project is to make the student familiar with the literature and implement this algorithm. Second, the student will conduct experiments with both synthetic and real-world datasets, to compare the performance of this algorithm with other methods. If the student is interested in front-end or full-stack development, they may work on developing some of CAvSAT's user interface components using technologies such as React and write code that connects to CAvSAT's backend via RESTful APIs.
| **Papers for Reference** | https://dl.acm.org/doi/10.1145/3299869.3300095, https://link.springer.com/chapter/10.1007/978-3-030-24258-9_8, https://dl.acm.org/doi/10.1145/303976.303983, https://dl.acm.org/doi/10.1145/3068334
| **Project Link**        | https://github.com/uccross/cavsat
| **Difficulty**  | Medium


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

### HDF5 - Ceph/RADOS Integration

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

### PDC - Ceph/RADOS Integration

  * **Topics**: `PDC`, `Ceph`, `object storage`
  * **Skills**: C, PDC, Ceph / RADOS
  * **Difficulty**: Medium
  * **Mentor**: Quincey Koziol <mailto:koziol@lbl.gov>, Suren Byna <mailto:sbyna@lbl.gov>

The [Ceph](https://ceph.io) distributed storage system provides object, block, and file system layer interfaces.
PDC has plugabble storage mechanisms and the [RADOS](https://ceph.io/geen-categorie/the-rados-distributed-object-store/) object storage layer
within Ceph is an ideal target for storing PDC objects.  This project would extend PDC to store its objects in RADOS pools.

