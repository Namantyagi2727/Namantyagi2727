![Naman Tyagi — an ink-blue notebook cover with a routing diagram sketched across it](assets/header.svg)

I build systems that sit in the unglamorous middle of AI infrastructure — gateways, retrieval pipelines, and the plumbing that keeps an LLM call reliable once it leaves a notebook. Most of what's below is code I wrote and ran myself, not a slide deck.

MS in Computer Science, NYU Tandon (2026) · Brooklyn, NY

[Portfolio](https://namantyagi.dev) · [LinkedIn](https://www.linkedin.com/in/naman-tyagi-nt2727) · [Email](mailto:namantyagi2727@gmail.com) · [Research](https://scholar.google.com/citations?hl=en&user=JNOaY9YAAAAJ)

## Selected builds

### [Prism](https://github.com/Namantyagi2727/prism) — LLM gateway & control plane
A self-hosted proxy that sits between an app and whichever provider it's actually calling — Ollama, OpenAI, Anthropic — with a hand-rolled circuit breaker for automatic failover, PII/prompt-injection guardrails, and per-request cost tracking. A Locust load test caught a real bug (every request opened a fresh Redis connection, driving a 77% error rate at ~300 req/s until fixed), then pushed a simulated total-provider outage through the fallback chain at a 0.00% failure rate across 31,488 requests.
`FastAPI · PostgreSQL/pgvector · Redis · Prometheus/Grafana/Jaeger` · [project page](https://namantyagi2727.github.io/prism/)

### [RAGBase](https://github.com/Namantyagi2727/ragbase) — offline document Q&A
Fully local RAG over your own PDFs, spreadsheets, and scanned images — no cloud, no API key. Hybrid retrieval merges FAISS semantic search with TF-IDF keyword search and reranks with a cross-encoder; numeric questions over CSV/Excel get answered by auto-generated pandas code instead of a guess from the LLM.
`Python · LangChain · FAISS · Ollama · Streamlit`

### [ConTicx](https://github.com/Namantyagi2727/ConTicx) — concert ticketing (Juspay take-home)
A booking flow with a real payment integration against Hyperswitch's sandbox. The server, never the client, computes the charge; inventory holds expire lazily and cancel the Hyperswitch payment intent first, so a seat can't be resold in the same window its hold happens to lapse. A spike-test script fires concurrent orders at one tier and confirms the atomic `DECRBY` never oversells.
`Next.js · TypeScript · Redis · Hyperswitch` · [live demo](https://conticx.vercel.app)

### [Immune Cell Population Analysis](https://github.com/Namantyagi2727/teiko-cell-population-analysis) — Teiko take-home
A normalized SQLite pipeline over a clinical-trial dataset: per-sample cell-population frequencies, a Mann-Whitney U comparison of treatment responders vs. non-responders with Benjamini-Hochberg correction, and an effect-size check (rank-biserial r) so a low p-value doesn't get over-read. Deterministic end to end — reruns are byte-identical — backed by a 15-test regression suite.
`Python · pandas · SQLite · Streamlit` · [live dashboard](https://teiko-cell-population-analysis-dashboard.streamlit.app/)

## Current work & research

Right now I'm contributing to a real-time detection pipeline over a continuous endoscopic camera feed at NYU's FAMS Lab, validating detection in a simulated renal environment — water and calcium-based model kidney stones — before any real-tissue work. Earlier this year I led the system design for a faculty-operations platform inside NYU's Office of Faculty Affairs, twelve Django apps and 306 automated tests, which stays internal to the university rather than public.

Alongside that, I've co-authored a handful of publications spanning IEEE, Wiley, and Cambridge Scholars Publishing, on topics from sign-language recognition to AI ethics in decision-making. The full list is on [Google Scholar](https://scholar.google.com/citations?hl=en&user=JNOaY9YAAAAJ).

## Tools

`Python · TypeScript · PyTorch · LangChain · FAISS · OpenCV`
`FastAPI · Next.js · PostgreSQL · Redis · Docker`
`Prometheus · Grafana · OpenTelemetry`

## Outside the work

Most resets are small: a pot of tea, an F1 session on in the background, a controller in hand, or a session at the gym before the next build starts.

---

More detail — diagrams, dashboards, case studies — lives on [my portfolio](https://namantyagi.dev). Otherwise, [say hi](mailto:namantyagi2727@gmail.com).
