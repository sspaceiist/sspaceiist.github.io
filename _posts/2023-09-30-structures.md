---
layout: post
title: "Structures"
categories: induction
author: Abhinas Meena
---

[PDF link](https://drive.google.com/file/d/1zvlHo8aX637TwcfnUJRWnP-jHJfKNHI9/view?usp=drive_link)

## Table Of Content
1. [Introduction](#introduction)
1. [Classification of Satellite based on size](#classification-of-satellites-based-on-size)
1. [Types of Mission](#types-of-mission)
1. [CubeSat Structure Design and Modelling](#cubesat-structure-design-and-modelling)
1. [Launch Environment and analysis](#launch-environment-and-analysis)
1. [Integration Plan](#integration-plan)
1. [Development Plan](#development-plan)
1. [P-pod Deployer](#p-podpoly-picosatellite-orbital-deployer)

## Introduction 
As for all space missions, including cubesats, the structure is one of the main satellite subsystems. In principle, the purpose of the structural subsystem is to provide a simple and robust structure that shall survive launch loads and provide a suitable environment for the operation of all subsystems.  

Furthermore, the structure mechanically supports all other spacecraft subsystems, attaches the spacecraft to the launch vehicle, and provides for ordnance-activated separation. Generally, structural design shall aim for simple load paths, simplified interfaces, and easy integration.  

The design of space structural systems is dictated by mass, stiffness, and strength requirements. 

## CubeSat
A CubeSat is a small satellite composed of one or more 10cm x 10cm x ~10cm cubes.   Sometimes referred to as a “U” as in unit, the cubes can be combined in configurations of 2U, 3U, 6U, and more.  

CubeSats provide many advantages that larger satellites cannot offer. They are relatively inexpensive and can be fabricated much faster. Small-scale projects that require a fast time line from conception up to completion are perfect for CubeSats. 

### classification of satellites based on size


| Category | Weight | Examples |
| - | - | - |
|Large | 1000Kg and more | Chandrayaan-3  |
|Medium |500-1000Kg | Jason-3 |
|Mini |100-500Kg |IMS-2 |
|Macro |10-100Kg |INS-2TD |
|Nano |1-10Kg |INSPIREsat-1 |
|Pico |Less Than 1 kg and up to 0.1kg ||
|Fenito |Less than 0.1Kg ||


The small 1U CubeSat has a maximum  ![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.007.jpeg)mass of 1.33 kg, and falls in the Nano- satellite category. The 3U CubeSat is  essentially three 1U CubeSats put  together, and is considered a Nano- satellite due to its mass of 4 kg. 6U up  to 27U CubeSat form factors are  microsatellites (masses range from  12.0 kg to 54.0 kg).  

## Types of mission
CubeSats can be broken up into 4 classes: E-class, C-class, S-class, and T-class. E-class satellites are educational satellites to train students, C-class satellites provide communication services, S-class satellites are science satellites that collect data, and T-class satellites test new industry technologies, so simply we can divide the mission into following  

- Technology Demonstration 
- Scientific Research 
- Educational Project 
- Commercial/communication services

### Standards for CubeSat Family
- 1U (size of 10 cm x 10 cm x 11.35 cm) 
- 2U (size of 10 cm x 10 cm x 22.70 cm) 
- 6U (size of 20 cm x 10 cm x 34.05 cm) 
- 12U (size of 20 cm x 20 cm x 34.05 cm) 

## Cubesat structure Design and Modelling
### 1. Cubesat structure design
The design process of the structure is an iterative process as is the case with the other subsystems. The process accounts for the upcoming necessary changes evolving from the interaction between the subsystems.  

For initial primary structure design we use 3D design/simulation software like SolidWorks, Fusion 360, Inventor and ABAQUS. Assembly of design/required simulations\analysis and tolerance also done in these Software. 

All components/subsystems (including PCB’s {Printed circuit board}, Solar panels which placed on external faces) are designed by Using CAD software. 

After completing the components design we doing an assembly of all components for making structure design, before doing assembly we make an assembly Plan (a processor of doing assembly means it is  ![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.013.png)decide which part will be  attached first and which later).  After completing structure, do  simulation/analysis.  

Fig01: Exploded view of the Slot- based 3U structural model 

![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.014.png) ![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.015.png)

Fig 02. CAD Model of 1U and 2U satellites with primary structure and PCB’s  

### 1. CubeSat Structure Materials  

Materials is very important aspect of a satellite design because the design of space structural systems is dictated by mass, stiffness, and strength requirements. On the one hand, stiffness is required to ensure the survivability of the instrumentation; on the other hand, by reducing the weight, it is possible to increase the payload, which extends the mission goals and also reduces the launch cost. The structural and mechanical parts of a satellite generally represent a large percentage of its mass, and therefore, it is important to choose the proper material which have minimum mass and good stiffness and strength which survive the launch conditions. 

Aluminum alloy 7075 (T6), one of the most commonly used aluminium alloys for such application and second one is the Aluminum alloy 6061(T6).  

All bolts (fasteners) used for the connection of different components considered to be made of stainless steel. 

Nowadays composite materials also used as structural materials because we know mass is also very important aspect of a structure so these composite materials have less mass comparatively Metal alloys ( Generally Al alloy). 

**mass budget** – The principle of a mass budget is a method of bookkeeping: each subsystem is designed according to the goals set by the mass budget so that the mass can be monitored during the spacecraft project. In order to do this, a detailed list is used to record the mass of all the components of the spacecraft, that is called Mass budget 

and sum of all components/PCB’s mass is defined as Total Mass of a satellite, this mass must be within the maximum mass limit of satellite. 

## Launch Environment and analysis

A typical cubesat device will be launched on a variety of launching rockets. To qualify for acceptance, the cubesat structure must not fail under certain static and dynamic loading that will be calculated based on the launching conditions. 

A modal analysis, a quasi-static analysis, and the random vibration (PSD) analysis In addition, considering the thermal loads during cubesat operation in low Earth orbit, a thermal analysis is also conducted. 

- **Modal Analysis** The first step during a dynamic analysis is the determination of natural frequencies (eigen-frequencies) and mode shapes of structure, considering zero damping. The results of this analysis characterize the dynamic behaviour of the structure and can show how the structure will respond under dynamic loads. The most important modal characteristic of the cubesat or space structure, is the natural frequency threshold—meaning that the first natural frequency of the structure must be above a specific value, which usually is determined by the launch vehicle. The typical range for such missions is between 50 and 90 Hz. 
- **Quasi static analysis** The quasi-static event is loads that are independent of time or vary slowly, so that the dynamic response of the structure is not significant. In this base, for design purposes, the quasi-static loads are normally calculated by combining both static and dynamic load contributions.
- **Vibrations** One of the most severe loads for the integrity of the cubesat structure (both internal and external) is the random vibrations coming from the spacecraft launch. 
The purpose of random vibration analysis is the verification of strength and structural integrity of the satellite by introducing random vibrations through the mechanical interface. This kind of analysis is best suited for subsystem/ equipment-level tests and serves for the verification of the satellite structure.

## Integration Plan
![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.025.jpeg)

The mechanical and electrical systems of CubeSats can be integrated in a very dense manner to a limited mechanical envelope. 

## Development Plan
- The method by which Small cubeSats are deployed into orbit is a critical part of the launch process. The choice of deployment method depends on the form factor of the satellite. 
- Various types of deployable can be there in a satellite such as antenna, Solar panel, boom etc. 

## P-POD(Poly-Picosatellite Orbital deployer)
The Poly Picosatellite Orbital Deployer (P-POD) is Cal Poly’s standardized CubeSat deployment system. It is capable of carrying three standard (3U) CubeSats and serves as the interface between the CubeSats and Launch Vehicle. The P-POD is a rectangular box with a door and a spring mechanism.  

Once the release mechanism of the P-POD is actuated by a deployment signal sent from the LV, a set of torsion springs at the door hinge force the door open and the CubeSats are deployed by the main spring gliding on its rails and the P-PODs rails (P-POD rails are shown in Figure 3). The P-POD is made up of anodized aluminum. CubeSats slide along a series of rails during ejection into orbit. 

Fig.04 Inserting the small satellite into P-POD ![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.036.png)![](Aspose.Words.036c8705-50d4-4043-a82a-6758a33d5015.037.png)

## Reference
1. Article on  Development of Innovative CubeSat Platform for Mass Production by Eyoas Ergetu Areda , Jose Rodrigo Cordova-Alarcon, Hirokazu Masui and Mengu Cho.
1. Research Article on Design, Analysis, Optimization, Manufacturing, and Testing of a 2U Cubesa by Andreas Ampatzoglou and Vassilis Kostopoulos.

