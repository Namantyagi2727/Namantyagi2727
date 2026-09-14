![Naman Tyagi — an ink-blue notebook cover with a routing diagram sketched across it](assets/header.svg)

I build AI infrastructure and applications, from LLM gateways and retrieval pipelines to computer-vision systems.

MS in Computer Science, NYU Tandon (2026) · Brooklyn, NY

[Portfolio](https://namantyagi.dev) · [LinkedIn](https://www.linkedin.com/in/naman-tyagi-nt2727) · [Email](mailto:namantyagi2727@gmail.com) · [Research](https://scholar.google.com/citations?hl=en&user=JNOaY9YAAAAJ)

## Selected builds

### [Prism](https://github.com/Namantyagi2727/prism) — LLM gateway & control plane
A self-hosted proxy that routes calls to Ollama, OpenAI, or Anthropic behind one interface, with a hand-rolled circuit breaker for failover, PII/prompt-injection guardrails, and per-request cost tracking. In a Locust load test simulating a total provider outage, the fallback chain held at a 0.00% failure rate across 31,488 requests — a controlled test at hundreds of requests/second, not a production-traffic claim.
`FastAPI · PostgreSQL/pgvector · Redis · Prometheus/Grafana/Jaeger` · [project page](https://namantyagi2727.github.io/prism/)

### [RAGBase](https://github.com/Namantyagi2727/ragbase) — offline document Q&A
Fully local retrieval-augmented Q&A over your own PDFs, spreadsheets, and scanned images — no cloud, no API key. Combines FAISS semantic search with TF-IDF keyword search and a cross-encoder reranker, running entirely against a local Ollama model.
`Python · LangChain · FAISS · Ollama · Streamlit`

### [ConTicx](https://github.com/Namantyagi2727/ConTicx) — concert ticketing (Juspay take-home)
A ticket-booking flow with a real payment integration against Hyperswitch's sandbox. The server always computes the charge, and inventory holds are reserved atomically in Redis so concurrent purchases can't oversell a tier — checked with a concurrent-request spike test.
`Next.js · TypeScript · Redis · Hyperswitch` · [live demo](https://conticx.vercel.app)

### [Immune Cell Population Analysis](https://github.com/Namantyagi2727/teiko-cell-population-analysis) — Teiko take-home
A statistical analysis of a clinical-trial dataset, asking whether immune-cell population frequencies predict treatment response. Runs significance testing with multiple-comparison correction and reports effect size alongside p-values, so a marginal result doesn't get oversold. Deterministic and regression-tested end to end.
`Python · pandas · SQLite · Streamlit` · [live dashboard](https://teiko-cell-population-analysis-dashboard.streamlit.app/)

### [Airspace Congestion Monitoring](https://github.com/Namantyagi2727/airspace-congestion-monitoring) — team project
A real-time flight-congestion pipeline built with two teammates, forked from [Sanyuktatuti's original](https://github.com/Sanyuktatuti/airspace-congestion-monitoring): Kafka ingestion, Spark Structured Streaming risk scoring over sliding windows, fanned out to InfluxDB, MongoDB, and a Streamlit dashboard. The 475K+-record historical dataset used for load testing is generated, not observed — live ingestion pulls the real OpenSky API.
`Apache Spark · Kafka · InfluxDB · MongoDB · Python`

## Current work & research

Currently contributing to a real-time detection pipeline over a continuous endoscopic camera feed at NYU's FAMS Lab, validating detection in a simulated renal environment before any real-tissue work. Earlier in 2026 I led the system design for a faculty-operations platform inside NYU's Office of Faculty Affairs — twelve Django apps, 306 automated tests — which stays internal to the university.

I've also co-authored publications spanning IEEE, Wiley, and Cambridge Scholars Publishing. Full list on [Google Scholar](https://scholar.google.com/citations?hl=en&user=JNOaY9YAAAAJ).

## Tools

`Python · TypeScript · PyTorch · LangChain · FAISS · OpenCV`
`FastAPI · Next.js · PostgreSQL · Redis · Docker`
`Prometheus · Grafana · OpenTelemetry`

## Outside the work

Outside work, I'm usually making tea, watching F1, gaming, or training.

---

More detail — diagrams, dashboards, case studies — lives on [my portfolio](https://namantyagi.dev). Otherwise, [say hi](mailto:namantyagi2727@gmail.com).
