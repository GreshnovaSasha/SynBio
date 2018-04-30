**Synthetic biology** is an engineering discipline where practitioners of it want to design systems, predict their behavior, and be able 
to control that behavior, often with external stimuli. These systems or subsystems can be **reused**.

Inspired by an Electrical Engineering and Computer Science (EECS)

These physical parts can be arranged to create **logic gates** or other fundamental components, which can be organized into **modules** 
carrying out some **functions**, such as remembering information, sensing or changing the environment. These modules make up large 
**systems**, which can be organized into networks

Same abstractions:
* the system level
* the network level
* the physical implementation level

Top-down design

Same workflow:

* engeneer the curcuit that perform specific function
* analyse the curcuit with computational tools
* test in the cells
* several iterations of design may be required
* debugging
* analysis of results

Synthetic biology is different from bioengineering in using of technologies:

* Recombinant DNA
* PCR
* DNA sequencing
* **DNA construction**
* **Abstraction**
* **Standardization**

What is **a standard biological part**?
[BioBrick](http://parts.igem.org/Main_Page)

The BioBrick **assembly standard**
* Easy hierarchical assembly

* it's time-consuming: assembly steps have to happen in series with each cloning step taking a few days
* if some early step in the assembly hierarchy fails, you might have to re-consider the whole assembly strategy
* each assembly step has to go through bacteria and thus there's a chance of mutations and this accumulates in the process
* hard to generate combinatorial libraries
* desired sequences can't contain the restriction sites used in the protocol so extra steps have to be taken to remove them

As engeneers we want systems to be **reliable**, **specific**, and **predictable**.

Challenges of engeneering in biology

* Noise
* Genetic mutations
* Cell death
* Incomplete models
* Cellular contex

**Parts and compositors**

Processes — our **parts** — change state of a system by converting molecules, creating new ones, destroying them, or transporting them. 
Tha state of a system can be written down as a vector. The the inputs to the part are the state variables — concentrations of the species — and the outputs are the reaction rates. The number of compositors is equal to the number of state variables. 
