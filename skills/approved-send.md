---
name: Approved send
description: >-
  Use when a human already wrote and approved customer copy and a recipient
  list, and it must go out through the system's sanctioned send path. Never
  invents a payload.
---
# Approved send

## Inputs (collect all of them before touching anything)
- Subject, plus each approved body version (with only the approved merge fields)
- The recipient/order list to send to, **and** the list to hold back
- An approval pointer: who said "send", where, and when

## Hard rules
1. Never rewrite approved copy. Never call a model to "improve" it.
2. Never hand-build an API payload from memory. The only valid payload is the one produced by the system's own builder function.
3. Check each record before sending: product, SKU, last message and price must agree. If anything disagrees, hold the record and name the mismatch.
4. Never send to a record on the hold list.
5. A send isn't done until the downstream system shows it as **sent** with no failure. "Accepted/queued" isn't sent.
6. Stop on the first hard failure. Never keep blasting.

## Steps
1. Find the sanctioned builder and send functions. Don't reimplement them.
2. Dry run: build every payload and diff it against the approved copy.
3. Send one record, then verify delivery.
4. Send the rest. Verify each one and record the sent timestamp.
5. Report: sent N, held M (with reasons), failed K (with errors).

## Never
Send without an approval pointer. Use a different channel (raw SMTP, a UI, a marketing tool) to get around a broken send path.
