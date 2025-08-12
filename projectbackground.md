---
layout: page
title: Project Background
subtitle: Introduction
---

In response to Canada’s Space Low Earth Orbit Architecture initiative (SpaceLEO), the University of Victoria Center for Aerospace Research (CfAR) has proposed the implementation and development of PolarLink a single CubeSat with the purpose of aiding research in the artic region. PolarLink requires the development of a communication system consisting of a radio transceiver and one or more patch antennas. Our team has been tasked with the development and initial testing of an S-band patch antenna to facilitate the communication of the CubeSAT with multiple domestic and/or international commercial constellations, as well as several remote terminals across northern Canada. The patch antenna is to transmit and receive signals within the 2-4 GHz frequency range, also known as the S-band. 

![Polar Link Concept](/assets/img/PolarLink_Concept.png)

## Motivation

Designing an S-band patch antenna for a CubeSat presents a compelling opportunity to apply theoretical knowledge in electromagnetics, RF design, and space systems to a practical, real-world engineering challenge. CubeSats are rapidly transforming space exploration and communication due to their affordability and modularity, and reliable antenna systems are critical to their performance. This project offers the chance to contribute to the advancement of small satellite technology by addressing the unique constraints of space communication such as size, weight, and efficiency, while gaining hands-on experience with modern design tools like HFSS and Altium as well as access to the specialized equipment and tools at CfAR. The interdisciplinary nature of the work, bridging PCB design, RF simulation, and space application, makes it both intellectually rewarding and highly relevant to current industry needs.

Our proposed patch antenna seeks to meet the functionality of current market satellite communication systems at a fraction of the cost, allowing for the development of CubeSats to be further accessible to the wider public. This facilitates the democratization of space by allowing the opportunity for new players to utilize the final frontier instead of being restricted by costs.

## Project Goals

The S band patch antenna is to meet the electrical and mechanical success criteria outlined in the project’s requirements in the following table. The results of our project will be utilized by CfAR to direct future development of PolarLink’s communication system. 

### Electrical Specifications

| **ID**  | **Shall Statement**                                                                                                                                                                  | **Method of Verification** | **Success Criteria**                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|----------------------------------------------------------------------------|
| EE-1    | The antenna shall be designed for operation in the 2025–2110 MHz and 2200–2290 MHz frequency range.                                                                                  | Test                       | Requirement EE-5 is verified.                                               |
| EE-2    | The antenna shall be a passive rectangular or circular patch antenna using printed circuit board (PCB) technology on Rogers 4003C or FR-4 substrate, or an array comprised of such antenna elements. | Design Review              | Review of design documents shows that the requirement is satisfied.        |
| EE-3    | The antenna shall be designed to have a nominal input impedance of 50 Ohms over its frequency range of operation in EE-I.                                                           | Design Review              | Review of design documents shows that the requirement is satisfied.        |
| EE-4    | The antenna electrical interface shall be a single female, SMA type connector located on the side opposite to the radiating element.                                                | Design Review              | Review of design documents shows that the requirement is satisfied.        |
| EE-5    | The antenna shall have a VSWR of 1.92:1 or better over its frequency range of operation in EE-I, as measured at the SMA connector.                                                  | Test                       | Measurement with a calibrated VNA indicates the desired VSWR at the connector. |
| EE-6    | The antenna shall be able to handle at least 5 W of RF power.                                                                                                                        | Analysis                   | Theoretical analysis or simulations justify that desired power level is ok (e.g. no excessive dielectric heating, arcing). |
| EE-7    | The antenna half-power beamwidth (HPBW) shall be at least 60 degrees.                                                                                                                | Test                       | Anechoic chamber measurement with calibrated VNA support the desired HPBW. |
| EE-8    | The antenna shall be circularly polarized, with the direction of circularity being either left hand circular polarization (LHCP) or right hand circular polarization (RHCP).      | Test                       | Review of design documents shows that the requirement is satisfied.        |
| EE-9    | Prior to production it shall be possible to configure the antenna for LHCP or RHCP, using the same main printed circuit board element.                                            | Design Review              | Review of design documents shows that the requirement is satisfied.        |
| EE-10   | The antenna shall have at least 6 dBi gain along its direction of maximum radiation, which shall be aligned with the boresight of the antenna.                                      | Test                       | Anechoic chamber                                                           |
| EE-11   | The nominal axial ratio of the antenna within its half power beamwidth (HPWB) shall be at most 3 dB.                                                                                  | Analysis                   | Simulations of the axial ratio indicate that the requirement is met.       |
| EE-12   | The efficiency of the antenna shall be at least 90% or better over its frequency range of operation in EE-I.                                                                         | Test                       | Analysis based on data from calibrated VNA supports the desired efficiency. |

### Mechanical Specifications

| **ID**  | **Shall Statement**                                                                                                                                                                  | **Method of Verification** | **Success Criteria**                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|----------------------------------------------------------------------------|
| ME-1    | The antenna shall be compatible with the Mechanical Interface Control Document below.                                                                                                | Fit Check                  | A 3D STEP model exported from Altium passes a SolidWorks fit check.        |
| ME-2    | The antenna shall comply with NASA guidelines for selecting all non-metallic materials based on available outgassing data. The antenna shall not utilize any non-metallic materials with a Total Mass Loss (TML) greater than 1.0 percent or a Collected Volatile Condensable Material (CVCM) value greater than 0.1 percent. | BOM Review                 | Review of bill of materials (BOM) shows that there are no parts of concern. |
| ME-3    | The antenna weight shall not exceed 100 grams.                                                                                                                                      | Test                       | Weighing of antenna in its final configuration shows that requirement is met. |
| ME-4    | The antenna shall comply with the CubeSat standard.                                                                                                                                 | Design Review              | Review of design documents shows that the requirement is satisfied.        |

![Mechanical Constraints](/assets/img/Mechanical_Constraints.png)