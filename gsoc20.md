# GSoC 2020

This is a list of summer projects for OSS incubators and research 
projects affiliated with CROSS. If you have any questions, please visit our Gitter channel: [![Join the chat at https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## LiveHD

This is a proposal of GSoC projects for 
[LiveHD](https://github.com/masc-ucsc/livehd).


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Parallel Mockturtle with LiveHD
| **Mentor(s)**   | [Jose Renau](https://www.soe.ucsc.edu/~renau)
| **Skills**      | C++
| **Description** | Mockturtle is being integrated with LiveHD. The goal of this project is to create a parallel version where each partition is "mockturtled" in parallel. This requires to create a regression testting.
| **Link**        | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#mockturtle-qian-chen
| **Difficulty**  | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Tree-sitter Pyrope
| **Mentor(s)**   | [Jose Renau](https://www.soe.ucsc.edu/~renau)
| **Skills**      | Javascript
| **Description** | Tree-sitter allows incremental parsers. Pyrope is the in-house HDL. We have a javascript (pegjs) Pyrope grammar, the goal is to have an equivalent tree-sitter that also incrementally update CFGs.
| **Link**        | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#tree-sitter-pyrope
| **Difficulty**  | high


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Liberty with LiveHD
| **Mentor(s)**   | [Jose Renau](https://www.soe.ucsc.edu/~renau)
| **Skills**      | C++
| **Description** | Liberty is the de-facto standard to specify ASIC/FPGA libraries. The goal is to parse a liberty file and populate LiveHD/LGraph nodes.
| **Link**        | https://github.com/masc-ucsc/livehd/blob/master/docs/projects.md#liberty
| **Difficulty**  | Medium


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Pyrope Format
| **Mentor(s)**   | [Jose Renau](https://www.soe.ucsc.edu/~renau)
| **Skills**      | C++
| **Description** | Improve the Pyrope code generation with LNAST to support alignment, comments
| **Link**        | https://github.com/masc-ucsc/livehd/tree/master/inou/cgen
| **Difficulty**  | Medium


## [Popper](https://github.com/systemslab/popper)

[Popper](https://github.com/systemslab/popper) is a workflow execution 
engine based on [Github actions](https://github.com/features/actions). 
This is a list of ideas for projects related to Popper:

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Example Workflows                             |
| **Mentor(s)**   | [Ivo Jimenez](http://www.ivotron.me)          |
| **Skills**      | Bash, Python, C++ (optional), Rust (optional) |
| **Description** | <p>One or more the following (time permitting):</p><ul><li>Machine learning: <a href="https://mlperf.org/">MLPerf</a>, <a href="https://github.com/aksnzhy/xlearn">xLearn</a>, <a href="https://github.com/Microsoft/LightGBM">LightGBM</a>, <a href="https://towardsdatascience.com/benchmarking-python-distributed-ai-backends-with-wordbatch-9872457b785c">Wordbatch</a></li><li>Systems software: <a href="https://spdk.io/">SPDK</a>, <a href="https://www.dpdk.org/">DPDK</a>, <a href="http://seastar.io/">Seastar</a>, <a href="https://www.scylladb.com/">Scylla</a>.</li><li>Data analytics: <a href="https://www.weld.rs/">Weld</a>.</li></ul> |
| **Link**        | See repos in <https://github.com/popperized>  |
| **Difficulty**  | High                                          |

<!--
More than one of the following:
  * Machine learning: [MLPerf](https://mlperf.org/), [xLearn](https://github.com/aksnzhy/xlearn), [LightGBM](https://github.com/Microsoft/LightGBM), [Wordbatch](https://towardsdatascience.com/benchmarking-python-distributed-ai-backends-with-wordbatch-9872457b785c)
  * Systems software: [SPDK](https://spdk.io/), [DPDK](https://www.dpdk.org/), [Seastar](http://seastar.io/), [Scylla](https://www.scylladb.com/).
  * Data analytics: [Weld](https://www.weld.rs/).
-->

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Add support for additional container engines  |
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)             |
| **Skills**      | Python (strong), Go (basic), Bash (basic)    |
| **Description** | Add support for executing workflows in one or more of the followin (time permitting): [Podman](https://podman.io), [LXD](https://lxd.readthedocs.io/en/latest/), [Vagga](https://github.com/tailhook/vagga), [Charliecloud](https://github.com/hpc/charliecloud). |
| **Link**        | https://github.com/systemslab/popper |
| **Difficulty**  | Medium                                          |

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Transparently run workflows in a Kubernetes cluster. |
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)             |
| **Skills**      | Python (strong), Go (basic), Kubernetes (basic) |
| **Description** | Given a [`kubeconfig`](https://rancher.com/docs/rke/latest/en/kubeconfig/) file, allow Popper users to execute a workflow in a kubernetes cluster. This involves implementing a module that resembles a container engine (`popper run --engine kubernetes`), with the difference that containers are deployed in the cluster. |
| **Link**        | https://github.com/systemslab/popper |
| **Difficulty**  | High                                          |


|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Workflow Viewer and Editor                    |
| **Mentor(s)**   | [Ivo Jimenez](https://ivotron.me)             |
| **Skills**      | GUI development (strong), Javascript (strong) |
| **Description** | Create a javascript-based viewer of Popper pipelines that allows users to visually explore a pipeline and its contents, similar to [Github's built-in](https://github.blog/2019-10-01-new-workflow-editor-for-github-actions/) (see live example [here](https://github.com/spack/spack/edit/develop/.github/workflows/minimum_python_versions.yaml)) workflow editor. As part of this project, action and workflows catalogs will also be implemented, allowing users to search from an existing list of workflows and actions. |
| **Link**        | https://github.com/blkswanio/blackswan        |
| **Difficulty**  | Medium                                        |


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
