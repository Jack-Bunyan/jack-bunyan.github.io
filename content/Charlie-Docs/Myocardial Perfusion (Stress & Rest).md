---
tags:
  - CB_Notion
  - Imaging
  - Nuclear_Medicine
title: Myocardial Perfusion (Stress/Rest)
wiki: http://wiki.heynm.org.uk/doku.php?id=diagnostic:imaging:d026-stress_mibi_myocardial_perfusion_imaging
wiki2: https://wiki.heynm.org.uk/doku.php?id=diagnostic:imaging:d037-stress_redistribution_thallium_imaging
---
>This scan primarily looks at ischemia and infarction of the [[Anatomy & Physiology-Heart|myocardium]] (left ventricle)

![[Tetrafosmin molecule.png]]
# Pharmaceutical, Uptake and Dose

---

| Pharmaceutical              | [[Tc99m]]-Sestamibi (MIBI) (a.k.a Cardiolite) or Tetrofosmin (a.k.a Myoview) | 201-Thallium                                 |
| --------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------- |
| ARSAC DRL                   | 800MBq (for [[SPECT]])                                                       | 80MBq                                        |
| Local DRL                   | Weight Based (7MBq/kg, 1GBq limit)                                           | 80(+40)MBq                                   |
| Effective Dose (mSv)        | 5.5(stress)/6.4(rest)                                                        | 11.2                                         |
| Paediatric Minimum Activity | 50MBq                                                                        | N/A                                          |
| Uptake Time                 | 30 minutes (stress)/45 minutes (rest)                                        | Immediate(Stress)/3-4 hrs for redistribution |
| Collimators                 | LEHRS                                                                        | ELEGP                                        |
MiBi can also be used but has a slightly higher effective dose and lower linearity than tetrafosmin which we now use locally.
- MIBI is widely used in MPS studies, other alternatives are available:
    -  99mTc-Tetrofosmin (Myoview)
    -  201-Thallium

