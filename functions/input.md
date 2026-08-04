---
title: "input"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_input
---

# input

**Category:** Function

## Syntax

_6 overloaded forms:_

```pinescript
input(defval, title, tooltip, inline, group, display, active) → input bool
```

```pinescript
input(defval, title, tooltip, inline, group, display, active) → input color
```

```pinescript
input(defval, title, tooltip, inline, group, display, active) → input int
```

```pinescript
input(defval, title, tooltip, inline, group, display, active) → input float
```

```pinescript
input(defval, title, tooltip, inline, group, display, active) → input string
```

```pinescript
input(defval, title, inline, group, tooltip, display, active) → series float
```

## Description

Adds an input to the Inputs tab of your script's Settings, which allows you to provide configuration options to script users. This function automatically detects the type of the argument used for 'defval' and uses the corresponding input widget.

## Arguments

- **`defval`** `const int/float/bool/string/color or source-type built-ins` — Determines the default value of the input variable proposed in the script's "Settings/Inputs" tab, from where script users can change it. Source-type built-ins are built-in series float variables that specify the source of the calculation: `close`, `hlc3`, etc.
- **`title`** `const string` (optional) — Title of the input. If not specified, the variable name is used as the input's title. If the title is specified, but it is empty, the name will be an empty string.
- **`tooltip`** `const string` (optional) — The string that will be shown to the user when hovering over the tooltip icon.
- **`inline`** `const string` (optional) — Combines all the input calls using the same argument in one line. The string used as an argument is not displayed. It is only used to identify inputs belonging to the same line.
- **`group`** `const string` (optional) — Creates a header above all inputs using the same group argument string. The string is also used as the header's text.
- **`display`** `const plot_display` (optional) — Controls where the script will display the input's information, aside from within the script's settings. This option allows one to remove a specific input from the script's status line or the Data Window to ensure only the most necessary inputs are displayed there. Possible values: [display.none](../constants/display/none.md), [display.data_window](../constants/display/data_window.md), [display.status_line](../constants/display/status_line.md), [display.all](../constants/display/all.md). Optional. The default depends on the type of the value passed to `defval`: [display.none](../constants/display/none.md) for [bool](../types/bool.md) and [color](../types/color.md) values, [display.all](../constants/display/all.md) for everything else.
- **`active`** `input bool` (optional) — Optional. Specifies whether users can change the value of the input in the script's "Settings/Inputs" tab. The script can use this parameter to set the state of the input based on the values of other inputs. If [true](../constants/true.md), users can change the value of the input. If [false](../constants/false.md), the input is grayed out, and users cannot change the value. The default is [true](../constants/true.md).

## Returns

Value of input variable.

**Return type(s):** `input bool`

## Remarks

Result of [input()](./input.md) function always should be assigned to a variable, see examples above.

## Examples

```pinescript
//@version=6
indicator("input", overlay=true)
i_switch = input(true, "On/Off")
plot(i_switch ? open : na)

i_len = input(7, "Length")
i_src = input(close, "Source")
plot(ta.sma(i_src, i_len))

i_border = input(142.50, "Price Border")
hline(i_border)
bgcolor(close > i_border ? color.green : color.red)

i_col = input(color.red, "Plot Color")
plot(close, color=i_col)

i_text = input("Hello!", "Message")
l = label.new(bar_index, high, text=i_text)
label.delete(l[1])
```

## See also

- [input.bool()](./input/bool.md)
- [input.color()](./input/color.md)
- [input.int()](./input/int.md)
- [input.float()](./input/float.md)
- [input.string()](./input/string.md)
- [input.symbol()](./input/symbol.md)
- [input.timeframe()](./input/timeframe.md)
- [input.text_area()](./input/text_area.md)
- [input.session()](./input/session.md)
- [input.source()](./input/source.md)
- [input.time()](./input/time.md)
