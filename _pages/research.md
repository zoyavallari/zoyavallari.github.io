---
layout: distill
permalink: /research/
title: research
description: brief overivew of projects
nav: true

toc:
 - name: neutrino oscillations
 - name: neutrino-nucleus interactions
 - name: detector development
 - name: high performance computing
---
 
## neutrino oscillations

In the last two decades, neutrino oscillation experiments have made significant advancement in the measurement of neutrino mixing parameters.
However, key questions such as the neutrino mass ordering and charge-parity violation in neutrinos still remain unknown.
These discoveries maybe consequential for investigating the origins of the matter-antimatter asymmetry in the early universe, searching for possible fundamental symmetries that govern neutrino mixing and determining whether neutrinos are Majorana fermions.

Long-baseline neutrino oscillation experiments measure the neutrino mixing parameters and mass-splittings by searching for a depletion in the muon neutrino content ($$\nu_\mu$$ disappearance) of the beam as a function of their energy and distance traveled over time.
This reduction can be attributed to those neutrinos oscillating to other flavors.
These experiments also search for an excess of electron neutrinos ($$\nu_e$$ appearance) created from the oscillation of the muon neutrinos.
Any asymmetry in the rate of $$\nu_e$$ appearance in the $$\nu_\mu$$ beam with the rate of $$\bar\nu_e$$ appearance in the $$\bar\nu_\mu$$ beam provides a mechanism to measure the $$\delta_{CP}$$ phase and the mass ordering of neutrinos.

My work focuses on combining the data from the two leading long-baseline experiments, NOvA and T2K, to perform a joint analysis of their data to neutrino oscillation parameters.
A significant difference in their baseline and beam energy offers advantageous complementarity that is useful to break degeneracies between the measurement of mass ordering and the CP violating phase.

<div class="fake-img l-body">
       {% include figure.html path="assets/img/DUNESchematic.jpeg" title="3-flavor neutrino oscillation" class="img-fluid rounded z-depth-1"%}
 </div>
<div class="caption">
     Schematic of the future DUNE experiment which will be analyze the neutrino beam from the Fermilab beam facility with two detectors located at Fermilab, Illinois and SURF, South Dakota.
     [Image Credit: <a href="https://www.dunescience.org/">DUNE Experiment</a>] 
</div>




***

## neutrino-nucleus interactions

<div class="row mt-3">
      <div class="col-sm mt-3 mt-md-0">
     <p>Neutrinos interact with matter via weak-interaction force. As they interact so rarely, we do not have a complete theoretical model that is able to accurately predict the particles that might be emitted as a result of such interaction, specially in complex nucleus targets. This puts a limitation on how accurately the current experiments are able to measure the neutrino oscillation and adds large systematic uncertainties to our measurements. Neutrino oscillation measurements employ a near detector to measure and constrain the uncertainties orgination from neutrino-nucleus interactions. 

</p>
     </div>
      <div class="col-sm mt-3 mt-md-0">
       {% include figure.html path="assets/img/nuscattering.jpg" title="neutrino scattering" class="img-fluid rounded z-depth-1"%}
<div class="caption">
     Particle tracks in a bubble chamber experiment. [Image Credit: <a href="https://www.sciencephoto.com/contributor/cer/">CERN Science Photo Library</a>] 
</div>
</div>
</div>

<p>      I measured the rate of neutral current neutrino interactions which produce a single neutral pion particle in the final state which is often indistinguishable from the signature of electron neutrino in the detector. This makes it a challenging background to remove from the electron neutrino signal for the oscillation analysis.
The next generation of oscillation experiments would need to precisely constrain and understand the neutrino-nucleus interactions. Neutrino-nucleus cross-section measurements will provide vital inputs to sucessfully acheive the stated sensitivites of neutrino oscillation measurements. </p>

***
## detector development

<p>  To meet its ambitious physics goals, the upcoming DUNE experiment will feature the most intense accelerator neutrino beam in the world and achieve extraordinary precision by employing and advancing the liquid argon (LAr) detector technology. The DUNE detectors are designed using several novel technologies, among them is a modular liquid argon (LAr) detector featuring pixel charge readout instead of traditional wire readout. This design will provides unambiguous 3D tracking of charged particles crossing the LAr time projection chamber (TPC) detector in a high-multiplicity environment.  Various technological breakthroughs to build this detector have been demonstrated successfully in small scale testing facilities. However, a fully integrated prototype detector is essential to test robustness and validate the scalabiltiy for the full detector.
We are testing a 2 x 2 grid of modular LAr detector in the NuMi beam facility at Fermilab to fully optimize and characterize features of this novel detector design.

</p>

<div class="row mt-3">
      <div class="col-sm mt-3 mt-md-0">
       {% include figure.html path="assets/img/cropped_evd_mod0.gif" title="3-flavor neutrino oscillation" class="img-fluid rounded z-depth-1"%}
     </div>

      <div class="col-sm mt-3 mt-md-0">
       {% include figure.html path="assets/img/cropped_evd3_mod0.gif" title="3-flavor neutrino oscillation" class="img-fluid rounded z-depth-1"%}
     </div>

      <div class="col-sm mt-3 mt-md-0">
       {% include figure.html path="assets/img/cropped_evd2_mod0.gif" title="3-flavor neutrino oscillation" class="img-fluid rounded z-depth-1"%}
     </div>
</div>
<div class="caption">
     Raw event displays from the trial runs of a single module of the modular pixelated LAr detector at University of Bern, Switzerlan in 2021. [Image Credit: <a href="https://argoncube.org/tracks.html">ArgonCube Collaboration</a>] 
     </div>

***
## high performance computing


<div class="row mt-3">
      <div class="col-sm mt-3 mt-md-0">
      {% include figure.html path="assets/img/larndsim-logo.png" title="neutrino scattering" class="img-fluid rounded z-depth-1" align="right"%}
       <div class="caption">
      <a href="https://doi.org/10.5281/zenodo.7023803"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.7023803.svg" alt="DOI"></a>	
     </div>
       </div>

     <div class="col-sm mt-3 mt-md-0">
     <p> A simulation predicting how neutrinos would behave inside a modular pixelated liquid Argon detector is critical for the characterization and development of the new detector technology that DUNE will feature.
     Considering the unprecedented amount of data that DUNE will produce, specially at the near detector which will be located close to the beam target of the most intense neutrino beam, we need to employ highly parallelized computational algorithma that are able to run efficiently and are compatibile with the next-generation of GPU powered supercomputers such as Perlmutter at Lawrence Berekeley National Lab.

</p>
     </div>
</div>


We developed `larnd-sim` package which is the first implementation of a full Monte Carlo simulator for a liquid argon time project chamber (LArTPC), implemented with an end-to-end set of GPU-optimized algorithms which achieves three orders of magnitude spped-up compared to CPU implementation .
The algorithms are translated into CUDA kernels using <a href="https://numba.pydata.org/">Numba</a>, a just-in-time compiler for Python. A publication on this is in progress.

***