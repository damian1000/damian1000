# Damian Howard

Senior / Staff Software Engineer in London with 20+ years of experience building
trading, pricing, risk, and post-trade systems for investment banks and financial
technology firms.

Currently working at **Citi via JUXT** (part of **Grid Dynamics**), focused on
distributed cross-asset risk orchestration and intraday/EOD risk processing.

[LinkedIn](https://linkedin.com/in/damianhoward) | [GitHub](https://github.com/damian1000)

## What I Work On

- Front-office pricing, risk, and trade-lifecycle platforms
- High-throughput and event-driven JVM systems
- Low-latency, concurrent, and memory-sensitive applications
- Kafka, FIX, REST, and gRPC integration
- AI-assisted engineering workflows for implementation, testing, and review

## Selected Experience

- **Citi via JUXT** — cross-asset risk orchestration and intraday/EOD risk
  processing *(March 2026 - present)*
- **Morgan Stanley** — front-office pricing and risk for CDS Index Options and
  Structured Credit *(September 2023 - February 2026)*
- **CMC Markets** — low-latency options pricing and FIX connectivity using
  Chronicle Map off-heap storage *(March 2023 - September 2023)*
- **Blockchain.com** — institutional prime brokerage and treasury automation
  across Coinbase, Kraken, Binance, and Bitfinex *(April 2021 - January 2023)*
- **Goldman Sachs and Credit Suisse** — earlier engagements across equities
  booking, securities lending, market risk, and reference-data platforms

## Selected Engineering Work

A live trading stack: a limit order book with three concurrency strategies (an LMAX Disruptor
ring buffer beats a read/write lock by roughly 6× under contention), a Black-Scholes risk engine
cross-validated against OpenGamma Strata, and a Kafka-based integration layer turning fills into
live positions, VaR, and PnL. All three run together in
[trading-desk](https://github.com/damian1000/trading-desk):

**▶ Explore it live: https://desk.damianhoward.com**

Individually: [orderbook](https://github.com/damian1000/orderbook),
[risk-engine](https://github.com/damian1000/risk-engine),
[trading-system](https://github.com/damian1000/trading-system).

Also: [portfolio-manager](https://github.com/damian1000/portfolio-manager) (dry-run-by-default
exchange clients for Binance and Bitfinex) and
[stocks-analysis-us](https://github.com/damian1000/stocks-analysis-us) (a six-stage
fundamentals-ranking pipeline for US equities). Smaller repos cover
[Kafka Streams patterns](https://github.com/damian1000/kafka-streams-patterns),
[real instrument quotes](https://github.com/damian1000/market-data),
[Dancing Links](https://github.com/damian1000/sudoku-dancing-links),
[blockchain internals](https://github.com/damian1000/kotlin-blockchain), and a
[bank CSV to QIF converter](https://github.com/damian1000/bank-csv-to-qif).

## AI-Assisted Engineering

Contributed to **[Meridian](https://www.juxt.pro/meridian/)**, JUXT's
equity-derivatives post-trade risk accelerator. Meridian supports valuation,
Greeks, scenario analysis, and continuously updating risk on a bitemporal
datastore.

My work covered the **ticking-risk engine**, **scenario-analysis workflow**, and
resilient recovery of long-running valuation tasks across Kotlin,
Python/QuantLib, and TypeScript. I used Claude Code as part of an agentic
engineering workflow spanning implementation, testing, and review — the same
workflow behind the repositories above.

I also contributed to a privately developed AI-assistant platform, delivering a
cross-platform notifications service for alerting, validated response capture,
and scoped delivery across distributed services.

## Technology

- **Languages:** Java, Kotlin, Scala, Python, TypeScript
- **Trading and integration:** FIX, Kafka, REST, gRPC
- **Platforms:** OpenShift, AWS, GCP, Docker
- **Domains:** pricing, risk, trade lifecycle, post-trade, prime brokerage,
  treasury automation

For professional enquiries, contact me through
[LinkedIn](https://linkedin.com/in/damianhoward).
