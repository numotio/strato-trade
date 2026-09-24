# strato-trade

A Rust workspace for crypto trading research I worked on in 2024. It holds strategy models, an order book imbalance backtest, and shared utilities.

## Crates

| Crate | What it holds |
| --- | --- |
| `strato-model` | The strategy models. Order book imbalance (OIR and VOI) with an [hftbacktest](https://github.com/nkaz001/hftbacktest) harness, grid trading, an EMA-cross trend model, delta scalping (Black-Scholes greeks and the futures size needed to hedge), and two options arbitrage screens that build portfolios with linear programming. |
| `strato-utils` | Indicators (SMA, EMA, RMA, ATR), OHLC types, and order book depth helpers. |
| `strato-ddhp` | Dynamic delta hedging with perpetual futures. This is a stub. The design later moved into my private desk. |
| `strato-client` | A client binary. It is currently empty. |
| `strato-portfolio`, `strato-exchange` | Placeholders. |

Option pricing (Black-Scholes and binomial) lives in [strato-pricer](https://github.com/numotio/strato-pricer).

## The imbalance backtest

`strato-model/examples/hft_oir_backtest.rs` runs the order book imbalance model on a month of 1000SHIBUSDT data with an interpolated order-latency model and maker/taker fees. It expects hftbacktest `.npz` data files, which are not in this repo.

## Status

Research code, not maintained.
