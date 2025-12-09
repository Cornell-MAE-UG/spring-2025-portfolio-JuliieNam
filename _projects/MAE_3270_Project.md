---
layout: project
title: Torque Wrench Design Project
description: MAE 3270 Final Project
technologies: [Autodesk Fusion, ANSYS, Granta]
image: /assets/images/3270 Torque Wrench Picture.png
---

For my materials class at Cornell, my final project was to design a non-ratcheting ⅜ drive torque wrench. The goal was to maximize the voltage output of the wrench (mV/V) at the rated torque. The wrench must sustain a fully reversed torque of T = 600 in-lbf for 10^6 cycles. The following design requirements had to be met:
- Attain at least 1.0 mV/V output at the rated torque of 600 in-lbf
- Safety factor of X_o = 4 for yield or brittle failure
- Safety factor of X_k = 2 for crack growth from an assumed crack of depth of 0.04 inches (1 mm) 
- Fatigue stress safety factor of X_s = 1.5
- Material must be a steel, aluminum, or titanium alloy

Images of the CAD model are shown below. 
![CAD Image 1]({{ "/assets/images/3270_Torque_Wrench_CAD1.png" | relative_url }}){: style="width: 600px"}

![CAD Image 2]({{ "/assets/images/3270_Torque_Wrench_CAD2.png" | relative_url }}){: style="width: 600px"}

The key dimensions of my design are:
L (distance from center of drive to where load is applied) = 20 inches
h (width of wrench handle) = 0.6 inches
b (thickness of wrench handle) = 0.25 inches
c (distance from center of drive to center of strain gauge) = 1.

The boundary condition used in this project was adding clamped conditions to the drive (meaning that the displacement in the x, y, and z directions was zero). Force was applied at the other end of the wrench in the x direction with a magnitude of M/L = 30 lbf. Photos are shown below of the boundary condition and force, respectively.
![Boundary Condition]({{ "/assets/images/3270_Torque_Wrench_BC.png" | relative_url }}){: style="width: 600px"}

![Force Applied]({{ "/assets/images/3270_Torque_Wrench_Force.png" | relative_url }}){: style="width: 600px"}

The material that I used was AISI 4340. This material was chosen because the goal here is to maximize the strain to get the highest output possible. So, we concluded that this can be achieved by choosing a material that maximizes yield strength and fracture toughness. Below is a fracture toughness vs. yield strength for alloys using Granta. The white oval on the graph is where AISI 4340 lies:
![Material]({{ "/assets/images/3270_Torque_Wrench_Material.png" | relative_url }}){: style="width: 600px"}

Here are the relevant mechanical properties of AISI 4340 that I used for my analysis:  
- Young’s Modulus: 29 x 10^6 psi
- Poisson’s ratio: 0.32
- Yield strength: 217 ksi
- Fracture toughness: 75 ksi*in^1/2
- Fatigue strength: 90 ksi

Normal strain contours (in the strain gauge direction) from FEM:
![Strain contour]({{ "/assets/images/3270_Torque_Wrench_Strain.png" | relative_url }}){: style="width: 600px"}

Contour plot of maximum principal stress:
![Maximum principal stress contour]({{ "/assets/images/3270_Torque_Wrench_MaxPrincipalStress.png" | relative_url }}){: style="width: 600px"}

Maximum normal stress is around 64151 psi. However, on the handle according to the beam theory, it is around 39044 psi.
![Max normal stress]({{ "/assets/images/3270_Torque_Wrench_Stress.png" | relative_url }}){: style="width: 600px"}

Load Point Deflection around 0.67334 inches
![Deflection]({{ "/assets/images/3270_Torque_Wrench_Deformation.png" | relative_url }}){: style="width: 600px"}

Strain at the strain gauge locations is around 1310.3 microstrain.
![Strain Probe]({{ "/assets/images/3270_Torque_Wrench_StrainProbe.png" | relative_url }}){: style="width: 600px"}

Torque wrench sensitivity using the half bridge: 1.3101 mV/V

Output goal is met! Now let's calculate the safety factors for yield, crack, and fatigue stress. I will be using the stress value on the handle according to beam theory, which is around 39044 psi.  
- Yield safety factor is around 5.558 > 4  
- Crack safety factor is around 4.723 > 2  
- Fatigue stress safety factor is around 2.305 > 1.5
Safety factor requirements are met!

Strain gauge selected:
SGD-3/350-LY13 from DWYEROMEGA. More information about the strain gauge is linked here: https://assets.dwyeromega.com/pdf/test-and-measurement-equipment/strain-gauges/SGD_LINEAR1-AXIS.pdf  
Dimensions are 0.157 in x 0.276 in, which would fit on the handle!  

As a little bonus, below are the MATLAB hand calculations that were used. The normal stress calculated by MATLAB is around 40,000 psi, which is very close to the beam theory ANSYS analysis value. The screenshots include the equations that I used when calculating my safety factors. 
