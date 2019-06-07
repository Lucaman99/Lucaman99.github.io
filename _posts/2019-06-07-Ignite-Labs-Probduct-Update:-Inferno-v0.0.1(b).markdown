---
layout: post
title:  "Ignite Labs Product Update"
tags: [ignite-labs, software, math, physics, forest-fires]
---

# Inferno v0.0.1(b) Stable Release

I am happy to announce that the first stable release of Ignite Labs' flagship software package, Inferno, will be available for download and use in the next couple weeks.
This first release of Inferno is essentially the bones off of which we want to build the rest of our software.

The Inferno software package aims to allow researchers to simulate
the spread of land wildfires using a simple, light-weight, versatile Python library. With this first release, the functionality of the software of still very limited. With the current version of Inferno, we take a cellular-automata-based approach to model forest fires, where forest are modeled as grids, with each square on the grid corresponding to a tree or empty space. Fire then spreads between adjacent trees. With the current version, a few different types of forests (described below) can be generated and "burned". In addition, multiple of these different forests can be joined together to create what we call a "composite" grid, which can then be burned.

The documentation for all of the new features will be released along with the package download, in the next couple weeks. In the meantime, here is a list of all the added functionality:
  - Added the ``generate_coordinates``, ``generate_grid``, and ``generate_prob_grid`` functions, to create the empty grids on which trees can be placed for the forest fire simulation.
  - Added the ``CreateRandomGrid`` function, which generates a forest grid with a fixed number of trees positioned at random locations.
  - Added the ``CreateFixedGrid`` function, where a used can enter in a file containing coordinates of where they would like trees to be positioned.
  - Added the ``CreateClusterGrid`` function, which generates a forest in which a certain percentage of total trees are placed in groups called "clusters" around the forest grid, and the remaining trees are positioned randomly.
  - Added the ``CreateEvenGrid`` function, which attempts to achieve maximum "even separation" of trees, by actively avoiding groups of trees (clusters) in localized positions on the grid.
  - Added the ``spread_fixed_fire`` function, which initializes a fire on a generated forest grid with a pre-selected coordinate.
  - Added the ``spread_random_fire`` function, which initializes a fire on a generated forest grid with a random coordinate.
  - Added the ``CompositeGrid`` function, which takes multiple forest grids as arguments, and joins them together to form one larger grid.


<br>
# Cluster Grid Burn Time Paper Released

In addition to the first release of Inferno, I am proud to announce that the first research utilizing the Inferno software package is being conducted at Ignite Labs, with the release of an informal paper, detailing the mathematical rigor behind the clustered forest grid, and some of the results in regards to varying parameters of the fixed grid can change the time it takes for a random fire to "burn out" when initialized on the grid. The PDF of this paper can be found [here](https://drive.google.com/file/d/1Q1auYICbICXWG1NFpQzeKT1_ae1eBO50/view?usp=sharing).


<br><br>

We always appreciate any feedback on our work, so if you have any comments or questions about the paper or our software package, do not hesitate to send me an email at [jackceroni@gmail.com](MAILTO:jackceroni@gmail.com)!
