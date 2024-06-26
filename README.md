# An exploratory study of bug reproduction in UAVs sytems : PX4 case study


The field of unmanned aerial vehicles has seen significant technological advancements over the years, leading to the emergence of numerous autopilot software solutions. However, like any system, they are prone to operational bugs. To better comprehend these bugs, often reported by users, developers must be able to replicate them under the same conditions as reported.
The uniqueness of drone systems lies in their dependence on hardware interaction for operation, making bug reproduction in such environments highly complex.
While numerous studies have been conducted on bug reproduction, there is a gap in research specifically focused on unmanned aerial vehicle autopilot systems. To address this gap, we conduct an empirical study using an open-source software called PX4 to reproduce reported bugs in the GitHub repository. The primary objective of this study is to establish a methodology that facilitates bug reproduction in autopilot software. From this study, we derive 10 key points serving as guidelines for reproducing a specific bug in UAV systems. Additionally, we identify three major challenges encountered in this task, leverage LLMs to assist bug reproduction.
Our study aims to assist researchers and practitioners in gaining a better understanding of bug reproduction in UAV systems and enhancing future bug reports in this field

## Table of Contents

- [An exploratory study of bug reproduction in UAVs sytems : PX4 case study](#an-exploratory-study-of-bug-reproduction-in-uavs-sytems--px4-case-study)
  - [Table of Contents](#table-of-contents)
  - [Prérequis](#prérequis)
  - [Installation](#installation)
  - [Replication:](#replication)


## Prérequis
For any mission configuration and planning in QGroundControl, please refer to the following detailed [tutorial](https://docs.qgroundcontrol.com/master/en/qgc-user-guide/plan_view/plan_view.html#plan_tools).

## Installation

To get a good configuration PX4 after Checking Out in a branch release, make follwing tasks:
- Go inside release folder and run this command
```bash
    bash ./PX4-Autopilot/Tools/setup/ubuntu.sh
```



## Replication:

- [bug #20260](./bug_20260.md)
- [bug #20477](./bug_20477.md)
- [bug #18574](./bug_18574.md)
- [bug #18573](./bug_18573.md)
- [bug #18271](./bug_18271.md)
- [bug #18576](./bug_18576.md)
