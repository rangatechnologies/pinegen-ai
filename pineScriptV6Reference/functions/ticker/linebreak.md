---
title: "ticker.linebreak"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.linebreak
---

# ticker.linebreak

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.linebreak(symbol, number_of_lines) → simple string
```

```pinescript
ticker.linebreak(symbol, number_of_lines) → series string
```

## Description

Creates a ticker identifier for requesting Line Break values.

## Arguments

- **`symbol`** `simple string` — Symbol ticker identifier.
- **`number_of_lines`** `simple int` — Number of line.

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker.linebreak", overlay=true)
linebreak_tickerid = ticker.linebreak(syminfo.tickerid, 3)
linebreak_close = request.security(linebreak_tickerid, timeframe.period, close)
plot(linebreak_close)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [request.security()](../request/security.md)
- [ticker.heikinashi()](./heikinashi.md)
- [ticker.renko()](./renko.md)
- [ticker.kagi()](./kagi.md)
- [ticker.pointfigure()](./pointfigure.md)
