---
title: On Dose
tags:
  - Imaging
  - Physics
  - Therapy
  - Radiotherapy
  - Nuclear_Medicine
---
Absorbed dose describes the absorbed-energy "density" of a material, with units of Gy \[Jkg$^{-1}$\].  This is one of the most important aspects of radiation physics and is how radiation protection is managed, and medical exposures are optimised.

Measurements of dose are taken in [[Radiotherapy]] using various different [[Chambers]], these measure the ionisation of the air as a current between two conductors, and convert this to a measurement of the dose in air.  It can be modelled 

# Equivalent Dose
Equivalent Dose is a a metric that is used to convert from the energy dose deposition that is measured using physical instruments, into one that takes into account the does deposition mechanisms in tissue.  They are normalised against the biological effectiveness of photons having a radiation weighting factor ($\omega_r$) of 1.  Heavier particles such as protons or heavy ions have larger values of $\omega_r$.  This increases their effect within [[Hypoxic]] environments and is one of the advantages of [[Proton Therapy]] compared to photons.  While measured using the same units (Jkg$^{-1}$) as absorbed dose, both equivalent and effective dose use the units of sieverts rather than grays.

> $\omega_r = \begin{cases} \text{Photons}: 1 \\ \text{Electrons and Muons}: 1 \\ \text{Protons and charged pions} = 2 \\ \text{Alpha particles, fission fragments, and heavy ions} = 20 \\ \text{Neutrons: See below}\end{cases}$

![[Neutron dose curve.png]]

These specific values are tragically, a bit scuffed and not real.
# Effective Dose
Effective dose is used exclusively for the determination of the stochastic cancer risk that a patient is exposed to.  It is calculated from the multiplication of the equivalent dose to an organ by its tissue weighting factor $\omega_T$.  This tissue weighting factor is important as different tissues within the body have different sensitivities.  These sensitivities are shown below:

| Organ                                                | $\omega_T$/Tissue |
| ---------------------------------------------------- | ----------------- |
| Lung, stomach, colon, bone marrow, breast, remainder | 0.12              |
| Gonads                                               | 0.08              |
| Thyroid, Oesophagus, bladder, liver                  | 0.04              |
| Bone surface, skin, brain, salivary glands           | 0.01              |
Current models of cancer induction assume that the increase in cancer risk associated with radiation exposure is linear and has no limits.  This is because the majority of data that is used for cancer induction is from radiation incidents and has little data for both low and high radiation exposures.
![[Radiation exposure cancer induction figure uni.png]]

We currently model that a mSv of effective dose puts a person at a 1/20,000 risk of fatal cancer; however, more recent data suggests that there is a lower limit to the induction of cancer from radiation.  With this, radiation standards are gradually moving away from current [ALARA](https://www.neimagazine.com/news/us-moves-to-revise-alara-standard/) standards to introduce a threshold limit; though, this is [controversial](https://thebulletin.org/2026/05/the-trump-administrations-reckless-attack-on-radiation-protection-will-have-long-term-consequences-for-public-safety/) as it will potentially decrease nuclear industry costs, so has clear economical motivations.  Silver-lining, we'll have more data in ~30 years!
# Deterministic 


Title: [The 2007 Recommendations of the International Commission on Radiological Protection. ICRP publication 103]()
Authors: 
Year: 2007
DOI: 10.1016/j.icrp.2007.10.003

Title: [A review of dosimetry studies on external-beam radiation treatment with respect to second cancer induction](https://pmc.ncbi.nlm.nih.gov/articles/PMC4009374/)
Authors: X George Xu, Bryan Bednarz, Harald Paganetti
Year: 2008
DOI: 10.1088/0031-9155/53/13/R01

Title: [It Is Time to Move Beyond the Linear No-Threshold Theory for Low-Dose Radiation Protection](https://pmc.ncbi.nlm.nih.gov/articles/PMC6043938/)
Authors: John J. Cardarelli, Brant A. Ulsh
Year: 2018
DOI: 10.1177/1559325818779651
