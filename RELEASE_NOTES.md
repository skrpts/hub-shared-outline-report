# Release Notes

## v1.0.1
GH#1100 migration wave — stop reading the brief positionally.

The body read `{{steps.previous.output}}` for the report brief, so the prompt received whatever ran immediately before it rather than the brief it declares it needs. It now reads `{{step.context.brief}}` and declares `brief` as a **required** context param, so a consumer must wire it with `bindings:` (contract §4.3.1) and an unbound slot fails loudly instead of degrading to empty.

No `default_from_previous` — revoked on GH#1100, so there is no positional fallback. Behaviour is unchanged for the one consumer, which binds `brief` from its Report Intake step: the value it receives is the value it received before.

## v1.0.0
GH#814 — new shared prompt. Turns a report brief into a structured section outline (headings, purpose, key points, word targets) for the drafting stage to expand. Runs on the report-authoring skill. First consumer: report-writing-flow.
