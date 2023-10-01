---
layout: post
title: "Propulsion Subsystem"
categories: induction
author: Malavika R S
---

[PDF link](https://drive.google.com/file/d/1RdKroRezY9S3izZB88bTlXfW0JMuRFDK/view?usp=drive_link)

## Table of Content
1. [Introduction](#introduction)
1. [Basic aspects to be considered](#basic-aspects-to-be-considered-for-propulsion-system-design)
1. [Requirements and constraints](#requirements-and-constraints)
1. [Types of propulsion system for cubesats](#types-of-propulsion-system-for-cubesats)
1. [General calculation Procedure](#general-calculation-procedure-for-propulsion-systems)
- [Analytics Approach](#1-analytical-approach)
- [Computational Approach](#2-computational-approach)
1. [References](#references)

## Introduction
**Thrust** is the reaction force which accelerates the spacecraft independent of any other external force in a specific direction.

![](Aspose.Words.cdb27b5a-33f6-4f0c-82b1-fb589a3a2f28.001.jpeg)

- Thrust is achieved by expelling mass in the direction opposite to the required acceleration direction. The mass should be ejected at a velocity appropriate to provide the required thrust.
- The rocket equation is used to calculate the required mass for a given delta-v (change in velocity). The same equation is used for satellites.

![](Aspose.Words.cdb27b5a-33f6-4f0c-82b1-fb589a3a2f28.002.png)

## Basic aspects to be considered for propulsion system design

- Propulsion system mainly depends on the utility and aim of the mission.
1. For example for earth orbiting satellites, the propulsion system must serve its purpose to maintain the orbit or for station keeping or for orbit transfer or orbit corrections.
1. For interplanetary missions, the propulsion system plays an extensive role,with additional complications and increased delta-v/thrust requirements which implies an increased amount of propellant required.
- As we are specifically designing for a small-satellite, mainly we will be dwelling into compatible propulsion systems for small-satellites.
- On what basis can a propulsion system be chosen from a variety of systems available? Efficiency is the key component among a few other factors which will be discussed later.
- Do we have anything to measure that efficiency? Specific impulse. It is the change in momentum (impulse) generated per unit mass of propellant consumed.
- We can use this parameter to compare and select the propellant and propulsion system.
- But actually do we need something else to decide? Here are some approximate specific impulse values for some propulsion systems.

Cold gas:150s

Electric:1000s

Which is better? We may think it is electric. But actually it depends on the exit mass flow rate and the requirement of the propulsion system. Because there are electric propulsion systems which have very high isp systems but still they produce very low thrust due to the mass flow rate (ions are thrown out, so the mass flow rate is very low) which can’t be used for high thrust demanding delta-v maneuvers which usually happen in short burn times.

Similarly, cold gas thrusters cannot be used for very long burn time maneuvers.

- Higher the exit mass flow rate, higher the thrust. It can be achieved by appropriate nozzle design.[^1]
- Propulsion system design highly depends on the type of propulsion system and its working principle, so the designer should thoroughly understand the working principle.[^2]

## Requirements and constraints:

- Delta-V Requirements: The mission's delta-v (change in velocity) requirements dictate the propulsion system's performance needs. High Isp is valuable when a mission demands significant velocity changes, but low-thrust, high-Isp systems may not be suitable for rapid changes.
- Power Availability: The power source available for the propulsion system can limit or expand the options. Electric propulsion systems, for example, require electrical power, which may come from solar panels or nuclear generators.
- Mass and Volume Constraints: The size and mass of the propulsion system must fit within the spacecraft's available space and weight budget. Smaller spacecraft like CubeSats may have more stringent constraints.
- Operational Environment: Consideration of the operational environment is essential. Spacecraft operating in Earth orbit may have different propulsion requirements compared to deep-space missions.
- Reliability and Redundancy: The reliability of the propulsion system is critical, especially for long-duration missions. Redundancy (backup systems) may be necessary to ensure mission success.
- Propellant Choice: The type of propellant used can impact Isp, thrust, and other factors. Different missions may require specific propellant characteristics, such as storability or non-toxicity.
- Cost and Budget: The budget for the mission can influence propulsion system choices. Some systems may be more cost-effective than others, but cost should not compromise mission success.

## Types of propulsion system (For cubesats):

- So based on the mission requirements,the feasible system can be chosen from the different types of systems.

Some of the common propulsion system which are used for cubesat are as below:

1. **Cold Gas Thrusters**:Cold gas propulsion systems use compressed gas, such as nitrogen or xenon, to generate thrust. They are relatively simple and reliable, making them suitable for attitude control, orbit maintenance, or deorbiting maneuvers. Cold gas thrusters are commonly used in CubeSats operating in low Earth orbit (LEO).
1. **Electric Propulsion**: Electric propulsion systems, like Hall Effect Thrusters or electrospray thrusters, provide higher efficiency than cold gas thrusters. They are often chosen for CubeSats with specific mission requirements, such as interplanetary missions or orbit raising to higher altitudes within Earth's magnetosphere.
1. **Pulsed Plasma Thrusters (PPT)**: PPTs use electrical discharges to create and expel plasma, producing thrust. They are suitable for attitude control and small orbit adjustments and have been used in Earth-orbiting CubeSats.
1. **Resistojet Thrusters**: Resistojet systems use resistive heating to vaporize a propellant, typically water, and expel it to generate thrust. They are used for orbit adjustments, altitude control, and deorbiting maneuvers.
1. **Solar Sails**: CubeSats equipped with solar sails have been deployed for missions in Earth's orbit. Solar sails use sunlight pressure to generate thrust and are typically used for missions with a focus on demonstrating solar sail technology

## General calculation procedure for propulsion systems:

### 1. Analytical approach

- The following method is mainly used in combustion rocket engines, here we use the same method for some small-satellite propulsion systems like cold gas thrusters.
- Determine thrust and period of burn(Time duration of producing constant thrust) using appropriate formulas according to the orbital plan.
- Choose appropriate gas as the fuel. Consider Isp and compatibility of the fuel while choosing.
- Calculate total mass of propellent using rocket equation

![](Aspose.Words.cdb27b5a-33f6-4f0c-82b1-fb589a3a2f28.003.png)

![](Aspose.Words.cdb27b5a-33f6-4f0c-82b1-fb589a3a2f28.004.png)

Where, mdot is the mass flow rate (kg/s).

F is the desired thrust (N).

Isp is the specific impulse (s).

g is the standard gravitational acceleration (Note g changes in deep space missions and should be calculated appropriately.Near earth approximately 9.8). 

#### To find the exit velocity,

1. Calculate mass at each thrust and delta v value assuming, initial mass = mass of total propellant + structural mass.
1. With the mass of propellant required at a specific burn,mass flow rate can be obtained by multiplying it with the period of burn.

#### To design the system,

1. Design a nozzle according to the exit velocity (Find the area ratio)
1. Using the ideal gas equation, find the pressure assume a fixed volume and temperature
1. With appropriate iteration,desired volume,temperature and pressure can be estimated.
1. Try changing the assumed volume and temperature to get the most compact and reliable thrust chamber.
- More complex propulsion systems like ion thrusters and pulsed plasma thrusters require rigorous calculations as we deal with excited particles instead of gasses. In that case, it is better to go with computational methods to avoid complexity.

### 2. Computational approach

- The above analytical calculations can be done using computation too. But mainly computation is used for propulsion systems with complex working mechanisms such as ion thrusters, pulsed plasma thrusters, etc.
- Softwares like GMAT are used to predict the parameters required for propulsion system design.
- GMAT lets us give inputs about the following
  1. Central body properties (Earth if our small satellite is set to orbit around earth).
  1. Spacecraft properties.
  1. Propulsion system properties (Isp, constant or impulse thrust, thrust value, thrust direction, etc)
  1. Initial position (using the Orbital elements).
  1. Maneuvers (delta-v, thrust direction, point of maneuver on the orbit and maneuver type)
- GMAT needs propulsion system properties as input to run the simulation. But we don't know them, in fact we need them.
- So, we have to input guessed propulsion system properties and run the simulation.
- Comparing the simulated results (trajectory) and expected results, we refine the properties such that we achieve the mission requirements as well as obtain the propulsion system properties to proceed with propulsion system design.

## References

[^1]: [https://www.ias.ac.in/article/fulltext/sadh/046/0076 ](https://www.ias.ac.in/article/fulltext/sadh/046/0076)The above article will be helpful for nozzle design.
[^2]: [https://s3vi.ndc.nasa.gov/ssri-kb/static/resources/KrejciLozano_PropSamllSat_ProcIEEE2018presub. pdf](https://s3vi.ndc.nasa.gov/ssri-kb/static/resources/KrejciLozano_PropSamllSat_ProcIEEE2018presub.pdf)

    The working principles and schematics of types of propulsion systems used in small satellites are given in the above article.
