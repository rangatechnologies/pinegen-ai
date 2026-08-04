---
title: "ta.wpr"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.wpr
---

# ta.wpr

**Category:** Function

## Syntax

```pinescript
ta.wpr(length) → series float
```

## Description

Williams %R. The oscillator shows the current closing price in relation to the high and low of the past 'length' bars.

## Arguments

- **`length`** `series int` — Number of bars.

## Returns

Williams %R.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("Williams %R", shorttitle="%R", format=format.price, precision=2)
plot(ta.wpr(14), title="%R", color=color.new(#ff6d00, 0))
```

## See also

- [ta.mfi()](./mfi.md)
- [ta.cmo()](./cmo.md)
