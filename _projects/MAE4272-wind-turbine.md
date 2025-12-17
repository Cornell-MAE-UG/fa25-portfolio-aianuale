---
layout: project
title: Wind Turbine Blade Design
description: MAE4272 Fluids and Heat Transfer Lab - Design Project
technologies: [Wind Tunnel, MATLAB, Autodesk Inventor]
image: /assets/images/windTurbineTunnel.png
---

## Project Overview
These wind turbine blades were developed in a group of 4 students for the semester-long design project in MAE4272 Fluids and Heat Transfer Lab. We were tasked with designing, testing, and characterizing performance of blades for a small-scale wind turbine. The goal of the turbine is to maximize power output across wind conditions at a fixed rotational rate. The deliverables include a full CAD model, a description of operating conditions, testing protocol, performance analysis, and a final written report.

The provided project scope included the following constraints and conditions:

* Maximum blade chord width and length dimensions
* Maximum operational rotation rate
* Weibull probability distribution of environmental wind velocity
* Maximum turbine torque and RPM for the testing apparatus


## Design Process
Our design focused on optimizing the blades for the average operating condition, determined by the most probable wind velocity from the given Weibull distribution and a rotation rate in the middle of the range defined by the problem statement. We hypothesized that optimizing the blades for the greatest lift-to-drag ratio at all points along the span will maximize power output. As such, we selected the NACA 4412 airfoil with a high C<sub>L</sub>/C<sub>D</sub> at its optimal angle of attack (AOA) as our blade cross section. A literature review informed blade taper profiles. 

Our design was based on simplified blade element momentum theory, which discretizes the blade into a finite number of sections. Using the design rotation rate, average wind speed, and target AOA for max lift-to-drag, we established a discrete function of optimal pitch ("twist") as a function of distance from the hub.
![Blade CAD]({{ "assets/images/bladeCAD.png" | relative_url }}){: width="60%"} ![Blade CAD Top View]({{ "assets/images/bladeCADTop.png" | relative_url }}){: width="35%"}
With blade geometry now fixed, we then varied wind speed and rotation rate to calculate three profiles: power, torque, and bending moment. This allowed us to predict performance across operating conditions, design a testing protocol within the limits of the lab apparatus, and demonstrate our blade's ability to withstand predicted loads. 

![Blade Design Space]({{"assets/images/bladeDesignSpace.png" | relative_url }}){: width="100%"}


## Testing Summary 
Our testing protocol aimed to classify performance for a variety of wind conditions. To do this, we assembled our 3D printed blades into the wind tunnel test assembly, equipped with pitot tube velocity sensors, rotation rate encoders, and a magnetic particle torque brake. We generated power curves (power output vs rotation rate data) for multiple wind speeds within the given probability distribution. For each wind speed, we started data collection at or near the turbine's free spin rotation rate (no power generation), and increased the magnetic particle brake load incrementally to lower rotation rate and increase torque. Our data processing derived power from rotation rate and torque readings and resulted in the power curves below.

![Power Curves]({{ "assets/images/powerCurves.png" | relative_url }}){: width="100%"}

The results of our testing demostrated an initial overprediction of power output, although our turbine's ability to produce ~1-2W is quite successful considering its 6" blade length. Additionally, our ideal operating rotation rate is around 1400 RPM, which is higher than our intended value of 1000 RPM. At highly probable wind speeds, it collects ~20% of incident wind power, as opposed to our initial assumed value of ~33%. 

## My Contribution
My contribution to the group project was mainly in the form of Matlab scripts to generate the blade profile and predict performance. I also contributed to the development and implementation of the experiment protocol, as well as figure generation and data analysis.


