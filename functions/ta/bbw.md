---
title: "ta.bbw"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.bbw
---

# ta.bbw

**Category:** Function

## Syntax

```pinescript
ta.bbw(series, length, mult) → series float
```

## Description

Bollinger Bands Width. The Bollinger Band Width is the difference between the upper and the lower Bollinger Bands divided by the middle band.

## Arguments

- **`series`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).
- **`mult`** `simple int/float` — Standard deviation factor.

## Returns

Bollinger Bands Width.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("ta.bbw")

plot(ta.bbw(close, 5, 4), color=color.yellow)

// the same on pine
f_bbw(src, length, mult) =>
    float basis = ta.sma(src, length)
    float dev = mult * ta.stdev(src, length)
    (((basis + dev) - (basis - dev)) / basis) * 100

plot(f_bbw(close, 5, 4))
```

## See also

- [ta.bb()](./bb.md)
- [ta.sma()](./sma.md)
- [ta.stdev()](./stdev.md)
