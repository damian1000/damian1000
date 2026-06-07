# Damian Howard

Senior / Staff Software Engineer with 20+ years building distributed trading, pricing, and risk platforms for global investment banks. Currently at **Citi** via **JUXT** (part of **Grid Dynamics**), based in London.

I specialise in high-throughput, event-driven systems across **front-office risk, pricing, and trade lifecycle workflows** using Java, Kotlin, Scala, Kafka, FIX, OpenShift, AWS, and GCP.

💼 [LinkedIn](https://linkedin.com/in/damianhoward)  
💻 [GitHub](https://github.com/damian1000)

---

## Recent

- **Citi** via JUXT — distributed cross-asset risk orchestration and intraday/EOD risk processing *(Mar 2026 – present)*
- **Morgan Stanley** — front-office pricing & risk for CDS Index Options and Structured Credit *(Sept 2023 – Feb 2026)*
- **CMC Markets** — low-latency options pricing and FIX connectivity using Chronicle Map off-heap storage *(Mar 2023 – Sept 2023)*
- **Blockchain.com** — institutional prime brokerage and treasury automation across Coinbase, Kraken, Binance, and Bitfinex *(Apr 2021 – Jan 2023)*
- Earlier: multiple contracts at **Goldman Sachs** and **Credit Suisse** across equities booking, securities lending, market risk, and reference data platforms

---

## Selected open-source

### [kotlin-orderbook](https://github.com/damian1000/kotlin-orderbook)

Thread-safe limit order book in Kotlin with time-priority modify support. Includes JMH benchmarks on JDK 25 with nanosecond-scale best-bid lookups and sub-microsecond order operations.

### [kotlin-blockchain](https://github.com/damian1000/kotlin-blockchain)

Small Kotlin blockchain demonstrating proof-of-work mining, UTXO accounting, and RSA-signed transactions. Pure JDK + Kotlin, no third-party crypto library.

### [sudoku-dancing-links](https://github.com/damian1000/sudoku-dancing-links)

Knuth's Algorithm X (Dancing Links) Sudoku solver in Java alongside a naive backtracking baseline. ~20× perf gap on hard puzzles, identical solutions verified by JUnit.

### [kafka-microservices-demo](https://github.com/damian1000/kafka-microservices-demo)

Spring Boot 4 + Kafka 4 quote/order workflow demonstrating non-blocking retry with `@RetryableTopic`, automatic dead-letter routing, and event-driven microservice patterns.

### [kafka-streams-patterns](https://github.com/damian1000/kafka-streams-patterns)

Four Kafka Streams DSL topologies — wordcount, tumbling-window aggregation, KStream–KStream join, and KStream–KTable enrichment join — with a single-node KRaft docker-compose for local runs.

### [portfolio-manager](https://github.com/damian1000/portfolio-manager)

Multi-venue position aggregation across Binance and Bitfinex with HMAC-signed REST integration, resilient transport abstractions, and mockable exchange connectivity. Kotlin.

### [stocks-analysis-us](https://github.com/damian1000/stocks-analysis-us)

Event-driven US equities analysis pipeline using Spring Boot 4 with pluggable ranking stages, screening workflows, and Excel export.

---

## Agentic engineering

Contributed to **Meridian** at JUXT (Grid Dynamics) — a derivatives-risk **solution accelerator** supporting live valuation, Greeks, scenario analysis, and continuous intraday revaluation on a bitemporal datastore.

My work covered the **live-ticking engine**, **scenario-analysis workflow**, and **crash-only task-recovery model** for long-running valuations across Kotlin, Python/QuantLib, and TypeScript. Built with Claude Code in an agentic workflow.

Also contributed to **Stellar AI** — a private AI-assistant platform built primarily through agentic coding workflows with Claude Code. Delivered a cross-platform notifications service for alerting, response capture, validation, and scoped delivery across distributed services.

---

## Focus

- High-throughput JVM systems: Java, Kotlin, Scala
- Event-driven architecture: Kafka, FIX, REST, gRPC
- Front-office pricing, intraday risk, and trade lifecycle workflows
- Low-latency and memory-sensitive systems
- Agentic engineering workflows and AI-assisted development

Happy to chat about JVM trading systems, risk platforms, or agentic engineering workflows — reach me on [LinkedIn](https://linkedin.com/in/damianhoward).
