---
title: "chart.right_visible_bar_time"
kind: variable
namespace: chart
source: https://www.tradingview.com/pine-script-reference/v6/#var_chart.right_visible_bar_time
---

# chart.right_visible_bar_time

**Category:** Variable

**Type:** `input int`

## Description

The [time](../time.md) of the rightmost bar currently visible on the chart.

## Remarks

Scripts using this variable will automatically re-execute when its value updates to reflect changes in the chart, which can be caused by users scrolling the chart, or new real-time bars.

Alerts created on a script that includes this variable will only use the value assigned to the variable at the moment of the alert's creation, regardless of whether the value changes afterward, which may lead to repainting.

## See also

- [chart.left_visible_bar_time](./left_visible_bar_time.md)
