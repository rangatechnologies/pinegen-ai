---
title: "input.text_area"
kind: function
namespace: input
source: https://www.tradingview.com/pine-script-reference/v6/#fun_input.text_area
---

# input.text_area

**Category:** Function

## Syntax

```pinescript
input.text_area(defval, title, tooltip, group, confirm, display, active) → input string
```

## Description

Adds an input to the Inputs tab of your script's Settings, which allows you to provide configuration options to script users. This function adds a field for a multiline text input.

## Arguments

- **`defval`** `const string` — Determines the default value of the input variable proposed in the script's "Settings/Inputs" tab, from where the user can change it.
- **`title`** `const string` (optional) — Title of the input. If not specified, the variable name is used as the input's title. If the title is specified, but it is empty, the name will be an empty string.
- **`tooltip`** `const string` (optional) — The string that will be shown to the user when hovering over the tooltip icon.
- **`group`** `const string` (optional) — Creates a header above all inputs using the same group argument string. The string is also used as the header's text.
- **`confirm`** `const bool` (optional) — If true, then user will be asked to confirm input value before indicator is added to chart. Default value is false.
- **`display`** `const plot_display` (optional) — Controls where the script will display the input's information, aside from within the script's settings. This option allows one to remove a specific input from the script's status line or the Data Window to ensure only the most necessary inputs are displayed there. Possible values: [display.none](../../constants/display/none.md), [display.data_window](../../constants/display/data_window.md), [display.status_line](../../constants/display/status_line.md), [display.all](../../constants/display/all.md). Optional. The default is [display.none](../../constants/display/none.md).
- **`active`** `input bool` (optional) — Optional. Specifies whether users can change the value of the input in the script's "Settings/Inputs" tab. The script can use this parameter to set the state of the input based on the values of other inputs. If [true](../../constants/true.md), users can change the value of the input. If [false](../../constants/false.md), the input is grayed out, and users cannot change the value. The default is [true](../../constants/true.md).

## Returns

Value of input variable.

**Return type(s):** `input string`

## Remarks

Result of [input.text_area()](./text_area.md) function always should be assigned to a variable, see examples above.

## Examples

```pinescript
//@version=6
indicator("input.text_area")
i_text = input.text_area(defval = "Hello \nWorld!", title = "Message")
plot(close)
```

## See also

- [input.string()](./string.md)
- [input.bool()](./bool.md)
- [input.int()](./int.md)
- [input.float()](./float.md)
- [input.symbol()](./symbol.md)
- [input.timeframe()](./timeframe.md)
- [input.session()](./session.md)
- [input.source()](./source.md)
- [input.color()](./color.md)
- [input.time()](./time.md)
- [input()](../input.md)
