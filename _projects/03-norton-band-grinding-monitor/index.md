---
layout: post
title: "Norton Band: Wrist-Worn Manual Grinding Monitor"
description: "Developed and evaluated a wearable prototype that converts wrist-mounted vibration and tool-speed-related signals into practical feedback for manual grinding operations."
skills:
  - "Arduino"
  - "Rapid Prototyping"
  - "Sensor Integration"
  - "Vibration Analysis"
  - "Data Analysis"
  - "Field Testing"
main-image: /cover.svg
---

> **Role:** Research Engineer, Saint-Gobain Abrasives  
> **Project period:** 2022 to 2024  
> **Public scope:** High-level portfolio summary only. Company-specific algorithms, raw signals, and unreleased hardware details are excluded.

## What

Manual grinding is inherently variable. Tool condition, grinding pressure, vibration, and operator technique all affect process performance. This project explored whether a wrist-worn device could collect useful signals during manual cutoff, deburring, and polishing, then turn those signals into feedback that operators and field engineers could act on.

I supported the prototype development and testing of a wearable monitoring concept designed to make vibration and tool-speed behavior easier to interpret in a real grinding environment.

## How

### Wearable Prototype Development

The initial concept used Arduino-based electronics packaged in a 3D-printed wrist-worn housing. The device captured wrist-mounted acceleration during manual grinding tasks without modifying the grinder itself.

### Cross-Checking Multiple Signals

A wrist sensor does not see tool vibration alone. It sees the combined response of the grinder, operator, hand, and arm. To improve interpretation, I compared acceleration behavior with microphone and grinder-current signals.

### Operator-Facing Metrics

The raw data was translated into two simplified outputs:

- **Grinding performance score:** A tool-RPM-related indication of process behavior.
- **Vibration quality score:** A frequency-based indicator intended to flag vibration conditions worth investigating.

The purpose was not to give an operator a raw spectrum. The purpose was to tie sensor behavior to a practical decision, such as checking tool balance, inspecting maintenance condition, or adjusting grinding technique.

## Results

- Built and evaluated Arduino-based wearable prototype hardware with a rapid-prototyped enclosure.
- Captured wrist-mounted acceleration during representative manual grinding tasks.
- Compared acceleration response with audio and motor-current behavior.
- Translated sensor features into simplified performance and vibration-quality indicators.
- Connected observed signal behavior to practical diagnostic categories including tool imbalance, aggressive grinding pressure, and maintenance needs.

## Validation and Engineering Challenges

| Challenge | Why it mattered | Engineering response |
| --- | --- | --- |
| Separating tool vibration from arm motion | Wrist data includes human-body dynamics and tool behavior | Cross-checked acceleration with microphone and motor-current signals |
| Repeatable sensor mounting | Strap tension, placement, and orientation can change response | Evaluated the prototype during representative use conditions |
| Packaging and ergonomics | The unit had to be wearable without interfering with the task | Used a 3D-printed enclosure for rapid mechanical iteration |
| Actionable output | Raw sensor data alone does not help an operator | Developed simple performance and vibration-quality indicators |

This was prototype-level work, not a certified safety-monitoring product. The public portfolio should not claim formal exposure measurement, medical relevance, or production readiness without approved validation evidence.

## Confidentiality Note

This project is based on employer work. Do not publish source code, detailed algorithm logic, internal test data, customer information, unreleased photos, or product specifications. Approved high-level prototype images and generalized diagrams can be added later.
