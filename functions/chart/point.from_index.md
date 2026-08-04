---
title: "chart.point.from_index"
kind: function
namespace: chart
source: https://www.tradingview.com/pine-script-reference/v6/#fun_chart.point.from_index
---

# chart.point.from_index

**Category:** Function

## Syntax

```pinescript
chart.point.from_index(index, price) → chart.point
```

## Description

Returns a [chart.point](../../types/chart/point.md) object with `index` as its x-coordinate and `price` as its y-coordinate.

## Arguments

- **`index`** `series int` — The x-coordinate of the point, expressed as a bar index value.
- **`price`** `series int/float` — The y-coordinate of the point.

**Return type(s):** `chart.point`

## Remarks

The `time` field values of [chart.point](../../types/chart/point.md) instances returned from this function will be [na](../../variables/na.md), meaning drawing objects with `xloc` values set to `xloc.bar_time` will not work with them.
