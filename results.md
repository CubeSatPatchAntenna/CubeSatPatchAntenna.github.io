---
layout: page
title: Results
subtitle: Testing & Validation
---
The performance of the prototype was tested either using HFSS simulations, or through use of a VNA in an anechoic chamber. 

<p align="center">
  <img src="/assets/img/Anechoic_Chamber.png" alt="Anechoic Chamber Test Setup" />
</p>

The table below summarizes and compares these results to the specifications found in the project background. It should be noted that all results shown are given for the specified bandwidth of 2025 – 2290 MHz. Further clarification for performance outside the specified band is given in the notes section below.

| ID     | Parameter                 | Result                                       | Test Method                   | Constraint Met? |
|--------|---------------------------|-----------------------------------------------|--------------------------------|-----------------|
| EE-<br>1   | Bandwidth                  | 1.9229 – 2.1786 GHz                           | VNA                            | No¹             |
| EE-<br>2   | Substrate Material         | FR-4                                          | N/A                            | Yes             |
| EE-<br>3   | Input Impedance            | Average: 23.3Ω<br>Spread: 20.54 ±             | VNA                            | No²             |
| EE-<br>4   | Connector Type             | Female SMA                                    | N/A                            | Yes             |
| EE-<br>5   | VSWR                       | 5.51 or better                                | VNA                            | No³             |
| EE-<br>6   | Power                      |                                               |                                |                 |
| EE-<br>7   | HPBW                       | Average: 83.6°                                | VNA & Anechoic Chamber         | Yes⁴            |
| EE-<br>8   | Polarization               | Prototype: LHCP                               | HFSS                           | Yes             |
| EE-<br>9   | Configurable Polarization  | PCB was not made to be configurable           | N/A                            | No⁵             |
| EE-<br>10  | Gain                       | 6.31 dBi                                      | VNA & Anechoic Chamber         | Yes⁶            |
| EE-<br>11  | Axial Ratio                | Average: 4.58 dB                              | VNA & Anechoic Chamber         | No⁷             |
| EE-<br>12  | Efficiency                 | 52%                                           | VNA                            | No⁸             |
| ME-<br>1   | Size                       | Antenna meets mechanical constraints          | 3D Model Export                | Yes             |
| ME-<br>2   | Material Requirements      | Antenna contains nylon which does not meet outgassing requirements | N/A              | No⁹             |
| ME-<br>3   | Weight                     | 46 g                                          | Scale                          | Yes             |

| Ref # | Notes                                                                                                                                                                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Bandwidth has been shifted down but is 256 MHz wide.                                                                                                                                                                                          |
| 2     | Across the measured bandwidth, the impedance is an average of 28.6 Ohm or a spread of 27.47 ± 16.66 Ohm, which is closer to the specifications.                                                                                              |
| 3     | The measured bandwidth from EE-1 was defined by the −10 dB crossings of the return loss. This corresponds to a VSWR of 1.92 or better within the band.                                                                                        |
| 4     | Estimated using gain measurements instead of directivity. As such, this is a conservative estimate.                                                                              |
| 5     | While the actual PCB manufactured is not configurable for LHCP and RHCP, the same design can achieve this requirement by adding another pad for SMA mounting and rotating the position of the SMA connector by 90°.                           |
| 6     | Within the specified band, the gain was as high as 7.8 dBi and as low as 4.8 dBi. For the measured bandwidth, the maximum and minimum gain was 5.87 dBi and 4.63 dBi, respectively.                                                           |
| 7     | The axial ratio matched the results of the HFSS simulation at the corner frequencies. Matching the results to a curve like that found from the simulations, the average reduces to 3.32 dB. This axial ratio cannot be claimed in full confidence without extensive testing. |
| 8     | Efficiency was estimated using the measured S11 parameter. Within the measured band, the efficiency was 90%.                                                                                                                                   |
| 9     | The prototype used nylon for cost savings. For deployment in space, ceramic should be used.                                                                                                                                                     |

### Return Loss and VSWR Plots of Physical Prototype ###

![Return Loss of Prototype](/assets/img/Return_Loss.png)

### Real and Imaginary Parts of Input Impedance of Physical Prototype ###

![Input Impedance of Prototype](/assets/img/Input_Impedance.png)

### Return Loss & Magnitude of Input Impedance of Physical Prototype ###

![Magnitude Impedance of Prototype](/assets/img/Magnitude_Impedance.png)

### Polar Gain Plots of Prototype ###
![Polar Gain Plots of Prototype](/assets/img/Polar_Gain_Plots.png)

### Weight of Prototype ###

<p align="center">
  <img src="/assets/img/Weight.png" alt="Weight of Prototype" />
</p>

