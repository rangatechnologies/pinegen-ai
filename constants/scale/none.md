---
title: "scale.none"
kind: constant
namespace: scale
source: https://www.tradingview.com/pine-script-reference/v6/#const_scale.none
---

# scale.none

**Category:** Constant

**Type:** `const scale_type`

## Description

A named constant for use as the `scale` argument in [indicator()](../../functions/indicator.md) and [strategy()](../../functions/strategy.md) declaration statements. A declaration statement can use this constant only if its `overlay` argument is `true`. Specifies that the script scales its visuals independently to fit the visual space of the main chart pane or another script's pane without displaying a separate scale. The script displays plotted numbers directly on the pane's existing price scale if the chart's settings allow it. If the user moves the script to a new pane, the script displays the values on a new scale to the left or right of that pane, depending on the chart's "Scales placement" setting.

## See also

- [indicator()](../../functions/indicator.md)
