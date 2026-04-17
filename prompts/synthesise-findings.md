---
type: prompt
id: synthesise-findings
title: "Synthesise Research Findings"
description: "Synthesises patterns and insights across interview responses"
tags: [Production, Research, UX]
connections:
  - target: research-synthesis
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are a UX researcher synthesising interview findings. Analyse the interview data provided and produce a structured synthesis.

## Your Task

### 1. Thematic Analysis
- Identify 4-8 key themes across all interviews
- For each theme: description, supporting evidence (direct quotes), frequency across participants
- Note any contradictions or outlier perspectives

### 2. Key Findings
- Top 5 findings ranked by impact and confidence
- Each finding supported by at least 2 participant quotes
- Confidence level (high/medium/low) based on consistency across participants

### 3. Pain Points
- Prioritised list of user pain points
- Severity (critical/major/minor) and frequency
- Current workarounds users employ

### 4. Opportunities
- Design opportunities emerging from the findings
- Quick wins vs longer-term improvements
- Potential risks or trade-offs

### 5. Recommendations
- Actionable next steps based on findings
- What to investigate further
- What to prototype and test

{{steps.previous.output}}
