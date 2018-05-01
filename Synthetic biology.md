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

**Compositors** aggregate the effects of parts. These are the total rates of change of some state variable, across the whole system in the framework of ordinary differential equations (ODEs).

There is one compositor for each state variable.

## Gene erxpression and regulation

The function of enzyme is its activity; this function depends on the contex it is in; we have to specify both the potential for function and the environment this potential can be realized in.

Assumptions

* everything is well-mixed
* reaction goes to completion
* no spontaneous degradation reactions of the components
* the enzyme is precise and always do the conversion we require

All of these assumptions have caveats, but ease the design process.

**A simple model of gene expressioin**
 ### Four-part model
These parts — processes — are transcription, transcript degradation, translation, and protein degradation.

RNA polymerase (RNAP) binds DNA and forms an "open complex" with the DNA, which is essentially the initiation of transcription. We assume that initiation always leads to the creation of full transcripts, without modeling the details of elongation, etc. The formed transcript, mRNA, is also degraded at some rate. Competing with the degradation is the binding of ribosomes, which result in translation. Proteins are degraded similarly to the mRNA, but at a different rate.

![the simple model of gene expression](https://github.com/GreshnovaSasha/SynBio/blob/master/the%20simple%20model%20of%20gene%20expression.png)

Strong promoters will have a small Kp (binds to RNAP tightly) and/or big kc (once RNAP binds, it readily initiates transcription); a weak promoter will have a large Kp (it binds to RNAP weakly) and/or a small kc (once RNAP binds, transcription initiation is not as frequent). It might be easier to engineer Kp rather than kc, as it can be achieved by changing the promoter sequence; changing kc might require engineering RNAP or its cofactors.

Drawbacks of this model

* no regulation (say by transcription factors) is included
* cell division is not accounted for directly
* stochastic effects might be relevant due to the low number of copies of the gene in question
* we haven't elucidated any aspects of how RNAP finds the promoter
* no details on the steps of initiation and elongation
* no effects from the secondary structure of mRNA, which could affect translation

What are the things that we as engineers can play around with?

* Degradation
** degradation tags for protein
** insert sequence into mRNA that will lead to frormation of secondary structure and/or codon choice in the mRNA
** ribozymes
* Copy number of plasmid
* Transcription and translation rate (strength of promoter)

### Two-part model

We can say that there is a single characteristic to a promoter: it's strength; to a translation: the strength of the ribosome binding site on the mRNA.

![two-part model of gene expression](https://github.com/GreshnovaSasha/SynBio/blob/master/two-part%20model%20of%20gene%20expression.png)

Time-scale separation: mRNA comes to equilibrium much faster than protein. Now we can get an explisit solution. 
![gene-expression model solution](https://github.com/GreshnovaSasha/SynBio/blob/master/gene%20expression%20model%20solution.png)

If we want to change the dynamics of this system, we must manipulate the degradation rate of the protein, but doing so will affect the steady-state levels. Hence if we want to change the dynamics without affecting the steady-state, we must also change one of the other rate constants through engineering. 
