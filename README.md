<p align="center">
  <a href="https://polyedge.dev">
    <img src="https://polyedge.dev/logo.svg" alt="PolyEdge Logo" width="160" />
  </a>
</p>

<h1 align="center">PolyEdge</h1>

<p align="center">
  <b>Ultra-Low-Latency Polymarket Mempool Trade Streaming & Real-Time On-Chain Analytics API.</b><br>
  <i>Engineered for Polymarket copy-trading bots, professional traders, and prediction market builders.<br>
  Capture pending trades pre-block and track smart money with institutional-grade on-chain analytics.</i>
</p>

<p align="center">
  <a href="https://polyedge.dev"><b>Website</b></a> •
  <a href="https://polyedge.dev/docs"><b>Documentation</b></a> •
  <a href="https://polyedge.dev/console"><b>Console</b></a> •
  <a href="https://github.com/PolyEdgeDev/polyedge-stream-benchmark"><b>Benchmarks</b></a>
</p>

---

## ⚡ The World's Fastest Polymarket Mempool Engine

PolyEdge peers directly with **100+ Polygon validator P2P gossip nodes** to detect raw `CTFExchange` matching transactions in the mempool before block confirmation:

- **Pre-Block Lead**: Sub-second execution detection before trades are packaged on-chain.
- **Data Completeness**: Natively bundles market question, condition ID, slug, and all matched CLOB maker orders into each trade event — **eliminating secondary REST queries**.
- **100% Reproducible Empirical Benchmarks**: [Verify the latency lead yourself](https://github.com/PolyEdgeDev/polyedge-stream-benchmark).

### 📊 Benchmark Results

| Comparison Target | PolyEdge Faster % | P50 Lead | P90 Lead | P99 Lead | Max Lead |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **PolyEdge vs On-Chain Block Time** | 100.0% | +2,038 ms ✓ | +2,924 ms ✓ | +3,293 ms ✓ | +3,411 ms ✓ |
| **PolyEdge vs Polymarket RTDS** | 100.0% | +1,747 ms ✓ | +2,534 ms ✓ | +2,944 ms ✓ | +3,047 ms ✓ |
| **PolyEdge vs PolyNode WS** | 98.9% | +25 ms ✓ | +42 ms ✓ | +62 ms ✓ | +245 ms ✓ |

*\* Positive lead time (+) with ✓ indicates PolyEdge delivered the trade faster than the target.*

---

## 📦 Official Client SDKs

PolyEdge provides official, production-ready SDKs across four major programming languages, featuring built-in 45s keep-alive watchdogs, automatic `Last-Event-ID` resumption, and full OpenAPI 3.1 coverage:

| Language | Repository | Package | Installation |
| :--- | :--- | :--- | :--- |
| **Node.js / TS** | [`PolyEdgeDev/polyedge-ts`](https://github.com/PolyEdgeDev/polyedge-ts) | [![npm](https://img.shields.io/npm/v/polyedge.svg?color=blue&cache=1)](https://www.npmjs.com/package/polyedge) | `npm install polyedge` |
| **Python** | [`PolyEdgeDev/polyedge-python`](https://github.com/PolyEdgeDev/polyedge-python) | [![PyPI](https://img.shields.io/pypi/v/polyedge.svg?color=blue&cache=1)](https://pypi.org/project/polyedge/) | `pip install polyedge` |
| **Go** | [`PolyEdgeDev/polyedge-go`](https://github.com/PolyEdgeDev/polyedge-go) | [![Go Reference](https://pkg.go.dev/badge/github.com/PolyEdgeDev/polyedge-go.svg)](https://pkg.go.dev/github.com/PolyEdgeDev/polyedge-go) | `go get github.com/PolyEdgeDev/polyedge-go` |
| **Rust** | [`PolyEdgeDev/polyedge-rust`](https://github.com/PolyEdgeDev/polyedge-rust) | [![Crates.io](https://img.shields.io/crates/v/polyedge.svg?color=blue&cache=1)](https://crates.io/crates/polyedge) | `cargo add polyedge` |

---

## 🏛️ Core Platform Capabilities

### 1. Real-Time Mempool Trade Streams
Subscribe to pending trade executions filtered by wallet addresses, market tags (e.g. `sports`, `crypto`, `elections`), or specific event series slugs with automatic reconnection and buffer replay.

### 2. On-Chain Trade Analytics Engine
- **Trade-by-Trade State Machine**: Dynamic weighted cost basis and realized net PnL derived directly from raw `CTFExchange` match events, eliminating deposit/transfer distortions.
- **Smart Money & Trader Dossiers**: Top trader performance tracking, 24-hour PnL equity curves, win-rate bounds, and Polymarket Taker Rebate Tier telemetry.
- **Protocol Friction Audit**: Automatic deduction of protocol fees and complete settlement resolution.

---

## 🚀 Get Started

1. Create a free developer account at **[polyedge.dev](https://polyedge.dev)**.
2. Obtain your API key from the **[Console](https://polyedge.dev/console)**.
3. Install the SDK for your stack and start streaming:

```bash
# TypeScript
npm install polyedge

# Python
pip install polyedge

# Go
go get github.com/PolyEdgeDev/polyedge-go

# Rust
cargo add polyedge
```
