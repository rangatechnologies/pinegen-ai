---
title: "chart.point.now"
kind: function
namespace: chart
source: https://www.tradingview.com/pine-script-reference/v6/#fun_chart.point.now
---

# chart.point.now

**Category:** Function

## Syntax

```pinescript
chart.point.now(price) → chart.point
```

## Description

Returns a [chart.point](../../types/chart/point.md) object with `price` as the y-coordinate

## Arguments

- **`price`** `series int/float` (optional) — The y-coordinate of the point. Optional. The default is [close](../../variables/close.md).

**Return type(s):** `chart.point`

## Remarks

The [chart.point](../../types/chart/point.md) instance returned from this function records values for its `index` and `time` fields on the bar it executed on, making it suitable for use with drawing objects of any `xloc` type.
