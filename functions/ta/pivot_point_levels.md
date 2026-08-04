---
title: "ta.pivot_point_levels"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.pivot_point_levels
---

# ta.pivot_point_levels

**Category:** Function

## Syntax

```pinescript
ta.pivot_point_levels(type, anchor, developing) → array<float>
```

## Description

Calculates the pivot point levels using the specified `type` and `anchor`.

## Arguments

- **`type`** `series string` — The type of pivot point levels. Possible values: "Traditional", "Fibonacci", "Woodie", "Classic", "DM", "Camarilla".
- **`anchor`** `series bool` — The condition that triggers the reset of the pivot point calculations. When [true](../../constants/true.md), calculations reset; when [false](../../constants/false.md), results calculated at the last reset persist.
- **`developing`** `series bool` (optional) — If [false](../../constants/false.md), the values are those calculated the last time the anchor condition was [true](../../constants/true.md). They remain constant until the anchor condition becomes [true](../../constants/true.md) again. If [true](../../constants/true.md), the pivots are developing, i.e., they constantly recalculate on the data developing between the point of the last anchor (or bar zero if the anchor condition was never [true](../../constants/true.md)) and the current bar. Optional. The default is [false](../../constants/false.md).

## Returns

An `array<float>` with numerical values representing 11 pivot point levels: [P, R1, S1, R2, S2, R3, S3, R4, S4, R5, S5]. Levels absent from the specified `type` return [na](../../variables/na.md) values (e.g., "DM" only calculates P, R1, and S1).

**Return type(s):** `array<float>`

## Remarks

The `developing` parameter cannot be `true` when `type` is set to "Woodie", because the Woodie calculation for a period depends on that period's open, which means that the pivot value is either available or unavailable, but never developing. If used together, the indicator will return a runtime error.

## Examples

```pinescript
//@version=6
indicator("Weekly Pivots", max_lines_count=500, overlay=true)
timeframe = "1W"
typeInput = input.string("Traditional", "Type", options=["Traditional", "Fibonacci", "Woodie", "Classic", "DM", "Camarilla"])
weekChange = timeframe.change(timeframe)
pivotPointsArray = ta.pivot_point_levels(typeInput, weekChange)
if weekChange
    for pivotLevel in pivotPointsArray
        line.new(time, pivotLevel, time + timeframe.in_seconds(timeframe) * 1000, pivotLevel, xloc=xloc.bar_time)
```
