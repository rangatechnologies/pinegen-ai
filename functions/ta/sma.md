---
title: "ta.sma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.sma
---

# ta.sma

**Category:** Function

## Syntax

```pinescript
ta.sma(source, length) → series float
```

## Description

The sma function returns the moving average, that is the sum of last y values of x, divided by y.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Simple moving average of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.sma")
plot(ta.sma(close, 15))

// same on pine, but much less efficient
pine_sma(x, y) =>
    sum = 0.0
    for i = 0 to y - 1
        sum := sum + x[i] / y
    sum
plot(pine_sma(close, 15))
```

## See also

- [ta.ema()](./ema.md)
- [ta.rma()](./rma.md)
- [ta.wma()](./wma.md)
- [ta.vwma()](./vwma.md)
- [ta.swma()](./swma.md)
- [ta.alma()](./alma.md)
