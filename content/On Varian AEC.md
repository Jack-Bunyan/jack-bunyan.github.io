---
tags:
  - Imaging
  - Radiotherapy
---
>It sucks

AEC is a technology that has been around within diagnostic radiology since the 50s, and is very well established as a tool utilised to [[IRMER|Optimise]] the dose from patient to patient. *It has not yet reached radiotherapy*.

Since [[Truebeam]] v3 there has been the capability of adding AEC to true-beam kv imaging.  While v4 has provided options for using it with [[Halcyon]] systems.  If clinically usable, it could make the scanning process on-set more efficient, reducing the number of radiotherapy incidents; potentially improve image quality on a patient-by-patient basis; and reduce administrative overhead.

ICT spent his masters project investigating this technology, intending to replace our 4 (small, medium, large, extra large) presets with just 1.  This was somewhat hampered by the way in which it controls the exposure.  This system is broadly mapped out below, and is most closely analogous to a mammography system:
![[flowchart of varian AEC v2.png]]

The main inputs that the user has on this process are the kV, mAS and the "Target".  the kV alters the kV of the [[X-ray Tube]] in the same was as in a typical [[Planar X-ray]] system.  However, mAs is slightly different.  This determines both the minimum and maximum exposure that is used by the system.

The pre-pulse is set to half of the set mAs, this will always be delivered to the patient.  From this pre-pulse image the system calculates what the required mAs would have to be to achieve the "Target" set—*varian does not state what this equation is*— using the central 25% of the image.  

>"A two-state \[preset\] solution is an easy one to replicate however doesn't solve any of the actual problems, just like Korea."
>-ICT , Annex B7 RP$^2$ Physicist
 
