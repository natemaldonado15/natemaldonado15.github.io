---
layout: post
title: "Low-Cost Non-Contact Flow Measurement"
description: "Designed and validated a sub-$1,000 flowmeter concept that measures the external reaction force generated as fluid turns through a bend."
skills:
  - "SolidWorks"
  - "ANSYS Fluent"
  - "Fluid Mechanics"
  - "3D Printing"
  - "Load-Cell Testing"
  - "Experimental Validation"
main-image: /flowmeter-cad-assembly.jpg
---

> **Role:** R&D Intern, Saint-Gobain Performance Plastics  
> **Project period:** May to August 2021  
> **Target:** A practical, non-intrusive concept below $1,000 for slurry-like and challenging flows.

## What

Many industrial flowmeters are expensive, intrusive, or difficult to apply to slurries and other challenging fluids. This project evaluated a lower-cost alternative based on a direct physical principle: when a fluid changes direction through a bend, its momentum change produces a reaction force. Measure that external force and it can be correlated with flow rate.

I designed and tested a prototype that converted the momentum-balance concept into a mechanical sensing problem, then compared theory, CFD, and experimental data.

## How

### First-Principles Model

I started with a control-volume momentum balance to relate the change in fluid momentum through the bend to the external force required to restrain it. For a fixed geometry and fluid density, the expected first-order relationship was **reaction force proportional to flow rate squared**.

### Mechanical Design and Prototype Build

The prototype used a 3D-printed bend assembly mounted in a frame with external load-cell sensing. Key design decisions centered on:

- Directing the bend reaction through the sensor rather than through a friction-dominated load path
- Maintaining repeatable seals and alignment
- Keeping the concept inexpensive and accessible for rapid iteration
- Allowing comparison with a reference turbine flowmeter

<img src="/_projects/02-low-cost-flowmeter/flowmeter-cad-assembly.jpg" alt="Annotated CAD and drawing of the flowmeter assembly" width="100%">

*Annotated CAD and drawing of the prototype flow path, sensor location, seals, and inlet/outlet configuration.*

### CFD and Test Planning

I used ANSYS Fluent to estimate bend reaction force and pressure-loss behavior before testing. The analysis provided expected load magnitudes, helped frame the experimental comparison, and exposed design factors that could reduce sensitivity.

<img src="/_projects/02-low-cost-flowmeter/flowmeter-prototype.jpg" alt="Flowmeter test setup with water tank, pump, turbine flowmeter, and prototype assembly" width="100%">

*Bench setup used to compare the prototype response with a reference turbine flowmeter.*

## Results

- Demonstrated a measurable force response for water and slurry-like test fluids.
- Observed approximately **8.5% error** for the reported measured-to-expected comparison.
- Confirmed the expected linear trend between reaction force and flow rate squared.
- Identified the dominant low-flow limitations: seal friction, pressure loss, and force-sensor creep.

<img src="/_projects/02-low-cost-flowmeter/flowmeter-test-rig.jpg" alt="Overhead view of the prototype load-cell fixture" width="100%">

*Overhead view of the load-cell fixture used to transfer the bend reaction into the sensor.*

## Validation and Engineering Lessons

| Validation method | Evidence | Engineering takeaway |
| --- | --- | --- |
| Momentum-balance calculation | Predicted force-versus-flow-squared trend | Grounded the sensor concept in fluid mechanics |
| ANSYS Fluent analysis | Estimated reaction force and pressure losses | Identified expected signal size and loss mechanisms before extensive testing |
| Prototype testing | Measured load-cell response for test fluids | Demonstrated that the physical assembly produced a usable signal |
| Error comparison | Approximate 8.5% reported error | Quantified performance rather than relying on a qualitative claim |

The project taught a practical point that applies to much more than flow measurement: a sound physical principle is not enough. The mechanical load path, friction sources, sensor behavior, and test-fixture stiffness determine whether the underlying physics reaches the sensor cleanly.

## Public Scope

The flowmeter project is suitable for public discussion at the design and validation level. Detailed drawings, CFD files, raw data, and source calculations should be published only after review for proprietary information.
