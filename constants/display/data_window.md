---
title: "display.data_window"
kind: constant
namespace: display
source: https://www.tradingview.com/pine-script-reference/v6/#const_display.data_window
---

# display.data_window

**Category:** Constant

**Type:** `const plot_display`

## Description

A named constant for use with the `display` parameter of the `plot*()` and `input*()` functions. Specifies that the values are available in the Data Window by default. The Data Window tab is accessible by clicking the "Object Tree and Data Window" icon in the chart's right sidebar.

## Remarks

The `display.*` constants support [+](../../operators/plus.md) and [-](../../operators/minus.md) operations, enabling custom combinations of display settings. For example, `display.data_window + display.status_line` specifies that the data for an input or plot appears in the Data Window and the script's status line, and `display.all - display.data_window` specifies that the data appears in all possible locations except for the Data Window.

Selecting a deselected plot in the script's "Settings/Style" tab changes its display settings, causing the plotted data to appear in all available chart locations. To restore the display settings coded in the script, select "Reset settings" from the "Defaults" dropdown menu at the bottom of the "Settings" dialog box.

## See also

- [plot()](../../functions/plot.md)
- [plotshape()](../../functions/plotshape.md)
- [plotchar()](../../functions/plotchar.md)
- [plotarrow()](../../functions/plotarrow.md)
- [plotbar()](../../functions/plotbar.md)
- [plotcandle()](../../functions/plotcandle.md)
