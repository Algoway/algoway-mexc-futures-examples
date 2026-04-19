# How to Automate TradingView Alerts to MEXC Futures with AlgoWay

Public examples and payload templates for automating TradingView alerts on MEXC Futures through AlgoWay.

## What this repository is

This repository shows how to automate TradingView alerts to MEXC Futures using AlgoWay as the execution bridge.

It contains public examples, JSON payload templates, and field documentation for MEXC Futures automation.

It does not contain the private AlgoWay MEXC connector source code.

## What this repository helps you do

With these examples, you can understand how to structure TradingView alert payloads for:

- opening long positions
- opening short positions
- closing positions
- using hedge mode
- using reverse mode
- passing stop loss and take profit parameters
- using trailing stop parameters for MEXC workflows

## How the flow works

TradingView alert or TradingView strategy  
→ JSON payload  
→ AlgoWay webhook  
→ private AlgoWay MEXC connector  
→ MEXC Futures order execution

## Supported order actions

- `buy`
- `sell`
- `flat`

## Supported trade types

- `hedge`
- `reverse`
- `opposite` — not available for MEXC yet

## Basic TradingView to MEXC payload example

```json
{
  "symbol": "BTCUSDT",
  "side": "buy",
  "quantity": 0.01,
  "trade_type": "hedge",
  "margin_mode": "isolated",
  "leverage": 10
}
```

## Available parameters

### Required fields

- `symbol`
- `side`
- `quantity`
- `trade_type`
- `margin_mode`
- `leverage`

### Optional risk parameters

- `stop_loss`
- `take_profit`
- `sl_price`
- `tp_price`
- `trailing_pips`
- `trigger`
- `close_side`

## Example files in this repository

- `examples/buy-hedge.json`
- `examples/sell-reverse.json`
- `examples/flat-hedge-long.json`
- `examples/buy-with-sl-tp.json`

## Repository structure

- `examples/` — ready-to-use JSON payload examples for TradingView alerts
- `docs/` — field descriptions, trade type notes, and MEXC-specific behavior
- `postman/` — API request collection if added later

## Important notes

- Quantity is provided as base asset size.
- The private AlgoWay connector converts the requested quantity internally for MEXC Futures execution.
- Symbol normalization and exchange-side symbol matching are handled by the private connector.
- This repository is public documentation and examples only.

## Why this repository exists

Many traders search for ways to automate TradingView alerts to MEXC, but most public examples are either very small bots or incomplete snippets.

This repository exists to provide a clearer public reference for TradingView webhook automation to MEXC Futures through AlgoWay.

## Related documentation

See the files in `docs/` for payload field explanations, trade types, and SL/TP or trailing behavior.
