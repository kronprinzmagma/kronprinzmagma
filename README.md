# Nils Seiter

**AI Product Practitioner and Senior Product Owner, Zurich.**

I take AI products from idea to production: multi-agent systems, privacy-first architectures that keep personal data on the machine, and agentic coding with Claude Code and Codex. 19+ years building digital products; founder of Localina (acquired by local.ch). Today I work where AI product management meets AI engineering, as a product lead who talks to engineers as a peer.

For every project below I write the spec, make the architecture calls and set the quality gates. Most of the code is written with Claude Code under that direction.

Currently open to Senior Product / AI Product roles in Zurich.

[LinkedIn](https://www.linkedin.com/in/nilsseiter)

---

## Selected work

Seven public repos: six below, plus an earlier one at the end. Each README starts with the business problem; architecture, tests, evals and cost tracking follow inside the repo.

Four of them are sanitised mirrors of a private working repo and are synced from it. The code is the same, real personal data is replaced by synthetic data, and a few modules that only make sense with my own source material are left out. `job-search-decision-support` is a curated port instead: its working repo holds a real job search, so only the core scripts were carried over and rebuilt around a synthetic persona. `ki-news-aggregator` and `Lead-Analyzer` are developed in the open because they never touch personal data.

- **[job-search-decision-support](https://github.com/kronprinzmagma/job-search-decision-support)**: The system behind my own job search, from market scan to interview debrief. Three sweeps a day, every posting logged with a reason for every drop. After each Go it researches the company and the people involved and drafts the cover letter from that research; it prepares interviews and case studies, and once a month it maps the AI skills the market asks for against my evidence. I make every Go/NoGo call and send every application. Synthetic persona and data. _Curated port of a private working repo._
- **[agentic-cv-tailoring](https://github.com/kronprinzmagma/agentic-cv-tailoring)**: Reframes a documented CV for a specific role without inventing anything: a dedicated factcheck agent vetoes any claim that cannot be traced to a source document. Ten agents, cross-provider review (Anthropic and OpenAI), deterministic quality gates. _Public version of `cv-tailor`._
- **[ai-listing-assistant](https://github.com/kronprinzmagma/ai-listing-assistant)**: Photo → complete bilingual (DE/FR) Ricardo.ch listing, with a human review step before publishing. Five agents, a standalone MCP server package and an LLM-as-judge eval suite; publishing to Ricardo.ch runs against a stub until partner API access is granted. _Public version of `verkaufshilfe-via-foto`._
- **[pdf-document-organizer](https://github.com/kronprinzmagma/pdf-document-organizer)**: Turns a pile of `scan0042.pdf` into clean, searchable filenames. Personal data is redacted in memory before any cloud call, and the local engine works without the cloud at all. _Public version of `dok-namer`._
- **[swiss-tax-document-extractor](https://github.com/kronprinzmagma/swiss-tax-document-extractor)**: A folder of Swiss tax PDFs becomes one transfer table for the Canton of Zurich tax return, every amount anchored to the exact words on the original page. Runs locally with Ollama; nothing leaves the machine. A local review UI turns each confirmation into a regression test, so the next run has to hit the number a human already checked. Used for a real tax return. _Public version of `steuer-extraktor`._
- **[ki-news-aggregator](https://github.com/kronprinzmagma/ki-news-aggregator)**: A daily AI briefing for product people who build. 15 sources, Claude Haiku for scoring, Claude Sonnet for writing and a review pass on every text; published as GitHub Issues with a [live archive](https://kronprinzmagma.github.io/ki-news-aggregator/) and an optional podcast feed.

Also public: **[Lead-Analyzer](https://github.com/kronprinzmagma/Lead-Analyzer)**, an earlier and deliberately non-agentic tool. It turns a raw customer list into a ranked sales call sheet; Excel in, Excel out, no API key or AI service needed.

Not public yet: an iPhone web app for finding and tracking German-language books, and a prototype AI shopping assistant for retail. Both are in active development in private repos.

---

## Currently exploring

_Last updated: 2026-10_

- RAG implementations beyond demos
- Conversational voice agents (OpenAI Realtime API). Text-to-speech already ships in [ki-news-aggregator](https://github.com/kronprinzmagma/ki-news-aggregator), which publishes each daily as a spoken-word episode with a podcast feed; the open part is real-time, two-way conversation.
- MCP servers beyond tool-wrapping: sampling, elicitation, resource subscriptions. A first server with tools and read-only resources ships in [ai-listing-assistant](https://github.com/kronprinzmagma/ai-listing-assistant).
- Eval harnesses that survive a model swap. Cross-provider review and LLM-as-judge are in use today (a review pass on every text in ki-news-aggregator, offline evals in ai-listing-assistant); making those verdicts comparable across model generations is the open problem.
- Human-in-the-loop state that outlives the system it lives in. A reviewer's hours of judgement are the one artefact no pipeline can regenerate. An audit of the correction loop in [swiss-tax-document-extractor](https://github.com/kronprinzmagma/swiss-tax-document-extractor) turned that into concrete rules: a withdrawal is stored as an explicit fact, never as an absence, and every merge only adds.

---

Working repos stay private to keep personal source material out of the open. The links above point to the public versions.
