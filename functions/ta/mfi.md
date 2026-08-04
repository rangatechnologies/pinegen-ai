---
title: "ta.mfi"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.mfi
---

# ta.mfi

**Category:** Function

## Syntax

```pinescript
ta.mfi(series, length) → series float
```

## Description

Money Flow Index. The Money Flow Index (MFI) is a technical oscillator that uses price and volume for identifying overbought or oversold conditions in an asset.

## Arguments

- **`series`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Money Flow Index.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("Money Flow Index")

plot(ta.mfi(hlc3, 14), color=color.yellow)

// the same on pine
pine_mfi(src, length) =>
    float upper = math.sum(volume * (ta.change(src) <= 0.0 ? 0.0 : src), length)
    float lower = math.sum(volume * (ta.change(src) >= 0.0 ? 0.0 : src), length)
    mfi = 100.0 - (100.0 / (1.0 + upper / lower))
    mfi

plot(pine_mfi(hlc3, 14))
```

## See also

- [ta.rsi()](./rsi.md)
- [math.sum()](../math/sum.md)
