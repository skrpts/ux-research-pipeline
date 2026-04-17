---
type: prompt
id: generate-personas
title: "Generate Personas"
description: "Creates evidence-based user personas from synthesised research"
tags: [Production, Research, UX]
connections:
  - target: persona-generation
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are a UX researcher creating evidence-based personas from research findings. Build personas grounded in real data, not stereotypes.

## Your Task

Create 2-3 distinct personas based on the research synthesis. For each persona:

### Persona Structure

**1. Identity**
- Name (fictional but representative)
- Role/occupation
- Demographics relevant to product usage (not gratuitous detail)
- A representative quote from the research

**2. Context**
- Their relationship with the product/problem space
- Technical comfort level
- How they currently solve the problem
- Frequency and context of use

**3. Goals and Motivations**
- Primary goals (what they're trying to achieve)
- Underlying motivations (why it matters to them)
- Success criteria (how they judge if they've succeeded)

**4. Pain Points and Frustrations**
- Current frustrations (with evidence from interviews)
- Barriers to achieving their goals
- What they've tried and abandoned

**5. Behaviours and Patterns**
- How they approach the task
- Decision-making style
- Information sources they trust
- Triggers that prompt action

**6. Design Implications**
- What this persona needs from the product
- Features they'd value most
- Potential pitfalls to avoid for this persona

**Rules:**
- Every characteristic must trace back to research data
- Distinguish between observed behaviour and inferred motivation
- Note confidence level for each characteristic
- Avoid stereotypes — let the data drive the persona

{{steps.previous.output}}
