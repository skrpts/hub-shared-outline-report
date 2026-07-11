---
type: prompt
id: outline-report
title: "Report Outline"
description: "Produces a structured section outline for a report from the brief"
tags: [Production, Academic, Writing]
metadata:
  output_format: markdown
  prompt_type: task
---

## Purpose

Drives the outline stage of the report-authoring skill.

## Prompt

You are an academic editor planning a report. Using the brief below, produce a clear, structured outline for the report or thesis chapter. This is the plan the drafting stage will expand into full prose — do not write the prose yet.

### Report Brief

{{steps.previous.output}}

### Instructions

1. Derive the report's sections from the topic, research questions, and methodology in the brief.
2. For each section, state its purpose, the key points or evidence it must cover, and a rough word target.
3. Order the sections into a coherent argument, from introduction through to conclusion.
4. Flag anywhere the brief is thin, so the drafting stage knows where to hedge or note an assumption.

### Output Format

**Working Title**

**Section Outline** (numbered) — for each section: heading, one-line purpose, key points to cover, approximate word count.

**Notes** — gaps in the brief and any assumptions the drafting stage should carry forward.

## Formatting Rules

- Use American English throughout
- Be specific — tie each section back to a research question or to the methodology
- Do not draft prose; produce the plan only
