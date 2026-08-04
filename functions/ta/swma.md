---
title: "ta.swma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.swma
---

# ta.swma

**Category:** Function

## Syntax

```pinescript
ta.swma(source) → series float
```

## Description

Symmetrically weighted moving average with fixed length: 4. Weights: [1/6, 2/6, 2/6, 1/6].

## Arguments

- **`source`** `series int/float` — Source series.

## Returns

Symmetrically weighted moving average.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.

## Examples

```pinescript
//@version=6
indicator("ta.swma")
plot(ta.swma(close))

// same on pine, but less efficient
pine_swma(x) =>
    x[3] * 1 / 6 + x[2] * 2 / 6 + x[1] * 2 / 6 + x[0] * 1 / 6
plot(pine_swma(close))
```

## See also

- [ta.sma()](./sma.md)
- [ta.ema()](./ema.md)
- [ta.rma()](./rma.md)
- [ta.wma()](./wma.md)
- [ta.vwma()](./vwma.md)
- [ta.alma()](./alma.md)
