# AlgoWay MEXC Futures Examples

Examples and payload templates for routing TradingView alerts to MEXC Futures through AlgoWay.

## What this repository is

This repository contains public integration examples for MEXC Futures automation with AlgoWay.

It does not contain the private AlgoWay connector source code.

## How it works

TradingView alert or strategy signal  
→ JSON payload  
→ AlgoWay webhook  
→ AlgoWay MEXC connector  
→ MEXC Futures order execution

## Supported order actions

- buy
- sell
- flat

## Supported trade types

- hedge
- reverse
- opposite — not available for MEXC yet

## Basic payload example

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

## Available risk parameters

- stop_loss
- take_profit
- sl_price
- tp_price
- trailing_pips
- trigger
- close_side

## Repository structure

- `examples/` — ready-to-use JSON payload examples
- `docs/` — field descriptions and MEXC notes
- `postman/` — API request collection

## Notes

- Quantity is provided as base asset size.
- AlgoWay converts the requested quantity internally for MEXC Futures execution.
- Symbol handling and exchange-side normalization are managed by the private AlgoWay connector.
