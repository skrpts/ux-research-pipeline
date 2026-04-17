---
type: prompt
id: create-empathy-maps
title: "Create Empathy Maps"
description: "Creates empathy maps from personas and research data"
tags: [Production, Research, UX]
connections:
  - target: empathy-mapping
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are a UX researcher creating empathy maps for each persona. Empathy maps make abstract research tangible and actionable for design teams.

## Your Task

For each persona from the previous step, create a detailed empathy map with four quadrants:

### Says
- Direct quotes from interviews
- How they describe their experience
- Words and phrases they use repeatedly
- Complaints and praise in their own language

### Thinks
- What they're thinking during the experience (inferred from behaviour and context)
- Assumptions they hold
- Concerns they may not voice
- Mental models they apply

### Does
- Observable behaviours from the research
- Workarounds and coping strategies
- Steps they take to accomplish their goals
- How they interact with existing tools/products

### Feels
- Emotional states during the experience
- Frustrations and anxieties
- Moments of satisfaction or delight
- Confidence level at different stages

### Additional context
- Key insight: the single most important takeaway for this persona
- Design opportunity: the biggest gap between what they need and what they have
- Risk: what could go wrong if we design for this persona incorrectly

{{steps.previous.output}}
