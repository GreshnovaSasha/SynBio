# Feed forward motifs

**Feed-forward circuits** have a network structure in which some starting node initiates a signal through multiple branches 
that later converge. 

**Toggles** are systems that can switch between two or more states. Toggles allow us to store memory of the last input that the system was given. 

**Oscillators** are important circuits that have a periodic nature. The output of these devices increases and decreases over time, 
leading to interesting sinusoidal-like behavior. Oscillators are particularly important for timing and creating clocks. 

**Generation of pulse response**
![pulse response](https://github.com/GreshnovaSasha/SynBio/blob/master/Pulse%20generation.png)
O=AND(I,NOT(I)) =OFF
When I is switched on, it could take a significant number of time for NOT(I) to go away, allowing O to transiently be high while I and NOT(I) are both present

**Sender-receiver system**
![sender-reciever](https://github.com/GreshnovaSasha/SynBio/blob/master/Sender-reciever.png)
In Cell 1, the small molecule aTC induces the creation of AHL by destabilizing the tetR repressor, which represses production of LuxI. LaxI facilitates the production of AHL and, since AHL is a small molecule, it can travel from Cell 1 (the sender cells) to Cell 2 (the receiver cells). In Cell 2, AHL induces co-activation of GFP with LuxR. Thus, when aTc is added to a system with both cell types, GFP will be expressed from receiver cells.

**The pulse generator in sender-reciever system**
![Sender-reciever](https://github.com/GreshnovaSasha/SynBio/blob/master/The%20pulse%20generator%20in%20sender-reciever%20system.png)
Once AHL enters Cell 2, there is a race condition to "get to" the output. A race condition is a term borrowed from electrical engineering meaning the output of the circuit depends on the timing of internal events (in this case it is signal propagation speed in different branches of the circuit).

Assuming cI starts absent in Cell 2, the constitutively-produced LuxR will immediately be activated by AHL, allowing expression of GFP. However, once cI expression reaches a high enough threshold, GFP expression will be shut down.

Two aspects of pulse generation:
1. The amplitude (or gain)
2. Duration
It can be changed by addition of cascade

Application:
tissue by design

**Spatiotemporal behavior**
The rate of addition of inducer is as important as its concentration: the response to a fast rate of increase is rapid and strong, whereas a slow rate of increase results in a delayed and lower amplitude pulse response.
With a slow increase in concentration, cI levels will be able to increase to levels that can outcompete activation by AHL. In the case of a slow rise in AHL levels, the branch with cI is able to "catch up" to the other branch and repression dominates. This is an example of a modified race condition which is more favorable for repression.
