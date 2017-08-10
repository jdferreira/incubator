# Incubator

**Incubator** is a program dedicated to the procedural creation of animal-like bodies starting from a single DNA-like file. The general goal is to create a system that can simulate evolution based on some sort of selection.

This document contains the main idea behind the project, and is complemented with several other documents:
- [Ideas](ideas.md)
- [History](history.md)


## Overview

Ultimately, the final objective is to create a game based on these ideas that allows players to breed their pets according to their own desire. For example, we can conceive a scenario where a player is interested in small pets with light colours and fur; by breeding their own pets, they can achieve the goal. Other functionalities will exist that allow players a broader set of actions to help achieve their own goals:
- A supplies store to buy shelters (individual or for groups), food, medicine, _etc._;
- A pet store where pets can be sold and bought by the actual players (NPCs that handle transactions may also be added);
- A husbandry programme to let a player `A` lend their pets to another player `B` in order to breed `A`'s pet traits into `B`'s stock;
- A eugenics laboratory that allows the production of embryos, testing their characteristics and selecting the desirable embryo to further development;
- Contests to measure pets against each other, which include beauty contests, trick contents, battles and possibly more;
- A &ldquo;kennel&rdquo; to house pets that their owners do not want any longer (a paid service&mdash;players can themselves start kennels);
- A way to &ldquo;set a pet free&rdquo;, which will most certainly mean that it will die, along with a _moral police_ to make sure not many pets are freed into the wild.

The idea of the game is not too far from an idle game, where a player sets up their environment and waits for things to happen. The big difference is that the events are procedurally generated based on a DNA-like seed that gets passed down generation to generation, with slight mutations, from parents to offspring.


## Genetic material

The genetic material of an individual is a file containing seemingly random bits.


