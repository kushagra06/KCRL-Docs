
# Knowledge Compilation with RL

Code for the paper [**Integrating Knowledge Compilation with Reinforcement Learning for Routes**](https://ojs.aaai.org/index.php/ICAPS/article/view/16002/15813) published at the 31st [*International Conference on Automated Planning and Scheduling (ICAPS) 2021*](https://icaps21.icaps-conference.org/home/).

***

## Getting Started

### Minimum prerequisites

#### For the training code:

* Python 3 (>=3.6)
* Tensorflow (1.7)
* Numpy (1.13)
* Scipy (1.3)
* Multiprocess (0.70)
* [Networkx](https://networkx.org/) (>=2.4)

#### For generating and manipulating SDDs:

* [Graphillion](https://github.com/takemaru/graphillion) 
* [PySDD](https://github.com/wannesm/PySDD)

Note: For generating and manipulating large maps, install the C++ [top-down compiler for binary hierarchical map](https://github.com/hahaXD/hierarchical_map_compiler) (for constructing hierarchical clustering) and the C++ [PSDD package](https://github.com/hahaXD/psdd) (for multiplying PSDDs). 

* To install prerequisites in bash 
```
bash install.sh
```
It is recommended to install all the dependencies in a conda environment.

## Running the code
To start the training process
```
python abc.py
```

### Generating the results

### Examples

### Steps to generate an sdd for an open-grid 5x5 map
* Using Graphillion generate sets of all paths i.e. a GraphSet or a zdd (e.g., using ./scripts/grid.py).
* Construct a file that maps sdd variables (literals) to edges (e.g., using ./scripts/grid.py).
* Convert the above generated zdd into sdd using *zdd2sdd.py* script.

#### Add constraints
* To add constraints (e.g., visiting some landmarks), generate another sdd using Graphillion.
* To combine the main sdd (sdd1) with the constraint sdd (sdd2), conjoin them using the conjoin operation in PySDD. (E.g.,``sdd1.conjoin(sdd2)``)
