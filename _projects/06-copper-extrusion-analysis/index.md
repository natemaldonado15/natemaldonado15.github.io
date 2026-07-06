---
layout: post
title: "2D Axisymmetric Copper Extrusion Analysis"
description: "Modeled copper wire extrusion in Nastran SOL 402 to examine stress and plastic deformation, then compared the response with hand-calculation expectations."
skills:
  - "Nastran SOL 402"
  - "Nonlinear FEA"
  - "Axisymmetric Modeling"
  - "Plasticity"
  - "Manufacturing Analysis"
main-image: /copper-extrusion-plastic-strain.png
---

> **Role:** Mechanical Engineering Student  
> **Project type:** Academic nonlinear FEA project  
> **Scope:** 2D axisymmetric analysis of a copper-extrusion geometry.

## What

This project examined the stress and deformation response during copper wire extrusion. The objective was to identify where plastic deformation and high stress develop as the material passes through a diameter reduction, then compare the finite-element response with first-principles expectations.

A 2D axisymmetric model was appropriate because the extrusion geometry and loading were rotationally symmetric. Using that simplification allowed the nonlinear material response to be studied with much lower computational cost than a full 3D model.

## How

### Nonlinear Axisymmetric Model

I built a structural axisymmetric model in Nastran using SOL 402. The analysis focused on:

- Stress distribution through the extrusion section
- Plastic-strain development as the copper passed through the restriction
- Identification of regions where the matrix material exceeded its yield limit

<img src="/_projects/06-copper-extrusion-analysis/copper-extrusion-stress-profile.png" alt="Stress profile and response plot from the copper extrusion analysis" width="100%">

*Stress-profile and response visualization from the extrusion analysis.*

### Interpretation Against Hand Calculations

The numerical response was reviewed against hand-calculation expectations for the extrusion process. The goal was not simply to generate a contour. It was to determine whether the simulated critical regions aligned with the physical expectation that the largest deformation should develop near the reduction.

## Results

The model indicated that the copper matrix exceeded its yield limit and localized critical regions upstream of the diameter restriction. The stress and plastic-strain fields made the material-flow behavior visible and highlighted the transition region most relevant to die design and process control.

<img src="/_projects/06-copper-extrusion-analysis/copper-extrusion-plastic-strain.png" alt="Plastic strain contour showing the critical region upstream of the diameter reduction" width="100%">

*Plastic-strain contour highlighting the critical region upstream of the diameter restriction.*

## Validation and Scope

| Question | Method | Result |
| --- | --- | --- |
| Does the model identify yielding? | Reviewed stress response against material yield behavior | Yield limit exceeded in the high-deformation region |
| Where is the critical location? | Compared stress and strain fields around the reduction | Critical zone located upstream of the diameter restriction |
| Is the solution physically reasonable? | Compared qualitative behavior with hand-calculation expectations | Response aligned with the expected extrusion deformation pattern |

No physical extrusion test was included in the project scope. The model should be treated as an academic process-analysis study, not a qualified manufacturing model.

## What This Work Demonstrates

- Choosing a computationally efficient representation for an axisymmetric manufacturing process
- Applying nonlinear FEA to a plastic-deformation problem
- Reading stress and strain results in the context of actual process physics
- Using hand calculations as a model-sanity check rather than treating solver output as unquestioned fact
