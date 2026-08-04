---
title: "ta.ema"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.ema
---

# ta.ema

**Category:** Function

## Syntax

```pinescript
ta.ema(source, length) → series float
```

## Description

The ema function returns the exponentially weighted moving average. In ema weighting factors decrease exponentially. It calculates by using a formula: `EMA = alpha * source + (1 - alpha) * EMA[1]`, where `alpha = 2 / (length + 1)`.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `simple int` — Number of bars (length).

## Returns

Exponential moving average of `source` with alpha = 2 / (length + 1).

**Return type(s):** `series float`

## Remarks

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("ta.ema")
plot(ta.ema(close, 15))

//the same on pine
pine_ema(src, length) =>
    alpha = 2 / (length + 1)
    sum = 0.0
    sum := na(sum[1]) ? src : alpha * src + (1 - alpha) * nz(sum[1])
plot(pine_ema(close,15))
```

## See also

- [ta.sma()](./sma.md)
- [ta.rma()](./rma.md)
- [ta.wma()](./wma.md)
- [ta.vwma()](./vwma.md)
- [ta.swma()](./swma.md)
- [ta.alma()](./alma.md)
