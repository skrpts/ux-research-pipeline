---
type: skill
id: interview-collection
title: Interview Collection
description: "Human gate — pauses execution for the user to paste interview responses"
tags: [Production, Gate, Research, UX]
connections:
  - target: llm-service
    type: runs_on
metadata:
  gate: true
---

## Capability

Pauses the workflow and presents the interview guide to the user, then waits for them to paste actual interview responses. This is a **gate step** — execution pauses until the user provides their data.

## When to Use

- After research planning has produced an interview guide
- When real user interview data is needed before synthesis can proceed

## What Happens

1. Execution pauses with status `awaiting_input`
2. The user sees the interview guide and instructions in the Runs view
3. The user conducts interviews (outside skrptiq) and pastes the responses
4. The user's pasted responses become this step's output, flowing into research synthesis

## Input Guidance

The gate prompt instructs the user on what to paste:

- Raw interview transcripts or detailed notes
- Responses from multiple participants (labelled by participant)
- Any observational notes from the sessions
- The more detail provided, the richer the synthesis
