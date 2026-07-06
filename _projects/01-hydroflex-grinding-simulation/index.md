---
layout: post
title: "Force-Controlled HydroFlex Grinding Simulation"
description: "Graduate thesis research developing a nonlinear LS-DYNA FEM-SPH model of force-controlled fixed-abrasive polishing for internal channels in L-PBF AlSi10Mg components."
skills:
  - "ANSYS LS-DYNA"
  - "FEM-SPH Modeling"
  - "Grinding Mechanics"
  - "Surface Characterization"
  - "MATLAB and Python"
  - "Experimental Validation"
main-image: /cover.svg
---

> **Role:** Graduate Researcher, Worcester Polytechnic Institute  
> **Project period:** 2024 to 2026  
> **Status:** Thesis research in progress. Public results are intentionally limited while experimental comparison and publication review continue.

## What

HydroFlex is a fixed-abrasive polishing process intended for finishing internal channels in additively manufactured metal components. The engineering problem is not simply to move a wheel to a prescribed depth. The wheel-workpiece interaction is governed by a force balance between the compliant spindle system, contact response, and process loads. Hydrodynamic coolant flow contributes a tangential force that drives the orbital motion inside the channel.

I am developing a numerical model that connects these physical inputs to local grain-scale interaction, material removal, and surface-finish evolution for L-PBF AlSi10Mg workpieces.

### Engineering Objective

Build a simulation method capable of evaluating how measured or statistically reconstructed surface topography, applied normal load, and sliding conditions influence:

- Contact force and dynamic penetration
- Local stress response and material separation
- Removed volume and surface-profile evolution
- The connection between force-controlled motion and polishing performance

## How

### Surface and Process Representation

I characterized representative wheel and workpiece surfaces using microscopy-derived topography. The public portfolio does not include proprietary wheel scans or unpublished experiment data. The simulation uses a millimeter-scale contact region so the model can retain meaningful local roughness while remaining computationally tractable.

### Nonlinear FEM-SPH Model

The model combines a rigid FEM representation of the abrasive wheel with a deformable SPH representation of the L-PBF AlSi10Mg workpiece. Normal engagement is load controlled rather than prescribed by a fixed depth of cut. Tangential motion is applied to represent the local sliding interaction.

The post-processing workflow extracts the signals required to evaluate a force-controlled process:

- Contact-force history
- Normal displacement and penetration behavior
- Stress response and local deformation
- Material-removal indicators and separated volume
- Surface-profile change

### Engineering Challenges

This work is a model-development project, not a polished animation exercise. The main engineering challenge is establishing that the response is physically credible before interpreting it as material removal.

- **Force control:** A nominal force match is insufficient if the wheel continues to penetrate. I review force and displacement together to distinguish stable engagement from runaway motion.
- **Grain-scale numerical stability:** Abrasive contact and SPH deformation can cause severe timestep reduction. I use simplified benchmark cases before applying a rough, multi-grain contact patch.
- **Material removal interpretation:** Isolated particle ejection is not automatically a chip. I evaluate deformation, stress response, and separation behavior before treating an output as a credible removal mechanism.
- **Computational cost:** SPH spacing must be fine enough to capture local interaction, yet practical enough to allow parameter studies and validation work.

## Results

The current framework produces a complete response chain from imposed loading and sliding conditions to contact force, penetration, stress response, material-removal indicators, and surface-profile outputs.

The active validation plan compares these model outputs with laboratory surface-roughness measurements from polished internal channels. Final predictive accuracy has not been claimed publicly. The project is valuable because it establishes a defensible modeling and validation workflow instead of using a prescribed-displacement scratch simulation as a surrogate for HydroFlex physics.

## Validation and Evidence

| Question | Evidence used or planned | Why it matters |
| --- | --- | --- |
| Does the model behave as a force-controlled system? | Contact-force and normal-displacement histories | Confirms stable engagement rather than uncontrolled penetration |
| Does the local response remain physically plausible? | Stress fields, SPH deformation, and material-separation review | Separates model behavior from numerical artifacts |
| Can the model describe surface response? | Removed-volume and surface-profile outputs | Connects grain-scale contact to measurable process outcomes |
| Does it agree with experiments? | Surface-roughness comparison on polished channels | Provides an external check on the simulation |

## Technical Scope and Confidentiality

This work uses publication-restricted and proprietary inputs. This public page intentionally omits wheel geometry, raw microscopy data, LS-DYNA decks, material-card details, unreleased figures, and experimental datasets. The project description focuses on the engineering approach and validation logic.
