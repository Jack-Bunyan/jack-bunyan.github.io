---
title: On Immobilisation And Respiration
tags:
  - Radiotherapy
---
During radiotherapy a dose is targeted at a specific tumour, while trying to avoid delivering dose to organs.  In the majority of treatments (everything but [[MR-Linac]]s), imaging cannot be done during treatment, hence the popularity of Surface Guided Radiotherapy ([[SGRT]]).  This makes it important to keep the patient in one place during treatment.

- Maxmise tumour control probability
- Minimise normal tissue complication probability

This is made difficult as patients are not perspex (sad), especially in sites such as [[Lungs]], where there is a large amount of motion, or [[Prostate]], where the volume of the bladder is highly unreliable.

The use of PTVs is due to this uncertainty, as we cannot be sure that the patient will always be perfectly setup, we know they will move during treatment, and there will be small mechanical errors.  Typically these errors are either
- Random, or
- Systematic
While the motion  of organs can be broken down into inter-fraction movement
- bladder size
- tumour shrinkage
- skin reaction ([[Breast Cancer]])
and intra-fraction movement during the treatment:
- digestion
- breathing
- wiggling

---
The 4 methods for minimisation of movement are:
- Imaging ([[CT#CBCT|CBCT]]), correcting setup, but not for movement
- Immobilisation, keep them still + rotation
- Patient Preparation, (DRINK YOUR WATER)
- (Respiratroty) Motion Management ((R)MM), wiggle correction/detection

# Immobilisation
Consideration of patient comfort, although we use flat beds for predictability of patient position, a comfortable patient is a static patient.  This position should be the same every day, so rigid non-continuous position settings are ideal.

Being easy to setup and clean for sterility, while low density to reduce impact on plan and enable skin sparing (also impact on image quality).

Anaesthetics are great for making people (children) comply, however they are an additional cost, both monetarily and risk budget wise.  Also worth considering individual patients, a claustrophobic patient ([[Weekly 12-10-26]]) may be less compliant on a tomotherapy unit, than a C-arm system.

Use of masks for [[Head and Neck]] cancers as well as top of Lung, while these are great for patient position intra-fraction, many patients will either lose weight (tumour shrinkage, poor diet), or swell (skin inflammation, steroid use).

> Vac bags exist but are a pain in the arse and not fantastic

Patients with breast cancer uniquely use an inclined setup for their scan and treatment, this aids in the sparing of the lung, but increases the collision risks with components of the linac.


# Patient Preparation
This is most often used for pelvic patients where the rectum and the bladder are close to the PTV, this is most commonly done in either empty, or full bladder.  Full bladder is a more classical approach to patient preparation, pushing the rectum away from the prostate (reducing dose).  However this can be more difficult to replicate, and especially in longer fractionations will become more difficult to hold during the end of treatments.  Empty filling regimes are of interest (e.g. EMPTY-RT trial), as they could improve patient throughput and comfort, but these do seem to increase organ dose.

Gas within the rectum can have a major impact on the patient's dosimetry, and if there is gas present in the rectum, the patient will often be encouraged to come back in a bit.  Movement of the digestive tract during treatment will also move the prostate as I saw during some work on prostate [[SABR -UN 16-10-2026]].

For many sites within the abdomen, a fasting preparation technique will be used as movement of the stomach will be significant.

# Respiration
>Patients suck (and blow) ((its called breathing))

For tumour positions in the lung it is highly likely that the tumour will move alongside the breathing cycle.  A 3D scan may capture the tumour at an extreme of the breathing cycle, which could result in a plan that irradiates a large amount of healthy tissue.  To avoid this, a [[CT#4D|4D]] image is acquired, the projection data is categorised using the breathing trace of the patient creating multiple images that represent each of the phases of the breathing cycle. 
This image data can produce either an Average Intensity (AI) or Maximum Intensity (MI) Projection (P),  I am more familiar with a MIP image in a diagnostic view such as is used in [[PET]], where it provides a useful 3D image.

The MIP image is typically used to create the ITV of the treatment plan, whereas the AIP is used for dose calculations.  Motion management strategies greatly with both passive techniques
- Big margins
- Motion encompassing target
- Strap (Patient comfort?)
and active methods
- Gating (lots of motion)
- Breath-hold (left breast)

# Surface Guided
This probable deserves a seperate page ergo [[SGRT]]

