---
layout: post
title:  "A Practice - Dimensions, Tolerance, and Loading Matter for 18650 Lithium ion Batteries"
date:   2024-01-20 08:40:22 -0500
categories: Models
---

Lithium-ion batteries can be designed into different shapes, such as coin cells, cylinder cells, pouch cells, and prismatic cells. Quite many manufacturers are producing pouch cells because its high energy storage density and lower cost. One day, a friend asked me why Tesla is not making pouch cells and picks cylinder cells instead, and what an 18650-battery cell is. This question recalled my memory of making 18650 LiFePO<sub>4</sub> cells in a pilot lithium-ion battery manufacturing line years ago. 
<!--more-->
A battery contains a cathode, anode, separator, electrolyte, leads, and packaging materials. As one of the most important components inside the battery cell, many electrode materials have been developed into use regarding their different lattice structures, intercalation/deintercalation potentials, nominal capacities, and cycling stability. Commercial LiFePO<sub>4</sub> and graphite were selected as the cathode and anode active materials, respectively. Commercial liquid electrolytes and PP microporous membranes were used as Li<sup>+</sup> diffusion media and e<sup>-</sup> blockers, respectively.

<h3>How is a battery designed?</h3>
Come back to the second question. How the battery is named. As taught in a battery course, the cylinder-shaped rechargeable battery is described as "xxx-#####" (3 letters + 5 numbers). The 1<sup>st</sup> letter represents the anode (<em>I</em> is Lithium-ion batteries, and <em>L</em> is lithium-metal batteries); The 2<sup>nd</sup> letter represents the active material of the cathode; The 3<sup>rd</sup> letter represents the shape of the battery where <em>R</em> is a cylinder-shaped battery; The 1<sup>st</sup> two numbers represent the diameter of the battery cylinder in millimeters; The rest numbers represent the height of the battery cylinder times 10 in millimeters. That is, 18650 is a cylinder-shaped battery with a diameter of 18 mm and a height of 65 mm.
<br>
<p align="center">
	<img src="/assets/images/p1-battery-18650.jpg" width="600" alt="Fig. 1. The 18650 cylinder-shaped lithium-ion battery configuration" class="figure-image-post"><br>
	<b>Fig. 1.</b> The 18650 cylinder-shaped lithium-ion battery configuration (Ref. Bosch-press)
</p>

When searching for the capacity of an 18650 cell, it can be 2000, 2500, 3000 mAh, or more.  
How to define the mass usage of cathode and anode to achieve this capacity goal? 
Regarding the LiFePO<sub>4</sub>-graphite 18650 battery, it has the following electrochemical reactions,
<p>Cathode: $$ LiFePO_4 \longleftrightarrow Li_{1-x}FePO_4 + xLi^{+} + xe^{-}  $$ </p>
<p>Anode: $$ xLi^{+} + xe^{-} + 6C \longleftrightarrow Li_{x}C_{6} $$ </p>
<p>Overall, $$ V_{theory} = -(E_{defect} + xE_{Li} - E_{perfect})/xF $$ </p>

where $$ E_{perfect} $$ and $$ E_{defect} $$ represent the energy of the perfect lattice and the deintercalation resulting defect lattice, respectively. $$ E_{Li} $$ is the energy for a single lithium atom. The theoretical potential of LiFePO<sub>4</sub> is 4.74 V. It for graphite is 1.35 V. So, the voltage of the  LiFePO<sub>4</sub>-graphite cell is 4.74-1.35 = 3.39 V.

In general, the capacity of the battery needs the anode capacity to exceed by 10%. Assuming a capacity be designed to 3000 mAh, with theoretical capacities of cathode and anode active materials being 170mAh/g and 372mAh/g, respectively, 
and with an efficiency of 100%, the required cathode material is 3000/170 = 17.65 g, and the negative electrode material is 3000 $$\times$$ 110% / 372 = 8.87 g. 
When choosing the ratio, it is important to avoid a small cathode/anode mass ratio that may result in incomplete utilization of the anode material. A large mass ratio could induce safety risks due to overcharging of the anode. 
Additionally, the required mass ratio of the two electrodes depends on their respective Coulombic capacities and the number of reversible lithium ions.

<h3>The mass loading, dimensions, and tolerance of the battery components need to be examined for consistent cell batches.</h3>

However, the corresponding nominal capacity of the electrode would be always lower than the theoretical values because of the kinetic factors and material defects. 
For example, 130 mAh/g for the LiFePO<sub>4</sub> cathode and 320 mAh/g of graphite anode may be achieved inside the 18650 cells on average. It is of great importance to design the cell with an updated LiFePO<sub>4</sub>/graphite ratio and the mass content of other components to meet the consumer requirements (e.g., 3000 mAh per cell). 
<br>
<p align="center">
	<img src="/assets/images/p2-battery-18650-sketch.jpg" width="600" alt="Fig. 2. The sketch of an as received 18650 stainless steel (SS) shell and crimped  cell" class="figure-image-post"><br>
	<b>Fig. 2.</b> The sketch of a received 18650 stainless steel shell and a crimped  cell
</p>

