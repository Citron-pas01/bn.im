---
layout: post
title:  "Cyclic Voltammetry Is Right There For A Battery"
date:   2020-12-19 20:47:52 -0500
categories: Characterizations
author: "Bo Nie"
permalink: /:categories
---
***Cyclic Voltammetry (CV)*** is almost everywhere in the electrochemistry (EC) world regarding its powerful analytic strength. 
Battery can’t be absent from an EC talk as CV has been widely explored for the complex electrochemical reactions and dynamics. 
Let’s talk about CV and its application in a battery.

<h3>Background</h3>
CV can not only preliminarily study the possible electrochemical reactions of the electrode system 
but evaluate the reversibility of the electrode process as well as the adsorption and desorption in the basic process of the electrode. 
Take one relatively complex electrochemical system of lithium-sulfur batteries as an example. 
Here is to demonstrate the electrode reaction history, the compatibility of the electrode materials and electrolytes, 
and the stability of cathode and anode.

Move to a little background of the lithium-sulfur battery. The electricity generates from the multi-electron reactions between lithium metal and sulfur molecule:

$$ {S_8} + 16{Li^{+}} + 16{e^{-}} \leftrightarrow 8{Li_2}{S}  $$           cathode discharge-charge reaction <br>
Sulfur as the cathode has 1672 mAh/g theoretical specific capacity. The lithium anode’s theoretical specific capacity is up to 3842 mAh/g. 
The average potential of the cathode to $$ Li^0/Li^+ $$ is 2.15 V which results in a high theoretical energy density of 2567 Wh/kg.

<h3> How does CV work?</h3>
CV works by applying a potential on an electrode with scanning from $${E_i}$$ to the negative potential direction at a rate of v. 
It switches to the other scanning direction when the time $$t = \lambda$$ where the potential is the $$E_{\lambda}$$ and keep scanning back the original potential at the same rate. 
This is one cycle but it usually repeats several cycles to take the continuous triangle wave as the potential signal. 
The generated CV curve provides two important parameters: peak current ratio $${i_p}$$ and peak potential difference $${\Delta{E}}$$ .
As the gradually increasing current during potential scanning in the negative direction, it continues with normal decay. 
As the gradually increasing current during potential scanning in the negative direction, it continues with normal decay. 
The magnitude of the current relies on the two steps in the process: the charge diffusion in the electrode and the electron-reactions. 
During the redox process, the electron transfer coefficient is a function of the potential:

$$ {k_f} = k^{0}exp{[}\frac{-\alpha nF}{RT}{E-E^0}{]} $$

$${k_0}$$ is the standard heterophase electron transfer rate coefficient, $$n$$ is the number of electrons transferred per molecule, 
$$F$$ is the Faradic coefficient, $$R$$ is the universal gas coefficient, $$E_0$$ is the standard redox potential, $$\alpha$$ is the transfer coefficient range in (0-0.5).

The ascend rate can be explained as the dependent exponent of electron transfer rate on the applied potential. 
Due to the concentration consumption near the electrode surface, the reactant diffusion rate to the surface gradually slows down and cannot keep a stable concentration area near the electrode. 
If the consumption area increases, the distance between reactant molecules will dramatically increase, the mass transfer rate decreases. 
Finally, the mass transfer becomes the bottleneck. With the further decrease of concentration, mass transfer causes a current delay which leads linear relationship between current and $$t^{-1/2}$$ in the diffusion-controlled area.

In the back scanning process, the products have a relatively high concentration and the same trend near the electrode area. 
It marks the current change in the same way. The electron transfer coefficient in the reverse process:

$$ {k_f} = k^{0}exp{[}\frac{1-\alpha nF}{RT}{E-E^0}{]} $$

For the reversible reactions, the oxidized and reduced concentration ratio in the electrochemical equilibrium reaction can be written as:

$$ E = {E^0} - \frac{RT}{nF}\ln{(}\frac{[R]}{[O]}{)_{}x=0} $$

The reduction peak gradually separates from the previous ones with increasing scanning rate. 
Two peaks will never overlap when $$k_0 \leq 2×{10^{-5}}v^{\frac{1}{2}}  cm/sec. $$ It will be called an irreversible reaction system.
In a reversible reaction, the peak height is proportional to the square root of the scanning rate.

$$ i_p = 2.69×{10^5} n^{\frac{3}{2}} A {D_0}^{\frac{1}{2}} v^{\frac{1}{2}} {C_0}^*  $$

$$ A: cm^2, D_0: cm^2{/}sec, v: volt{/}sec, {C_0}^*: mole{/}{cm^3} $$, at room temperature.

The side reactions can be identified from the anode peak current to cathode peak current ratio ($$i_pa{/}i_pc$$):

<body>
	<div align="center">
	<b>Table 1 </b> The reactions of the oxidation-reduction process.
		<table BORDER=1 HEIGHT=180 width=500>
			<tr><td><b>EC reaction category</b></td><td align="center"><b>Reation</b></td></tr>
			<tr><td><small>Reversible reaction </small> </td><td><small>$$ O + ne^- \rightleftharpoons R $$</small> </td></tr>
			<tr><td><small>Reversible reaction after</small> </td><td><small>$$ O + ne^- \rightleftharpoons R, R\rightleftharpoons Z $$</small>  </td></tr>
			<tr><td><small>Irreversible reaction after </small>  </td><td><small>$$ O + ne^- \rightleftharpoons R, R\rightarrow Z $$ </small>   </td></tr>
			<tr><td><small>Side reversible reactions before </small>  </td><td><small>$$ Z \rightleftharpoons O, O + ne^- \rightleftharpoons R $$</small> </td></tr>
			<tr><td><small>Irreversible reactions </small> </td><td><small>$$ Z \rightleftharpoons O, O + ne^- \rightarrow R $$ </small> </td></tr>
		</table>
	</div>
