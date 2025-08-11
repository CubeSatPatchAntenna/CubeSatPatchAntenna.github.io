---
layout: page
title: Project Background
subtitle: Placeholder
---

## Design Overview

The finalized design is a square stacked patch hybrid feed antenna with corner truncation. It features a smaller lower (direct) patch and larger upper (coupled) patch which are proximity-coupled to facilitate a large bandwidth. An airgap which acts as a low-permittivity dielectric between the upper and lower substrate exists to further tune the patch coupling and increase bandwidth. The lower patch is fed directly via the inner conductor of a female SMA connector in alignment with the project requirements. 

{% figure "/assets/img/Model_Isometric.png" Isometric View of Design used for Simulation %}
{% endfigure %}

The design consists of separate PCBs for the upper and lower patches which are mechanically distanced from one another by standoffs. The lower patch is contained on a 2-layer PCB. On its top layer is the exposed lower radiating patch while the ground plane forms the bottom copper layer. A through-hole (THT) female SMA connector is mounted on the bottom side of the lower PCB. The THT SMA center conductor feeds through a non-plated through hole in the board and is soldered to the top patch. The ground pins of the SMA are shaved down and soldered to surface pads on the bottom ground plane. The fabricated prototype is shown below in Figure 8.3. 

{% figure "/assets/img/Fab_Isometric.png" Isometric View of Physical Prototype %}
{% endfigure %}

## Key Features

The key features of the design and justification for their implementation in meeting the project constraints are provided in this section:

### Mismatched Direct and Coupled Patch Sizes

Differing upper (44.8mm) and lower (33.3mm) patch sizes were selected to enhance dual-band operation and increase the overall impedance bandwidth. The main factor underlining the center frequency at which a patch antenna operates is its dimensions. Therefore, offsetting the two patch lengths from each other allowed them to target different center frequencies. In the outlined design, the upper patch 11.5mm larger to extend the range of operation to lower frequencies which helped meet the uplink frequency requirement. Oppositely, the lower patch targeted higher frequencies extending the impedance pass band over the downlink transmission frequency range. In the design, a lower return loss was favored in the downlink band to minimize reflection back to the signal generator in the CubeSat. 

### Probe Location Impedance Matching

The input impedance of the antenna was controlled by the feed location of the probe within the patch area. Feeding the patch at its center results in a very low impedance (near 0 Ω) since the electric field is weakest and current is maximum, while feeding the patch at its edge results in a large impedance (near open circuit). Additionally, changing the feed location in the x-plane versus y-plane alters the active dominant mode which can assist dual-mode behaviour to achieve circular polarization. An optimal feed location of x = -15mm and y = 2.5mm was selected (see below) to achieve an antenna input impedance of near 50Ω and to increase excitation of the TM010 mode.

{% figure "/assets/img/Fab_Top.png" Lower Patch of Physical Prototype Showing Probe Location %}
{% endfigure %}

### Large Air Gap

A large air gap acting as a low permittivity dielectric between the radiating patches was required to achieve the frequency range of operation. The airgap height controlled the electromagnetic coupling strength between the upper and lower patches. Increasing the height weakened the coupling strength and induced shallower return loss over a wider frequency range. Oppositely, decreasing the gap height and thus the coupling strength resulted in dual-band with two distinct S11 troughs or narrow-band operation in the extreme case. A very low return loss resulted in a poor axial ratio as primarily the dominant mode was activated. It was found through HFSS simulation that the optimal airgap height was 12.7mm for achieving the outlined impedance bandwidth and low axial ratio. 

### Corner Truncation

Corner truncation was applied to opposite corners of both the top and bottom patch (See below) acting as the main stimulus for dual orthogonal mode activation to achieve circular polarization. Increasing the truncated area promotes stronger dual-mode behaviour reducing the axial ratio but at the expense of decreased impedance bandwidth and poorer overall return loss. A trade off was made between axial ratio bandwidth and impedance bandwidth, with a lower return loss being prioritized over the frequency range. Through HFSS simulations it was determined that the optimal corner truncation was 20% (of the patch area) for the direct fed patch and 25% for the coupled patch. The direct fed patch showed a greater impact on the return loss when trimming the corners which is why its truncation area was scaled back compared to the top patch.

{% figure "/assets/img/Fab_Top_Patch.png" Top Board of Physical Prototype %}
{% endfigure %}

### Substrate Material

FR4 was chosen as the antenna substrate for both the upper and lower patches. In the original project constraints, Rogers 4003C substrate was specified to be used as the antenna substrate due to its lower electrical permittivity, low-loss tangent, higher efficiency, and overall greater stability for RF applications. However, as the antenna operating frequency range is relatively low in the microwave realm it was found that the antenna performed similarly with FR4 and Rogers 4003C in HFSS simulations. Therefore, FR4 was selected to decrease the overall antenna cost by a significant factor (10x) and reduce the manufacturing time.

### Mechanical Considersations

To ensure compliance with CubeSat standards and manufacturability, several mechanical design features were implemented. The top patch antenna was reshaped into a circular form with a 64 mm diameter to fit within the standard "tuna can" volume constraints, allowing for a larger air gap while respecting the maximum height of 5 mm. A through-hole female SMA connector was selected as the simplest and most cost-effective method for connecting the center pin to the top patch, avoiding the increased complexity and cost associated with blind vias or surface-mount options. To maintain electrical isolation, a non-plated through hole was used for the SMA center pin between the ground plane and radiating patch. The PCB copper surface finish was chosen as Electroless Nickel Immersion Gold (ENIG) for its superior surface flatness, corrosion resistance, and stable RF performance compared to the more common Hot Air Solder Leveling (HASL), which is less suitable for high-frequency patch antennas. Non-conductive nylon standoffs were utilized to mechanically separate the upper and lower patches without affecting the antenna radiation pattern, balancing cost and function for the prototype stage; ceramic standoffs are recommended for final space deployment. Finally, the board outline and mounting holes were precisely designed in accordance with the CubeSat mechanical constraints to ensure seamless integration.
