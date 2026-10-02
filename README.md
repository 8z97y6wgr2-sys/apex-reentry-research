# Apex Reentry Research

A rule-based quantitative research project studying a New York opening-candle breakout, return and rejection sequence with predefined risk management.

## Project Status

**Methodology stage.** Supplied rules are recorded, but no executable implementation, historical dataset or backtest results were found in connected GitHub. This repository contains research documentation only.

## Methodology

1. Identify the first candle of the New York session and its range.
2. Observe a breakout from that opening range.
3. Wait for a return to the relevant range boundary.
4. Require a rejection before entry.
5. Use a target reward/risk ratio of 3:1 and move the stop to break-even at 2R.
6. Risk 1% of the defined account equity per trade, with at most one entry per day.

The opening timestamp, candle timeframe, breakout/rejection definitions, stop placement and fill rules require precise specification before coding. See [methodology](methodology/README.md).

## Repository Structure

`methodology/` · `code/` · `backtests/` · `results/` · `charts/`.

## Tech Stack

Implementation language and engine are not selected in this repository. Python, Pine Script or MQL5 may be evaluated after the rules and data requirements are fixed. No executable code or dependencies are included yet.

## Usage

Read the rule specification and resolve its open definitions. There is currently no indicator, expert advisor or backtest command to run.

## Limitations

The instrument, intraday timeframe and exact New York session definition remain unspecified here. Break-even management can realize a loss after spreads, fees, slippage or gaps. The 1% sizing target does not guarantee a 1% maximum realized loss. No win rate, expectancy, profitability or live-performance guarantee is claimed.
