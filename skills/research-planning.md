---
type: skill
id: research-planning
title: Research Planning
description: "Plans interview questions and research methodology based on research goals and target users"
tags: [Production, Research, UX]
connections:
  - target: llm-service
    type: runs_on
---

## Capability

Translates high-level research goals into a structured interview guide with specific questions, probes, and a research methodology tailored to the target user group. Produces questions that elicit genuine behaviours and motivations rather than hypothetical preferences.

## When to Use

- At the start of a UX research project before conducting interviews
- When you have research goals but need to translate them into actionable interview questions
- When planning moderated or unmoderated user interviews

## What It Does

1. **Goal decomposition** — breaks research goals into specific learning objectives
2. **Question design** — generates open-ended interview questions that avoid leading or biased phrasing
3. **Probe planning** — creates follow-up probes for each question to dig deeper into responses
4. **Methodology framing** — recommends interview structure, session length, and participant criteria
5. **Screening criteria** — suggests participant screening questions based on target users

## What It Does NOT Do

- Conduct the interviews (that requires human interaction)
- Analyse responses (use `research-synthesis` for that)
- Recruit participants
