# ALPs-phenomenology

## What is it?

Mathematica notebook summarizing the accelerator phenomenology of GeV-scale axion-like particles (ALPs) with hadronic couplings. It produces decay widths and production probabilities of the ALPs depending on their coupling pattern as defined at some scale Lambda. Details of the phenomenology are summarized in the accompanying papers [2310.03524](https://arxiv.org/abs/2310.03524) and [2501.04525](https://arxiv.org/abs/2501.04525).

Updates compared to the previous version: added many new production channels, improved the description of the ALPs coupled to gluons, changed the interaction structure with scalar mesons to account for the proper eta-eta' mixing. 


### Dependencies

To run the notebook, one tool has to be installed: [FeynCalc](https://feyncalc.github.io/). 

### Code structure

The main notebook is _Phenomenology. ALPs.nb_. It has sections **Definitions**, **ALP decay widths calculation**, **Plots: decay widths**, and **ALP production**. The code is modular, with various modules located in the folder `notebooks`. 

The section **Definitions** defines the available ALP models based on the pattern of the couplings to B bosons, gluons, fermions, W bosons (the module _alp-models.nb_), various functions and parameters (_parameters-functions.nb_), evaluates the RG flow of the couplings for various initial patterns defined at the scale Lambda following 2110.10698 and 1708.00443 (_alp-running.nb_), finds the model-independent diagonalization of the quadratic Lagrangian of ALPs and neutral pseudoscalar mesons (_alp-diagonalization.nb_), computes the total Lagrangian of the interaction of ALPs with pseudoscalar, scalar, vector, and tensor mesons (_alp-SVT.nb_ and _lagrangian-widths.nb_), as well as defines Feynman rules for various vertex (_feynman-rules.nb_) and kinematics of n-body decays (_n-body-decays.nb_). 

If you want to compute and export ALP decay widths, launch the chapter **ALP decay widths calculation**. It first evaluates squared matrix elements of various decays (_defining-decay-matrix-elements.nb_ and _calculating-decay-matrix-elements.nb_), and finally exports the widths and squared matrix elements assuming the coupling f = 1 GeV (see Eq. 2 of the associated paper [2310.03524](https://arxiv.org/abs/2310.03524) for the definition of f). The f dependence may be recovered considering that the scaling of the widths with f is f^-2. When exporting, it calculates the matching ALP mass where the hadronic width in terms of ChPT gets converted into the width in terms of perturbative QCD. The exporting is in the .csv format, the file is located in the directory `phenomenology/<model>/decays`. 

The exported widths may be plotted by launching the chapter **Plots: decay widths**. 

If you want to compute and export ALP production probabilities, launch the chapter **ALP production**. It evaluates the production probabilities of the following processes: decays of B mesons (_B-decays.nb_), kaons, eta/eta' mesons, rho0, omega mesons (_mesons-decays.nb_) into ALPs, Drell-Yan process (_drell-yan.nb_), and proton bremsstrahlung (_proton-bremsstrahlung.nb_), and fragmentation (_mixing-fragmentation.nb_). When exporting tabulated probabilities/branching ratios, f = 1 GeV is assumed. The dependence may be recovered considering that the scaling of all the exported quantities except for the modulus of the gluon coupling is f^-2, while for the gluon coupling it is f^-1. The exporting is in the .csv format, the file is located in the `directory phenomenology/<model>/production`.


## (Currently) implemented models, limitations, and bugs (to be improved in the next versions)

Currently, the fully supported models are ALPs with flavor-diagonal universal couplings to quarks, leptons, and gluons. More models will be added in the future.

The production via fragmentation (the improved version of the production channel previously known as "Mixing") has not yet been implemented.

For the ALPs coupled to gluons, the implemented exclusive decay modes produce too small width to match it with the perturbative QCD widths properly

This is a beta version of the notebook, so there may be issues. You are very welcome to report about them.

Some parts of the code work much slower on Mathematica < 14.1.
 
