# ATLAS HIGGS BOSON ML
##### v.0.5.0

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NadiaLL/atlas-higgs-boson-ml/blob/main/atlas-higgs-boson-ml-v.0.5.0.ipynb)


## Abstract
The dataset has been built from official ATLAS full-detector simulation, with "Higgs to tautau" events mixed with different backgrounds. The simulator has two parts. In the first, random proton-proton collisions are simulated based on the knowledge that we have accumulated on particle physics. It reproduces the random microscopic explosions resulting from the proton-proton collisions. In the second part, the resulting particles are tracked through a virtual model of the detector. The process yields simulated events with properties that mimic the statistical properties of the real events with additional information on what has happened during the collision, before particles are measured in the detector.

The signal sample contains events in which Higgs bosons (with a fixed mass of 125 GeV) were produced. The background sample was generated by other known processes that can produce events with at least one electron or muon and a hadronic tau, mimicking the signal. For the sake of simplicity, only three background processes were retained for the Challenge. The first comes from the decay of the Z boson (with a mass of 91.2 GeV) into two taus. This decay produces events with a topology very similar to that produced by the decay of a Higgs. The second set contains events with a pair of top quarks, which can have a lepton and a hadronic tau among their decay. The third set involves the decay of the W boson, where one electron or muon and a hadronic tau can appear simultaneously only through imperfections of the particle identification procedure.

Due to the complexity of the simulation process, each simulated event has a weight that is proportional to the conditional density divided by the instrumental density used by the simulator (an importance-sampling flavour), and normalised for integrated luminosity such that, in any region, the sum of the weights of events falling in the region is an unbiased estimate of the expected number of events falling in the same region during a given fixed time interval. In our case, the weights correspond to the quantity of real data taken during the year 2012. The weights are an artifact of the way the simulation works and so they are not part of the input to the classifier. For the Challenge, weights have been provided in the training set so the AMS can be properly evaluated. Weights were not provided in the qualifying set since the weight distribution of the signal and background sets are very different and so they would give away the label immediately. However, in the opendata.cern.ch dataset, weights and labels have been provided for the complete dataset.


## References
https://higgsml.ijclab.in2p3.fr/documentation/
