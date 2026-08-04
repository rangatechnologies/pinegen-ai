---
title: "chart.point"
kind: type
namespace: chart
source: https://www.tradingview.com/pine-script-reference/v6/#type_chart.point
---

# chart.point

**Category:** Type

## Description

Keyword to explicitly declare the type of a variable or parameter as `chart.point`. Scripts can produce `chart.point` instances using the [chart.point.from_time()](../../functions/chart/point.from_time.md), [chart.point.from_index()](../../functions/chart/point.from_index.md), [chart.point.now()](../../functions/chart/point.now.md), and [chart.point.new()](../../functions/chart/point.new.md) functions.

## Fields

- **`index`** `series int` — The x-coordinate of the point, expressed as a bar index value.
- **`time`** `series int` — The x-coordinate of the point, expressed as a UNIX time value, in milliseconds.
- **`price`** `series float` — The y-coordinate of the point.

## See also

- [polyline](../polyline.md)
