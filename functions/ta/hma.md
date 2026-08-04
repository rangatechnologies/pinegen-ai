---
title: "ta.hma"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.hma
---

# ta.hma

**Category:** Function

## Syntax

```pinescript
ta.hma(source, length) → series float
```

## Description

The hma function returns the Hull Moving Average.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `simple int` — Number of bars.

## Returns

Hull moving average of 'source' for 'length' bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("Hull Moving Average")
src = input(defval=close, title="Source")
length = input(defval=9, title="Length")
hmaBuildIn = ta.hma(src, length)
plot(hmaBuildIn, title="Hull MA", color=#674EA7)
```

## See also

- [ta.ema()](./ema.md)
- [ta.rma()](./rma.md)
- [ta.wma()](./wma.md)
- [ta.vwma()](./vwma.md)
- [ta.sma()](./sma.md)
