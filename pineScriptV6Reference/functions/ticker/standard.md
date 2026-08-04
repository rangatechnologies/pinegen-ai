---
title: "ticker.standard"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.standard
---

# ticker.standard

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.standard(symbol) → simple string
```

```pinescript
ticker.standard(symbol) → series string
```

## Description

Creates a ticker to request data from a standard chart that is unaffected by modifiers like extended session, dividend adjustment, currency conversion, and the calculations of non-standard chart types: Heikin Ashi, Renko, etc. Among other things, this makes it possible to retrieve standard chart values when the script is running on a non-standard chart.

## Arguments

- **`symbol`** `simple string` (optional) — A ticker ID to be converted into its standard form. Optional. The default is [syminfo.tickerid](../../variables/syminfo/tickerid.md).

## Returns

A string representing the ticker of a standard chart in the "prefix:ticker" format. If the `symbol` argument does not contain the prefix and ticker information, the function returns the supplied argument as is.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker.standard", overlay = true)
// This script should be run on a non-standard chart such as HA, Renko...

// Requests data from the chart type the script is running on.
chartTypeValue = request.security(syminfo.tickerid, "1D", close)

// Request data from the standard chart type, regardless of the chart type the script is running on.
standardChartValue = request.security(ticker.standard(syminfo.tickerid), "1D", close)

// This will not use a standard ticker ID because the `symbol` argument contains only the ticker — not the prefix (exchange).
standardChartValue2 = request.security(ticker.standard(syminfo.ticker), "1D", close)

plot(chartTypeValue)
plot(standardChartValue, color = color.green)
```

## See also

- [request.security()](../request/security.md)