Specifically, during the slurry coating workshop, there are critical parameters that need to be calculated. For example, the width ($$ w_c, w_a $$), effective length ($$ l_c, l_a $$), thickness ($$ t_c, t_a $$), areal density ($$ d_c, d_a $$) of 
the coated cathode and anode electrode pieces. The mass of the double-side coated cathode can be calculated as $$ m_c = 2w_c l_c d_c $$. Considering the composition of the cathode coating, ~85% of LiFePO<sub>4</sub> results in the capacity of:
$$ Capacity_c = m_c \times 85\% \times 130 mAh/g $$. The anode mass can be calculated in the same way. 

The 18650 cell has an approximate volume of 14.5ml after being crimped. The volume of a winded cathode/separator/anode roll, leads, lead tape, winding terminal tape, electrolytes, and bottom insulator will be combined to calculate the assembling volume ratio and evaluate the space utilization. 
Then the groove can be determined. Normally, put the winding roll into an 18650-steel shell and use a machine to create a groove with a depth of 1.9 mm and 3.4 mm away from the upper edge.

Considering the dimensions of the electrodes, separator, and lead, the calculation needs to be done to make the best use of an 18650 cell. For example, the width of the separator might be 2 or 2.5 mm less than the SS cylinder height. The width of the anode piece may need to further 2 mm less than the separator. 
The cathode piece will be 1 or 2 mm narrower than the anode piece. Regarding lead welding, the size and the surface finishing of the weld influence the conductivity of the charging/discharging current and any potential risk of short circuits.

<h3> Why the 18650 cell is so popular in the battery industry? </h3>
The 18650 cylinder cell stands out because of its safety. There are several feature designs to maintain this safety control. 
 * <b>Inside lead:</b> The welded lead gathers the current generated by the battery's active material to form a larger current for external output. Therefore, the contact between the current collector and the lead needs to be sufficient.
 * <b>PTC (Positive Temperature Coefficient):</b> It is a thermistor. When it detects the temperature of the lead rises, its resistance increases, and vice versa. When the circuit returns to normal, the temperature of PTC also decreases. The circuit can then resume operation. PTC serves as a resettable fuse. When a large current passes through PTC, the temperature rises sharply, increasing the resistance, and thereby protecting the battery circuit.
 * <b>Safety valve:</b> When the internal temperature of the battery is abnormal and the pressure rises to 1.0-1.2 MPa, the safety valve automatically opens to release internal gas, preventing explosion due to excessive pressure.

<h3>A Tesla Model S has over 7104 of 18650 cells, can we use fewer cells and make the vehicle lighter?</h3>
Since the nominal capacities of the electrodes are relatively lower than theoretical ones, it has great potential to improve the amount of energy storage for a single cell. 
First, we may require a high lithium-ion intercalation/deintercalation potential for the cathode and a lower lithium-ion intercalation/deintercalation potential for the anode. 
Then, the active materials need to be optimized at the highest activity. To do that, different carbon additives were added to enhance the electronic conductive network and increase the electrolyte wettability simultaneously. 
Some carbon additives (e.g. KS-6) can fill the gap between particles and increase the tap density as well as modify the flexibility of the rolling electrode pieces. 
<br>
<p align="center">
	<img src="/assets/images/p3-battery-slurry-coating.jpg" width="600" alt="Fig. 3. The schematic of slurry coating for electrode manufacturing." class="figure-image-post"><br>
	<b>Fig. 3.</b> The schematic of slurry coating for electrode manufacturing.
</p>

Regarding the anode, the dispersive additive (CMC) and binder (SBR) are added separately. CMC disperses the hydrophobic graphite and carbon into water. It can also increase the uniformity of the slurry by adjusting the viscosity.
The combination of CMC and SBR enables the electrode to a great integrity and robustness after the calender. 

Since these additives influence the homogeneity and viscosity during the slurry coating process, together with the controlled coating speed, thickness, and the heat field of the oven, the electrode pieces can be maintained at high consistency. 
The tolerance of trimming the electrode matrix into separated pieces also plays a role in the variation between different 18650 cells. 

Once the electrode materials are in high activity, and all the battery cells are almost identical, a much lower cost and high energy density can be provided by a single battery cell and later integrated pack.

<h3>How the battery cell is being tested?</h3>
Every cell has been activated for 2 days. Then, run the formation program (rest, galvanostatic charge sequentially with different current densities of 50, 100, and 200 mA respectively; rest again). 
The cell can be tested for capacity separation after aging for about one week.
The capacity separation was operated twice. Each separation uses different charge-discharge programs. The first charge-discharge runs at a higher current density for several cycles. The second is at a smaller current density for several cycles.  
<h3>Summary</h3>
Throughout the battery design, electrode processing, and battery assembly, it is apparent that the battery size, component dimensions, and processing details are critical to the final performance.
For example, the adhesion of the electrode material to the current collector, the electrode uniformity, and the thickness variation determine whether the cathode/separator/anode roll could be inserted into the 18650 cylinder shell and achieve the designed capacity.
Measuring the tolerance and controlling the process precision are crucial for successful battery fabrication. Six Sigma may be needed to examine the pilot line. That's a lot of measurements though.
