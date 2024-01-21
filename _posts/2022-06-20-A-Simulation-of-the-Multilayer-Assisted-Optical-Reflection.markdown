---
layout: post
title:  "A Simulation of the Multilayer Assisted Optical Reflection"
date:   2022-06-20 20:47:52 -0500
categories: Models
---

A multilayer light reflection model is designed based on the stacking unit of oxide films, metallic films, and a vacuum gap. 
By tuning the number of units, the thickness of each layer, and the stacking sequence, 
an effective light-reflection medium is expected to be applied to the building windows or vehicle windows. 
Beyond the model design, the genetic algorithm is cooperated to optimize these variables. 
In the python-based simulation, an initial demonstration is introduced to pave a direction for maximizing the light reflectance.
<!--more-->
<h3>Introduction</h3>
Light is a daily observation that has been interpreted into several categories: geometrical optics; light as a wave; 
light as electromagnetic radiation; and the quantum theory of light. 
In the engineering space, the first two interpretations are often used for device design or measurement.

In geometrical optics, we take light as rays. When the light traveling in one transparent medium encounters a boundary with a second transparent medium, 
a portion of the light is reflected and a portion is transmitted into the second medium. 
The transmitted portion of light changes the traveling direction. It follows the law of refraction:

$$ {n_1}sin{\theta_1} = {n_2}sin{\theta_2} $$

<br>
<p align="center">
	<img src="/assets/images/p2-reflection.jpg" width="400" alt="Fig. 1. The schematic of the light reflection and refraction" class="figure-image-post"><br>
	<b>Fig. 1.</b> The schematic of the light reflection and refraction
</p>
The index of refraction ($$n$$) varies across different mediums (air, water, or glass). 
The value for any medium is a dimensionless constant equaling the ratio of the speed of light in a vacuum to its speed in that medium.

Take light as a wave, which contains vibration energy. We can use a harmonic wave equation to represent the light

$$ \Phi(x,t) = A cos(\frac{2\pi x}{\lambda} - 2\pi ft)  $$

the wavelength $$\lambda$$ of the wave is the physical separation between successive crests. The maximum displacement of the wave, 
or amplitude, is denoted by $$A$$. The number of oscillations per second is the wave frequency $$f$$. 
The traveling speed in a medium ($$v$$) equals the distance between crests multiplied by the frequency ($$v = \lambda f$$ ).

Because the refraction indexes for different materials are different. The potion of the transmitted light can be adjusted by changing the characteristics of the material. 
One of the strategies is designing the multilayer medium and increasing the number of reflection-refraction interfaces. 
Based on this approach, there is a possibility of minimizing the transmitted portion of the light which is preferred in the summer hot weather. 
By tuning the refraction index to different stacking layers, the number of stacking layers, and the thickness of each stacking layer, 
an effective light-reflection medium is expected to be used on the building windows or vehicle windows.

With this in said, a model of multilayer medium reflection is designed to optimize the light reflection. 
The variables are the number of stacking layers, the material for each stacking layer, and the thickness of each layer. 
In order to maintain the transparent property and the mass efficiency, the thickness is expected to be controlled in nanometers.

<h3> Model Set-up</h3>
Some assumptions need to be revealed before the model setup:
1. The intensity of the light is quantified as a relative ratio by the transfer-matrix method.<br>
2. The interaction at the interface for the back-ward traveling light potion is not considered.<br>
3. The light wave range defaults as the visible light.<br>

The material for the stacking layers can be metal: (silver, gold, aluminum, copper, etc.) and oxide compounds (alumina, silica, titanium oxide, etc.). 
In general, the metallic film gives a good reflectance. However, due to the plasma effect, the metals show a poor reflection at the ultraviolet and short visible wavelengths. 
In the model, we use silica, alumina, silver, and titanium oxide as the stacking unit pair because the TiO<sub>2</sub>, SiO<sub>2</sub>, and Al<sub>2</sub>O<sub>3</sub> do not absorb light in the visible and near-infrared range. 
For some conditions, the vacuum gap inside the glass can stop the noise propagation. In return, it increases the interaction interfaces. 
Therefore, we also design a vacuum gap in the stacking unit to increase the ability of both light reflection and noise shield. 
<br>
<p align="center">
	<img src="/assets/images/p2-multilayer-reflection.jpg" width="400" alt="Fig. 2. The refection unit of layer stacking" class="figure-image-post"><br>
	<b>Fig. 2.</b> The refection unit of layer stacking
</p>

