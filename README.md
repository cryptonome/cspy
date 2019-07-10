[![CircleCI](https://circleci.com/gh/torressa/cspy/tree/master.svg?style=svg&circle-token=910e28b03dd0d32967fae038a3cf28b6cdf56334)](https://circleci.com/gh/torressa/cspy/tree/master)
[![Documentation Status](https://readthedocs.org/projects/cspy/badge/?version=latest)](https://cspy.readthedocs.io/en/latest/?badge=latest)
[![PyPI version](https://badge.fury.io/py/cspy.svg)](https://badge.fury.io/py/cspy)
[![codecov](https://codecov.io/gh/torressa/cspy/branch/master/graph/badge.svg?token=24tyrWinNT)](https://codecov.io/gh/torressa/cspy)
<!-- [![BCH compliance](https://bettercodehub.com/edge/badge/torressa/cspy?branch=master)](https://bettercodehub.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) -->

# cspy


A collection of algorithms for the (resource) Constrained Shortest Path (CSP) problem. 

The CSP problem was popularised by Inrich and Desaulniers (2005) [@inrich]. It was initially introduced as a subproblem for the bus driver scheduling problem, and has since then widely studied in a variety of different settings including: the vehicle routing problem with time windows (VRPTW), the technician routing and scheduling problem, the capacitated arc-routing problem, on-demand transportation systems, and, airport ground movement; among others.

More generally, in the applied column generation framework, particularly in the scheduling related literature, the CSP problem is commonly employed to generate columns.

Therefore, this library is of interest to the operational research community, students and academics alike, that wish to solve an instance of the CSP problem.

## Algorithms

Currently, the algorithms implemented include:

 - [X] Monodirectional forward labeling algorithm;
 - [X] Monodirectional backward labeling algorithm;
 - [X] Bidirectional labeling algorithm with static halfway point;
 - [X] Bidirectional labeling algorithm with dynamic halfway point Tilk et al. (2017) [@tilk];
 - [X] Heuristic Tabu search;
 - [X] Greedy elimination procedure;
 - [X] Greedy Randomised Adaptive Search Procedure (GRASP). Adapted from Ferone et al. (2019) [@Ferone];
 - [X] Particle Swarm Optimization with combined Local and Global Expanding Neighborhood Topology (PSOLGENT) Marinakis et al. (2017) [@Marinakis].


## Getting Started


### Prerequisites

Conceptual background and input formatting is discussed in the [docs](https://cspy.readthedocs.io/en/latest/how_to.html).

Module dependencies are listed in [requirements.txt](requirements.txt).

### Installing

Installing the ``cspy`` package with ``pip`` should also install all the required packages. You can do this by running the following command in your terminal

```
  pip install cspy
```
or

```
  python3 -m pip install cspy
```

### Usage Examples

Please see the individual algorithms API Documentation for specific examples and more details:

- [Bidirectional and monodirectional algorithms](https://cspy.readthedocs.io/en/latest/api/cspy.BiDirectional.html)
- [Heuristic Tabu Search](https://cspy.readthedocs.io/en/latest/api/cspy.Tabu.html)
- [Greedy Elimination Procedure](https://cspy.readthedocs.io/en/latest/api/cspy.GreedyElim.html)
- [GRASP](https://cspy.readthedocs.io/en/latest/api/cspy.GRASP.html)
- [PSOLGENT](https://cspy.readthedocs.io/en/latest/api/cspy.PSOLGENT.html)


## Running the tests

Tests can be run using the standard ``unittest`` by running

```
  python3 -m unittest
```

## License

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.

## Contributing

Feel free to contribute to this project either by either working trough some of issues flagged as help wanted, or raise a new issue with any bugs/improvements.

If you have a question or need help, feel free to raise an issue explaining it.


### TODO

 - [ ] Implement generic resource extension functions for bidirectional algorithm
 - [ ] Greedy elimination algorithm tests.
 
### Changelog

pre-release v0.0.4: 9/07/2019

```
Implemented PSOLGENT
GreedyElim simple test
fixed prune_graph preprocessing routine
YAPF google style
```

[@inrich]: https://www.researchgate.net/publication/227142556_Shortest_Path_Problems_with_Resource_Constraints

[@tilk]: https://www.sciencedirect.com/science/article/pii/S0377221717302035

[@Marinakis]: https://www.sciencedirect.com/science/article/pii/S0377221717302357

[@Ferone]: https://www.tandfonline.com/doi/full/10.1080/10556788.2018.1548015