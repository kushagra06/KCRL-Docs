# Code for the paper Integrating Knowledge Compilation with Reinforcement Learning for Routes
    Published in International Conference on Automated Planning and Scheduling (ICAPS) 2021

## Prerequisites
* Python 3 (>=3.6)
* [Networkx](https://networkx.org/)
* [Graphillion](https://github.com/takemaru/graphillion) 
* [PySDD](https://github.com/wannesm/PySDD) 


### Steps to generate an sdd for an open-grid map
* Using Graphillion generate sets of all paths (a zdd).
* Convert the above generated zdd into sdd using *zdd2sdd.py* script.

#### Add constraints
* To add constraints (e.g., visiting some landmarks), generate another sdd using Graphillion.
* To combine the main sdd (sdd1) with the constraint sdd (sdd2), conjoin them using the conjoin operation in PySDD. (E.g.,``sdd1.conjoin(sdd2)``)

## Running the code


## Organization
