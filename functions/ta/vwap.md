---
title: "ta.vwap"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.vwap
---

# ta.vwap

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.vwap(source, anchor) → series float
```

```pinescript
ta.vwap(source, anchor, stdev_mult) → [series float, series float, series float]
```

## Description

Volume weighted average price.

## Arguments

- **`source`** `series int/float` — Source used for the VWAP calculation.
- **`anchor`** `series bool` — The condition that triggers the reset of VWAP calculations. When [true](../../constants/true.md), calculations reset; when [false](../../constants/false.md), calculations proceed using the values accumulated since the previous reset. Optional. The default is equivalent to passing [timeframe.change()](../timeframe/change.md) with "1D" as its argument.

## Returns

A VWAP series, or a tuple [vwap, upper_band, lower_band] if `stdev_mult` is specified.

**Return type(s):** `series float`

## Remarks

Calculations only begin the first time the anchor condition becomes [true](../../constants/true.md). Until then, the function returns [na](../../variables/na.md).

## Detailed Description



```pinescript
//@version=6
indicator("Simple VWAP")
vwap = ta.vwap(open)
plot(vwap)
```

---



```pinescript
//@version=6
indicator("Advanced VWAP")
vwapAnchorInput = input.string("Daily", "Anchor", options = ["Daily", "Weekly", "Monthly"])
stdevMultiplierInput = input.float(1.0, "Standard Deviation Multiplier")
anchorTimeframe = switch vwapAnchorInput
	"Daily"   => "1D"
	"Weekly"  => "1W"
	"Monthly" => "1M"
anchor = timeframe.change(anchorTimeframe)
[vwap, upper, lower] = ta.vwap(open, anchor, stdevMultiplierInput)
plot(vwap)
plot(upper, color = color.green)
plot(lower, color = color.green)
```

## See also

- [ta.vwap](../../variables/ta/vwap.md)
