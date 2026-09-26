# Nils Seiter

**AI Product Practitioner & Senior Product Owner — Zurich, Switzerland.**

I take AI products from idea to production: multi-agent systems, privacy-first hybrid architectures, and agentic coding with Claude Code and Codex. 19+ years building digital products; founder of Localina (acquired by local.ch). Today I work at the intersection of AI Product Management and AI Engineering — a product lead who can talk to engineers as a peer.

Currently open to Senior Product / AI Product roles in Zurich.

[LinkedIn](https://www.linkedin.com/in/nilsseiter)

---

## Selected work

Six public repos — five below, plus an earlier one at the end. The business problem comes first in every README — the engineering proof (architecture, tests, evals, cost-tracking) is one click away inside each repo.

Four of them are sanitised mirrors of a private working repo, kept in sync after every release: the same code, minus a handful of modules that only make sense against my own source material, and with real personal data replaced by synthetic test sets. `ki-news-aggregator` is the exception — it is developed in the open, because it never touches personal data in the first place.

- **[agentic-cv-tailoring](https://github.com/kronprinzmagma/agentic-cv-tailoring)** — Reframes a documented CV for a specific role without inventing anything: a dedicated factcheck agent vetoes any claim that can't be traced to a source document. 10-agent pipeline, cross-provider review (Anthropic + OpenAI), deterministic quality gates. _Public version of `cv-tailor`._
- **[ai-listing-assistant](https://github.com/kronprinzmagma/ai-listing-assistant)** — Photo → complete bilingual (DE/FR) Ricardo.ch listing in under two minutes. 5-agent pipeline, a standalone MCP server package, and an LLM-as-judge eval suite. _Public version of `verkaufshilfe-via-foto`._
- **[pdf-document-organizer](https://github.com/kronprinzmagma/pdf-document-organizer)** — Turns a pile of `scan0042.pdf` into clean, searchable filenames — without ever sending personal data to the cloud. PII is redacted in memory before any cloud call; can run fully local. _Public version of `dok-namer`._
- **[swiss-tax-document-extractor](https://github.com/kronprinzmagma/swiss-tax-document-extractor)** — A folder of Swiss tax PDFs becomes one transfer table for the Canton of Zurich tax return, every amount anchored to the exact words on the original page. Runs local-first with Ollama; nothing leaves the machine. A local review UI turns each confirmation into a regression test, so the next run has to hit the number a human already checked. Used for a real tax return. _Public version of `steuer-extraktor`._
- **[ki-news-aggregator](https://github.com/kronprinzmagma/ki-news-aggregator)** — A daily AI briefing for product people who build, not just spec. 15 sources, Claude Haiku scoring + Sonnet writing, published as GitHub Issues with a live archive. [Live archive](https://kronprinzmagma.github.io/ki-news-aggregator/).

Also public: **[Lead-Analyzer](https://github.com/kronprinzmagma/Lead-Analyzer)** — an earlier, deliberately non-agentic tool. Turns a raw customer list into a ranked sales call sheet; Excel in, Excel out, runs offline.

---

## Currently exploring

_Last updated: 2026-09_

- RAG implementations beyond demos
- Conversational voice agents (OpenAI Realtime API) — text-to-speech already ships in [ki-news-aggregator](https://github.com/kronprinzmagma/ki-news-aggregator), which publishes each daily as a spoken-word episode with a podcast RSS feed; the open part is real-time, two-way
- MCP servers beyond tool-wrapping — sampling, elicitation, resource subscriptions (a first server already ships in [ai-listing-assistant](https://github.com/kronprinzmagma/ai-listing-assistant))
- Eval harnesses that survive a model swap — cross-provider review and LLM-as-judge run in production today; making those verdicts comparable across model generations is the open problem
- Human-in-the-loop state that survives the system it lives in — a reviewer's hours of judgement are the one artefact no pipeline can regenerate. Treating a withdrawal as an explicit fact rather than as an absence, and every merge as additive, is what keeps it; an audit of the correction loop in [swiss-tax-document-extractor](https://github.com/kronprinzmagma/swiss-tax-document-extractor) turned that into concrete rules

---

Working repos stay private to keep personal source material out of the open. The "Selected work" links above point to the public versions.
