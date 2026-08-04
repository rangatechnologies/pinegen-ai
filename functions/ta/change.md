---
title: "ta.change"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.change
---

# ta.change

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
ta.change(source, length) → series float
```

```pinescript
ta.change(source, length) → series bool
```

```pinescript
ta.change(source, length) → series int
```

## Description

Compares the current `source` value to its value `length` bars ago and returns the difference.

## Arguments

- **`source`** `series int/float` — Source series.
- **`length`** `series int` — How far the past `source` value is offset from the current one, in bars. Optional. The default is 1.

## Returns

The difference between the values when they are numerical. When a 'bool' source is used, returns `true` when the current source is different from the previous source.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.

## Examples

```pinescript
//@version=6
indicator('Day and Direction Change', overlay = true)
dailyBarTime = time('1D')
isNewDay = ta.change(dailyBarTime) != 0
bgcolor(isNewDay ? color.new(color.green, 80) : na)

isGreenBar = close >= open
colorChange = ta.change(isGreenBar)
plotshape(colorChange, 'Direction Change')
```

## See also

- [ta.mom()](./mom.md)
- [ta.cross()](./cross.md)
