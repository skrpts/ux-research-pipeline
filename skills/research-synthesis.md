---
type: skill
id: research-synthesis
title: Research Synthesis
description: "Synthesises findings across multiple interview responses to identify patterns, themes, and insights"
tags: [Production, Research, UX]
connections:
  - target: llm-service
    type: runs_on
---

## Capability

Analyses interview responses from multiple participants and synthesises them into structured findings. Identifies recurring themes, contradictions, surprising insights, and evidence-backed patterns across the data set.

## When to Use

- After collecting interview responses from multiple users
- When you need to move from raw data to structured insights
- Before generating personas or empathy maps

## What It Does

1. **Theme identification** — finds recurring patterns across participant responses
2. **Contradiction surfacing** — highlights where participants disagree or report conflicting experiences
3. **Insight extraction** — identifies non-obvious findings that go beyond surface-level patterns
4. **Evidence linking** — ties every finding back to specific participant quotes
5. **Frequency mapping** — notes how many participants mentioned each theme
6. **Priority ranking** — ranks findings by frequency, severity, and strategic relevance

## What It Does NOT Do

- Generate personas (use `persona-generation` for that)
- Make design recommendations directly
- Validate statistical significance (qualitative research does not require this)
