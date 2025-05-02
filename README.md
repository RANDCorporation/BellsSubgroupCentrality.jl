# BellsSubgroupCentrality.jl

Implementatino of Bell's subgroup centrality measure. Allows for the calculation of key measures of subgroup centrality, including:

* **Overall (O)**
* **Global (G)**
* **Local (L)**
* **Boundary (B)**

See `demo_calculations.ipynb` for a reproduction of Betweenness Centrality as calculated in Appendix B of Bell (2014) using a Dolphin network (Figure 4).

##  Use 


### Requirements

`BellsSubgroupCentrality.jl` requires `Graphs.jl`. The optional `BellsSubgroupCentralityExt` module requires Graphs, CSV, XLSX, DataFrames, and DiscreteGraphAlgorithms. 


### Calculating


The quickest way to access one of the 4 subgroup centralities is to

1. Load a `Graphs.jl` graph
2. Define vertices in a group
3. Use `get_sugroup_centrality` to calculate the type of subgroup centrality desired.

E.g., 

```
get_subgroup_centrality(
    graph,
    TYPE,
    group
)[group]
```

where `TYPE` is any of the following symbols:

* `:boundary` or `:b`,
* `:global` or `:g`
* `:local` or `:l`
* `:overall` or `:o`


## Project information

This package is [one of five](https://github.com/RANDCorporation/black-knights-and-dark-network) created during the research phase of a RAND project.

In their report [_North Korea's Black Knights and Dark Network: Towards the Disruption and Typology of DPRK Sanctions Evasion Networks_ (RAND, RR-A3413-1)](https://www.rand.org/pubs/research_reports/RRA3413-1.html) researchers describe how they created a network representation of the DPRK sanctions-evasion system, comprising over 4,100 nodes and 6,500 links derived from UN Panel of Experts reports and the Center for Advanced Defense Studies (C4ADS) dataset. Together, the five code packages supported the team's ability to rank nodes and links, calculate priority scores, and compare the results to sanctioned entities, thus offering a rigorous, computationally driven approach to network disruption and target prioritization.

See the [parent repository](https://github.com/RANDCorporation/black-knights-and-dark-network) for a full list and additional details.

##  References

Bell, JR. Subgroup centrality measures. Network Science. 2014;2(2):277-297. [doi:10.1017/nws.2014.15](https://www.cambridge.org/core/journals/network-science/article/abs/subgroup-centrality-measures/875D8E7EBF4E33008CB45C6A417C3C66)


## Copyright and License

Copyright (C) <2025> RAND Corporation. This code is made available under the MIT license.

 

## Authors and Reference

James Syme

```
@misc{BGC2025,
  author       = {Syme, James},
  title        = {BellsSubgroupCentrality.jl: Implementatino of Bell's subgroup centrality measure.},
  year         = 2025,
  url          = {https://github.com/RANDCorporation/BellsSubgroupCentrality.jl}
}
```
