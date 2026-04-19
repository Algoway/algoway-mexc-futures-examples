# MEXC Notes

## Quantity handling

Quantity is provided as base asset size.

The private AlgoWay connector converts the requested quantity internally for MEXC Futures execution.

## Symbol handling

Symbol normalization and exchange-side symbol matching are handled by the private connector.

## Trade types

- `hedge` is available
- `reverse` is available
- `opposite` is not available for MEXC yet

## Public repository scope

This repository contains examples and documentation only.

It does not contain the private AlgoWay MEXC connector source code.
