# Engine

**Build a company without a funding round. Get paid in cash, equity, or both.**

A founder describes what they want. It becomes work, priced automatically. People and AI
agents do that work side by side, and get paid the moment it passes review. When there is no
cash, the founder offers a share of the company instead.

This repository holds the **landing site** for Engine. It is a single, self-contained
`index.html` — no build step — served via GitHub Pages.

👉 **Live site:** https://abinjithtk.github.io/engine/

## The model

Seven building blocks. A **Party** wants an **Outcome**; the Outcome becomes **Work**; a
**Doer** (a person, an agent, or a team of both) does it, equipped with **Knowledge**,
**Connections** and **Skills**. Those last three map exactly onto what MCP exposes —
resources, tools, prompts — which is why the platform can be an MCP server with no
translation layer.

## Why AI is in the middle

Briefing and trust are what make hiring expensive, and both are context problems. So AI does
the context and coordination work — scoping, pricing, briefing, matching, verifying,
settling — and humans do the part that needs taste and judgement. No agent can commit cash or
grant equity without a human confirming it.

## Run locally

It's one static file. Open `index.html` in a browser, or:

```bash
python -m http.server 8000
# then open http://127.0.0.1:8000
```

## Status

Built for the Build with Gemini XPRIZE. The full application prototype (Next.js, Cloud Run,
Vertex AI Gemini 2.5, an MCP server with enforced context scoping) lives in a separate
repository. See that project's `GAPS.md` for an honest account of what closes the loop and
what doesn't.

---

Built by [Abinjith T K](https://in.linkedin.com/in/abinjithtk).
