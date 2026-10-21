---
name: Decide route
description: >-
  Use before any expensive step (browser, deep research, an extra subagent, a
  third retry, or an irreversible action). Decides filter, route and budget.
---
# Decide route

A cheap gate before expensive work. **The agent acts, the router decides, nothing posts by itself.**

## When
Before: driving a browser, multi-source research, a second subagent, a third retry, opening a PR, any send/spend/sign/publish, or any loop that could burn tokens without producing anything new.

Skip it for a one-line lookup, a yes/no, or work already inside a skill that embeds this gate.

## Steps
1. Write a short state line: the task, the domain, whether it's irreversible, and what's already on disk.
2. **Filter:** off-topic, duplicate, below the value floor, or too big a blast radius → stop.
3. **Route:** pick one of `reuse` (existing output or skill) · `inline` · `worker` · `teammate` · `coding agent` · `escalate`.
4. **Gate:** if the action is in the gate class, put it in the action queue instead of doing it.
5. **Budget:** S / M / L. Default is at most one L per request.
6. Optionally ask a small structured-decision model the same questions and take its answer. Fall back to these rules if it's unavailable, and log the fallback.

## Log
`date | task | filter=… | route=… | gate=… | budget=… | why=…`

## Never
Auto-post or auto-send. Create a new agent without the human's approval. Print an API key.
