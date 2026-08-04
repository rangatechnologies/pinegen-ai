---
title: "timeframe.change"
kind: function
namespace: timeframe
source: https://www.tradingview.com/pine-script-reference/v6/#fun_timeframe.change
---

# timeframe.change

**Category:** Function

## Syntax

```pinescript
timeframe.change(timeframe) → series bool
```

## Description

Detects changes in the specified `timeframe`.

## Arguments

- **`timeframe`** `series string` (optional) — String formatted according to the [User manual's timeframe string specifications](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications).

## Returns

Returns [true](../../constants/true.md) on the first bar of a new `timeframe`, [false](../../constants/false.md) otherwise.

**Return type(s):** `series bool`

## Examples

```pinescript
//@version=6
// Run this script on an intraday chart.
indicator("New day started", overlay = true)
// Highlights the first bar of the new day.
isNewDay = timeframe.change("1D")
bgcolor(isNewDay ? color.new(color.green, 80) : na)
```