According to the light traveling speed v = λf, the light of different wavelengths results in different refraction indexes in a specific medium. 
So, the input data include the thickness of the constructing layers, the refraction index of each layer, the incident angle, and the wavelength range. 
In the model, the input data matrix is set as *[n_list, d_list, th_θ, lam_vac]* which contains the geometrical information of the multilayer stacking. 
Using the transfer-matrix method, the calculation is based on the core “tmm_core.py” (referred to Steve Byrnes as “Multilayer optical calculation”). 
The output data is presented as reflectance vs. wavelength, transmission vs. wavelength, absorption vs. wavelength, and extinction vs. wavelength.


<h3>Starting with a Demo</h3>
Fixing the thickness of the gold film layer, use the model to get the maximum reflectance by changing the thickness of other SiO<sub>2</sub> and TiO<sub>2</sub> layers. 
The corresponding ranges of thickness are [10nm, 15nm] for SiO<sub>2</sub> and [5 – 55nm] for TiO<sub>2</sub>. To get the optimal reflection, 
the maximum cumulative reflectance across the wavelength range [200 – 1500nm] is selected. Meanwhile, the minimum cumulative absorption is selected as optimal. 
So as the optimal transmission. By traversing the thickness range, the model shows an optimal thickness pair as [SiO<sub>2</sub>: 10nm, TiO<sub>2</sub>: 5nm]. 
The simulated reflectance and absorption plot can be plotted as well.
<br>
<p align="center">
	<img src="/assets/images/p2-modeling-info.jpg" width="400" alt="Fig. 3. The simulation of the demo for changing the layer thickness" class="figure-image-post"><br>
	<b>Fig. 3.</b> The simulation of the demo for changing the layer thickness<br>
	<img src="/assets/images/p2-model-spectrum.jpg" width="400" alt="Fig. 4. The simulated reflectance and absorption vs. the wavelength" class="figure-image-post"><br>
	<b>Fig. 4.</b> The simulated reflectance and absorption vs. the wavelength
</p>

Due to the multiple variables and the complicated varying ranges, the manually adjusted input ranges for some of them cannot meet the model optimization goal. 
Therefore, the Genetic Algorithm is used to optimize the variables and achieve an effective multilayer light reflection design. 
As known that a genetic algorithm is a search heuristic, it reflects the process of natural selection where the fittest individuals are selected for reproduction in order to produce offspring for the next generation. 
The algorithm includes initial population, fitness function, selection, crossover, and mutation. When Implementing the optimization method, the variable ranges, parameter precision, mutation probability, cross probability, group size, and the number of generations are preset. 
Especially the population group size and the number of generations are set as 20 and 20 for a demonstration. 
A complete optimization will be launched in a computational task center. The result of this initial demonstration shows that the reflectance gradually increases along with the generations iterating.
<br>
<p align="center">
	<img src="/assets/images/p2-model-computation.jpg" width="400" alt="Fig. 5. The simulation result of the genetic algorithm optimization" class="figure-image-post"><br>
	<b>Fig. 5.</b> The simulation result of the genetic algorithm optimization<br>
	<img src="/assets/images/p2-model-optimization.jpg" width="400" alt="Fig. 6. The iteration plot for the optimized refletance via genetic algorithm" class="figure-image-post"><br>
	<b>Fig. 6.</b> The iteration plot for the optimized refletance via genetic algorithm
</p>
No doubt the reflectance would be pushed close to the optimum value with increasing numbers of population size and iterating generations. 
This demonstration gives a direction for the multilayer light reflection model optimization, but more needs to be worked out and made to complete the model.  
For further modification, the code for this demonstration can be found at:  <a href="https://github.com/Citron-pas01/Multilayer-light-reflection-model">Multilayer-light-reflection-model</a>.


<h1>Reference</h1>
Keçebaş, Muhammed Ali, and Kürşat Şendur. “Enhancing the spectral reflectance of refractory metals by multilayer optical thin-film coatings.” JOSA B 35, no. 8 (2018): 1845-1853.

Steve Byrnes “Multilayer optical calculation.” arXiv:1603.02720 [physics.comp-ph].

<a href="https://www.britannica.com/science/light/Reflection-and-refraction">https://www.britannica.com/science/light/Reflection-and-refraction</a>.

Kumar, Manippady Krishna, Sivashankar Krishnamoorthy, Lee Kheng Tan, Sing Yang Chiam, Sudhiranjan Tripathy, and Han Gao. “Field effects in plasmonic photocatalyst by precise SiO2 thickness control using atomic layer deposition.” Acs Catalysis 1, no. 4 (2011): 300-308.

Schürmann, Mark, Stefan Schwinde, P. J. Jobst, O. Stenzel, Steffen Wilbrandt, A. Szeghalmi, A. Bingel, P. Munzert, and N. Kaiser. “High-reflective coatings for ground and space based applications.” In International Conference on Space Optics—ICSO 2014, vol. 10563, pp. 171-179. SPIE, 2017.
