---
title: "ta.stoch"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.stoch
---

# ta.stoch

**Category:** Function

## Syntax

```pinescript
ta.stoch(source, high, low, length) → series float
```

## Description

Stochastic. It is calculated by a formula: 100 * (close - lowest(low, length)) / (highest(high, length) - lowest(low, length)).

## Arguments

- **`source`** `series int/float` — Source series.
- **`high`** `series int/float` — Series of high.
- **`low`** `series int/float` — Series of low.
- **`length`** `series int` — Length (number of bars back).

## Returns

Stochastic.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## See also

- [ta.cog()](./cog.md)
