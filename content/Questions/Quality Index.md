---
title: Energy Definition
tags:
  - Radiotherapy
  - Physics
  - Question
---
Quality Indexes are used to describe the spectrum of energy used in a clinical beam, this is because while an energy such as "18MeV" could describe the peak energy of a beam (or average or median or whatever).  However, different filters, [[Bending Magnets|Bending Systems]], or scattering foils could change the spectrum of the photons that come out.

For this reason it is typical that different energies are instead described using some kind of quality index, which depends on the energy(ironic) of the beam.  

# TPR 20, 10
The Tissue Phantom Ratio 20,10 is the standard quality index that is used for MeV [[On Particle Interactions#Photons|Photons]], it is measured at a SDD of 100cm and depths of 20cm and 10cm.  With a field size of 10x10cm.
$$TPR_{20/10}=\frac{M_{20}\times k_{ion,20}}{M_{10}\times k_{ion, 10}}$$
For example, at Sheffield I took part in an audit which measured the TPR_20,10 of 3 energies.

| 6x   | 0.6674                 |
| ---- | ---------------------- |
| 6FFF | 0.6302, similar to 4MV |
| 10x  | 0.7376                 |
Title: [Determination of beam quality index, TPR20/10, on the NPL Elekta linac.](https://eprintspublications.npl.co.uk/4748/)
Authors: J. A. D. Pearce, G. A. Bass
Year: 2010
DOI: 

# R 50, D
For [[On Particle Interactions#Electrons|Electrons]] the quality index is the depth where the dose is half the maximum dose, this is important to measure as the reference conditions for outputs uses Z_ref which is derived from the quality index.
$$Z_{ref}=0.6R_{50,D}-0.1\text{cm}$$
In experimental conditions the depth dose and depth ionisation is identical, although they can be measured by:
$$R_{50,D}=1.029R_{50,I}-0.063$$
During my audit, the values of the dose of half depth were measured.

| 6e  | 2.34cm |
| --- | ------ |
| 12e | 4.98cm |
| 16e | 6.60cm |
For higher energies this becomes harder and harder to measure as the peak of the curve becomes smoother making an exact measurement of the maximum dose more difficult.

These are relatively similar to the measurements for the energies of elekta systems

| 6e     | 8e     | 10e    | 12e    | 15e    | 18e    |
| ------ | ------ | ------ | ------ | ------ | ------ |
| 2.53cm | 3.36cm | 4.10cm | 5.01cm | 5.93cm | 7.08cm |
Title: [Electron beam energy QA - A note on measurement tolerances](https://www.researchgate.net/publication/301288231_Electron_beam_energy_QA_-_A_note_on_measurement_tolerances)
Authors: Juergen Meyer, Matthew Nyflot, Wade Smith, Landon Wottoon, Lori Young, Fei Yang, Minsun Kim, Kristi Hendrickson, Eric Ford, A. Kalet, Naifu Cao, Claire Dempsey, George Sandison
Year: 2016
DOI: 10.1120/jacmp.v17i2.6049

# HVL
Used for low energy photons, this is the amount of material required to attenuate the beam to be half of the dose, similar to $R_{50, D}$.  This is most often measured using either copper, or aluminium, with copper having thinner HVLs than aluminium due to there being more free electrons.
I have no useful example : )