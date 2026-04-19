# SL TP and Trailing

## Absolute price parameters

- `sl_price` sets an exact stop loss price
- `tp_price` sets an exact take profit price

## Distance parameters

- `stop_loss` sets stop loss distance
- `take_profit` sets take profit distance

## Trailing

- `trailing_pips` sets trailing stop distance
- `trigger` defines the reference price type:
  - `last`
  - `mark`
  - `index`

## Notes

- Absolute price parameters and distance parameters should not be mixed unless the connector logic explicitly supports it.
- `trigger` is mainly relevant when trailing or trigger-based execution is used.
