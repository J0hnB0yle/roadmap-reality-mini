# Roadmap-Reality Orchestration — live mini-version

A single-file, in-browser demo of a signal → triage → route orchestration that
matches AE commitments against engineering reality, scores gaps by revenue at
risk and renewal proximity, drafts honest reset language for the AE, and emits
a weekly leadership digest.

Mock data, vanilla JS, no build step, no dependencies. One HTML file.

## Run

Open `index.html` in any browser, or visit the hosted version.

Click **Run orchestration** to walk the pipeline end-to-end. Edit the backlog
tags, status fields, or the call-note commitment text to see how the matcher,
severity classifier, and digest react.

## Logic

Mirrors the Python orchestrator `run.py` from the parent mini-demo:

- Three input sources: product backlog, CRM call notes, renewal calendar.
- Keyword anchor matcher (production swap: model read over call-summary text).
- Severity classifier from (tag, status) → CRITICAL / HIGH / MEDIUM / LOW.
- Gap score = `revenue_at_risk ÷ days_to_renewal × 100`.
- Template-based reset language (production swap: model generation step).

## Context

Built as a follow-up artifact to the Scribd Product Operations Lead final-round
presentation, 2026-05-14. The live version Ed can poke at on his own time.

— John Boyle
