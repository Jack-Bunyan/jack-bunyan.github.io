---
tags:
  - Physics
title: On Particle Interactions
---
# Photons
Photon interactions with matter consist of 3 main kinds:
- Pair production
- Photoelectric effect
- Compton Scatter
- Elastic Scatter
![[Photon-cross-section-RTBible.png]]
Overall, this leads to 3 main regions in most materials, a low energy region where the photo-electric effect is dominant, and intermediate region where Compton scatter is dominant, and a final region where pair production becomes dominant.
## Pair-production
![[feynman-Pair-Production.png]]
Pair production is only possible for photons that have a total mass greater than 1.022MeV (twice the fundamental mass of an electron).  When this is reached there is a probability that when interacting with the electric field of a charge they will produce a positron and electron.

The probability of an with the [[Atom#nucleus|Nucleus]] of an atom occurring is proportional to the square of the charge of the nucleus ($\sigma_{pp-n} \propto Z^2$), while occurring within the field of it's electrons (a process known as triplet production) is proportional to the number of electrons ($\sigma_{pp-e} \propto Z$).

Title: [Cross section data for electron–positron pair production by photons: a status report](https://www.sciencedirect.com/science/article/pii/S0168583X03015246)
Authors: J. H. Hubbell, S. M. Seltzer
Year: 2004
DOI: 10.1016/S0168-583X(03)01524-6

## Photo-electric effect
![[feynman-Photo-Electric.png]]

The photo-electric effect is the process by which a photon is completely absorbed by an electron in the [[Atom#Orbital Shell|Orbital Shell]] of an [[Atom]].  This is the dominant process at low energies with the cross section of the interaction being inversely proportional to the cube of energy and the 4-5th power of the nucleus charge ($\sigma_{pe} \propto \frac{Z^{4\rightarrow 5}}{E^3}$).  This cross-section increases significantly when close to the transmission level of an orbital electron, this can be used by [[Photon Counting CT]] to perform spectroscopy on low Z contrast agents.
![[Ray-Spectrum_Iodine.png|697]]
The locations of these spikes will depend on the orbital energy levels of the atoms, this means that in elements (e.g. [[Iodine]], [[Calcium]], [[Lead]]) there will be sharp peaks at the locations of orbital transitions.  Whereas in more complex mediums (e.g. [[Bone]], soft tissue) these sharp transitions will overlap, creating a more continuous attenuation function.

## Compton Scatter
![[feynman-Compton_Scatter.png]]
Unlike the photo-electric effect where the energy from the photon is absorbed completely by the electron into kinetic and electrostatic energy; Compton scatter is a process by which the photon scatters from an electron, changing angle.
![[Figure_Compton-Scatter.gif]]
This results in a deflection of the photon by an angle $\theta_\gamma$, and a electron travelling away at an angle $\theta_e$ from the initial path of the photon.  Given the conservation of momentum and energy the transfer of energy to the electron can be calculated based on the angles of these deflections.
$$\lambda'-\lambda =\frac{h}{m_ec}(1-\cos\theta_\gamma)$$
For photon energies lower than the electron mass, the cross section of photon scatter remains relatively constant ($\sigma_{cs} =\frac{8}{3} \pi r_e^2$), and remains the dominant photon interaction within the 1-10MeV range for photons.

## Rayleigh and Thompson Scatter
Rayleigh and Thomspon scatter are both forms of elastic scattering from charges.  In the case of Rayleigh scatter this is a result of scatter from an entire atom, whereas Thompson is from an unbound electron.  The cross-section of Rayleigh is proportional to the inverse square of energy ($\sigma_{rs}\propto E^{-2}$), whereas the cross section of Thompson is more complex the correlation is slightly stronger than the inverse square.
# Cross-section

The Cross-section of an interaction will be dependant on the nature of the particle, its energy, and the medium that it is passing through.   Analytically, if the cross section of a particle is described as $\sigma$ the total flux of particles passing through a medium can be described to be:
>$$\Phi  =\Phi_0 e^{-n\sigma z}$$

This comes from the idea that the rate of interaction within the medium is described as 
>$$\frac{d\Phi}{dz}=-n\sigma \times \Phi$$

Since this is a probabilistic situation it will correlate with the total number of events when it could happen, and the more particles are in a medium the more likely an interaction.  
# Electrons
The primary source of energy loss in charged particle interactions are collisions, electrons being the lightest of these charged particles have 3 main interactions:
- Moller scattering- collisions with bound electrons
- Bremsstrahlung- radiative losses from charge acceleration
- Elastic scattering- mostly a result of collisions with heavy charged particles
![[Electron-Stopping-Power-RTBible.png]]


## Collision Losses
When an electron approaches another charged particle it interacts via the coulomb force and will lose energy.  This can be calculated classically assuming that the other particle has a charge $e$.
>$$Q=\frac{2k^2z^2e^4}{mb^2v^2}$$

Where b is the distance of closest approach, in some cases this energy will be enough that the charged particle will itself have a significant path length, in these cases the excited particle is known as a "delta ray".  The cross section of this interaction against energy can be found
>$$\frac{d\sigma}{dQ}=\frac{2\pi z^2e^4k^2}{mV^2}\frac{1}{Q^2}$$
>$$\frac{d\sigma}{d\epsilon}=\frac{2\pi e^4k^2}{Tm_eV^2}\left[\frac{1}{\epsilon^2}+\frac{1}{(1-\epsilon)^2}+\left(\frac{\tau}{\tau+1}\right)^2-\frac{2\tau+1}{(\tau+1)^2}\frac{1}{\epsilon(1-\epsilon)}\right]$$
>Horrid equation.  T is the electron kinetic energy, $\epsilon$ is the fraction of electron energy transferred, $\tau$ is the electron k.e. in units of its rest mass. 

The occurrence of these many small interactions along the path of an electron means that often, we use stopping power as the measurement of choice for electron interactions.  Stopping power is defined as the energy loss per unit length—$\frac{dE}{ds}$—along the path of a particle, often being characterised using the ratio mass stopping power $\frac{1}{\rho}\left(\frac{dE}{ds}\right)$. 

Initial analytical approaches to the calculation of stopping power in materials came to finding that it was infinite, this was due to an infinite number of very low-energy interactions slowly sapping the energy from the particles, with the advent of quantum mechanics, approaches were considered that applied a lower bound on the allowable energy transfer, this has a significant impact on the distribution of events.
![[quantum efect stopping power.png]]

In dense materials the charges close to the track of the is screened by the material, this leads to the "density effect", which reduces the size of the relativistic rise in denser materials such as water compared to in air.

## Radiative Losses
Bremstrahlung is the release of energy from particles that are accelerating within an electric field.  It is the primary mechanism behind the production of x-rays in [[X-ray Tube|X-ray tubes]].  The approximiation that:
>$$\frac{S_{rad}}{\rho}\propto\frac{Z^2}{A}EB$$
>Where B is a slowly varying function of Z and E

![[rad vs col stopping power graph.png]]

# Neutrons
They're Weird.

Neutrons don'd interact via the coulomb force since they are uncharged particles.  They interact via classical collision interactions with other particles at high energies, until they have lost enough energy that they can be absorbed by the nucleus.  This will typically create an unstable nucleus which will [[Decay Events|Decay]]

This has interesting applications such as [[Boron Neutron Capture Therapy]]

---
Title: [Handbook of Radiotherapy Physics: Theory and Practice](https://www.goodreads.com/book/show/42925734-handbook-of-radiotherapy-physics)
Authors: 
Year: 2007
DOI: 10.1201/9781420012026


