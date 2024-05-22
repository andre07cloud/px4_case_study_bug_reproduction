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
  - [Replication](#replication)
  - [bug-20260](#bug-20260)
        - [Step to Reproduce](#step-to-reproduce)


## Prérequis

- [Nom du logiciel] version x.x.x
- [Dépendance] version x.x.x
- [Autre dépendance]

## Installation

1. Clonez le dépôt :
    ```bash
    git clone https://github.com/votre-utilisateur/votre-projet.git
    ```
2. Naviguez dans le répertoire du projet :
    ```bash
    cd votre-projet
    ```
3. Installez les dépendances :
    ```bash
    pip install -r requirements.txt
    ```

## Replication
## bug-20260
| GitHub bug link |  https://github.com/PX4/PX4-Autopilot/issues/20260     |
|-----------------|---------------------------------------------|
| Code Release         | v1.13.0 & v1.13.2                                 |
| Os version           | Ubuntu 20.04                                      |
| Vehicle model        | Plane                                             |
| Simulator type       | Gazebo SITL                                       |
| Bug Description      | When running takeoff in SITL without QGC running, the plane immediately goes into failsafe, goes into RTL and then crases                                 |
| Expexted Behavior    | When takeoff command is done in gazebo simulator, the plane must takeoff normaly.                                 |
| Observed Behavior    | The first time that takeoff command is done, the plane drone tries to takeoff, but fails after a little distance on the ground.                                 |
| Output               | Here the output is the behavior of the vehicle observed in the gazebo inteface.                                 |
##### Step to Reproduce


1. clone px4 software form github official repository :
    ```bash
    git clone https://github.com/PX4/PX4-Autopilot.git --recursive
    ```
2. clean submodules from main branch :
    ```bash
    make clean
    ```
    ```bash
    make distclean
    ```
3. checkout to the branch release :
    ```bash
    git checkout v1.13.2
    ```
4. update submodules for the new release :
    ```bash
    make submodulesclean
    ```
5. execute the following commands inside terminal :
    ```bash
    make px4_sitl gazebo_plane
    ```
    hit Enter and run :
    ```bash
    commander takeoff
    ```
