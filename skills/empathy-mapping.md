---
type: skill
id: empathy-mapping
title: Empathy Mapping
description: "Creates empathy maps for each persona covering what users think, feel, say, and do"
tags: [Production, Research, UX]
connections:
  - target: llm-service
    type: runs_on
---

## Capability

Produces structured empathy maps for each user persona, organising research evidence into four quadrants: Think, Feel, Say, and Do. Adds Pains and Gains sections to capture the emotional and practical dimensions of the user experience.

## When to Use

- After persona generation has produced evidence-based personas
- When the team needs to build shared understanding of user motivations
- To facilitate design workshops or sprint planning sessions

## What It Does

1. **Quadrant mapping** — organises evidence into Think, Feel, Say, and Do categories for each persona
2. **Pain identification** — lists specific frustrations, obstacles, and anxieties each persona experiences
3. **Gain identification** — lists desired outcomes, motivations, and success criteria
4. **Evidence attribution** — links each empathy map entry to specific research findings or quotes
5. **Gap highlighting** — flags quadrants with thin evidence, suggesting areas for follow-up research

## What It Does NOT Do

- Replace direct user observation
- Generate empathy maps without research data to support them
- Prescribe design solutions (empathy maps inform decisions, they do not make them)
