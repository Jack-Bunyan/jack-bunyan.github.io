---
title: On Beam Data
tags:
  - Radiotherapy
  - Question
---
# Learning Outcomes
- Understand the reasons why beam data collection may be required
- Knowledge of the key basic measurements
- Tank set-up considerations and their effects on beam data collection

---

Reasons for collecting beam data
- QA
- Commissioning a new
	- Machine
	- Beam Model
- Commissioning of a treatment planning system

# Measurements that are taken
- Depth dose
	- PDD
	- TMR
	- TPR (not [[Quality Index|20 10]])
- Profiles
	- In-plane
	- Cross-plane
- Output Factors

## Depth Dose
Pecentage Depth [[Dose]], often calculated by moving the detector from the bottom of the water tank towards the surface of the water, decreasing the depth in water while maintaining a distance to the surface of the water.  This means that it will include the affect of inverse square law as the source to detector distance changes.

Alternatively TMR and TPR are more appropriate for plans which are made using a fixed SDD, this is done by changing the depth into water of the detector while maintaining the SSD, mostly by moving the entire tank and detector at the same time.


| Increased Field Size | Increased PDD | From internal scatter                                                                 |
| -------------------- | ------------- | ------------------------------------------------------------------------------------- |
| Increased SSD        | Increased PDD | Normalisation over-corrects for inverse square<br>(decreasing gradient with distance) |
> Regarding increased SSD, consider that if @1cm, going from 1cm->2cm is a double of distance to a quarter of dose.  Going from 3cm->4cm is a roughly half (9/16)

# Profiles
Defined both from the MLCs and the Jaws, these are at different heights, which means that the penumbra effects from a 5x5cm MLC field will be different to a 5x5cm Jaw defined field.

We may measure the penumbra, the flatness, and the symmetry of differently sized profiles.  These will all change at different depths due to differing levels of [[On Particle Interactions|Attenuation]] and energy, this is especially the case for flattened fields, as the thicker metal towards the centre of the filter hardens the beam compared to the edges of the field.

# Output Factors
These describe how the dose at the reference point changes with the size of the field, this is often also split into the head scatter (from the linac) and the patient scatter (from the patient).  Larger field sizes typically have larger outputs factors as they have more scatter.

# Tank Set-up
It is quite a big lad.  Typically done on its own stand due to this to avoid loading the couch with a large amount of weight, although tomotherapy units are special.  Very important to ensure the setup of the unit is correct given that any difference between reality and what you think is the situation will cause error, which if commissioning could be v. significant.

> Use of the shadow of the [[Chambers|Chamber]] on the bottom of the tank to check for setup errors.

