---
title: "ta.rma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.rma
---

# ta.rma

**Category:** Function

## Syntax

```pinescript
ta.rma(source, length) → series float
```

## Description

Moving average used in RSI. It is the exponentially weighted moving average with alpha = 1 / length.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `simple int` — Number of bars (length).

## Returns

Exponential moving average of `source` with alpha = 1 / `length`.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Examples

```pinescript
//@version=6
indicator("ta.rma")
plot(ta.rma(close, 15))

//the same on pine
pine_rma(src, length) =>
	alpha = 1/length
	sum = 0.0
	sum := na(sum[1]) ? ta.sma(src, length) : alpha * src + (1 - alpha) * nz(sum[1])
plot(pine_rma(close, 15))
```

## See also

- [ta.sma()](./sma.md)
- [ta.ema()](./ema.md)
- [ta.wma()](./wma.md)
- [ta.vwma()](./vwma.md)
- [ta.swma()](./swma.md)
- [ta.alma()](./alma.md)
- [ta.rsi()](./rsi.md)
