---
title: On Ion Recombination
tags:
  - Physics
  - Question
  - Niche
  - Radiotherapy
---
When measuring [[Dose]] in [[Radiotherapy]] we use [[Chambers]], these measure the charge that is created by a voltage across the chamber.  There is typically some amount of ion re-combination in any chamber, as a result of ionised electrons re-combining (badum tsch) with a positively charged nucleus.

Whilst some of these [[Ionisation]] are immediate, others are delayed, as the voltage across a chamber increases, the number of re-combinations decreases, as the charges are separated quicker.  However the other variable in a clinical radiotherapy beam that can impact this is the "instantaneous dose-rate".

Due to the structure of the [[Waveguide]] used to accelerate the [[On Particle Interactions#Electrons|Electrons]] within the [[Linear Accelerator.canvas|Linac]], the dose delivered in a typical therapy will arrive in pulses, this increases the  ion density of the volume within the chamber, which itself would increase the level of ion-recombination.

# Calculation
Calculating the percentage ion recombination is done using a different voltage for multiple measurement, with the reduced voltage intended to be at most one third of the output—although measuring at a higher one can produce correct results.
$$k_{ion}=1+\frac{(M_1/M_2)-1}{(V_1/V_2)-1}$$
This measurement will have to be done at any point that has a differing dose-rate.  For instance, for [[Quality Index]] measurements this must be repeated at both 20 and 10cm.  Further if performing measurements of the dose of a VMAT plan perfect ion-recombination correction is impossible due to dose-rate variations.




