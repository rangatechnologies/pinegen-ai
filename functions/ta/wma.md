---
title: "ta.wma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.wma
---

# ta.wma

**Category:** Function

## Syntax

```pinescript
ta.wma(source, length) → series float
```

## Description

The wma function returns weighted moving average of `source` for `length` bars back. In wma weighting factors decrease in arithmetical progression.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Weighted moving average of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.wma")
plot(ta.wma(close, 15))

// same on pine, but much less efficient
pine_wma(x, y) =>
    norm = 0.0
    sum = 0.0
    for i = 0 to y - 1
        weight = (y - i) * y
        norm := norm + weight
        sum := sum + x[i] * weight
    sum / norm
plot(pine_wma(close, 15))
```

## See also

- [ta.sma()](./sma.md)
- [ta.ema()](./ema.md)
- [ta.rma()](./rma.md)
- [ta.vwma()](./vwma.md)
- [ta.swma()](./swma.md)
- [ta.alma()](./alma.md)
