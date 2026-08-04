---
title: "chart.point.from_time"
kind: function
namespace: chart
source: https://www.tradingview.com/pine-script-reference/v6/#fun_chart.point.from_time
---

# chart.point.from_time

**Category:** Function

## Syntax

```pinescript
chart.point.from_time(time, price) → chart.point
```

## Description

Returns a [chart.point](../../types/chart/point.md) object with `time` as its x-coordinate and `price` as its y-coordinate.

## Arguments

- **`time`** `series int` — The x-coordinate of the point, expressed as a UNIX time value, in milliseconds.
- **`price`** `series int/float` — The y-coordinate of the point.

**Return type(s):** `chart.point`

## Remarks

The `index` field values of [chart.point](../../types/chart/point.md) instances returned from this function will be [na](../../variables/na.md), meaning drawing objects with `xloc` values set to `xloc.bar_index` will not work with them.
