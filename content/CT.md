---
Title: On Computed Tomography
tags:
  - Imaging
  - Physics
---
Computed Tomography (CT) scans will from here one be called CAT scans cause I find it funnier.

CAT scans are a technology which produces 3D axial images of a patient, when compared to [[MRI]] they are quicker, cheaper, have fewer contra-indications, and have better bone imaging capabilities; MRI on the other hand, has higher resolution, better soft-tissue contrast, and functional-imaging capabilities.

CAT images are taken by taking many planar X-ray projections from around the subject, which are then reconstructed into axial images.

# Projection Imaging

X-ray generation in CAT systems is done using an [[X-ray Tube]], this imaging is then captured using a panel.  While historically this would have been a film, modern systems operate using a scintillation crystal-based design.
![[Scintillation crystal diagram PCCT.png]]
While the scintillation crystal is similar to those that are used within [[Gamma Cameras, Classical and Solid State#Scintillation Camera|Gamma Cameras]] the chemical structure and design considerations are different.  Chemical structures used in these crystals vary greatly, including poly crystalline ceramics ( Gd$_2$O$_2$S:Pr,Ce (GOS), (Y,Gd)$_2$O$_3$:Eu), CdWO$_4$ ), and more recently garnet-type crystals such as (Lu, Gd, Y, Tb)$_3$(Ga, Al)$_5$O$_{12}$.

In gamma camera systems anger logic is used to compute the location of events, this is neccesary due to the sensitivty requirements of the system, detecting such a small number of emissions.  In comparison, to create spatial resolution in CAT systems, septa are used to separate adjacent photo-diodes, which convert the visible photons into voltage.

These projections are captured at a range of angles, modern CAT systems will also capture "helically", this means that the camera rotates around the patient while moving vertically.  
![[helical scan for radiology.png]]
The efficiency of the camera can be defined by the "pitch"
> Pitch=(Scan Width)/(Travel in One Rotation)

A pitch of 1 would mean that every slice of the image is captured from 360$^\circ$.  Higher pitches can be used to increase the dose efficiency of the scan, however decrease the sampling.  Typically pitches will be set less than 1 (e.g. 0.8 for most RT scans), this decreases the chance of losing small details from it moving between rotations.  

Title: [Photon Counting CT: Technical Principles, Clinical Applications, and Future Prospects](https://www.sciencedirect.com/science/article/pii/S1076633223002842)
Authors: Yingyi Wu, Zheng Ye, Jie Chen, Liping Deng, Bin Song
Year: 2023
DOI: 10.1016/j.acra.2023.05.029

Title: [State of the Art of CT Detectors and Sources: A Literature Review](https://doi.org/10.1007/s40134-012-0006-4)
Authors: Efrat Shefer, Ami Altman, Rolf Behling, Raffy Goshen, Lev Gregorian, Yalon Roterman, Igor Uman, Naor Wainer, Yoad Yagil, Oren Zarchin
Year: 2013
DOI: 10.1007/s40134-012-0006-4

Title: [Acquiring an image part 1 - Radiology Cafe](https://www.radiologycafe.com/frcr-physics-notes/ct-imaging/acquiring-an-image-part-1/)
Authors: 
Year: 2017
DOI: 

# Reconstruction
Reconstruction is a key aspect of the creation of 3D CAT images, the majority of systems today will use advanced iterative reconstruction algorithms with a sprinkling of machine learning.
Historically systems used filtered back projection to reconstruct images.  Back-projection "smears" each of the projections over the reconstruction space, this will obscure higher frequency details.  These details are re-captured using a filter.  Simple ramp filters will increase the resolution of the image but by increasing the higher frequency details.  Since noise is made up of high frequency details an unlimited ramp filter will dramatically increase the noise of the image.  For this reason commonly used filters instead drop off, suppressing very high frequency features.
![[CT recon filters.png]]
Below shows image that have been reconstructed using separate filters.  Compared to the unfiltered image the importance of using these filters to create usable images is clear.
![[filtbackrecons curtains.png]]
# Contrast
Iodinated contrast is frequently used within CAT imaging, this is used because iodine can absorb a large amount of x-rays through the [[On Particle Interactions#Photo-electric effect|Photo-electric Effect]].  This makes it useful in CAT imaging to make details stand out.  For example, the use of iodinated contrast in enables the use of [CAT coronary angiography](https://www.nice.org.uk/guidance/cg95/ifp/chapter/investigations-for-stable-angina) or [CAT pulmonary angiography](https://www.nice.org.uk/guidance/ng158/chapter/recommendations) imaging the [[Iodine]] as it passes through the vessels.  

# QA
## CTDI and DLP
The key [[dose]] metrics for CAT scans are CTDI and Dose Length Product (DLP).
![[CTDI graph diagram.png]]
The measurement of charge measured by the farmer chamber gives the value.
> $Q\propto\int_0^LD(x)dx$ 

CTDI is effectively a measurement of the dose per unit length of the scan.  It has the equation:
 > $CTDI = \frac{1}{NT}\int^L_0D(x)dx$
 
While the DLP of a scan is calculated from the product of CTDI and length.
An important aspect to consider during dose optimisation is the penumbra of the field the beam, though it does not provide useful imaging information, the beam is not perfectly contained within the length that is being scanned, this means that as the beam width decreases the CTDI of the scan will increase, as the penumbra will not decrease linearly with the dose from the usable portion of the beam($\frac{x+P}{x}$).
# Other Technologies
## 4D
Gating of imaging is an important aspect of imaging, by separating frames of an image by their location within a periodic process e.g. heart beats of breaths.  This can be done through very low pitches to acquire a large amount of data from each of the axial slices, or through an axial scan (0 pitch).

In radiotherapy we typically use [i4DCT](https://pubmed.ncbi.nlm.nih.gov/32115724/) algorithms for our 4D acquisitions, this is an axial acquisition procedure which predicts the breathing trace of the patient, acquiring for sufficient time to create a 4D acquisition image, optimising the dose to the patient while still capturing sufficient detail.

This gating can be done using various different technologies, in [[MRI|MRI]] I experienced using a bellows which is a physical bar which is moved. In Radiotherapy CT we frequently use a marker block that is placed on the patient and is tracked during the process.  Some systems can use internal structures such as the diaphragm ([[Lung MRI]]).  This can be binned wither using the phase of the breathing cycle or the amplitude, there are arguments for both of these but typically phase gating is seen as the better choice due to resistance to unstable breathing traces.
## CBCT

## Photon-Counting

