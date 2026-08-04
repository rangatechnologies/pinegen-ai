---
title: "ta.cog"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.cog
---

# ta.cog

**Category:** Function

## Syntax

```pinescript
ta.cog(source, length) → series float
```

## Description

The cog (center of gravity) is an indicator based on statistics and the Fibonacci golden ratio.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Center of Gravity.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.cog", overlay=true)
plot(ta.cog(close, 10))

// the same on pine
pine_cog(source, length) =>
    sum = math.sum(source, length)
    num = 0.0
    for i = 0 to length - 1
        price = source[i]
        num := num + price * (i + 1)
    -num / sum

plot(pine_cog(close, 10))
```

## See also

- [ta.stoch()](./stoch.md)
