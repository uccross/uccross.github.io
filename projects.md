# Open Source Project Ideas

<img src="woman-draw-a-light-bulb-in-white-board-3758105.jpg" alt="Woman draw a light bulb in white board" valign="middle" />

This is a list of projects and ideas associated to each. Each of this can be developed into class, senior, or summer projects. 
If you are interested in any of these projects, please [read this](https://uccross.github.io/getinvolved) on how to get involved. If you have any questions, please visit our Gitter channel: [![Join the chat at 
https://gitter.im/uccross/gsoc](https://badges.gitter.im/uccross/gsoc.svg)](https://gitter.im/uccross/gsoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

ANNOUNCING - [Summer Undergraduate Research Program in Open Source Projects at UCSC](https://cross.ucsc.edu/programs/summerprogam2020.html). 

Table of contents:

  * [LiveHD](#livehd)
  * [Skyhook](#skyhook)
  * [CAvSAT](#cavsat)
  * [Popper](#popper)
    + [CI Starter Workflows](#ci-starter-workflows)
    + [Machine Learning Performance Validation Workflows](#machine-learning-performance-validation-workflows)
    + [Systems Performance Validation Workflows](#systems-performance-validation-workflows)
    + [Boombox - Container-native Task and Workflow Specification](#boombox---container-native-task-and-workflow-specification)
    + [Breakdancer - YAML-based Task Automation](#breakdancer---yaml-based-task-automation)
    + [Podman Container Engine](#podman-container-engine)
    + [Kaniko support](#kaniko-support)
    + [Port website and documentation to Hugo Docsy](#port-website-and-documentation-to-hugo-docsy)
    + [Add Introduction Section to Documentation](#add-introduction-section-to-documentation)
    + [Computational Research Guide](#computational-research-guide)
    + [Dockerfile Generator Application](#dockerfile-generator-application)
    + [Improve Presentation of Underlying Concepts in Documentation](#improve-presentation-of-underlying-concepts-in-documentation)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## LiveHD

Projects for [LiveHD](https://github.com/masc-ucsc/livehd).

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


## [Skyhook](http://www.skyhookdm.com)

The Skyhook Data Management project extends object storage in the cloud with data management functionality. Skyhook enables storing and query database tables in Ceph distributed object storage, and supports multiple data formats including [Google Flatbuffers](https://google.github.io/flatbuffers/) and [Apache Arrow](https://arrow.apache.org) as well as text and scientific file formats.  Skyhook partitions and formats data as objects, and we utilize Ceph's object class extension mechanism to develop custom read/write and processing methods that can be executed directly within storage.  

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Compaction of formatted database partitions within objects
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | This project will develop object class methods that will merge (or conversely split) formatted data partitions within an object.  Self-contained partitions are written (appended) to objects and over time objects may contain a sequence of independent formatted data structures.  A compaction request will invoke this method that will iterate over the data structures, combining (or splitting) them into a single larger data structure representing the complete data partition.  In essences, this methods will perform a read-modify-write operation on an object's local data.
| **Link**        | https://github.com/uccross/skyhookdm-ceph/issues/33
| **Difficulty**  | high

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Database statistics collection on partitioned data
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | This project will develop object-class methods to compute data statistics (histograms) for each object and store them in a query-able format within each storage server’s local RocksDB, then write client code to accumulate all the object-local statistics into global statistics for a given database table.
| **Link**        | https://github.com/uccross/skyhookdm-ceph/issues/77
| **Difficulty**  | high

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Extend current aggregations to include sort/groupby for database partitions
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | We have developed methods (C++) for data management including data processing and indexing. This project will develop object-class methods methods to sort/group query result sets.  This requires extending the current code (select/project/basic-aggregations - min/max/sum/count) to support groupby and/or orderby.
| **Link**        | https://github.com/uccross/skyhookdm-ceph/issues/23
| **Difficulty**  | medium

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Port wiki to ReadTheDocs or other documentation platform |
| **Mentor(s)**   | [Jeff LeFevre](https://users.soe.ucsc.edu/~jlefevre)          |
| **Description** | Skyhook's documentation is currently written as Github Wiki pages. We would like to move it to another platform such as <https://readthedocs.org>, to reorganize it and rewrite some sections as part of this effort. |
| **Link**        | <https://github.com/uccross/skyhookdm-ceph>  |

|                 |                                               |
|-----------------|-----------------------------------------------|
| **Title**       | Augment SkyhookDM with in-storage support for a relevant subset of Awkward Array operations
| **Mentor(s)**   | [Jeff LeFevre](https://www.soe.ucsc.edu/people/jlefevre)
| **Skills**      | C++
| **Description** | Awkward arrays are currently stored as [lists within Arrow tables](https://arrow.apache.org/docs/cpp/api/datatype.html#classarrow_1_1_list_type) inside Skyhook.  This project will investigate and implement a small subset of [awkard array](https://github.com/scikit-hep/awkward-array) operations that can be offloaded ("pushed down") into storage for query processing. Common list manipulations that perform data reduction such as filters or summary/agg methods will be most useful to apply withing storage, since these will reduce network IO transferred back to the client from the storage layer.  
| **Link**        | https://github.com/uccross/skyhookdm-ceph-cls/issues/38
| **Difficulty**  | hard

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


## [Popper](https://github.com/systemslab/popper)

[Popper](https://github.com/systemslab/popper) is a container-native 
workflow execution engine. This is a list of ideas for projects 
related to this project is below. For any question, please visit the 
[Gitter channel][gitter] or [Slack channel][slack].

[gitter]: https://gitter.im/falsifiable-us/popper
[slack]: https://join.slack.com/t/getpopper/shared_invite/zt-dtn0se2s-c50myMHNpeoikQXDeNbPew

-------------------

### CI Starter Workflows

  - **Topics**: `example workflows`, `CI`, `development environment`
  - **Skills**: Bash, Python, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Create example workflows for using Popper for CI’ing projects in 
distinct languages. Would create an `examples/` folder in the Popper 
repo, and then create one YAML file per example, where every example 
represents a distinct example for a distinct language. For example, 
take [this example of the Github Actions starter workflow][ghastart]. 
We would write the same but using in the syntax of Popper. In this 
case, there would be an `examples/ci/python-app.yml` file, but the 
syntax is not the one for Github Actions, it is the syntax for Popper. 
As part of this, How-To guides will be added to the documentation 
(`docs/sections/guides`) for each distinct language.

[ghastart]: https://github.com/actions/starter-workflows/blob/master/ci/python-app.yml

-------

### Machine Learning Performance Validation Workflows

  - **Topics**: `example workflows`, `machine learning`
  - **Skills**: Bash, Python, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Take a machine learning library and create a workflow for reproducing 
results presented in an academic article, a blog post, or a repository 
README file. For example, take the 
[xLearn](https://github.com/aksnzhy/xlearn) main `README.md`, where 
they show some charts about the performance of the library. For this 
project, we would create a workflow that obtains data, installs the 
library, runs the benchmarks, and produces the charts in PDF/PNG 
format.

Other examples for which the same can be done are [Horovod][horovod], 
[Light GBM][lightgbm], [Wordbatch][wordbatch], [Open Graph 
Benchmarks][ogb] or any other blog post, README, or article that you 
find for which you would like to reproduce its results.

[ogb]: https://github.com/snap-stanford/ogb
[lightgbm]: https://github.com/Microsoft/LightGBM
[horovod]: https://github.com/horovod/horovod/blob/master/docs/benchmarks.rst
[wordbatch]: https://towardsdatascience.com/benchmarking-python-distributed-ai-backends-with-wordbatch-9872457b785c

-------

### Systems Performance Validation Workflows

  - **Topics**: `example workflows`, `systems research`
  - **Skills**: Bash, Python, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Same as above but for reproducing performance reports for 
high-performance systems frameworks. For example, we can take the 
performance report that is periodically generated for 
[SPDK](https://spdk.io/), and create a workflow that builds SPDK, 
prepares the storage drives (SSDs), runs the performance benchmarks, 
and lastly creates a PDF containing the resulting charts.

Other projects for which this can be done as well are 
[DPDK](https://www.dpdk.org/), [Seastar](http://seastar.io/), 
[Scylla](https://www.scylladb.com/), or any other you would like to 
work on.

-------

### Boombox - Container-native Task and Workflow Specification

  - **Topics**: `example workflows`, `systems research`
  - **Skills**: Bash, Python, YAML
  - **Difficulty**: Medium
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Extract the [Workflow Spec][wfspec] from the Popper repository and 
place it in a [standalone repository][bbox]. As part of this, we will 
also extend the definition so that it can also be used to define 
generic, container-native tasks. For example:

```yaml
tasks:
  install-deps:
    uses: docker://node:12-alpine
    runs: [yarn, install]
  build:
    uses: docker://node:12-alpine
    runs: [yarn, build]
  test:
    uses: docker://node:12-alpine
    runs: [yarn, test]
```

A task has the same structure as a [Popper Workflow step][ppstep], 
with the difference there is no ordering implied in its definition. In 
other words, a workflow YAML file represents a sequence of steps, 
whereas a task definition file doesn't. In YAML terms, `tasks` is a 
dictionary whereas `steps` is a list.

[ppstep]: https://popper.readthedocs.io/en/latest/sections/cn_workflows.html#syntax
[wfspec]: https://github.com/systemslab/popper/blob/e739b60/cli/popper/parser.py#L17
[bbox]: https://github.com/getpopper/boombox

-------

### Breakdancer - YAML-based Task Automation

  - **Topics**: `CLI tools`, `automation`, `open source project from 
    scratch`
  - **Skills**: Go, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Create a tool called `breakdancer` (installed as `bd`) in Go that 
takes a YAML file containing Boombox task definitions (see above), and 
executes them on-demand. This allows users to easily automate tasks 
without having to code them in a programming language, as they only 
need to provide a YAML file describing which images to run, what 
arguments to pass, and define Bash scripts inline if needed. Another 
way of looking at this: breakdancer is as a CLI on-the-fly tool.

Given a YAML file with tasks like the one shown above, assuming it is 
stored in a `tasks.yml` file, the following runs the `install-deps` 
task:

```bash
bd install-deps
bd test
```

For this project, we will create a brand new repository, containing 
all the usual elements of an open source project.

-------

### Podman Container Engine

  - **Topics**: `podman`, `container engine`
  - **Skills**: Bash, Python, Podman, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Using the [Podman Python API][podman-py], add support for building and 
running containers on the Podman engine. Similarly to how it is 
currently done for Docker (see code [here][docker-runner]).

[podman-py]: https://github.com/containers/podman-py
[docker-runner]: https://github.com/systemslab/popper/blob/ab2ee40/cli/popper/runner_host.py#L104

-------

### Kaniko support

  - **Topics**: `docker`, `container images`
  - **Skills**: Bash, Docker
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

[Kaniko](https://github.com/GoogleContainerTools/kaniko) is a tool 
that makes it possible to build docker images without root privileges. 
The Kaniko builder runs inside a docker container as a normal 
container and pushes images directly to a container registry. In 
addition, it can be used to speed up the build of images in scenarios 
where the Docker cache is cold (e.g. in CI systems).

This project consists of adding support for Kaniko in Popper. The main 
idea is to expose a `--kaniko` flag that enables the use of Kaniko 
when building images. For this, the user needs to specify a registry 
account in the configuration options.

-------

### Port website and documentation to Hugo Docsy

  - **Topics**: `documentation`, `hugo`
  - **Skills**: Hugo, Docker
  - **Difficulty**: Medium
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Consolidate the documentation and landing page of the project by 
migrating to Hugo, and use the 
[Docsy](https://themes.gohugo.io/docsy/) template. This page will 
reside in [its own repository](https://github.com/getpopper/website).

-------

### Add Introduction Section to Documentation

  - **Topics**: `documentation`, `workflows`
  - **Skills**: Workflows, Docker
  - **Difficulty**: Medium
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Add an introduction section to [the documentation][pp-docs]. With the 
aid of diagrams, this section will explain the concepts of: workflows, 
containers, container runtimes, container engines, container-native 
workflows, and resource managers.

[pp-docs]: https://github.com/systemslab/popper/tree/master/docs

-------

### Computational Research Guide

  - **Topics**: `documentation`, `workflows`, `computational research`
  - **Skills**: Workflows, Docker, Bash
  - **Difficulty**: High
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Create a guide on how to run python- and R-based computational 
projects using Docker, Popper, Travis and Zenodo in order to address 
the “long tail” of computational research. One way in which we can 
guide this work is by looking at codeocean.com and how they address 
these issues of usability. We would have a list of predefined 
workflows that someone using Jupyter (R or Python) for computational 
science research can copy to their projects so that they can launch a 
jupyter notebook in interactive mode and also run it in 
non-interactive mode. This guide would explain how to download/upload 
datasets to Zenodo as well.

You can think of computational projects like R or Python code, that 
make use of Jupyter and that download data from Zenodo. For example, 
we can create a github repository template like this one 
https://drivendata.github.io/cookiecutter-data-science/ that people 
can checkout. We would modify that one so that it includes a Popper 
workflow to run the distinct steps. We can create two templates, one 
for python and another for R. For example this one too: 
https://arxiv.org/abs/1401.200. Make it so that it reads like Popper 
as an alternative to codeocean.com

-------

### Dockerfile Generator Application

  * **Topics**: `gui`, `widgets`
  * **Skills**: Python, GUI, Docker
  * **Difficulty**: Medium
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Create a cross-platform GUI to aid in the generation of Dockerfiles. 
Similar to what <https://phpdocker.io/generator> but for creating 
images that are based on Debian (or Ubuntu) or Python, with support 
for specifying a list of `apt` and `pip` packages to include in the 
Dockerfile. To implement this in a cross-platform manner, a library 
such as [Kivy](https://kivy.org) can be used.

-------

### Improve Presentation of Underlying Concepts in Documentation

  * **Topics**: `documentation`, `containers`
  * **Skills**: Technical writing, Docker, Containers, Workflows
  * **Difficulty**: Medium
  * **Mentor**: Ivo Jimenez <mailto:ivotron@ucsc.edu>

Provide introductory material that serves as an overview to the 
different concepts and technologies involved in executing 
container-native workflows: Operating System (Linux), Language 
Runtimes (e.g. Python), Containers (Docker, Singularity), Resource 
Managers (Kubernetes, SLURM). The goal being to explain clearly what 
Popper does and what can users accomplish by using it. Currently, the 
documentation assumes expertise in all those topics but we would like 
to lower the entry barrier for new users.
