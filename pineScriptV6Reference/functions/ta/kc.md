---
title: "ta.kc"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.kc
---

# ta.kc

**Category:** Function

## Syntax

```pinescript
ta.kc(series, length, mult, useTrueRange) → [series float, series float, series float]
```

## Description

Keltner Channels. Keltner channel is a technical analysis indicator showing a central moving average line plus channel lines at a distance above and below.

## Arguments

- **`series`** `series int/float` — Series of values to process.
- **`length`** `simple int` — Number of bars (length).
- **`mult`** `simple int/float` — Standard deviation factor.
- **`useTrueRange`** `simple bool` — An optional parameter. Specifies if True Range is used; default is true. If the value is false, the range will be calculated with the expression (high - low).

## Returns

Keltner Channels.

**Return type(s):** `[series float, series float, series float]`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("ta.kc")

[middle, upper, lower] = ta.kc(close, 5, 4)
plot(middle, color=color.yellow)
plot(upper, color=color.yellow)
plot(lower, color=color.yellow)


// the same on pine
f_kc(src, length, mult, useTrueRange) =>
    float basis = ta.ema(src, length)
    float span = (useTrueRange) ? ta.tr : (high - low)
    float rangeEma = ta.ema(span, length)
    [basis, basis + rangeEma * mult, basis - rangeEma * mult]

[pineMiddle, pineUpper, pineLower] = f_kc(close, 5, 4, true)

plot(pineMiddle)
plot(pineUpper)
plot(pineLower)
```

## See also

- [ta.ema()](./ema.md)
- [ta.atr()](./atr.md)
- [ta.bb()](./bb.md)