</body>
<br>
<p align="center">
	<img src="/assets/images/c-v.jpg" width="400" alt="Fig. 2. The current ratio calculation based on the Nicholson method [1]" class="figure-image-post"><br>
	<b>Fig. 2.</b> The current ratio calculation based on the Nicholson method [1]
</p>

Use the Nicholson method to calculate the current ratio from CV spectra:

$$ \frac{i_{pa}}{i_{pc}} = \frac{(i_{pa})_0}{i_{pc}} + \frac{0.485(i_{\lambda})_0}{i_{pc}} + 0.086  $$

So, the current ratio can be used to identify the side reactions in an EC system. 
It also helps to identify the reaction steps in the complex reaction systems.

<h3>CV analytic in lithium-sulfur battery</h3>
Lithium-sulfur battery uses sulfur as cathode active material, lithium as anode active material, and the electrolyte is usually the lithium salt (LiTFSI) dissolved and ether-based solution (DOL/DME). 
The separator can be the microporous polyethylene film. During the EC reaction process, there are multi-step reactions in the charge and discharge processes [2].


<body>
	<div align="center">
	<b>Table 2 </b> The multi-step reaction in lithium-sulfur battery[2]
		<table BORDER=1 width=500px>
			<tr><td align="center"><b>Steps</b></td><td style="width:70%" align="center"><b>Reation</b></td></tr>
			<tr><td><small>$$ step 1  $$ </small> </td><td><small>$$ S_8 + 2e^- \rightarrow {S_8}^{2-} $$</small> </td></tr>
			<tr><td><small>$$ step 2-1  $$</small> </td><td><small>$$ 3{S_8}^{2-} + 2e^- \rightarrow 4{S_6}^{2-}; $$</small>  </td></tr>
			<tr><td><small>$$ step 2-2  $$ </small>  </td><td><small>$$ 2{S_6}^{2-} + 2e^- \rightarrow 3{S_4}^{2-} $$ </small>   </td></tr>
			<tr><td><small>$$ step 3  $$ </small>  </td><td><small>$$ {S_4}^{2-} + 4Li^{+} + 2e^- \rightarrow 2{Li_2}{S_2} $$</small> </td></tr>
			<tr><td><small>$$ step 4  $$ </small> </td><td><small>$$ {Li_2}{S_2} + 2Li^{+} + 2e^- \rightarrow 2{Li_2}S $$ </small> </td></tr>
		</table>
	</div>
</body>
<br>

In the discharge process, the anode lithium metal loses electrons and converts into lithium-ion. lithium-ion goes through the electrolyte, 
separator and diffuses to the cathode surface. The lithium-ion reacts with a sulfur molecule ($$S_8$$) and forms lithium sulfides. 
In the charge process, the lithium sulfides lose electrons and change back to the sulfur molecule, 
then the lithium metal is regenerated when the lithium-ion diffuses back to the anode and receives the electron which is from the cathode side by the outer circuit. 
However, there are supposed to generate several intermediates as the discharging products on the cathode side. 
In the 4 step reactions, it derives two potential plateaus (2.4 V & 1.9~2.1V) during the discharge process, 
which can be easily identified by the CV spectra. Each potential plateau generates a peak current because of the electron-transfer reaction. 
In the multiple cycle scanning, the degree of peak overlapping from redox scanning processes is useful to compare the EC reaction reversibility for different lithium-sulfur systems.  
i.e. the different electrolyte solutions have been compared in lithium-sulfur batteries by CV spectra [3].

<p align="center">
	<img src="/assets/images/li-s-cv.jpg" width="400" alt="Fig. 3. The CV of sulfur in LiTFSI/Triglyme and LiTFSI/PEGDME electrolyte [3]" class="figure-image-post"><br>
	<b>Fig. 3.</b> The CV of sulfur in LiTFSI/Triglyme and LiTFSI/PEGDME electrolyte [3]
</p>

The peak at 2.37V corresponds to the reduction of the sulfur molecule to polysulfides ($$ Li_2S_n, (4 < n < 8)$$), the peak at 2.04 V represents the 2nd reduction of lithium polysulfides to lithium sulfide ($$Li_2S$$). 
The oxidation process experiences two peaks (2.43 V & 2.47 V) corresponding to the reversed reactions.

Since CV can be used to identify the reaction details and dynamics, it can explain the decay mechanism from the battery and discover new charge transfer or mass diffusion process inside an EC system.

<h3>Reference</h3>
H. Yamin, A. Gorenstein, J. Penciner, Y. Sternberg & E. Peled. Lithium-Sulfur Battery Oxidation/Reduction Mechanisms of Polysulfides in THF Solutions. Journal of the Electrochemical Society 1988, 135(5), 1045-1048.

Gary A. Mabboi. An Introduction to Cyclic Voltammetry. Journal of Chemical Education, 1983, 60(9), 697-702

Joongpyo Shim, Kathryn A. Striebel & Elton J. Cairns. The lithium/sulfur rechargeable cell – Effects of electrode composition and solvent on cell