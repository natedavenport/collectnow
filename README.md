# collectnow
Collect Now — Prototype (README)
Interactive prototype for "Collect Now," a concept for the Housecall Pro FinTech Mobile team: at job close-out, an AI judges whether this job is likely to be paid late if invoiced, and — only when it's worth it — nudges the Pro to collect on the spot.
How to run it
Option A — open the file: download index.html, then double-click it (or open it in Chrome, Edge, or Safari). It runs fully offline with no install, build step, or account.

Option B — hosted version: https://natedavenport.github.io/collectnow/
What to try (≈2 minutes)
Start on the hero job (new customer, large emergency ticket) — the prompt appears with a plain-language "why" and payment options. Tap Tap to Pay to see the collect-and-confirm flow.
Use the scenario switcher to compare:
a trusted repeat customer (the prompt stays silent — restraint is intentional, not a bug),
the small-but-risky vs. large-but-safe pair (shows the model weighs the combination of factors, not a single dollar threshold),
a large ticket the customer can't cover today (recommends financing instead of "pay now").
Flip the Offline toggle — the prompt still works via an on-device fallback.
Flip the neighborhood/ZIP toggle — the output does not change (the model never uses location or demographics).
A note on the AI (please read)
The risk decision is a transparent simulation. A real payment-risk model can't be trained inside a take-home, so scoring here is a rule-based stand-in. How the production model would actually be trained, evaluated, and gated is specified in the accompanying Eval Spec and Measurement Plan.
The generative copy uses AI. The customer-facing "ask" and the rationale are produced by a live language model during the live demo. In this standalone file they fall back to pre-written examples so the prototype is complete without any API key or network.
