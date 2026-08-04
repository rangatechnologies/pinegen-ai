---
title: "ticker.kagi"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.kagi
---

# ticker.kagi

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
ticker.kagi(symbol, reversal) → simple string
```

```pinescript
ticker.kagi(symbol, reversal) → series string
```

```pinescript
ticker.kagi(symbol, param, style) → simple string
```

```pinescript
ticker.kagi(symbol, param, style) → series string
```

## Description

Creates a ticker identifier for requesting Kagi values.

## Arguments

- **`symbol`** `simple string` — Symbol ticker identifier.
- **`reversal`** `simple int/float` — Reversal amount (absolute price value).

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker.kagi", overlay=true)
kagi_tickerid = ticker.kagi(syminfo.tickerid, 3)
kagi_close = request.security(kagi_tickerid, timeframe.period, close)
plot(kagi_close)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [request.security()](../request/security.md)
- [ticker.heikinashi()](./heikinashi.md)
- [ticker.renko()](./renko.md)
- [ticker.linebreak()](./linebreak.md)
- [ticker.pointfigure()](./pointfigure.md)
