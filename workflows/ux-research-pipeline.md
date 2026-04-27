---
type: workflow
id: ux-research-pipeline
title: UX Research Pipeline
description: "Plan user interviews, collect responses, synthesise findings, generate personas, and create empathy maps"
tags: [Production, Customer-Facing, Research, UX, Gate]
connections:
  - target: research-planning
    type: uses
  - target: interview-collection
    type: uses
  - target: research-synthesis
    type: uses
  - target: persona-generation
    type: uses
  - target: empathy-mapping
    type: uses
  - target: language-polish
    type: uses
  - target: consistency-check
    type: uses
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "15-30 minutes"
  trigger: manual
output_step: "language-polish"
composite_steps:
  - "research-planning"
  - "interview-collection"
  - "research-synthesis"
  - "persona-generation"
  - "empathy-mapping"
  - "language-polish"
  - "consistency-check"
execution:
  - skill: "research-planning"
    prompt: "plan-research"
    step_type: "generation"
  - skill: "interview-collection"
    prompt: "collect-responses"
    step_type: "validation"
  - skill: "research-synthesis"
    prompt: "synthesise-findings"
    step_type: "synthesis"
  - skill: "persona-generation"
    prompt: "generate-personas"
    step_type: "generation"
  - skill: "empathy-mapping"
    prompt: "create-empathy-maps"
    step_type: "generation"
  - skill: "language-polish"
    prompt: "polish-language"
    step_type: "content"
  - parallel:
    - skill: "consistency-check"
      prompt: "check-consistency"
      step_type: "review"
---

## Overview

This workflow takes you from research goals to actionable deliverables: interview plans, synthesised findings, evidence-based personas, and empathy maps. It uses a **gate step** to pause for you to conduct and paste actual interview data, making the output grounded in real user research rather than assumptions.

## Pipeline Stages

### Stage 1: Research Planning

**Input:** Research goals, target users, product context

Invoke the **research-planning** skill to produce an interview guide with research objectives, screening criteria, core questions with probes, and an analysis framework.

**Output:** Complete research plan and interview guide.

### Stage 2: Interview Collection (Gate Step)

**Input:** Research plan from Stage 1

Execution **pauses** via the **interview-collection** gate step. You conduct interviews using the generated guide, then paste your notes, transcripts, or summaries. The more detail you provide, the richer the synthesis.

**Output:** Your interview data, ready for analysis.

### Stage 3: Research Synthesis

**Input:** Interview data from Stage 2

Invoke the **research-synthesis** skill to identify themes, key findings, pain points, opportunities, and recommendations across all interview responses.

**Output:** Structured research synthesis with evidence-backed findings.

### Stage 4: Persona Generation

**Input:** Research synthesis from Stage 3

Invoke the **persona-generation** skill to create 2-3 evidence-based personas. Every characteristic traces back to the research data.

**Output:** User personas with goals, pain points, behaviours, and design implications.

### Stage 5: Empathy Mapping

**Input:** Personas from Stage 4

Invoke the **empathy-mapping** skill to create four-quadrant empathy maps (Says, Thinks, Does, Feels) for each persona.

**Output:** Empathy maps with key insights and design opportunities.

### Stage 6: Language Polish

Invoke **language-polish** to clean up the final deliverables.

### Stage 7: Consistency Check (Parallel)

Invoke **consistency-check** to verify terminology and findings are consistent across all deliverables.

## Error Handling

- If fewer than 3 interview responses are provided, the synthesis flags lower confidence and recommends additional interviews
- If interview data is sparse, personas are marked as preliminary with specific gaps identified
- If the gate step receives "skip" or minimal input, the pipeline proceeds with available data and notes limitations

## Inputs

| Name | Required | Description | Example |
|------|----------|-------------|---------|
| `{{input.research_goals}}` | Yes | What you want to learn | `Understand why users abandon the checkout flow` |
| `{{input.target_users}}` | Yes | Who you want to research | `E-commerce shoppers aged 25-45` |
| `{{input.product_context}}` | No | Product or service description | `Online fashion retailer with 50k MAU` |

## Outputs

| Name | Description |
|------|-------------|
| Research plan and interview guide | Objectives, questions, probes, analysis framework |
| Research synthesis | Themes, findings, pain points, opportunities |
| User personas | 2-3 evidence-based personas with design implications |
| Empathy maps | Says/Thinks/Does/Feels for each persona |

## Setup

1. No external services required — paste your interview data when prompted.
2. Conduct interviews using the generated guide before the gate step.
3. For best results, interview at least 3-5 participants.

## Provider Notes

- Research synthesis benefits from stronger models for nuanced pattern detection.
- Persona generation works well on most capable models.
- Total output is moderate — the gate step is the primary time investment.

## Example Input

```
Research Goals: "Understand why users abandon the checkout flow after adding items to cart. Identify the top 3 friction points and what information users need to complete purchase."
Target Users: "E-commerce shoppers aged 25-45 who have abandoned checkout at least once in the past month"
Product Context: "Online fashion retailer with 50k monthly active users, average order value £65, current checkout abandonment rate 72%"
```
