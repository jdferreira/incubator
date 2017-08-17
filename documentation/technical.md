# Procedural generation of a pet

This document explains the technical details associated with the algorithm that creates the pet's body.

## Womb

We start with a representation of the womb. The womb is a 3D structure that contains the space where the body will develop. The womb already contains a series of agents that set up the womb's attractor field (see section [The womb's attractor field](ideas.md#the-wombs-attractor-field) in the Ideas file). It also contains the embryo, which starts as a simple ball-like 3D mesh. There is also room to innovate, as the actual form of the embryo may not be the same and may be dependent on the children's genome.
