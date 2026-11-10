# Engine

**Work that pays itself the moment it's done.**

A client describes the job. Engine scopes and prices it, a freelancer and their AI agents do
the work, and an AI reviewer checks it against the agreed criteria. When it passes, PayPal pays
the freelancer. Nobody writes or chases an invoice.

This repository holds the **landing site**: a single self-contained `index.html`, served by
GitHub Pages.

👉 **Live site:** https://abinjithtk.github.io/engine/

## How payment works

Built on the [PayPal Agent Toolkit](https://github.com/paypal/agent-toolkit) and MCP server.

1. The client approves the price. The PayPal order is **authorized**, so the money is held before work starts.
2. The freelancer submits. The Review agent checks each acceptance criterion and records its reasoning.
3. On a pass, the payment agent **captures** the authorized amount and issues a PayPal **invoice** and receipt.
4. Cancelled or failed work is voided or **refunded**. The criteria and verdicts are the evidence trail for any **dispute**.

## Guardrails

- The payment agent can never capture more than the client authorized for that job.
- Payment tools take no amount or recipient as input; both come from the approved job.
- The agent that reviews work holds no payment tools.
- Either side can appeal a verdict to a person before payment releases.

## Status

- **Working:** job model, integer-only money maths, MCP server with scoped context.
- **Being built:** PayPal authorize, capture and invoicing in the PayPal sandbox.
- **Next:** accounts, persistence, Review agent wired into the app.

## Run locally

```bash
python -m http.server 8000 --bind 127.0.0.1
# open http://127.0.0.1:8000
```

---

Built by [Abinjith T K](https://in.linkedin.com/in/abinjithtk). PayPal is a trademark of PayPal, Inc.
