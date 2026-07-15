---
type: skill
id: persona-generation
title: Persona Generation
description: "Creates evidence-based user personas from synthesized research findings"
tags: [Production, Research, UX]
connections:
  - target: llm-service
    type: runs_on
---

## Capability

Transforms synthesized research findings into structured user personas. Each persona is grounded in real interview data rather than assumptions, with direct quotes and behavioral evidence supporting every attribute.

## When to Use

- After research synthesis has identified user segments and behavioral patterns
- When the team needs shared reference models for design and development decisions
- To communicate user needs to stakeholders who were not present during research

## What It Does

1. **Segment identification** — identifies distinct user segments from the synthesized findings
2. **Persona construction** — builds a complete persona for each segment including goals, frustrations, behaviors, and context
3. **Evidence grounding** — attaches specific quotes and observations to each persona attribute
4. **Scenario mapping** — describes typical scenarios where each persona interacts with the product
5. **Differentiation** — clearly articulates what makes each persona distinct from the others

## What It Does NOT Do

- Invent demographic details not supported by the research
- Create fictional backstories unconnected to observed behaviors
- Produce marketing segments (these are design personas, not market segments)
