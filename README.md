# Fatjet-Construction
A study on the impact of various clustering algorithms, subjet axes definitions and choice of input particles on the construction of fatjets and their discrimination between high and low pT boosted hadronically decaying SM bosons and top quarks.

Here we will use Delphes for dector response and object reconstruction. The SM processes considered are $t\bar{t}$, $VV$, $VH$, $HH$, where $V=W^\pm, Z$ (50k events each). The signal process considered are pair-produced type III seesaw heavy leptons ($m=1.0$ TeV). All bosons are allowed to decay either hadronically or leptonically to eveluate impace on $\min\Delta R(\ell, J)$.

Scan (1) config region:
- Input Particles: "EFlowMerger/eflow", "EFlowFilter/eflow"
- Clustering Algorithms : 5 (CA), 6 (anti-$k_T$), 7 (anti-$k_T$ with WTA recombination scheme)
- Characteristic Radius : 0.8, 1.0, 1.2
- N-subjettiness $\beta$ paramater : 1.0, 2.0
- N-subjettiness axis mode : 1.0 (WTA_KT_Axes), 2.0 (OnePass_WTA_KT_Axes), 3.0 (KT_Axes), 4.0 (OnePass_KT_Axes)
- Jet min $p_T$ : 100.0 GeV, 200.0 GeV

Goal of this scan: identify config paramaters that maximize AUC under ROC curve of $\min\Delta R(\ell, J)$, $\tau_2/\tau_1$ and $\tau_3/\tau_2$.
