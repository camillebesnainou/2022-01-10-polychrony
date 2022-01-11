# polychronization and heterosynaptic delays

## code

* https://github.com/SpikeAI/pyTERtorch/issues/1
* TODO see INRC proposal

## scientific scope

* [Polychronization: Computation With Spikes](https://direct.mit.edu/neco/article/18/2/245/7033/Polychronization-Computation-with-Spikes) [http://www.math.pitt.edu/\~bard/bardware/jc/polyc.pdf](pdf)
  * cites *Multistability in Recurrent Neural Loops Arising From Delay* <https://journals.physiology.org/doi/full/10.1152/jn.2000.84.2.975> - check out <https://laurentperrinet.github.io/publication/perrinet-adams-friston-14/> to solve delayed differential equations
  * uses STDP to select subsets of neuronswhile "fixed conduction delays, which are random integers between 1 ms and 20 m" (we could used delay learning instead, see below) and "An unexpected result is that the number of co-existing polychronous groups could be far greater than the number of neurons in the network, sometimes even greater than the number of synapses." - to apply to Hopfield-like networks
  * polychronous group defined as a graph directed in time
  * intriniséquement, il existe une invariance à la translation dans le temps du groupe tel qu'il est défini de façon anatomique
  * comes with MATLAB code but...
* Reproducing Polychronization: A Guide to Maximizing the Reproducibility of Spiking Network Models <https://www.frontiersin.org/articles/10.3389/fninf.2018.00046/full>
  * comes with python code
* blog post by Paxon Frady <https://epaxon.blogspot.com/2012/07/izhikevich-2006-polychronization.html>
* dynamic networks & learning delays:
  * Huning H., Glunder H., and Palm G. (1998) Synaptic delay learning in pulse-coupled neurons. Neural Computation, 10:555–565. <https://www.deepdyve.com/lp/mit-press/synaptic-delay-learning-in-pulse-coupled-neurons-DGMiNHxp0A>
  * [Eurich C., Pawelzik K., Ernst U., Cowan J., and Milton J. (1999) Dynamics of self-organazed delay adaptation. Phys. Rev. Lett., 82:1594–1597.](https://www.researchgate.net/publication/37921636_Dynamics_of_Self-Organized_Delay_Adaptation)
  * The recent "multi-neuronal spike sequence detector" (MNSD) architecture integrates the weight- and delay-adjustment methods by combining heterosynaptic plasticity with the neurocomputational feature spike latency : <https://pubmed.ncbi.nlm.nih.gov/33679293/>
  * an extensive (graph-centric) review on [Synchronization in time-varying networks](https://arxiv.org/abs/2109.07618)
* related 
  * Rosa Cossart?
  * cortical songs rafael yuste
  * A Benucci

## implementation

* reproduction des résultats classiques
* event-based
* spiNN3 board ? zeromq ?
* LoiHi - <https://spik.xyz/nc/index.php/s/BmrR2sFJ3MLnYNR>