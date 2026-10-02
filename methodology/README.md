# Apex Reentry methodology

Status: supplied-rule specification; execution definitions and backtests pending.

Sequence: first New York session candle → breakout → return → rejection → entry. Target 3R; break-even stop adjustment at 2R; planned risk 1% of defined account equity; maximum one entry per day.

## Open definitions

- Select the instrument, data provider and candle timeframe.
- Define the session opening timestamp in `America/New_York` and its daylight-saving behavior. Do not hard-code a fixed Mexico-time offset.
- Define breakout by wick, close or another precise criterion; define what counts as a return and a rejection.
- Define entry timing, stop placement, signal expiration, cancellation and one-entry-per-day behavior after stop or break-even.
- Define whether break-even means entry price or cost-adjusted entry, how 2R is detected and when the new stop becomes executable.
- Define position sizing, tick size, contract value, spreads, fees, slippage, gaps and same-bar SL/TP ordering.

## Evaluation plan

Freeze rules before evaluating. Store data provenance, configuration, strategy version, time range and trade logs. Separate development and out-of-sample data and assess sensitivity to costs and session definitions. Report realized R multiples, trade count, drawdown, net expectancy and holding times only from actual runs. No results currently exist.
