# Trade Types

## hedge

Hedge mode allows separate long and short positions on the same symbol.

## reverse

Reverse mode uses one-way position logic. A new order follows the current direction logic of the connector.

## opposite

Opposite mode is not available for MEXC yet in this repository.

## flat action

`flat` is used to close an existing position.

In hedge mode, `close_side` can be used to specify which side should be closed:

- `long`
- `short`
