# GSoC 2020

This is a list of summer projects for OSS incubators and research 
projects affiliated with CROSS. If you have any questions, please visit our Gitter channel: [![Join the chat at https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## [Popper](https://github.com/systemslab/popper)

Popper is a workflow execution engine based on [Github 
actions](https://github.com/features/actions) (GHA). This is a list of 
ideas for projects related to Popper:

  * Example workflows (will likely work on more than one of the 
  following):
      * Machine learning: [MLPerf](https://mlperf.org/), 
      [xLearn](https://github.com/aksnzhy/xlearn), 
      [LightGBM](https://github.com/Microsoft/LightGBM).
      * Systems software: [SPDK](https://spdk.io/), 
      [DPDK](https://www.dpdk.org/), [Seastar](http://seastar.io/), 
      [Scylla](https://www.scylladb.com/).
      * Data analytics: [Weld](https://www.weld.rs/).
  * Add support for [Podman engine](https://podman.io).
  * Transparently run workflows on a [Kubernetes](https://kubernetes.io) cluster.

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

