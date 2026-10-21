# Skill templates

Generic versions of skills the fleet runs every day. Each one is a single markdown file:

```markdown
---
name: <Short name>
description: >-
  Use when <trigger>. <What it produces>. <The one thing it never does>.
---
# <Short name>
## When / Skip
## Steps
## Never
```

| Template | What it shows |
|---|---|
| [plan-first.md](plan-first.md) | Plan → sort ship/gate/never → pre-act line → execute |
| [decide-route.md](decide-route.md) | A cheap routing and budget gate before expensive work |
| [inbox-triage.md](inbox-triage.md) | Owner and urgency triage, drafts only, send-identity lock |
| [approved-send.md](approved-send.md) | Shipping human-approved copy through the one sanctioned send path |
| [stale-facts-audit.md](stale-facts-audit.md) | Re-checking memory against live sources without inventing updates |
