## Oscillators

**Evolution of Synthetic Oscillators**

|Year |Scientist   |Model                               |
|-----|------------|------------------------------------|
|2000 | Leiber     |Repressilator                       |
|2003 | Nifna      | Relaxation (activator/inhibitor)   |
|2005 | Liao       | Metabollator                       |
|2009 | Hasty      | Tunable relaxation oscillator      |
|2009 | Fussengger | Mammalian oscillator               |
|2010 | Hasty      | Synchronised oscillator            |
|2012 | Hasty      | Radically coupled genetic biopixels|

### [Repressilator](http://sci-hub.tw/10.1038/35002125)

![Repressilator](https://github.com/GreshnovaSasha/SynBio/blob/master/Oscillator.png)

![repressilator_scheme](https://github.com/GreshnovaSasha/SynBio/blob/master/repressilator.png)

Consist of *three negative feedback loops*

The two genes no longer directly interact; having intermediary **delay**. 

Negative times negative times negative is negative

**Mathematic model**

![repressilator_math_model](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/repressilator_math_model.png)

basal decay + repressed production + basal production

**Phase plane**

![repressilator_phase_plain](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/repressilator_phase_plane.png)

![repressilator_phase_plain_slide](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/repressilator_phase_plain_slide.png)

Designs should have very large regions where they behaive

### Relaxation oscillator

![Relaxation_oscillator](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/relaxation_oscillator_scheme.png)

![Relaxation_oscillator_slide](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/relaxation_oscillator_slide.png)

Saddle-node bifurcation

![Relaxation_oscillator_vector_field](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/relaxation_oscillator_vector_field.png)

### [A fast, robust, and tunable synthetic gene oscillator](http://sci-hub.tw/10.1038/nature07389)

![Hasty_2008_oscillator_scheme](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_oscillator.png)

Two inducers in the system

Three similar promoters (Arabinose, IPTG)

[![Hasty_2008_oscillator_video](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_oscillator_video.png)](https://youtu.be/4xicQrWkiKw)

Cells were grown in microfluidic chambers

**Effect of IPTG on oscillations**

![Hasty_2008_dynamics](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_dynamics.png)

*a* non-monotonic effect of IPTG on oscillation period

**no IPTG** -> high level of repression by LacI -> low expression 

lower level of IPTG -> lower level of repression by LacI -> higher expression

**hight IPTG** -> no negative feedback -> disappearance of oscillatons

There is some optimal level of IPTG: protein expression can take on a wider range of values when the feedback is not too strong or weak

**Effect of Arabinose on oscillations**

*b* increase level of arabinose -> increase oscillatory period

There is some level of an effective saturation, in which all  complexes are active on all promoters -> Arabinose can not be able to becaome dominant over lacI

**Effect of temperature**

*c, d* Tempreture affects the doubling time (the cell divides faster at higher temperatures) and the doubling time will directly effect the dilution -> lower overall expression of proteins and a smaller dynamic range of expression (shorter oscillation periods)

**Model**

simple model -> expand model

![Hasty_2008_model](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_model.png)

The critical improvement to the model was the inclusion of fine-grained details in the protein production process, which better captured the delay in initiation of gene expression to final protein completion. 

![Hasty_2008_equations](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_equations.png)

**The takeaway message**: abstraction is very useful in modeling, but we need to be careful in what exactly we abstract away. Simplification is great, but your models should still capture the important behavior of the system. And what is "important" depends on your design goals and your system.

**An oscillator with a short negative feedback loop**

![Hasty_2008_simple_model](https://github.com/GreshnovaSasha/SynBio/blob/master/oscillator/Hasty_2008_simple_model.png)

a damping ratio

Negative feedback loop is a mechanism that allows to reach steday-state faster than constitutive promoter.

*But* in this model we can see oscillations

Essentially, the delay in feedback causes the system to overshoot its set point (steady-state), and then again undershoot once the feedback kicks in and drives levels down. This continues periodically with a gradual decrease in over/undershoot as time progresses. Thus, the oscillator is ultimately unstable, and the level of *LacI* will eventually reach a steady-state.
