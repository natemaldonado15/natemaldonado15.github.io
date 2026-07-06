---
layout: post
title: "Composite Wing Panel Optimization"
description: "Automated Abaqus studies to identify lower-weight laminate configurations that satisfied strength and structural-stability requirements for a wing skin panel."
skills:
  - "Abaqus"
  - "Composite Laminates"
  - "Structural Analysis"
  - "Buckling Analysis"
  - "Python Automation"
main-image: /wing-panel-results.png
---

> **Role:** Mechanical Engineering Student  
> **Project type:** Academic FEA project  
> **Scope:** Structural performance and laminate-design trade study for a Lavochkin La-156 wing skin panel.

## What

The project examined how laminate design choices affect the strength, stiffness, and structural stability of a composite wing skin panel. The goal was to reduce mass while retaining acceptable margin against the assigned strength and buckling requirements.

Rather than selecting a single laminate by intuition, I treated ply orientation, placement, thickness, and material selection as design variables within a repeatable analysis workflow.

## How

### Abaqus Structural Model

I imported the wing-panel geometry into Abaqus and modeled the composite panel with ribs and longerons. Material properties and ply behavior were defined so the model could evaluate laminate response under the assigned loading and boundary conditions.

<img src="/_projects/05-wing-panel-optimization/wing-panel-geometry.png" alt="Wing panel finite-element model with ribs and longeron" width="100%">

*Finite-element representation of the wing skin panel with ribs and longeron.*

### Python-Driven Design Iteration

I used Python to automate repeated simulation iterations while varying laminate design variables:

- Ply orientation
- Ply placement within the stack
- Layer thickness
- Material selection

The automation made the comparison more systematic and reduced the risk of manual setup inconsistency across iterations.

## Results

The study identified lower-weight laminate configurations that still met the specified strength and buckling constraints. The final iteration selected an appropriate stacking angle and layer thickness based on the trade between structural response and mass.

<img src="/_projects/05-wing-panel-optimization/wing-panel-results.png" alt="Composite wing panel analysis result contour" width="100%">

*Representative Abaqus contour result used to assess panel response during the laminate trade study.*

## Validation and Scope

| Validation question | Method | Limitation |
| --- | --- | --- |
| Does the selected laminate meet strength criteria? | Reviewed model stress and failure-related response against assigned limits | No full-scale structural test was included |
| Does the panel retain structural stability? | Evaluated buckling behavior across laminate variants | Results depend on the assigned geometry, loads, and boundary conditions |
| Is the comparison repeatable? | Used Python automation for the parameter sweep | The study is an academic optimization exercise, not a released aircraft design |

This project demonstrates how to turn a composite-structure problem into a disciplined trade study. The credible result is not merely a contour plot. It is a documented relationship between laminate variables, structural constraints, and mass.

## Public Files

The repository can safely include the supplied FEA visuals and a sanitized Python automation example. Do not present this project as work for an aerospace manufacturer or as flight-qualified design work.
