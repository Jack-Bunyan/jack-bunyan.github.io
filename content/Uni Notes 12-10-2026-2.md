---
Title: On Planning Imaging
---
This note covers
- Image Quality
- [[CT]] protocol configurations
- [[CT#4D|4D]]
- Something else I missed at the start of the lecture

# Image Quality
the 3 measured metrics are contrast, noise, and spatial resolution.  
Contrast is how easy it is to view features within the image (difference between signal and background).



| Voltage down         | Contrast up | [[On Particle Interactions#Photo-electric effect\|Photo-Electric Effect]] |
| -------------------- | ----------- | ------------------------------------------------------------------------- |
| Intravenous contrast | Contrast up | Intake of heavy atoms                                                     |
Noise is the random variation seen in a region that should be uniform, quantum noise is the main source of this, however any way to increase the signal per-pixel will improve this:

| Current up     | Noise Down    | $Noise\propto \frac{1}{\sqrt{Number of photons}}$ |
| -------------- | ------------- | ------------------------------------------------- |
| Bigger Pixel   | Noise down    | Resolution Worse                                  |
| Less thickness | Noise Down    | More signal to Measure                            |
| Voltage up     | Noise down    | Worse contrast                                    |
| Diff Algorithm | Noise Changes |                                                   |

Detectibility is determined by a combination of the noise of the image and the contrast of that image.

Spatial resolution is the ability to separate two items within an image.

| Smaller Pixel | Resolution Up | Noise up |
| ------------- | ------------- | -------- |
|               |               |          |

# Configuration

Typically the kV of a radiotherapy scanner is a fixed kV, this is because each of the tube voltages that are used requires a separate curve for converting between the HU measured by the scanner and the stopping power of that voxel.

mA; almost all CT scans will use some form of Automatic Exposure Control([[AEC]]), this is because a high current will improve the image quality, but will also deliver dose to the patient, to comply with the optimisation requirement of IR(ME)R we need to optimise the patient plan.

Pitch, is an inherent feature of any helical scan, defined by the distance per rotation divided by the width of the slice; high pitch over samples the image, increasing dose and image quality.  Pitch also alters how long a scan will take, potentially being important for a patient in breath hold.

Projections; see 1st year coursework.

Reconstruction parameters such as the FOV, slice thickness, and matrix size can be altered during the reconstruction of the image.  The slice thickness would improve your vertical resolution, but will annoy your clinicians, and increase your image noise.  While matrix size will directly impact the resolution but will make the noise worse.

Use of filters can improve the image quality with no dose implication, but could introduce image artefacts.

>Matrix size is a computational limitation, as opposed to a physical limitation, decreasing the field of view of the patient will increase resolution using the same data as was used for a larger field of view image.

[[Metal Artefact Reduction]]  Probably deserves its own page, ergo.

# Imaging Dose

> Imaging dose is not real

While the doses that we are delivering to plan treatments are justified (thanks practitioner), it is still important that we (the operator) *optimise*, this means that we wont to achieve the lowest practicable dose which produces an image of appropriate quality.  

Without planning (/setup) imaging, we would have less accurate target and organ contours, and without a planning CT the calculation of an accurate VMAT dose distribution would be very difficult.  In some locations this can be done using [[MRI|MRI]], cause its the best, but this is not current standard of care.

The most common metric that we use to evaluate the dose of CT protocols is the [[CT#CTDI and DLP|CTDI]].


| kV up     | Dose up   | $\propto kV^2$ |
| --------- | --------- | -------------- |
| mAs up    | Dose up   | linear         |
| scan less | dose down | linear(ish)    |

# Processing
Each modality of imaging is incredibly useful in its own different way, anatomical information required to plan a treatment required CT, whereas metabolic imaging i.e. used for staging, can be acquired from [[PET]], and useful soft tissue contrast can be achieved using MR.  However, PET gives low anatomical imaging (and is private), while MR is susceptible (pun intended) to distortion further from the isocentre.

MR can be especially useful for [[Prostate]] Cancer, as these tumours typically increase cellularity and reduce the free movement of water, diffusion imaging can enable staging of prostate cancers that only make up part of the prostate capsule.

Also [[BOLD]] and [[Tractography]] are cool fMRI scans for the brain.  While MRI is a far cooler technology, PET opens up a wide range of tracer options, while [[FDG]] is the clear front-runner other tracers that are attracted to regions of hypoxia, could indicate regions deserving of a boost.

# Look-up tables
These are what are used to take the values recorded within a matrix, and convert them to a visual representation, most obviously this can be for converting from a measured CT number to a grey value.  They are also used for the conversion between HU and stopping power/density.

# Registration
The process of matching two image such that a geometric co-ordinate in one of them matches with the same geometric location in the other.  This is especially important if using the combined information e.g. if contouring using a PET scan, then planning using a separate CT scan, or with an MRI and CT scan respectively.

When matching similar modalities the sum of the difference of the pixel values can be used, whereas different modalities, would have to use feature based optimisers e.g. edge detection.
Modern registration systems are capable of using deform-able registrations, to create a better match of the image; given we know that there are likely to be distortions within MRI images, this is useful to correct for these.