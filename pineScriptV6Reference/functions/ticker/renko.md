---
title: "ticker.renko"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.renko
---

# ticker.renko

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.renko(symbol, style, param, request_wicks, source) → simple string
```

```pinescript
ticker.renko(symbol, style, param, request_wicks, source) → series string
```

## Description

Creates a ticker identifier for requesting Renko values.

## Arguments

- **`symbol`** `simple string` — Symbol ticker identifier.
- **`style`** `simple string` — Specifies the ticker's box size assignment method. Possible values: "ATR" for Average True Range sizing, "Traditional" to use a fixed size, or "PercentageLTP" to use a percentage of the last trading price. 
- **`param`** `simple int/float` — Represents the ticker's "ATR length" value if the `style` value is "ATR", "Box size" value if the `style` is "Traditional", or "Percentage" value if the `style` is "PercentageLTP". 
- **`request_wicks`** `simple bool` (optional) — Specifies if wick values are returned for Renko bricks. When [true](../../constants/true.md), [high](../../variables/high.md) and [low](../../variables/low.md) values requested from a symbol using the ticker formed by this function will include wick values when they are present. When [false](../../constants/false.md), [high](../../variables/high.md) and [low](../../variables/low.md) will always be equal to either [open](../../variables/open.md) or [close](../../variables/close.md). Optional. The default is [false](../../constants/false.md). A detailed explanation of how Renko wicks are calculated can be found in our [Help Center](https://www.tradingview.com/support/solutions/43000481040-what-do-renko-wicks-mean/).
- **`source`** `simple string` (optional) — The source used to calculate bricks. Optional. Possible values: "Close", "OHLC". The default is "Close".

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Detailed Description



```pinescript
//@version=6
indicator("Renko candles", overlay=false)
renko_tickerid = ticker.renko(syminfo.tickerid, "ATR", 10)
[renko_open, renko_high, renko_low, renko_close] = request.security(renko_tickerid, timeframe.period, [open, high, low, close])
plotcandle(renko_open, renko_high, renko_low, renko_close, color = renko_close > renko_open ? color.green : color.red)
```

## Examples

```pinescript
//@version=6
indicator("ticker.renko", overlay=true)
renko_tickerid = ticker.renko(syminfo.tickerid, "ATR", 10)
renko_close = request.security(renko_tickerid, timeframe.period, close)
plot(renko_close)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [request.security()](../request/security.md)
- [ticker.heikinashi()](./heikinashi.md)
- [ticker.linebreak()](./linebreak.md)
- [ticker.kagi()](./kagi.md)
- [ticker.pointfigure()](./pointfigure.md)
