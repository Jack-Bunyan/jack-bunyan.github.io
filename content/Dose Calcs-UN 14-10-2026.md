---
title: On Dose Calculation
tags:
  - Physics
  - Radiotherapy
---
During [[Planning-UN 13-10-2026#Planning methods|Planning]] it is important to understand how the [[Dose]] being utilised will be delivered to the patient.  There are many different algorithms available to calculate this, with each having trade-offs which make the appropriate for different situations.

In ye olden days hand calculations were quite popular, and could be reasonably accurate for what the dose would be at different depths, however this is a very slow process so makes it difficult to optimise.  Also can only use limited information, how to account for bones, shaping, movement, or many many fields.

As treatments have gotten more advanced and the standards we have for treatments have improved using hand calculations has become less possible.  We also increasingly have more computing power and more information that can be used to create a dose calculation.

>Would you want to calculate a VMAT plan by hand?!?!

The requirements for an algorithm are that they:
- accurately report the dose to the patient
- quickly predict the delivered dose distribution
These two variables are the two that have to be traded off between, monte-carlo algorithms are great, but very slow.  If actively optimising using a much faster algorithm could be vital to calculate an optimal plan.  As we have a constant throughput of patients that need to be planned.

![[Pasted image 20261014103853.png]]
Figure of where the dose delivered during a treatment that can be from.

Algorithms can be broadly split into being a few different methods.

Pencil-Beam and point dose calculate dose to water, whereas Monte carlo and FEM calculate dose to medium.  Can convert between the two using cavity theory but that is an additional step.
# Empiricle
$$Dose(f,s,d,W,r)=MU\times \left(\frac{100+d_{max}}{f+d_{max}}\right)^2\times O(s)\times PDD(f,s,d)\times W(s)\times P(r) $$
The depth used for this equation is an effective depth, and this does not model secondary electron transport, which makes up 25-30% of the dose distribution.  While this broad beam method is quite simple, it is also possible to establish one broader beam from a large range of other beams.  Or simulation knowing the dose from other points.

It is understood that the dose at a given point D can be found from
$$D_P(x,y,z)=\int\int\int p(x',y',z')s(x,x',y,y',z,z')dx'dy'dz'$$
this works quite well, however begins to break down near the boundaries of tissues such as bone where charged particle equilibrium cant be established.  Also worse for small fields were the cross section is less than the scatter distance of secondary electrons

## Point Dose Kernels
This algorithm functions using the calculation of how the scattered electrons from each voxel of the primary beam deliver dose to other points.  At low energies this will be quite isotropic but as the energy of the beam increases more of the electrons will be forward scattered.  This changes the pencil beam equation to becomes
$$D_P(x,y,z)=\int\int\int \frac{\mu}{\rho}\Phi_E (x',y',z')K_{PB}(x-x',y-y',z-z')dx'dy'dz'$$

This again struggles with the lateral scatter of dose, especially at inhomogeneities.

## Monte Carlo
Nightmare

Macro monte-carlo is a quicker but slightly less accurate method.

## Finite Element Method
$$Q(\vec x,e, \Omega)=\Omega \cdot \vec\Delta \phi +\sigma\Omega$$

This can be solved over a mesh and is both very quick but also very accurate.  This is what we use locally at Hull under the name of accuros, it can be slower for simpler plans but as plans get more complex it becomes more efficient compared to pencil beam algorithms (AAA).

# Classifications
In 2006 it was decided that algorithms could be roughly grouped into two types.
- Type A, lack of modelling for lateral transport of electrons.
- Type B, lateral transport of electrons should be modelled.
- ![[Pasted image 20261014112403.png]]
![[Pasted image 20261014112053.png]]
![[Pasted image 20261014112321.png]]This was the worst case scenario for the pencil beam algorithm in comparison to the others.

# Learning Outcomes
1)  Explain how common classes of dose calculation algorithms calculate dose distributions for EBRT plans
2) Critically assess the differences between dose distributions created using Type (a) and Type (b) algorithms
3) Analyse the clinical situations where Type (a) or Type (b) algorithms are most appropriate
4) Illustrate algorithms for calculating dose distributions for electron radiotherapy plans


---

# Manual Calculations

>2005 is a million years ago

## Case Study 2005 NY
43yo patient with orophangeal cancer was treated with 2Gy/#

at fraction 4 they were re-planned to try and improve the plan.  An attempt was made to try and save the re-plan, while it saved the fluence data and the DRRs (images) were were reverted the MLC positions were not saved.

2 days into new treatment radiographers incidentally realised that the MLCs were missing.  Rather than 2Gy 13Gy was delivered in each fraction for a BED in the hundreds.  This occurred before independent dose calculations were popular, which were made mandatory within Towards Safer Radiotherapy.

## Independent Checks
Independent dose checks are easily possible using 3-dimensional arrays of diodes, however takes a lot of effort.  Would also be a lot easier however to measure using an EPID panel.  Although this doesn't test the HU curves used for dose calculations.  The differences between what is measured and delivered can be analysed using a "gamma analysis"; this is used to compare how much difference there is spatially and outputly.

$$\Gamma=\sqrt{\left(\frac{DTA}{DTA Criteria}\right)^2+\left(\frac{\%DD}{\%DD Criteria}\right)^2}$$
This can also be be used for in-vivo dosimetry, in a process known as "Transit Dosimetry", which satisfies the requirements of TSR.

## Finally Manual Calculations
the setup to consider for manual calculations is the one shown below.
![[Pasted image 20261014153229.png]]
> Rules of thumb for single fields
> 1cm further = 2% colder
> 1cm less depth = 3% warmer
> (100cm ssd)

## Rules of thumb for electrons

Energy in Mev
Dmax=2x
d90=3x
d50=4x
d10=5x

Counting is hard.


---
# Seminar Calcs

>$$Dose=MU\times PDD\times S_{cp}\times \text{(inverse square)}$$

Correction for SSD at d_max

$$\times \left(\frac{100+d_{max}}{SSD_2+d_{max}}\right)^2$$

Which is a special case of the correction for SSD at all points:
>$$PDD(SSD_2,FS,d) = PDD(SSD_1, FS,d)\times \left[\frac{(SSD_2+d_{max})(SSD_1+d)}{(SSD_1+d_{max})(SSD_2+d)}\right]$$

Equivalent square correction ($S_{cp}$) for rectangles can be calculated as:
$$ES=\frac{4\times Area}{Perimeter}=\frac{2\cdot XY}{X+Y}$$

## Example 1
- 6cm deep:read off table
- 10x10: 1.00 correction
- 6MV
- 100cm SSD: 1.00 correction
- 200 MU

ergo
$$Dose=200\times1\times 0.821\times 1 = 164.2cGy$$
## Example 2
- 5cm deep: read off table
- 6.3x11cm field : correction
- 6MV
- 90cm SSD: correction
- 300MU

this is a worst case scenario

1) find the equivelant square
	- $=\frac{2*6.3*11}{6.3+11}=8$
2) Read off PDD: 0.857
3) Correct PDD for SSD
	- $0.857\times\frac{(90+1.6)(100+5)}{(100+1.6)(90+5)}=0.993$
	