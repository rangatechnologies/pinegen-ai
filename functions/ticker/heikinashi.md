---
title: "ticker.heikinashi"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.heikinashi
---

# ticker.heikinashi

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.heikinashi(symbol) → simple string
```

```pinescript
ticker.heikinashi(symbol) → series string
```

## Description

Creates a ticker identifier for requesting Heikin Ashi bar values.

## Arguments

- **`symbol`** `simple string` — Symbol ticker identifier.

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker.heikinashi", overlay=true)
heikinashi_close = request.security(ticker.heikinashi(syminfo.tickerid), timeframe.period, close)

heikinashi_aapl_60_close = request.security(ticker.heikinashi("AAPL"), "60", close)
plot(heikinashi_close)
plot(heikinashi_aapl_60_close)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [request.security()](../request/security.md)
- [ticker.renko()](./renko.md)
- [ticker.linebreak()](./linebreak.md)
- [ticker.kagi()](./kagi.md)
- [ticker.pointfigure()](./pointfigure.md)
