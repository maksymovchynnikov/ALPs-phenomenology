# ALPs-phenomenology

## What it is?

Mathematica notebook summarizing the phenomenology of axion-like particles (ALPs). It produces decay widths and production probabilities of the ALPs depending on their coupling pattern as defined at some scale Lambda. Details of the phenomenology are summarized in the accompanying paper [2310.03524](https://arxiv.org/abs/2310.03524).


### Dependencies

To run the notebook, one tool have to be installed: [FeynCalc](https://feyncalc.github.io/). 

### Code structure

First, you have to launch the chapter **Definitions**. It will import all the relevant data, define various ALP coupling patterns (section _ALP models and typical scales used in this notebook_), evaluate the RG flow of the couplings for various initial patterns defined at the scale Lambda (section _ALP low-energy couplings (following 2110.10698 and 1708.00443)_), and find the model-independent diagonalization of the quadratic Lagrangian of ALPs and neutral pseudoscalar mesons (_ChPT with ALPs_). 

If you want to compute and export ALP decay widths, launch the chapter **ALP decay widths**. It first evaluates the phase space of n-body decays (_Kinematics of n-body decays_), calculates the full ALP-meson Lagrangian - including pseudoscalar, scalar, vector, and tensor mesons (_Total ALP-meson Lagrangian used to compute the widths_), defines Feynman rules for the ALP Lagrangian for tree-level decay processes(_Feynman rules_), then computes the matrix elements of the decay processes (_Matrix elements calculation_), and finally exports the widths and squared matrix elements (_Widths/matrix elements exporting_) assuming the coupling f = 1 GeV (see Eq. 2 for the definition of f). The f dependence may be recovered taking into account that the scaling of the widths with f is f^-2. When exporting, it calculates the matching ALP mass where the hadronic width in terms of ChPT gets converted into the width in terms of perturbative QCD. The user may select the couplings pattern of interest and the scale at which it is defined via dialog windows. The exported widths may be plotted by launching the chapter **Plots: decay widths**. 

If you want to compute and export ALP production probabilities, launch the chapter **ALP production**. It evaluates the production probabilities of the following processes: decays of B mesons and kaons into ALPs, Drell-Yan process, and mixing with light mesons. When exporting tabulated probabilities/branching ratios, f = 1 GeV is assumed. The dependence may be recovered taking into account that the scaling of all the exported quantities except for the modulus of the gluon coupling is f^-2, while for the gluon coupling it is f^-1.




## (Currently) implemented models, limitations, and bugs

Currently, the fully supported models are ALPs with flavor-diagonal universal couplings to quarks, leptons, and to gluons. More models will be added in the future.

This is a beta-version of the notebook, so there may be issues. You are very welcome to report about them.

 
