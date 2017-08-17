# Incubator

**Incubator** is a program dedicated to the procedural creation of animal-like bodies starting from a single DNA-like file. The general goal is to create a system that can simulate evolution based on some sort of selection.

This document contains the main idea behind the project, and is complemented with several other documents:

- [Ideas](ideas.md)
- [History](history.md)
- [Procedural generation of a pet](technical.md)

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

The genetic material of an individual (its genome) is a file containing seemingly random bits. These bits are used as the DNA of the individual. They contain information on where to put attractors and repellers in the womb, which will guide the vertices of the mesh when the pet is developing. The genetic material is also responsible for providing all the other data needed to create the pet's body and characteristics.

A more thorough description of the mathematics involved can be found by following the information on the 3D-mesh algorithm.

## Womb

Ideally, the genetic material will contain all the information necessary to create the pet's body. This includes the actual algorithm. This is not straightforward. And, in fact, in real biological life, DNA does not contain all information necessary to recreate the individual's body. For example, the proteins used to read the DNA exist in the mother's ovule (when such cell exists) and are the ones responsible for scanning, interpreting and performing the instructions in the DNA (the *SIP procedure*).

I want to create a system that mimics this behaviour. As such, the womb will be part of a parent's body, or it will be an external egg created by a parent. It already contains the _agents_ (this part needs clarification) needed for the SIP procedure. For example, the womb will contain agents (objects in the program) that look for sequences of bits in the genome that identify attractors and repellers. Creating these agents will also happen (later in life) based on the genome. This means that the genome must have an effect in a post-development phase of the pet's life.

## Post-development genome effects

Specialized _cells_ (we still haven't found this term in the project, but I believe the meaning is apparent here) in the pet's body will be responsible for activating certain genome sequences that will create agents that have an effect on the pet (either visible in the 3D body or invisible, such as the creation of a womb; see previous section). Only these cells execute the genetic code. Not all cells are equal: each contains a different set of agents that will allow them to go through the *SIP procedure* and by that producing different results. These differences come from the fact that the womb's three-dimensional space contains different values for different variables&mdash;in essence, several property fields (one of these fields is the one responsible for the attractors and repellers, which guide the cells throughout the development process in order to create the body).
