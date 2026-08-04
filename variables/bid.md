---
title: "bid"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_bid
---

# bid

**Category:** Variable

**Type:** `series float`

## Description

The bid price at the time of the current tick, which represents the highest price an active buyer is willing to pay for the instrument at its current value. This information is available only on the "1T" timeframe. On other timeframes, the variable's value is [na](./na.md).

## Remarks

If the bid/ask values change since the last tick but no new trades are made, these changes will not be reflected in the value of this variable. It is only updated on new ticks.

## See also

- [open](./open.md)
- [high](./high.md)
- [low](./low.md)
- [volume](./volume.md)
- [time()](../functions/time.md)
- [hl2](./hl2.md)
- [hlc3](./hlc3.md)
- [hlcc4](./hlcc4.md)
- [ohlc4](./ohlc4.md)
- [ask](./ask.md)
