---
title: "display.price_scale"
kind: constant
namespace: display
source: https://www.tradingview.com/pine-script-reference/v6/#const_display.price_scale
---

# display.price_scale

**Category:** Constant

**Type:** `const plot_display`

## Description

A named constant for use with the `display` parameter of the `plot*()` functions. Specifies that the price scale displays a label for the plot's data, but only if the chart's settings allow it. 

## Remarks

The `display.*` constants support [+](../../operators/plus.md) and [-](../../operators/minus.md) operations, enabling custom combinations of display settings. For example, `display.price_scale + display.data_window` specifies that the plot's data appears on the price scale and in the Data Window, and `display.all - display.price_scale` specifies that the data appears in all possible locations except for the price scale.

Selecting a deselected plot in the script's "Settings/Style" tab changes its display settings, causing the plotted data to appear in all available chart locations. To restore the display settings coded in the script, select "Reset settings" from the "Defaults" dropdown menu at the bottom of the "Settings" dialog box.

## See also

- [plot()](../../functions/plot.md)
- [plotshape()](../../functions/plotshape.md)
- [plotchar()](../../functions/plotchar.md)
- [plotarrow()](../../functions/plotarrow.md)
- [plotbar()](../../functions/plotbar.md)
- [plotcandle()](../../functions/plotcandle.md)
