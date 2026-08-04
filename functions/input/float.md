---
title: "input.float"
kind: function
namespace: input
source: https://www.tradingview.com/pine-script-reference/v6/#fun_input.float
---

# input.float

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
input.float(defval, title, minval, maxval, step, tooltip, inline, group, confirm, display, active) → input float
```

```pinescript
input.float(defval, title, options, tooltip, inline, group, confirm, display, active) → input float
```

## Description

Adds an input to the Inputs tab of your script's Settings, which allows you to provide configuration options to script users. This function adds a field for a float input to the script's inputs.

## Arguments

- **`defval`** `const int/float` — Determines the default value of the input variable proposed in the script's "Settings/Inputs" tab, from where script users can change it. When a list of values is used with the `options` parameter, the value must be one of them.
- **`title`** `const string` (optional) — Title of the input. If not specified, the variable name is used as the input's title. If the title is specified, but it is empty, the name will be an empty string.
- **`minval`** `const int/float` (optional) — Minimal possible value of the input variable. Optional.
- **`maxval`** `const int/float` (optional) — Maximum possible value of the input variable. Optional.
- **`step`** `const int/float` (optional) — Step value used for incrementing/decrementing the input. Optional. The default is 1.
- **`tooltip`** `const string` (optional) — The string that will be shown to the user when hovering over the tooltip icon.
- **`inline`** `const string` (optional) — Combines all the input calls using the same argument in one line. The string used as an argument is not displayed. It is only used to identify inputs belonging to the same line.
- **`group`** `const string` (optional) — Creates a header above all inputs using the same group argument string. The string is also used as the header's text.
- **`confirm`** `const bool` (optional) — If true, then user will be asked to confirm input value before indicator is added to chart. Default value is false.
- **`display`** `const plot_display` (optional) — Controls where the script will display the input's information, aside from within the script's settings. This option allows one to remove a specific input from the script's status line or the Data Window to ensure only the most necessary inputs are displayed there. Possible values: [display.none](../../constants/display/none.md), [display.data_window](../../constants/display/data_window.md), [display.status_line](../../constants/display/status_line.md), [display.all](../../constants/display/all.md). Optional. The default is [display.all](../../constants/display/all.md).
- **`active`** `input bool` (optional) — Optional. Specifies whether users can change the value of the input in the script's "Settings/Inputs" tab. The script can use this parameter to set the state of the input based on the values of other inputs. If [true](../../constants/true.md), users can change the value of the input. If [false](../../constants/false.md), the input is grayed out, and users cannot change the value. The default is [true](../../constants/true.md).

## Returns

Value of input variable.

**Return type(s):** `input float`

## Remarks

Result of [input.float()](./float.md) function always should be assigned to a variable, see examples above.

## Examples

```pinescript
//@version=6
indicator("input.float", overlay=true)
i_angle1 = input.float(0.5, "Sin Angle", minval=-3.14, maxval=3.14, step=0.02)
plot(math.sin(i_angle1) > 0 ? close : open, "sin", color=color.green)

i_angle2 = input.float(0, "Cos Angle", options=[-3.14, -1.57, 0, 1.57, 3.14])
plot(math.cos(i_angle2) > 0 ? close : open, "cos", color=color.red)
```

## See also

- [input.bool()](./bool.md)
- [input.int()](./int.md)
- [input.string()](./string.md)
- [input.text_area()](./text_area.md)
- [input.symbol()](./symbol.md)
- [input.timeframe()](./timeframe.md)
- [input.session()](./session.md)
- [input.source()](./source.md)
- [input.color()](./color.md)
- [input.time()](./time.md)
- [input()](../input.md)
