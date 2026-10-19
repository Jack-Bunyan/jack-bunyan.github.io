---
title: Q-Brachytherapy TG43 graph
tags:
  - Physics
  - Radiotherapy
  - Therapy
---
# Background
The TG43 graph shows how the dose rate from a [[Brachytherapy#HDR|HDR Brachytherapy]] source varies with the distance from the source.  This graph does not take into effect the [[Dose#Build-up|Build-up]] region, yet despite this produces a build-up region to peak—as well as insignificance of this in the keV region, as well as a smaller region at the centre of the region where dose falls off.  
![[TG43 graph.png]]

![[TG43 Diagram.png]]
TG-43 itself describes that the dose rate from a brachytherapy source should be described using one of two different formalisations:
> For 1D
> $\dot D(r)= S_k \cdot \Lambda \cdot (\frac{r_0}{r})^2\cdot g_p(r) \Phi_{an}(r)$
> For 2D
> $\dot D(r,\theta)=S_k \cdot \Lambda \cdot \frac{G_L(r,\theta)}{G_L(r_0,\theta_0)}\cdot g_L(r)\cdot F(r,\theta )$ 

Where
> - $S_k$ air-[[kerma]] strength measured on the source transverse plane.  units of U=cGycm$^2$h$^{-1}$.  Differs slightly in Europe where Reference Air Kerma Rate (RAKR) which specified a measurement distance.
>-  $\Lambda$ dose rate constant, converts the air-kerma strength to dose rate to water in water, with units cGyh$^{-1}$U$^{-1}$ or cm$^{-2}$ in SI.  This can be measured through experiment or modelled using [[Monte Carlo]] simulations.
>- $G_L(r,\theta)$ or $\frac{1}{r^2}$ are the geometry functions, with the latter correcting using the inverse square law, while the first is based of the line source and is equal to $G_L(r,\theta)\frac{\beta}{Lrsin(\theta)}$
> - $g_{L,P}(r)$ **This is the radial dose function that is the subject of this question, correcting for attenuation from either a line source or a point source.** 
> - $F(r,\theta)$ and $\Phi_{an}(r)$ are the anisotropy functions and account for all other difference within the dose distributions. 

In cases where a line source has an unknown direction at distances r<L, a modified form of the 1D source formalisation may be used where the inverse square law $\frac{r_0}{r}^2$ term is replaced with an isotropic form of the 2D geometry function may be used $\frac{G_L(r,\theta_0)}{G_L(r_0,\theta_0)}$.  For both of these cases $r_0$ is set to be 1cm and $\theta_0$ is set to be $\frac{\pi}{2}$.

![[radial dose graph.jpg]]

# Modelling
When considering what causes this region, it is important to consider the structure of what this graph represents.  At any given point there are x-rays travelling from various points of the source, each of which must travel through the shielding of the applicator.

From our understanding of [[On Particle Interactions#Cross-section|Attenuation]] we know that
> $\Phi = \Phi_0 \exp(-\mu x)$ 

Where the particle flux $\Phi$ will be proportional to the [[Dose]].  For a path that travels through multiple materials the attenuation can be combined as follows
> $\Phi = \phi_0 \exp(-\mu_1 x_1)\cdot \exp(\mu_2 x_2) = \Phi_0 \exp(-\mu_1 x_1 -\mu_2 x_2)$

This takes into account the attenuation from the portion of travel both within the applicator and the tissue surrounding it.  
![[brachytherapy source question diagram.png]]
From the geometry of the situation the distances $x_1$ and $x_2$ can be expressed as

> $x_1 = \sqrt{A^2+\left(\frac{A}{x}y\right)^2}$
> $x_2 =\sqrt{(x-A)^2+\left(\frac{x-A}{x}y\right)^2}$

We can use an integral to consider a line source where the radiation path passes through materials with those distances.

> $D\propto \int_{-\infty}^{\infty}\exp\left(-\mu_1 \sqrt{A^2+\left(\frac{A}{x}y\right)^2}-\mu_2 \sqrt{(x-A)^2+\left(\frac{x-A}{x}y\right)^2}\right)\text{d}y$ 

The graph below shows that the psuedo build-up in dose can be replicated with a purely analytical model using arbitrary variables.  Though, when including the distance falloff, the linear falloff dominates this attenuation affect (magnitudes in graph are arbitrary).
<iframe src="https://www.desmos.com/calculator/4zvgrovafk?embed" width="700" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

The cause for this is that the capsule is the dominant attenuator in this situation; when the reference point is further from the source the incident rays pass through the shielding at a lower angle, travelling through and being attenuated by less of the material.  Closer to the source it must travel at a steeper angle, this means that a greater portion of the distance is through the attenuating material decreasing the dose.

However, even when substituting the variables that are more physically correct this doesn't seem to be completely accurate (dashed red line is assuming tissue has 0 attenuation).
<iframe src="https://www.desmos.com/calculator/cc5ftaheiz?embed" width="700" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

# Reflections
![[Design of a gammamed HDR source.png]]

Upon looking at the structure of the brachy sources that we use, I believe that there are two primary reasons for the differences between my plot and the data in literature.
1)  $g_L(r)$ considers both the attenuation from the material as well as scatter, my algorithmic approach only considers the attenuation of the source and tissue.
2) Line source assumption.  Approach made the assumption that the radiation was distributed from a 1D line in space.  Meaning that self attenuation and distribution was not considered.

May be worth re-approaching this once I have done more work with Monte Carlo simulations.  However, clinical importance of this relationship at low distances—which we are most interested in theoretically—is low due to the dominance of the geometric reduction in dose.

---
Title: [Dosimetry of interstitial brachytherapy sources: recommendations of the AAPM Radiation Therapy Committee Task Group No. 43. American Association of Physicists in Medicine](http://www.ncbi.nlm.nih.gov/pubmed/7565352)
Authors: R. Nath, L. L. Anderson, G. Luxton, K. A. Weaver, J. F. Williamson, A. S. Meigooni
Year: 1995
DOI: 10.1118/1.597458

Title: Handbook of Radiotherapy Physics: Theory and Practice
Authors: 
Year: 2007
DOI: 10.1201/9781420012026

Title: [Dose Calculation for Photon-Emitting Brachytherapy Sources with Average Energy Higher than 50 keV: Full Report of the AAPM and ESTRO](https://www.aapm.org/pubs/reports/RPT_229_full.pdf)
Authors: 
Year: 
DOI: 