|                      | 99mTc-Sestamibi                                      | 99mTc-Tetrofosmin                                | 201-Thallium                                |
| -------------------- | ---------------------------------------------------- | ------------------------------------------------ | ------------------------------------------- |
| Uptake Mechanism     | passive [[diffusion]], negative electrical potential | passive diffusion, negative electrical potential | [[active transport]]:  <br>Na/K ATPase pump |
| Myocyte Localisation | [[Cells#mitochondria\|mitochondria]]                 | mitochondria                                     | [[Cells#Cytosol\|Cytosol]]                  |
| Intracellular State  | bound                                                | bound                                            | free                                        |
| Preparation          | [[generator]] & kit                                  | generator & kit                                  | cyclotron                                   |
| Cardiac Uptake %     | 1.5%                                                 | 1.2%                                             | 3%                                          |
| Myocardial Clearance | minimal                                              | minimal                                          | 4 hour physiological half-life              |
| Body Clearance       | hepatic                                              | hepatic                                          | [[Anatomy & Physiology-Kidneys\|Renal]]     |

## Uptake Mechanism
### Tc-99m
![[Image of Mibi.png]]
*Molecular structure of 99mTc-Sestamibi. Comprised of 99mTc bound to 6x methoxyisobutylisonitrile (MIBI) ligands, hence sesta (6x ligands) MIBI.*

Uptake mechanisms for both tetrafosmin and MiBi are the same, utilising the high mitochondrial density of the [[Anatomy & Physiology-Heart|Myocardium]].

- MIBI is characterised as lipophilic and cationic.
- It has a predilection for tissues with high mitochondrial content and negative plasma membrane potentials.
- After intravenous injection, MIBI is passively diffused into the heart proportional to myocardial blood flow.
    - the positively charged lipophilic molecule is attracted to the negatively charged mitochondria where it becomes bound
        - biological half-life of the heart is ~3 hours after administration
- Myocardial uptake is prompt, and blood clearance is rapid due to renal and hepatic excretion.
    - [[Liver]] and [[gallbladder]] activity is seen within 1 hour of injection
        - biological half-life of the liver is ~30 minutes after administration
    - ~27% of injected dose is excreted in urine
    - ~33% of injected dose is excreted through faeces within 48 hours
    - [source for figures](https://go.drugbank.com/drugs/DB09161)

### Thallium-201

Thallium-201 is a synthetic radio-isotope with a half-life of 3.04 days, it decays via [[Decay Events#Electron Capture|Electron Capture]] into mercury.
![[thalliun decay graph.png]]Whilst the decay itself produces characteristic x-rays of 160keV(10%) and 135keV(2.6%), the emissions that are used for the imaging are the characteristic x-rays of the mercury it decays into when the electrons drop into the lower orbital shells left over from the electron absorption.
![[Emissons graph Ti-201.png]].
Title: [Optimum energy window setting on Hg-201 x-rays photopeak for effective Tl-201 imaging]()
Authors: Akihiro Kojima, Akihiro Takaki, Teruya Noguchi, Masanori Matsumoto, Noboru Katsuda, Seiji Tomiguchi, Yasuyuki Yamashita
Year: 2005
DOI: 10.1007/BF02985046

Thallium is produced via the irradiation of thallium-203 with helium-3 ions, this produces lead-201 which itself will decay into thallium 201.  This has to be done in a [[cyclotron]] which restricts its production compared to generation of cheaper radio-isotopes such as generators.  The thallium has a peak myocardial uptake around 5 minutes after injection in stress patients and 30 minutes for non stress.  

Unlike the mitochondrial binding mechanism which is used by the technetium based tracers, thallium uses the active transport mechanisms of the cell surface.  The thallium isotope mimics the chemical properties of the potassium and are therefore pump the thallium ions from the extracellular space into the cardiac muscle tissue.
![[cells heart active transport tl.png]]
This uptake of the thallium ion is inhibited by [ouabain](https://en.wikipedia.org/wiki/Ouabain) and [[hypoxia]], this is alongside its relatively strong linearity with coronary blood flow.  This means that for there to be uptake the cardiac muscle must be viable, having both alive cells and active blood flow.

The unique difference between Tl-201 and Tc-99m based agents is the process of redistribution.  Technetium agents are strongly fixed within the mitochondria, and remain there long term, whereas technetium rest scans are performed on a separate day, this rest scan can be done done hours after the initial injection.  The thallium passively leaves the myocytes re-entering the extracellular environment, and will then be actively transported into other tissue.


Title: [Chapter 26: Heart | Radiopharmaceuticals in Nuclear Pharmacy and Nuclear Medicine, 4th Edition | PharmacyLibrary](https://pharmacylibrary.com/doi/abs/10.21019/9781582122830.ch26)
Authors: 
Year: 
DOI: 

Title: [The extraction of thallium-201 by the myocardium]()
Authors: H. F. Weich, H. W. Strauss, B. Pitt
Year: 1977
DOI: 10.1161/01.cir.56.2.188

### Thallium vs Technetium

When considering the use of a radio-pharmaceutical there are two components to consider, these being the radioactive tracer that is attached to the molecule, and the pharmaceutical molecule itself.  When considering useful radio-pharmaceuticals technetium is perfect; with a half-life of 6 hours being short enough that it doesn't result in high effective doses, yet long enough that it is easy to deal with practically; it is easy to generate within a department using a generator; and it has an energy that is high enough that it isn't heavily attenuated, but also low easy to attenuate with a [[Collimator]].  

Thallium on the other hand has a lower energy and longer half-life, this means that it is more impacted by attenuation, and remaining in the body for longer.

HUTH uses Tc-99m tracers in larger patients >100kg for the attenuation resistance of the tracer.  Whilst for smaller patients Thallium is preferable, this is strictly for the pharmokinetic advantages it provides.
![[heart tracer linearity.png]]
The difference in tracer uptake as coronary flow increases is known as its "linearity", both sestamibi and tetrofosmin have poor linearity, with their signal change reducing significantly at relatively low blood flows.  This makes it much poorer than Thallium for picking up on minor defects.

Despite having superior linearity than the other technetium tracers, teboroxime has significantly higher clearance rate from the cardiac muscle, this requires a much faster imaging procedure which was previously impossible with the lower spectral sensitivity of [[Gamma Cameras, Classical and Solid State#Scintillation Crystal|sodium iodide]] gamma cameras, however using [[Gamma Cameras, Classical and Solid State#Solid State|CzT]] cameras that are now available the re-consideration of this tracer may be possible.

Title: [Radiotracers to Address Unmet Clinical Needs in Cardiovascular Imaging, Part 1: Technical Considerations and Perfusion and Neuronal Imaging](https://jnm.snmjournals.org/content/63/5/649)
Authors: John C. Stendahl, Jennifer M. Kwan, Darko Pucar, Mehran M. Sadeghi
Year: 2022
DOI: 10.2967/jnumed.121.263506

Title: [Recent Advances in Nuclear Cardiology](https://pmc.ncbi.nlm.nih.gov/articles/PMC4977260/)
Authors: Won Woo Lee
Year: 2016
DOI: 10.1007/s13139-016-0433-x

## Patient Preparation

---
### Preparation from Wiki

- Avoid caffeine for 12 hours prior to the appointment (A list of foods and medications that contain caffeine is shown in [Appendix 1](http://wiki.heynm.org.uk/doku.php?id=diagnostic:imaging:d026-stress_mibi_myocardial_perfusion_imaging#appendix1-foodsandmedicationswhichcontaincaffeine))
    - caffeine blocks the same receptors (a2a) as adenosine and regadenoson, meaning a pharmacological stress could not be performed if the patient cannot exercise
- Fast for four hours prior to the appointment time [1](http://wiki.heynm.org.uk/doku.php?id=diagnostic:imaging:d026-stress_mibi_myocardial_perfusion_imaging#refnotes:1:note1). Diabetics may eat as required. All patients should drink as normal. Patients should eat a light fatty meal or drink milk after injection.
    - fasting fills the gallbladder with bile, ready to be used for digestion of fats. eating a fatty meal promotes emptying of the gallbladder and liver.
    - MIBI is cleared through the hepatobiliary system, so liver/bowel overlapping the heart is common, so these steps should hopefully clear any activity away.
- Do not take Beta Blockers ((e.g. Atenolol, Bisoprolol, Propranolol, Carvedilol, Timolol, Nebivolol) for 48 hours before the appointment. These can be taken after the stress part of the test is completed.
    - beta blockers reduce blood pressure by making the heart beat slower and less forcefully. a stress test wants to see the heart working under pressure with high blood flow.
    - may not be able to reach 85% of max heart rate if beta blocker has been taken.
- Do not take dipyridamole (sometimes known as persantin or asasantin) or any other medications containing aminophylline or theophylline for 24 hours prior to the appointment
    - dipyridamole inhibits blood clots, and may be given during a pharmacological stress
- Take other medication as normal (bring a list of current medication to the appointment)
### Exercise Stress Testing (EST)

- This is known as a “safe” test, with serious adverse effects occurring with 1/10,000 tests.
> The aim of the stress test is to reach 85% of the patient's maximum heart rate (MHR)
- The stress test can be performed on a treadmill or a bike, and the patient’s must be fit enough to exercise intensely.
![[Bruce protocol.png|570]]
- In our department, we follow the BRUCE protocol on a treadmill, standard protocol shown above.
    - Exercise is performed in 3-minute stages, at increasing speed and gradient, with a maximum of 7 stages. The following flowchart explains what is happening to the heart:
![[Bruce protocol 2.png]]
*Flowchart of body's response to EST.  Note: in CAD, stenosis limits flow of blood and oxygen to myocardium - so limited coronary flow means limited oxygen supply for the myocardium limiting the intensity and duration of exercise to be performed.*

- At least 4-6 minutes of exercise is desired, and activity is injected once the patient reaches 85% of MHR.
- Ideally, the patient would continue to exercise for 1 minute post-injection.
    - this is to ensure the radiopharmaceutical has had time to properly localise within the myocardium under peak-stress conditions.
- Once the patient has finished on the treadmill, the patient is observed for 3-5 minutes to check that readings return to normal as well as checking for ST-wave changes that can occur during this recovery period.
![[quit cardiac stress.png]]
### Pharmacological Stress Testing

- This is performed instead of an EST in the following cases:
    - cannot perform or tolerate adequate exercise
    - patient has taken beta blocker or calcium channel blocker
    - patient has pacemaker rhythm
    - presence of left bundle-branch block (LBBB) which may produce septal perfusion defects
- The two different types of pharmacological stressing agents are either described as:
    1. coronary vasodilator - widens the coronary artery, allowing increased blood flow to myocardium.
    2. ionotropic - causes the heart to contract with more force (positive), or can weaken the contractions (negative) which in turn widens the coronary artery.


|                     | Adenosine                       | Dobutamine                          | Regadenoson                     | Dipyridamole                    |
| ------------------- | ------------------------------- | ----------------------------------- | ------------------------------- | ------------------------------- |
| Type of Agonist     | a2a                             | beta-1                              | a2a                             | a2a                             |
| Category            | coronary vasodilator            | positive ionotropic effect          | coronary vasodilator            |                                 |
| Administration      | intravenous infusion            | intravenous infusion                | intravenous bolus               | intravenous infusion            |
| Effect Duration     | ~6s once infusion stopped       | ~11 minutes                         | ~2.3 minutes                    | ~12 minutes                     |
| Patient Preparation | no caffeine for 12 hours before | no beta blocker for 24 hours before | no caffeine for 12 hours before | no caffeine for 12 hours before |

- In healthy hearts, these agents produce increased myocardial perfusion when compared to the EST, meaning a larger proportion of the dose is concentrated in the myocardium.
- In patients with vessel stenosis, these show diminished dilation as they are already maximally dilated due to the body’s natural response to the ischemia or regional myocardial hypo perfusion.

### Scan Preparation

- Ensure patient has had hot drink/biscuits before imaging to help pass uptake through the gut and stop overlap.
    - This is not required for the treadmill patients as there is little to no gut uptake.
- Once patient is on the bed, apply three ECG stickers as per photo.
- Ensure patient’s heart is below 160cm on the ruler as this is CT limit.
- Strap patient in, with left arm above head and make sure detectors aren’t touching.
- The heart should sit towards the top of the FOV with the detector as close to the left armpit as possible.
    - Raise the bed as required and get detectors as close as possible.
- Spin the detectors to ensure they aren’t touching on the way round.

![[ECG locations.png]]
### Waiting Times
|Stress (Treadmill)|Stress (Pharmacological)|Rest|
|---|---|---|
|0 minutes|1 hour|1 hour|
## Normal Results

![[Heart lkayour myocard.png]]
*Example of standard views for an MPS with relative anatomical position of heart.  Left to right: short axis (ant/transaxial view), vertical long axis (VLA), and horizontal long axis (HLA).*
![[Pretty pics myocardium.png]]*A normal MPS scan, showing normal tracer distribution throughout the myocardium with no defects. Report "Normal perfusion at high exercise workload - Prognosis Good”.  The right ventricle is faintly visible in the short axis and HLA images*

In order to capture an image with sufficient resolution, gating is done via the ECG trace, images can then be reconstructed using the ECG trace to produce video images of how the ventricle evolves over time.
![[TypicalHeart.gif|697]]

| |Defects on Stress & Rest|Defect only on Stress|
|---|---|---|
|Condition|Infarct|Ischemia|
|Meaning|Suffered a heart attack which has killed the muscle meaning no blood flow.  <br>_**This is irreversible.**_|Muscle is viable under rest, no blood flow under stress conditions. Stent can be put in to allow blood flow. _**This is reversible.**_|
# Referral Criteria Explanation

---

![[Myocardial referral criteria.png]]
There are a lot of possible criterion for referral for this test, however the main two we currently look at are ischemia and infarct.  This imaging is also done to evaluate the potential impact of cardiotoxix medicines, for example in patients that are receiving organ donations.  It is the current [NICE reccomended](https://www.nice.org.uk/guidance/cg95/chapter/Recommendations#people-presenting-with-stable-chest-pain) non-invasive method for the investigation of myocardial ischaemia, though stress echocardiograpy and MRI are both alternatives.

# Look up hibernating myocardium and stunned

## Detecting Coronary Artery Disease (CAD)…

## … by Localising Myocardial Ischemia (Reversible Defects)

### What is it?

### How do we scan for it?

## … by Localising Myocardial Infarction (Non-reversible Defects)

### What is it?

### How do we scan for it?
## Extras

Get patient to eat something fatty which causes gallbladder to excrete bile which clears bowel uptake and get them to go for a walk.

Time window most important, after too long, there is high bowel uptake.

Thallium is the best heart agent for no bowel uptake.

If stressing with dobutamine, dose is upped incrementally (every 3 minutes) until 85% of maximum heart rate is achieved, the MIBI can then be injected.

If stressing with adenosine, inject MIBI after 3 minutes maximum blood flow through veins has been achieved.

# 

Title: [Nuclear Cardiology](https://doi.org/10.1093/med/9780198759942.001.0001)
Authors: Andrew Kelion, Parthiban Arumugam, Nikant Sabharwal
Year: 2017
DOI: 10.1093/med/9780198759942.001.0001

Title: [A New Approach to the Presentation of Myocardial SPECT Images—Radial Slices—Data Reduction without Loss of Information](https://www.scirp.org/journal/paperinformation?paperid=38588)
Authors: Niloufar Darvish, Fatma Nadide Öçba, Hamed Hamid Muhammed, Dianna Bone
Year: 2013
DOI: 10.4236/eng.2013.510B023

Title: [Pharmacologic Stress Testing Technique: Approach Considerations, Adenosine Technique, Dipyridamole (Persantine) Technique](https://emedicine.medscape.com/article/1827166-technique)
Authors: 
Year: 
DOI: 

Title: [EANM procedural guidelines for radionuclide myocardial perfusion imaging with SPECT and SPECT/CT: 2015 revision]()
Authors: Hein J. Verberne, Wanda Acampa, Constantinos Anagnostopoulos, Jim Ballinger, Frank Bengel, Pieter De Bondt, Ronny R. Buechel, Alberto Cuocolo, Berthe L. F. Eck-Smit, Albert Flotats, Marcus Hacker, Cecilia Hindorf, Philip A. Kaufmann, Oliver Lindner, Michael Ljungberg, Markus Lonsdale, Alain Manrique, David Minarik, Arthur J. H. A. Scholte, Riemer H. J. A. Slart, Elin Trägårdh, Tim C. Wit, Birger Hesse, undefined undefined
Year: 2015
DOI: 10.1007/s00259-015-3139-x

[Technologist's guide]([https://file.notion.com/f/f/045ecbdf-5b8b-4421-94e4-b1947b03aee0/386f9783-9934-4ada-a44b-864413c90736/EANM_2014_Myocardial_Tech_Guide.pdf?table=block&id=81f7aaab-ae6e-4e2c-8a21-60880bbe50ab&spaceId=045ecbdf-5b8b-4421-94e4-b1947b03aee0&expirationTimestamp=1785254400000&signature=ry44tU9OeCI0NcJJeVckhWm0TN55_NPcNafr0Wq1b_s&downloadName=EANM_2014_Myocardial_Tech_Guide.pdf](https://eanm.org/wp-content/uploads/2024/06/EANM_2014_Myocardial_Tech_Guide.pdf))
