## Negative-feedback loop

![Negative-feedback loop](https://github.com/GreshnovaSasha/SynBio/blob/master/Negative-feedback%20loop.png)

## The toggle switch 

![Togggle switch](https://github.com/GreshnovaSasha/SynBio/blob/master/Toggle%20switch.png)

Consist of two negative feedback loops

Actually, is a positive loop

Negative times negative is positive!

Bi-stable switch

### The Gardner-Collins toggle

[The Gardner-Collins toggle](http://sci-hub.tw/10.1038/35002131)

![The Garden-Collins toggle](https://github.com/GreshnovaSasha/SynBio/blob/master/Garden%20Collins%20toggle%20switch.png)

Logic: A OR NOT(B)

Inducers (A) [can turn off these repressions] generally are low.

Repressors are outputs. 

![logic for the toggle](https://github.com/GreshnovaSasha/SynBio/blob/master/the%20toggle%20switch%20logic.png)

Switching is accomplished by transiently introducing an inducer of the currently active repressor

If two operators were one that won't work.

Requirements 
* sigmoid function

**Dynamics**

![G-C toggle dynamics](https://github.com/GreshnovaSasha/SynBio/blob/master/G-C%20toggle%20Dynamics.png)

Data extrapolation

**Mathematical model**

![mathmatical model](https://github.com/GreshnovaSasha/SynBio/blob/master/G-C%20toggle%20model.png)

Hill-function
The repressor-promoter binding constant is taken as one

a1 and a2 are the normalized maximum synthesis rates, and gamma and beta are the cooperativity of the repressor-promoter binding.

Biological noise

![Noise](https://github.com/GreshnovaSasha/SynBio/blob/master/noise.png)

n is a number of molucules

IPTG induces expression from LacI-repressed promoters (by causing LacI to disengage its operator sites), and 42°C temperature induces expression from cI-repressed promoters (because it is heat labile).

Why we can see two subpopulations?

![fluerescence](https://github.com/GreshnovaSasha/SynBio/blob/master/GFP%20fluorescence.png)

Because of noise and stochasticity in the number of proteins, DNA, and inducer in each cell  not all cells switch states at a given concentration of inducer. This explains why the entirety of the cell population does not switch at the same time/level of inducer, but there are no "in between" cells.

**Sources of biological noise**

* cell division
* mutations
* load on the cell

The state switches within *40 hours.* Fixes?

* reduce the amount of protein the cell will express by reducing copy number, using weaker promoters, and/or using weaker ribosome binding sites
* make the otput selectable (ex. put an antibiotic resistance gene next to the GFP -> it can only produce GFP and antibiotic together)
