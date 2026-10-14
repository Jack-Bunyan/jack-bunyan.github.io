---
title: On Radiotherapy Planning
tags:
  - Radiotherapy
---
![[Pasted image 20261013091150.png]]
I genuinely have no idea what this figure could possibly be trying to show me.  What is a?  What is b?  Why are some of the lines wiggly?!?!?  Why is it in polar coords!

Considerations of where it is likely that the tumour has spread, e.g. cropping away from [[Anatomy & Physiology-Bone & Skeleton|Bone]].  In the [[Brain|Brain]] It is unlikely that the tumour has spread to the other hemisphere. 

Updated terminology for target volumes includes the type of disease (tumour, nodes, mets).  And is intended to describe the method of identification and the former dose delivered.

e.g. GTV-T (CT, 20Gy) would be a Tumour GTV, that was identified using CT and has already received 20Gy of radiation.

# Parallel vs Serial Organs
![[Pasted image 20261013091615.png]]

While a very simple model, the idea that organs can be either serial (and their $D_{max}$ matters), whereas in a parallel organ it is the [[Dose]] distribution/ extent that matters.  In a Serial organ using a more generous organ at risk expansion is important to account for hot spots, whereas in a parallel organ increased expansion of the organ could make the dose distribution look better or worse than it actually is.

What the planning guidelines for organs at risk should be is determined from research and trials, which analyse the tissue effects from dose to local organs.  When considering compromise for coverage of organs understanding what these mean is important.

Dose volume histograms are a useful way of visualising the distribution of the dose to an organ and comparing between different plans.  The prescription however is defined by a single "point" within the organ, with the dose to the PTV being between 95% and 107% of this prescribed dose.

Title: [Quantitative Analyses of Normal Tissue Effects in the Clinic (QUANTEC): An Introduction to the Scientific Issues](https://pmc.ncbi.nlm.nih.gov/articles/PMC3431964/)
Authors: Søren M. Bentzen, Louis S. Constine, Joseph O. Deasy, Avi Eisbruch, Andrew Jackson, Lawrence B. Marks, Randall K. Ten Haken, Ellen D. Yorke
Year: 2010
DOI: 10.1016/j.ijrobp.2009.09.040

# ICRU Reference Point

1) Clinically relevant and representative of the dose throughout the PTV
2) The point should be easy to define and clear and unambiguous
3) The point should be selected where the dose can be accurately determined
4) The dose should be selected in a region where there are no dose gradients

While TPS systems have made it easier to visualise a reference point, it is important to consider that these definitions were created prior to modern treatment planning.   This means that as treatments have become more complex the definition of a good reference point has become more difficult; with dose gradients everywhere, moving tissues and organ compromises.

- [Parallel Opposed Pairs](https://spark.iop.org/radiotherapy-planning-interactive): halfway point in the middle
- VMAT, it is advised to avoid the use of a single point as the dose point, instead us $D_{50\%}$ or $D_{98\%}$

# Planning methods
1) Simple V-Sim plans, may not even have a 3D dose calculated for them
2) Forward planning
3) Inverse Planning
4) *Specialist techniques*

## Forward Planning
Technically these uni notes are from [[Dose Calcs-UN 14-10-2026|The Day After]] but they fit better here tbh.

Forward planning is a technique where we adjust the parameters to adjust the dose, and continue to vary the plan until it meets the objectives.  It is a bit fiddly but also a very simple method.  This becomes more complex as the planning technique becomes more advanced, for example, by varying the positions of the [[MLC]]s during delivery of the beam we can Vary the Intensity of the beam (IMRT).  Step-and-Shoot can also be used by turning off the beam between MLC shifts but this kind of sucks and would be silly to use.
## Inverse Planning
Inverse planning works in reverse, providing a list of conditions that want to be met for different organs, and then using algorithms to gradually discover an optimal solution.  This allows more complex plans such as Dynamic Delivery (DMLC) and Volumetric Modulated Arc Therapy (VMAT).  VMAT alters the position of the leaves, the dose rate, and the position of the rotation speed; this provides far more degrees of freedom.

The downside of VMAT is that while the therapeutic dose is more conformal there is a larger dose bath to healthy tissue.  VMAT does potentially require more work in other areas of the treatment process, such as increasing the number of contours that need to be created, as well as establishing dose targets for each of the structures that wants to be considered during planning.

This optimisation is done my minimise a cost function that represents how "bad" a plan is, gradually aiming to reach an optimal solution.  Ideas such as normal tissue optimisation are used to just generally lower dose outside of the PTV

In some cases a site will have a class solution, this will give a template of objectives that may allow for quicker optimisation with less required alteration of goals.  Similarly Knowledge based plans such as RapidPlan estimates what the achievable clinical plan will be.
# Dose Distribution
Back to today
![[Pasted image 20261013093831.png]]
This might be important to know/ have a general vibes for. 

Since patients are not uniform spheres they have regions of different density inside of them, this means that at the surfaces of bone there will be a higher dose due to secondary build up, while at the exiting surface of a lung dose will be lower due to the lack of build-up.

The quicker build up of lower energies is why we like 6FFF for [[lungs|Lung]] treatments.  As higher energies may not reach peak dose before the end of the tumour.  At the surface of the skin build-up could prevent the treatment of [[Skin Cancer|Skin]] legions.  Bolus is used to allow for dose build-up prior the the beams entry into the skin.  While "Skin Flash" accounts for the tissue swelling during treatment, this is very common in breast treatments.

Wedges are a historical approach for correcting for angled skin surface, where a literal wedge is used to lower the incident dose to regions that have less tissue that must be passed through.  The use of virtual wedges is where instead the MLCs are used, they also can be used to correct for beams at an angle of less than 180 degrees

$$Optimal Wedge \approx 90^\circ -\frac{hinge angle}{2}$$


> More fields= More good

# Plan Evaluation

> Conformal = Good

When reporting the dose it is advised against using min/max, as these are both heavily effected by the size of the voxels/ an individual voxel, and is unlikely to have much clinical affect.

Exceptions exceptions everwhere:
- How to evaluate compromised PTVs
- Which PTV dose do you prioritise
- Reporting dose outside body?!?


I should look into [Space OAR](https://www.spaceoar.com/us/en/home.html) Which is a injected gel between the prostate and the prostate and rectal to reduce side effects by changing the internal anatomy of the patient.  Trials need to be ran to alter the prescriptions/ fractionation regimes that we use, e.g. prior to 60Gy/20# we used 72Gy/37#.  Soooooo many prostate trials are ongoing that could impact the way that we plan treatments
- flame
- radicals
- atlanta
- pivotalboost

Could be worth considering that a more conformal plan will be more fragile with variation in the position of the patients, if you had a "perfect" plan that dropped immediately outside of the PTV, any shift could have large impact.

# Clinical Evaluation: Brain

Brain disease can be either a primary tumour of the brain or metastasis, main source is from the lung.  

approximately 13,000 (3% of cases) people every year are diagnosed, with a 3 year survival rate of 20% after 10 years.  Also a frequent location of small cell lung cancer tumours.

MR for soft tissue contrast of the brain.  CT for positioning and HU, 1mm slice width

Exact Track


SRS-Sterotactive Radio Surgery
AVM-Alterior Venous Malformation

Often use specialist systems
- Cyberknife
- Gammaknife






