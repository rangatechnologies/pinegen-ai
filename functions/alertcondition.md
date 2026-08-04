---
title: "alertcondition"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_alertcondition
---

# alertcondition

**Category:** Function

## Syntax

```pinescript
alertcondition(condition, title, message) → void
```

## Description

Creates alert condition, that is available in Create Alert dialog. Please note, that [alertcondition()](./alertcondition.md) does NOT create an alert, it just gives you more options in Create Alert dialog. Also, [alertcondition()](./alertcondition.md) effect is invisible on chart.

## Arguments

- **`condition`** `series bool` — Series of boolean values that is used for alert. True values mean alert fire, false - no alert. Required argument.
- **`title`** `const string` (optional) — Title of the alert condition. Optional argument.
- **`message`** `const string` (optional) — Message to display when alert fires. Optional argument.

**Return type(s):** `void`

## Remarks

Please note that an alertcondition call generates an additional plot. All such calls are taken into account when we calculate the number of the output series per script.

## Examples

```pinescript
//@version=6
indicator("alertcondition", overlay=true)
alertcondition(close >= open, title='Alert on Green Bar', message='Green Bar!')
```

## See also

- [alert()](./alert.md)
