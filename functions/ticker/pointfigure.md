---
title: "ticker.pointfigure"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.pointfigure
---

# ticker.pointfigure

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.pointfigure(symbol, source, style, param, reversal) → simple string
```

```pinescript
ticker.pointfigure(symbol, source, style, param, reversal) → series string
```

## Description

Creates a ticker identifier for requesting Point & Figure values.

## Arguments

- **`symbol`** `simple string` — Symbol ticker identifier.
- **`source`** `simple string` — The source for calculating Point & Figure. Possible values are: 'hl', 'close'.
- **`style`** `simple string` — Specifies the ticker's box size assignment method. Possible values: "ATR" for Average True Range sizing, "Traditional" to use a fixed size, or "PercentageLTP" to use a percentage of the last trading price. 
- **`param`** `simple int/float` — Represents the ticker's "ATR length" value if the `style` value is "ATR", "Box size" value if the `style` is "Traditional", or "Percentage" value if the `style` is "PercentageLTP". 
- **`reversal`** `simple int` — Reversal amount.

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker.pointfigure", overlay=true)
pnf_tickerid = ticker.pointfigure(syminfo.tickerid, "hl", "Traditional", 1, 3)
pnf_close = request.security(pnf_tickerid, timeframe.period, close)
plot(pnf_close)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [request.security()](../request/security.md)
- [ticker.heikinashi()](./heikinashi.md)
- [ticker.renko()](./renko.md)
- [ticker.linebreak()](./linebreak.md)
- [ticker.kagi()](./kagi.md)
