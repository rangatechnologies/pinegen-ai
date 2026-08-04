---
title: "ta.vwma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.vwma
---

# ta.vwma

**Category:** Function

## Syntax

```pinescript
ta.vwma(source, length) → series float
```

## Description

The vwma function returns volume-weighted moving average of `source` for `length` bars back. It is the same as: sma(source * volume, length) / sma(volume, length).

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Volume-weighted moving average of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.vwma")
plot(ta.vwma(close, 15))

// same on pine, but less efficient
pine_vwma(x, y) =>
    ta.sma(x * volume, y) / ta.sma(volume, y)
plot(pine_vwma(close, 15))
```

## See also

- [ta.sma()](./sma.md)
- [ta.ema()](./ema.md)
- [ta.rma()](./rma.md)
- [ta.wma()](./wma.md)
- [ta.swma()](./swma.md)
- [ta.alma()](./alma.md)
