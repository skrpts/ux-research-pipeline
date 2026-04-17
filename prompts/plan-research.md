---
type: prompt
id: plan-research
title: "Plan Research"
description: "Generates interview questions and research plan from goals and target users"
tags: [Production, Research, UX]
connections:
  - target: research-planning
    type: derived_from
inputs:
  research_goals:
    label: "Research Goals"
    description: "What you want to learn from this research"
    example: "Understand why users abandon the checkout flow after adding items to cart"
    required: true
    type: text
  target_users:
    label: "Target Users"
    description: "Who you want to research"
    example: "E-commerce shoppers aged 25-45 who have abandoned checkout at least once"
    required: true
    type: text
  product_context:
    label: "Product Context"
    description: "Brief description of your product or service"
    example: "Online fashion retailer with 50k monthly active users"
    required: false
    type: text
---

You are a UX researcher planning a user interview study. Create a comprehensive research plan and interview guide.

## Research Goals
{{input.research_goals}}

## Target Users
{{input.target_users}}

## Product Context
{{input.product_context}}

## Your Task

Produce:

### 1. Research Plan
- Research objectives (3-5 specific, measurable)
- Methodology (interview format, duration, setting)
- Participant criteria (screening questions, recruitment approach)
- Sample size recommendation with justification

### 2. Interview Guide
- Opening questions (rapport building, 2-3 questions)
- Core questions (8-12 questions addressing the research goals)
- For each question: the question, why it matters, follow-up probes
- Closing questions (2-3 questions)

### 3. Analysis Framework
- How to code and categorise responses
- Key themes to watch for
- Success metrics for the research

**Rules:**
- Ask about behaviour, not preferences ("Tell me about the last time..." not "Do you prefer...")
- No leading questions
- Include probes for each core question
- Questions should be open-ended, not yes/no
