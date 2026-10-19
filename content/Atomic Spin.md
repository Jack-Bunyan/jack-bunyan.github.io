---
title: On Atomic Spin
tags:
  - Physics
---
Atomic spin is a fundamental feature of particles, with different elements oscillating at different rates, it is a quantised state, all of the classic subatomic particles have quantised spin of $\frac{1}{2}$, the net spin of a $^1H$ nucleus is $\frac{1}{2}$.  This net spin being non-zero is required for a nucleus to undergo resonance with an electromagnetic wave within a magnetic field.

This spin directly relates to the magnetic moment of a particle.
> $$\hat{\mu} = \gamma \hat{S}$$   

Whilst the precession rate of a particle inside of a magnetic field will be given by.
> $$\omega^0 = -\gamma B_0$$

Where B is the total magnetic field at the particle location and $\gamma$ is the gyromagnetic ratio of the particle (unique for any given particle or nuclei).  The most commonly used nuclei for MRI is $^1H$, it has a gyromagnetic ratio of $42.58\text{MHz}\cdot \text{T}^{-1}$.  You can remember this using the mnemonic that DC came up with:

> "I figured out a way of remembering the larmor frequency, it's like \[LK\], he's 42 and hes about 5'8"."
> 			-DC, Trainee RP$^2$ Clinical Scientist

This precession can be visualised using various classical equivalents, such as gyroscopes, basketballs, or driedels.
![[spinAnimation.gif]]
If we consider the many spins that are in any given voxel of space they will be distributed isotropically.  Their individual spins will be at random phases so the only magnetisation in the unexcited state is in the longitudinal direction, given they aren't directly measured it isn't correct to discuss individual spins as being in the spin up or down state, but as a function of temperature the ratio of these can be described using a Boltzmann distribution.
 $$\frac{N_\uparrow}{N_\downarrow} = \exp\left(\frac{\hbar \gamma B_0}{kT}\right)$$

During excitation more spins are put into the spin-down state than the spin-up state, this is a population inversion state which has a hypothetically "negative" temperature, so will only last during the excitation period, after which the spin will de-excite.

This excitation is done using a radiofrequency pulse with a magnetic component rotating at 90$^\circ$ to the B$_0$ field.  This is known as the B$_1$ field and typically has a strength of ~$25\micro T$ taking 0.23ms to rotate the spins 90$^\circ$.

# $T_1$ Contrast

This de-excitation of the spins from a spin-down to a spin-up state within the volume is what creates the $T_1$ of the image.  This decay is known as spin lattice relaxation, it can be modelled using the equation
>$$M_z(t)=M_0(1-e^{-t/T_1})$$

![[T1 relaxaiosn.png]]
Title: [A review of normal tissue hydrogen NMR relaxation times and relaxation mechanisms from 1-100 MHz: dependence on tissue type, NMR frequency, temperature, species, excision, and age](https://aapm.onlinelibrary.wiley.com/doi/10.1118/1.595535)
Authors: P. A. Bottomley, T. H. Foster, R. E. Argersinger, L. M. Pfeifer
Year: 1984
DOI: 10.1118/1.595535


These differences between how quickly the hydrogen atoms within different tissues of the body can lose their energy introduces [[contrast]] into the image.  It can also be used in [[Inversion Recovery]] sequences to suppress materials such as fat or fluid which can appear bright within images.


