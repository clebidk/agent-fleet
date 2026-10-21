---
name: Inbox triage
description: >-
  Use when sorting inbound email before drafting. Assigns an owner and an
  urgency, drafts only, and respects send-identity locks. Never sends.
---
# Inbox triage

## Steps
1. **Check the send lock first.** Work out which domain the thread belongs to (company / other business / personal) and which single identity may reply. Never mix them.
2. **Classify** each thread: `owner` (which lane), `urgency` (now / today / this week / ignore), `needs_human` (yes/no).
3. **Route** through the router: customer and order mail goes to sales & support, shipping and vendor mail to operations, and so on. Ignore → an archive note only.
4. **Draft** a reply only if someone asked for one or a standing permission covers it. Drafts go in the correct identity's drafts folder.
5. Anything gated goes in the action queue with a one-line pre-act note.
6. Log one decision line per thread.

## Never
Send. Reply from the wrong identity. Spend. Paste customer data into a channel that doesn't need it.
