# ALPs-phenomenology

## What it is?

Mathematica notebook summarizing the phenomenology of axion-like particles (ALPs). It produces decay widths and production probabilities of the ALPs depending on their coupling pattern as defined at some scale Lambda. Details of the phenomenology are summarized in the accompanying paper XXX.


### Dependencies

To run the notebook, one tool have to be installed: [FeynCalc](https://feyncalc.github.io/). 

### Code structure

First, you have to launch the chapter <dt><code>Definitions</code></dt>. It will import all the relevant data, evaluate the RG flow of the couplings for various initial patterns defined at the scale Lambda, define the kinematics of n-body decays, calculate the total Lagrangian of the ALP interaction with light mesons and photons, and find the model-independent diagonalization in the space of ALPs and neutral pseudoscalar mesons. The available models are defined in section <dt><code>ALP models and typical scales used in this notebook</code></dt>.

If you want to compute and export ALP decay widths, launch the chapter <dt><code>ALP decay widths</code></dt>. It first defines Feynman rules for the ALP Lagrangian for tree-level decay processes, then computes the matrix elements of the decay processes, and finally exports the widths and squared matrix elements. When exporting, it calculates the matching ALP mass where the hadronic width in terms of ChPT gets converted into the width in terms of perturbative QCD. The user may select the model of interest via dialog windows. The exported widths may be plotted by launching the chapter <dt><code>Plots: decay widths</code></dt>. 

If you want to compute and export ALP production probabilities, launch the chapter <dt><code>ALP production</code></dt>. It evaluates the RG flow of the FCNC couplings, the production probabilities of the following processes: decays of B mesons and kaons into ALPs, Drell-Yan process, and mixing with light mesons. 




## (Currently) implemented models, limitations, and bugs

Currently, the fully supported models are ALPs with flavor-diagonal universal couplings to quarks, leptons, and to gluons. More models will be added in the future.

This is a beta-version of the notebook, so there may be issues. You are very welcome to report about them.

 
