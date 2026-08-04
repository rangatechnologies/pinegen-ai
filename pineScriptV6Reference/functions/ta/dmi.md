---
title: "ta.dmi"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.dmi
---

# ta.dmi

**Category:** Function

## Syntax

```pinescript
ta.dmi(diLength, adxSmoothing) → [series float, series float, series float]
```

## Description

The dmi function returns the directional movement index.

## Arguments

- **`diLength`** `simple int` — DI Period.
- **`adxSmoothing`** `simple int` — ADX Smoothing Period.

## Returns

[Tuple](https://www.tradingview.com/pine-script-docs/language/type-system/#tuples) of three DMI series: Positive Directional Movement (+DI), Negative Directional Movement (-DI) and Average Directional Movement Index (ADX).

**Return type(s):** `[series float, series float, series float]`

## Examples

```pinescript
//@version=6
indicator(title="Directional Movement Index", shorttitle="DMI", format=format.price, precision=4)
len = input.int(17, minval=1, title="DI Length")
lensig = input.int(14, title="ADX Smoothing", minval=1)
[diplus, diminus, adx] = ta.dmi(len, lensig)
plot(adx, color=color.red, title="ADX")
plot(diplus, color=color.blue, title="+DI")
plot(diminus, color=color.orange, title="-DI")
```

## See also

- [ta.rsi()](./rsi.md)
- [ta.tsi()](./tsi.md)
- [ta.mfi()](./mfi.md)
