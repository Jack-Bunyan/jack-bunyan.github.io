---
tags:
  - Imaging
  - Radiotherapy
title: On Varian AEC
---
>It sucks

AEC is a technology that has been around within diagnostic radiology since the 50s, and is very well established as a tool utilised to [[IRMER|Optimise]] the dose from patient to patient. *It has not yet reached radiotherapy*.

Since [[Truebeam]] v3 there has been the capability of adding AEC to true-beam kv imaging.  While v4 has provided options for using it with [[Halcyon]] systems.  If clinically usable, it could make the scanning process on-set more efficient, reducing the number of [[Radiotherapy]] [[Incidents]]; potentially improve image quality on a patient-by-patient basis; and reduce administrative overhead.

ICT spent his masters project investigating this technology, intending to replace our 4 (small, medium, large, extra large) presets with just 1.  This was somewhat hampered by the way in which it controls the exposure.  This system is broadly mapped out below, and is most closely analogous to a [[mammography]] system:
![[Varian AEC flow-chart v4.png]]

The main inputs that the user has on this process are the kV, mAS and the "Target".  the kV alters the kV of the [[X-ray Tube]] in the same was as in a typical [[Planar X-ray]] system.  However, mAs is slightly different.  This determines both the minimum and maximum exposure that is used by the system.

The pre-pulse is set to half of the set mAs, this will always be delivered to the patient.  From this pre-pulse image the system calculates what the required mAs would have to be to achieve the "Target" set—*varian does not state what this equation is*— using the central 25% of the image. 

While this is, abstractly, quite similar to the AEC method for mammography, mammography systems will typically use a much smaller pre-pulse allowing a greater range of exposure ranges to be delivered, allowing a single preset to be used for all patients.

In some cases this pre-pulse will over-expose the patient, in which case an image is produced which used more dose than required, and may have lower contrast due to panel saturation.  In a second group the pre-pulse will be ideal and no second-pulse is used.  A third cohort will be within the range of 0.5-10mAs, these patients will recieve a customised exposure which should provide an optimsed image.

The fourth and final group are those who require greater than 10x mAs, these patients will receive the 10x mAs and will often still not produce a clinically useful imae of the patient for matching.  In order to produce images that are usable for these larger patients a higher exposure limit would need to be set, overdosing the patients that are larger.

During his project, ICT created a single preset that was optimised for our medium patients; however, due to the small range of mAs values that a single preset can deliver, this resulted in clinically "too good" images of smaller patients and clinically not great images of larger patients.  To avoid the fourth cohort problem, a multiple preset system would need to be used, this is without consideration of lateral fields.  Which are much attenuation and have more issues.  This loses some of the on-set advantages that good AEC could have, making it an unsatisfying solution, though the only one currently available.  Maybe hypersight will be better.

>"A two-state \[preset\] solution is an easy one to replicate however doesn't solve any of the actual problems."
>-ICT , Annex B7 RP$^2$ Physicist
 
# TL;DR
- Varian AEC sucks
- WHAT IS THE TARGET?!?
- Please let us increase the mAs range.
- Just use the mammo system.
- Ask Siemiens how they do it on planar, they own you.
- Please?