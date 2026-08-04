---
title: "library"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_library
---

# library

**Category:** Function

## Syntax

```pinescript
library(title, overlay, dynamic_requests) → void
```

## Description

Declaration statement identifying a script as a [library](https://www.tradingview.com/pine-script-docs/concepts/libraries/).

## Arguments

- **`title`** `const string` — The title of the library and its identifier. It cannot contain spaces, special characters or begin with a digit. It is used as the publication's default title, and to uniquely identify the library in the [import](../keywords/import.md) statement, when another script uses it. It is also used as the script's name on the chart.
- **`overlay`** `const bool` (optional) — If [true](../constants/true.md), the script's visuals appear on the main chart pane if the user adds it to the chart directly, or in another script's pane if the user applies it to that script. If [false](../constants/false.md), the script's visuals appear in a separate pane. Changes to the `overlay` value apply only after the user adds the script to the chart again. Additionally, if the user moves the script to another pane by selecting a "Move to" option in the script's "More" menu, it does not move back to its original pane after any updates to the source code. The default is [false](../constants/false.md).  Strategy-specific labels that display entries and exits will be displayed over the main chart regardless of this setting.
- **`dynamic_requests`** `const bool` (optional) — Specifies whether the script can dynamically call functions from the `request.*()` namespace. Dynamic `request.*()` calls are allowed within the local scopes of conditional structures (e.g., [if](../keywords/if.md)), loops (e.g., [for](../keywords/for.md)), and exported functions. Additionally, such calls allow "series" arguments for many of their parameters. Optional. The default is [true](../constants/true.md). See the User Manual's [Dynamic requests](https://www.tradingview.com/pine-script-docs/concepts/other-timeframes-and-data/#dynamic-requests) section for more information.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
// @description Math library
library("num_methods", overlay = true)
// Calculate "sinh()" from the float parameter `x`
export sinh(float x) =>
	(math.exp(x) - math.exp(-x)) / 2.0
plot(sinh(0))
```

## See also

- [indicator()](./indicator.md)
- [strategy()](./strategy.md)
