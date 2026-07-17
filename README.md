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

Live trading infrastructure, built end-to-end outside any employer's codebase:

### [orderbook](https://github.com/damian1000/orderbook)

**▶ Live: https://orderbook.damianhoward.com** — submit an order and watch it
match resting liquidity in real time.

A thread-safe limit order book and price-time-priority matching engine in Kotlin.
It preserves FIFO time priority across size changes and offers three
interchangeable concurrency strategies — lock-based, single-writer, and an LMAX
Disruptor busy-spin ring buffer that wins every contended JMH workload (about 6×
the lock's throughput on write-heavy load, with far tighter variance) — behind a
dependency-free web front end over Server-Sent Events. Backed by deterministic
concurrency stress tests, tail-latency (p50/p99/p99.9) and allocation benchmarks,
and a 90% coverage gate under CI, CodeQL, and dependency review.

### [risk-engine](https://github.com/damian1000/risk-engine)

**▶ Live: https://risk.damianhoward.com** — edit a book and market, and watch
the valuation, Greeks, both VaR methods, and the day's PnL recompute.

A risk framework for a vanilla equity option: closed-form Black-Scholes pricing
with bump-and-reprice Greeks, hand-written in Kotlin rather than delegated to a
pricing library.
Correctness is validated two independent ways — golden-value tests against a
published textbook reference, and property-based tests (put-call parity, delta
bounds, monotonicity) generating thousands of cases per invariant.

### [trading-system](https://github.com/damian1000/trading-system)

**▶ Live: https://trading.damianhoward.com** — watch positions, risk, and PnL
update as orders fill on the live order book.

The integration layer over the two systems above, consumed as versioned
libraries rather than rebuilt. A plain kafka-clients consumer takes the order
book's fill stream, books net positions into an Oracle Autonomous Database
(Flyway-managed, exact-decimal upserts), reprices the book through risk-engine
on every fill, and pushes each snapshot to the dashboard over Server-Sent
Events. Poison records route to a dead-letter topic with error and provenance
headers after bounded retries — a flow integration-tested against a real broker
and a real Oracle instance via Testcontainers, under the same 90% coverage gate.

### [trading-desk](https://github.com/damian1000/trading-desk)

**▶ Live: https://desk.damianhoward.com** — orderbook, risk-engine, and
trading-system in one shell, no separate tabs to juggle.

A reverse-proxy gateway that mounts the three live sites above under one
origin, stripping path prefixes and streaming responses so each service's
own Server-Sent Events keep working unbuffered end to end.

### [portfolio-manager](https://github.com/damian1000/portfolio-manager)

Kotlin clients for authenticated Binance and Bitfinex APIs, including venue-local
HMAC signing and mockable HTTP boundaries. The Bitfinex withdrawal workflow is
dry-run by default and requires explicit confirmation, with destination redaction
and local audit logging.

### [stocks-analysis-us](https://github.com/damian1000/stocks-analysis-us)

Spring Boot US-equities screener with six synchronous, in-process pipeline stages,
PostgreSQL/Flyway persistence, configurable PEG-style ranking, and Excel export.
Tests include fixture-driven source parsing and Testcontainers validation against
PostgreSQL 17.

Other repositories cover
[Kafka Streams patterns](https://github.com/damian1000/kafka-streams-patterns),
[real instrument quotes for the live order book](https://github.com/damian1000/market-data),
[Dancing Links / Algorithm X](https://github.com/damian1000/sudoku-dancing-links),
[proof-of-work and UTXO mechanics](https://github.com/damian1000/kotlin-blockchain),
and a [bank CSV to QIF converter](https://github.com/damian1000/bank-csv-to-qif).

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
