---
Title: On Chambers and Corrections
tags:
  - Physics
  - Radiotherapy
---
There are several different designs for chambers to detect radiation, with the most popular being cylindrical and parallel plate.  In radiotherapy the most common chamber designs are farmer chambers (used for routine photon outputs) and Roos chambers (used electron outputs).

# Chamber Principles

>Radiation+Particle=Ionisation

Chambers don't directly measure the [[Dose]] that is at a given point, instead what they measure is the quantity of ionisations that occur within the chamber.  By applying a voltage across the chambers, the amount of charge can be measured.  The response of a chamber varies greatly with the voltage that was applied across it.
![[Pasted image 20261001123145.png]]
Title: [Operating regions of gaseous ionisation detectors | Radiology Case | Radiopaedia.org](https://radiopaedia.org/cases/operating-regions-of-gaseous-ionisation-detectors)
Authors: Siang Ching Raymond Chieng
Year: 
DOI: 10.53347/rID-164267

Chambers used in dosimetry all operate in the "ionisation region", below this region, a large proportion of the ionised particles re-combine reducing the signal.  Above this region, the energy of the ionised electrons is large enough to cascade, making it more difficult to predict the signal from the charge liberated.  The Geiger-Muller region is used in radiation protection, where incredibly high sensitivity is required, measuring the counts rather than dose in a region.

# Code of Practice Corrections
The equation for dose measurements calculated for photons:
$$D_{w,Q}=[M_{raw}k_{elec}k_{TP}k_{h}k_{ion}k_{pol}k_{vol}]N_{D,w,Q_0}k_{Q,Q_0}$$
![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAATCAMAAADCvy/4AAAAAXNSR0IArs4c6QAAAJxQTFRFAAAAAAAAAAA6AABmADpmADqQAGaQAGa2OgAAOgA6OgBmOjqQOmZmOma2OpC2OpDbZgAAZgA6ZgBmZjoAZjqQZmZmZpCQZpDbZrbbZrb/kDoAkDo6kGY6kGaQkJBmkJDbkNv/tmYAtmY6tmZmtpA6trbbttvbttv/tv//25A625Bm27Zm27a229uQ2////7Zm/9uQ/9u2//+2///b7yZbjQAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAxklEQVQoU9WQyRLCIBBEG7fEuOAWDXED1+BCEP7/3xzKW6qwvNpVw2WamTcN/JsUa1fEbNPONYbu8qkEfMlE9Di7DBY97NMbkS5KAbc4dU3UcpCK4yBUEnW4hVHcjjyNismOoHtrab+hcNSMKo4SFtisgiLLa57cUg6/Ya2uUZSWEm6SQH+C04wmPZ79oua+HBudwE2lTQVujSioQzEPDH2HX8vjjrt94wbqIFDds8sZKl/VvW0jLDcLO928VZSdCjQyQP6iNxRlEtNQJ9b6AAAAAElFTkSuQmCC) are read from the electrometer of the charge measured from the chamber.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAATCAMAAACwcE1OAAAAAXNSR0IArs4c6QAAAIRQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OgBmOjqQOmaQOma2OpC2OpDbZgAAZgA6ZjqQZma2ZrbbZrb/kDoAkDo6kGY6kGaQkNv/tmYAtmY6trb/ttu2ttv/tv/btv//25A625Bm27Zm29uQ29vb2////7Zm/9uQ/9u2//+2///bGcVYRQAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAApUlEQVQoU82Q0Q6CMAxFb1FQVECkoIAKEx1j+///U9BEMGHP7qE5WbubnQJ/fHTk5Lbvta60tYVndSsYDc2O6H0OEc4GKL8qk/l4QbSov+3ix6MI1XpkpuOJh47YpGHDgCnJYbS7D5kjEUP5NQT1d1nyKBmC35SkgbyNUtWKnECaLMdA9810Wa2H7iR1fDkP1LiyO4yETErLK3TkyoFeZWtddv/0CSD4DP1r/DYVAAAAAElFTkSuQmCC) is the calibration coefficient of the electrometer.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAATCAMAAABMZWaEAAAAAXNSR0IArs4c6QAAAGBQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgA6OgBmOjqQOma2OpDbZgAAZgA6ZrbbZrb/kDoAkDo6kNv/tmYAtmY6tv/btv//25A627Zm2////7Zm/9uQ/9u2/9vb//+2///bAnE7ZwAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAiklEQVQoU8WPyxaCMAxEExBEiwZbJZRq+/9/adIVQvZmk3Nm8rgD8K/KY+PN32sXTZ17GzUQLHj08s0Du+NKGl7Pu3GJEdtZ9RW1nLaTCMGlcwVlSsPMVB6+BAd5pDK5hepGD58opv6rDa/1gZCJ2cW3oGxKycREbH450kWCy90dXJlQYgQj4mbwCyM5Bt/eQ7GUAAAAAElFTkSuQmCC) is the temperature-pressure correction factor (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGoAAAAeCAMAAADzTHtyAAAAAXNSR0IArs4c6QAAAIpQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OgBmOjqQOmaQOma2OpDbZgAAZgA6ZgBmZjqQZma2ZpDbZrbbZrb/kDoAkDo6kDpmkGZmkGaQkLb/kNv/tmYAtmY6tmZmttv/tv/btv//25A625Bm27Zm27aQ2////7Zm/9uQ/9u2/9vb//+2///b5k+jdAAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAB6ElEQVRIS81W7VLCQAy8QwRRiooU/KCIlFpae+//em6SKzBMq5cKM+ZHW9L0NtnLZTHmn1r5sg7OLHsKDm0IrB5zxefFWBF8GprG8GRDe5dXE2tt5BYWz7UP9zTCZYdXeGnMaik/+hs1pnvGN8VtXk7iEuy8L1FldY/1xFdDpXEx2lBWBOwWS5dQAjqrHiQ9hjTFlJ4/p8Kp+LgqlDIwX3DjZoBaezVgNdSWCmB6qknPbz58xZCI68GdcABD7a7zkgpXmmRutm909ZsuxHmfz59J9TUmAJ+Zle0r4bgtkP8OdyoKe+TmcTqofR4KboZCSMWZwIEgJiEUkZqdaQJbtJxbWTs26cD7/F65ObWf1J1YggCTRCbTGcpk+boODTVHRxh5bRmda7usYa94m9EvGdd5caN+8efhBAukiwVv5i/JFqOP1SykII/b+YatsvaKifSzq+PUCkk2iYob7nY/uw5T69wE4pC5eZTxmefZ1XFqBVTFK+Mg+l78cWpplFGg2/RRZpdMrSbTKaOs0KKPPGxkajWaUhlljUZ9lNklU6vJtMooa3TSR60yClQnfdQq4wFKrY8qZdyLIRHY3mk/tkWYMtZieKSPbau2NnugMu7F8KCPKigTroy1GP7tL25YdrUYhkWfO+obspc9o7GoDxUAAAAASUVORK5CYII=)).

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAATCAMAAACuuX39AAAAAXNSR0IArs4c6QAAAG9QTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgA6OgBmOjqQOmaQOma2OpDbZgAAZgA6ZgBmZjqQZrbbZrb/kDoAkDpmkGY6kNv/tmYAtmY6trbbttvbttv/tv/btv//25A627Zm2////7Zm/9uQ//+2///bWtwbFwAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAeElEQVQoU7WORxKDMAxFJUgoiQlgitMsQOL+Z8R4MoPNPn+0eipPAH+JVMkYH16ucwwoO5mNhgkDKI8RSAVDXHyfbbhEiKndgfnZjOLce6XxNqn02qlJA/BtQHeLCwuEd9ei9LNEHzi9qyNS27V/vw7A5SzdxfuibL8oBozoIBxbAAAAAElFTkSuQmCC) is the humidity correction factor; this is 1 between 20-70% humidity.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAATCAMAAAC5m+00AAAAAXNSR0IArs4c6QAAAH5QTFRFAAAAAAAAAAA6AABmADqQAGa2OgAAOgA6OgBmOjqQOma2OpDbZgAAZgA6ZgBmZjoAZjqQZrbbZrb/kDoAkDo6kGY6kLb/kNv/tmYAtmY6tpA6tpC2tra2trb/ttu2tv/btv//25A627Zm29uQ2////7Zm/9uQ/9u2//+2///bJtZRsgAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAm0lEQVQoU82QSRLCIBBFmwgmCg7gQOKUgEDg/he0WViVsmBvb38P7zXAn1QUja6heOpqkWFV/l6BJcU47jQYXhwM3TjI8kpDyGrKUTr/kvY8tGX6KFQ6casgCkRJF9Jc5wOzazQK3QSGbHEhsmATePp4tzIel7KDhrBx4Bmgqc/N34r71xMfMwsFaNrL+yIS1OVTErLprf5YHPkA6xYKSPKQj3gAAAAASUVORK5CYII=) is the ion-recombination factor; this is calculated for each energy and depth, as it is dependent on the instantaneous dose rate (dose/pulse) it is recalculated for each measurement.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAUCAMAAACknt2MAAAAAXNSR0IArs4c6QAAAH5QTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OgBmOjqQOmaQOma2OpDbZgAAZgA6ZjoAZjqQZrbbZrb/kDoAkDo6kGY6kLb/kNv/tmYAtmY6tpBmtrb/ttu2tv/btv//25A627Zm27a229uQ2////7Zm/9uQ/9u2//+2///bZma+EwAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAApUlEQVQoU72R2xaCIBBFz1iaVmiKldhFLED4/x8Me8mW0mPzxFpnhr0HgH+WzaMmxNOxCkUyCUoKjp4WY1s0kGxx0GT3tlq+UhKtulkkRm3BTDq3t6WCzbmrWc8xHOLLZt3BnSg6Q+8Bk3WQ5A+PZ1q5Y+P74DeVfMrQDN7WbBV04numkeCuTcaJIee2vF0/mauJduqNqrzB9PWM5wVK0hf55+e/ALWZC3WkQk+XAAAAAElFTkSuQmCC) is the polarity correction factor; this is negligible for NPL2611 chamber.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABkAAAATCAMAAABSrFY3AAAAAXNSR0IArs4c6QAAAHtQTFRFAAAAAAAAAAA6AABmADqQAGa2OgA6OgBmOjqQOma2OpDbZgAAZgA6ZjoAZjqQZpDbZrbbZrb/kDoAkDo6kGY6kLb/kNv/tmYAtmY6trb/ttu2tv/btv//25A625Bm27Zm29u22//b2////7Zm/9uQ/9u2/9vb//+2///bynJoMAAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAmElEQVQoU8WQ0RaCIBBEB5MsLHWtpEzCAIP//8LwzUqe26c9Z3Zm7y7w//Jl1iUobG4SiuIpcEnQbE31hw5KrNlccb82q3mKsc3wrciZVwq3/cH2lYEvKbRCE6YjD21uwpllF9g94IoBisVm1PzVV89WIB6oaJkfAS25nYHl4fSRL+lRz/NTSb7qbwuTzGpgXtPE5cmPRcMbezMJwAB0FKUAAAAASUVORK5CYII=) is the volume effects related to perturbations; this is included in the calibration factor for measurements performed at reference conditions.

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAVCAMAAAAKL/xWAAAAAXNSR0IArs4c6QAAAI1QTFRFAAAAAAAAAAA6AABmADpmADqQAGaQAGa2OgAAOgA6OgBmOjpmOjqQOmaQOma2OpDbZgAAZgA6ZgBmZjoAZjqQZmY6ZmZmZpDbZrb/kDoAkDo6kGaQkJBmkJDbkLbbkNv/tmYAtmY6tmZmtpA6ttv/tv//25A625Bm27Zm2////7Zm/9uQ/9vb//+2///bK8gKdwAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAA9ElEQVQ4T92S2RqCIBCFh/bd9rQNtESF4P0frzP2lX3VBdfNFcKcc/4Bif6/lOhW5OYiChnVbReSyEARUHanYKqDjEnH7JrCPaBS6RbSLfOAVnLryieRnYQhzwDcLYFshBCd62eAXYnOC5Ens8NNTOT30l8+L8W0zlQ+N33CbUkbyHaUE/CJFL5U7OZ9PmGvJ6MW3KdZa3BYDwqFHcRUQMcGP99AIaNWgSc7Ru4EfDZl9/QNnKdignIoOUBtd6Z3qLC0o6u/tHNoNHKbUriMMS4DzTh45PepGIgpq2rI78qa5+ElAm8VnIug/0GxNZiDnrjJvgMOjhh5JQxIaQAAAABJRU5ErkJggg==)is the chamber calibration factor between dose to water and charge for beam quality Q

And ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB8AAAAVCAMAAACJ68VtAAAAAXNSR0IArs4c6QAAAHhQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OgBmOjqQOmaQOma2OpDbZgAAZgA6ZjoAZrbbZrb/kDoAkLbbkNv/tmYAtmY6tmZmtpA6ttuQttv/tv/btv//25A625Bm27Zm29uQ2////7Zm/9uQ/9vb//+2///bUeIp0gAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAs0lEQVQoU82QbQ+CMAyEb6goKKgo4BtjbhP+/z+062KGJuyzDYEndL1dD/j3Gsqkjno0Kx3tyzS+YlNBifkzw76GLOYlbPZoj5EbpBCLjvv2IJZ+lUBAU9gN/zXJGYp3CQQMZTWeClWB3jSYUz+Qk8o6SLHzAM4i0NSWG+VJFiFqP278KZvdxys5NamnW66/k+vXYkvqJgUTfemZFiX10riQDUfPXPc/sTUs4MoR3e9zidUbzQIOcHOUVEkAAAAASUVORK5CYII=) is the chamber-specific correction factor to correct between a local beam quality ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAATCAMAAACeNWzcAAAAAXNSR0IArs4c6QAAAFpQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OmaQOma2OpDbZgAAZrb/kDoAkGY6kNv/tmYAtpA6tpCQttv/tv//25A62////7Zm/7aQ/9uQ/9u2//+2///b3oVbYAAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAYElEQVQYV51NSRKAIAwruOCCuAsq/P+bpsUZ7+bQSZNJQvQb96hUuXH8Mp1Pc+WJkqvxBz29J1OxKBQ7/J4DLEQ7gEULIdMDvlhp4RDKMNDKAG80oonu6rRyI3AazdkPD425BJ3fBGE3AAAAAElFTkSuQmCC) and reference quality ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAATCAMAAACuuX39AAAAAXNSR0IArs4c6QAAAGNQTFRFAAAAAAAAAAA6AABmADpmADqQAGa2OgAAOgA6OgBmOjqQOmaQOma2OpDbZgAAZrb/kDoAkDo6kGY6kNv/tmYAtpA6tpCQttv/tv//25A62////7Zm/7aQ/9uQ/9u2//+2///bLOZATgAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAAAg0lEQVQoU7WO2xKCMAxEU1CKCljlIm0J5P+/0myRgfGdPJ3sbDZLdNLMb2Munz2cbRWku4ZNEVcoxqzdhBUPwmqO+fhziKtBe8bSPHVfGpXZmgoIweuFvNq0qFl6BPNtpE6NorUeqMX3QB4ViMvUAQ6fPmg1GQLSxCGQaLIZIKYv//MFeYAHswguVecAAAAASUVORK5CYII=)

---
Whereas for electrons is given by:
$$D_w(z_{ref,w})=[M_{raw}f_{TP}f_{pol}f_{ion}f_{elec}]N_{D,w}(R_{50,D})$$
The main difference between this and the photon output is the method for the calculation of $N_{D,w}(R_{50,D})$.  

# Calibration Coefficients
The calibration certificate for [[On Particle Interactions#Photons|Photons]] chambers includes an equation for the value $k_{vol}N_{D,w,Q_0}$.  This is given as a polynomial equation $CC=a+b[TPR]+c[TPR]^2+d[TPR]^3$, which is a function of the [[Quality Index]] $TPR_{20/10}$.

On the other hand, [[On Particle Interactions#Electrons|Electron]] measurements are only given for a set of given beam qualities, these can be corrected to a given energy using the stopping power ratio as given by:
$$N_{D,w}(R_{50,D,u})=D_{D_w}(R_{50,D,ref})\frac{S_{w/air}(R_{50,D,u},Z_{ref,u})}{S_{w/air}(R_{50,D,cal},Z_{ref,cal})}$$
Where the stopping power ratio is calculated using:
$$S_{w,air}(Z_{ref})=1.253-0.1487(R_{50})^{0.214}$$

# Ion Recombination
The ion-recombination factor corrects for the loss of charge due to the recombination of liberated charges.  While some of these re-combinations will be instantaneous with the source of the electron, as the dose per pulse (instantaneous dose rate) of an exposure increases so does this factor.  This is because there are more ions that the charge could re-combine with. 

The ion-recombination factor for beam can be calculated using the two-voltage method.  Ideally this should be done with a voltage ratio of greater than 3.
$$k_{ion}=1+\frac{(M_1/M_2)-1}{(V_1/V_2)-1}$$
