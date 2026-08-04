---
title: "ta.kcw"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.kcw
---

# ta.kcw

**Category:** Function

## Syntax

```pinescript
ta.kcw(series, length, mult, useTrueRange) → series float
```

## Description

Keltner Channels Width. The Keltner Channels Width is the difference between the upper and the lower Keltner Channels divided by the middle channel.

## Arguments

- **`series`** `series int/float` — Series of values to process.
- **`length`** `simple int` — Number of bars (length).
- **`mult`** `simple int/float` — Standard deviation factor.
- **`useTrueRange`** `simple bool` — An optional parameter. Specifies if True Range is used; default is true. If the value is false, the range will be calculated with the expression (high - low).

## Returns

Keltner Channels Width.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("ta.kcw")

plot(ta.kcw(close, 5, 4), color=color.yellow)

// the same on pine
f_kcw(src, length, mult, useTrueRange) =>
    float basis = ta.ema(src, length)
    float span = (useTrueRange) ? ta.tr : (high - low)
    float rangeEma = ta.ema(span, length)

    ((basis + rangeEma * mult) - (basis - rangeEma * mult)) / basis

plot(f_kcw(close, 5, 4, true))
```

## See also

- [ta.kc()](./kc.md)
- [ta.ema()](./ema.md)
- [ta.atr()](./atr.md)
- [ta.bb()](./bb.md)
