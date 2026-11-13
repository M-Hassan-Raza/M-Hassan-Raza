# Muhammad Hassan Raza

CIO at [Entropy & Co.](https://entropyand.co) in Lahore. I run product and engineering and write a good share of the backend: mostly systems where a small mistake becomes a wrong balance, a leaked tenant, or an agent spending money it shouldn't.

[mhassan.dev](https://mhassan.dev) · [Resume](https://mhassan.dev/assets/muhammad-hassan-raza-resume.pdf) · [LinkedIn](https://www.linkedin.com/in/hassanraza22/)

## Platforms

**[Portus](https://portusai.co)**: a workflow engine for business operations. A workflow is a versioned plan graph, and the same document is what the engine executes and what the canvas draws. Describe a process in plain words and Portus composes the agents, tools and approval steps for it. The engine is our own interpreter over the graph, with nine node types (step, tool, condition, map, approval and more). Runs are durable: each node's result is persisted, approvals park a run at no cost and resume only on a decision bound to a hash of the exact arguments, and every non-idempotent tool call goes through a ledger so a retry never sends twice. Recruitment, contracts, invoicing, expenses and tickets plug in as domain packages the core never imports. English and Arabic throughout. Python, FastAPI, Pydantic AI, Postgres, TanStack Start.

**[Obelisk](https://theobelisk.app)**: AI marketing platform. More than fifteen specialist agents in production, each with its own tools and guardrails. Retrieval is scoped per tenant so one customer's brand never reaches another's, and every spend or send action stops for human approval. Python, FastAPI, LangGraph, Postgres with pgvector.

**[Anatomia](https://tryanatomia.com)**: medical inbox for clinics. Patient calls and requests are sorted, routed and closed, with each callback documented and timed for billing. Recordings and transcripts are encrypted and access-controlled by default; the model only summarizes, scores urgency and drafts, and staff decide.

**[Polaris](https://polariserp.app)**: billing, stock and ledgers for Pakistani retail, in daily use by shops since 2024. Invoices, refunds and batch stock stay consistent with several cashiers selling at once, each organization is isolated at the database level, and tax exports match FBR's format. Django, Postgres.

**October**: campaigns between brands, agencies and creators, from brief to report. Three kinds of users with overlapping data, each seeing exactly their share; analytics built only from verified records; realtime messaging over authenticated WebSockets. Django, Next.js.

**RISQ**: fraud scoring for legal-intake calls. Each call ends as transfer, review or quarantine, along with the gate that produced the decision so a reviewer can follow it. New campaigns are configuration, not code.

**Bonnet**: turns a creative brief into research, strategy, creative direction and a usable document. Long-running generation you can watch, cancel and rerun step by step, with exports that come out clean and cited however messy the model output was.

## Client systems

- **Call audio analytics.** A Rust ingest service decodes recordings, splits channels by speaker, resamples to 16 kHz and detects speech, then hands off to GPU speech recognition and LLM analyzers that load into Postgres. Every stage writes outputs keyed by recording, so a retry or a rerun after a crash never pays twice. Rust types are generated from the Python contracts' JSON Schema, and CI fails on drift.
- **Collectibles market intelligence.** Valuation from sold comps with provenance, anomaly signals on recent sales, and vision models that read live-stream frames. Web, Chrome extension, desktop (Electron) and phone (Expo) clients share one generated OpenAPI client, and import-linter enforces the backend's module layering.
- **Insurance retention models.** Lapse and commission models built from the carrier reports agencies already receive. CatBoost and survival models tuned with Optuna and tracked in MLflow, published as versioned bundles the API promotes, with Python and TypeScript SDKs generated from the API contract.
- **Insurance agency platform.** Agency management for a network of agents. Django, Next.js, Postgres.
- **Partner messaging and billing.** An immutable, idempotent credit ledger for SMS: credits are reserved before a send, consumed on a confirmed delivery and released on a confirmed failure, so duplicate receipts and retries never double-charge.

## Open source

About 200 merged pull requests in tools I use every day, mostly bug fixes and performance work:

| Project | Merged | Examples |
|---|---|---|
| [kitty](https://github.com/kovidgoyal/kitty/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 31 | cursor reports in origin mode, alpha-mask leak when growing the font canvas |
| [calibre](https://github.com/kovidgoyal/calibre/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 28 | content-server path traversal and HTTP framing, book restrictions in full-text search |
| [libtorrent](https://github.com/arvidn/libtorrent/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 25 | SOCKS5 auth bounds, DHT reply matching, disk jobs stranded behind fences |
| [docling](https://github.com/docling-project/docling/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 11 | faster layout and table-cell matching, pipeline cache key collisions |
| [qBittorrent](https://github.com/qbittorrent/qBittorrent/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 8 | macOS UI fixes |
| [Mole](https://github.com/tw93/Mole/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) | 24 | fail-closed deletes, cancellable scans, faster purge |
| [fallow](https://github.com/fallow-rs/fallow/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) (Rust) | 34 | barrel re-export resolution, framework conventions, MCP trace tools |
| [pyscn](https://github.com/ludo-technologies/pyscn/pulls?q=is:pr+author:M-Hassan-Raza+is:merged) (Go) | 33 | clone detection (APTED, LSH), dependency analysis that scales |

## Smaller things

- [cogitator](https://github.com/M-Hassan-Raza/cogitator): local code search in about 500 lines of OCaml. TF-IDF over code chunks, ranked by cosine similarity.
- [go-load-balancer-dash](https://github.com/M-Hassan-Raza/go-load-balancer-dash): an HTTP load balancer and dashboard in Go, written to see what a reverse proxy does before trusting one.

## Tools

Python (FastAPI, Django, SQLAlchemy, Pydantic AI, LangGraph), TypeScript (React, TanStack, Next.js, Vue), Rust, Go, C++, Postgres, Redis, AWS.
