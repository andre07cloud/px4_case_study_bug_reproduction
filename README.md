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

## Replication:

- [bug #20260](./bug_20260.md)
