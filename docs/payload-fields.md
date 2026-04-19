# Payload Fields

## Required fields

- `symbol` — instrument symbol, for example `BTCUSDT`
- `side` — `buy`, `sell`, or `flat`
- `quantity` — base asset quantity
- `trade_type` — `hedge` or `reverse`
- `margin_mode` — `isolated` or `cross`
- `leverage` — integer leverage value

## Optional fields

- `stop_loss` — stop loss distance in pips
- `take_profit` — take profit distance in pips
- `sl_price` — absolute stop loss price
- `tp_price` — absolute take profit price
- `trailing_pips` — trailing stop distance
- `trigger` — `last`, `mark`, or `index`
- `close_side` — `long` or `short`, used for hedge flat actions

## Notes

- `sl_price` and `tp_price` are absolute price values.
- `stop_loss` and `take_profit` are distance-based values.
- `close_side` is only relevant when `side` is `flat` in hedge mode.
- `opposite` mode is not currently available for MEXC in this public example repository.
