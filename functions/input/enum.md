---
title: "input.enum"
kind: function
namespace: input
source: https://www.tradingview.com/pine-script-reference/v6/#fun_input.enum
---

# input.enum

**Category:** Function

## Syntax

```pinescript
input.enum(defval, title, options, tooltip, inline, group, confirm, display, active) → input enum
```

## Description

Adds an input to the Inputs tab of your script's Settings, which allows you to provide configuration options to script users. This function adds a dropdown with options based on the [enum](../../keywords/enum.md) fields passed to its `defval` and `options` parameters.

The text for each option in the resulting dropdown corresponds to the titles of the included fields. If a field's title is not specified in the enum declaration, its title is the string representation of its name.

## Arguments

- **`defval`** `const enum` — Determines the default value of the input, which users can change in the script's "Settings/Inputs" tab. When the `options` parameter has a specified tuple of enum fields, the tuple must include the `defval`.
- **`title`** `const string` (optional) — Title of the input. If not specified, the variable name is used as the input's title. If the title is specified, but it is empty, the name will be an empty string.
- **`options`** `tuple of enum fields: [enumName.field1, enumName.field2, ...]` (optional) — A list of options to choose from. Optional. By default, the titles of all of the enum's fields are available in the dropdown. Passing a tuple as the `options` argument limits the list to only the included fields.
- **`tooltip`** `const string` (optional) — The string that will be shown to the user when hovering over the tooltip icon.
- **`inline`** `const string` (optional) — Combines all the input calls using the same argument in one line. The string used as an argument is not displayed. It is only used to identify inputs belonging to the same line.
- **`group`** `const string` (optional) — Creates a header above all inputs using the same group argument string. The string is also used as the header's text.
- **`confirm`** `const bool` (optional) — If `true`, then user will be asked to confirm input value before indicator is added to chart. Default value is `false`.
- **`display`** `const plot_display` (optional) — Controls where the script will display the input's information, aside from within the script's settings. This option allows one to remove a specific input from the script's status line or the Data Window to ensure only the most necessary inputs are displayed there. Possible values: [display.none](https://www.tradingview.com/pine-script-reference/v6/#var_display.none), [display.data_window](https://www.tradingview.com/pine-script-reference/v6/#var_display.data_window), [display.status_line](https://www.tradingview.com/pine-script-reference/v6/#var_display.status_line), [display.all](https://www.tradingview.com/pine-script-reference/v6/#var_display.all). Optional. The default is [display.all](https://www.tradingview.com/pine-script-reference/v6/#var_display.all).
- **`active`** `input bool` (optional) — Optional. Specifies whether users can change the value of the input in the script's "Settings/Inputs" tab. The script can use this parameter to set the state of the input based on the values of other inputs. If [true](../../constants/true.md), users can change the value of the input. If [false](../../constants/false.md), the input is grayed out, and users cannot change the value. The default is [true](../../constants/true.md).

## Returns

Value of input variable.

## Remarks

All fields included in the `defval` and `options` arguments must belong to the same enum.

## Examples

```pinescript
//@version=6
indicator("Session highlight", overlay = true)

//@enum        Contains fields with popular timezones as titles.
//@field exch  Has an empty string as the title to represent the chart timezone.
enum tz
	utc  = "UTC"
	exch = ""
	ny   = "America/New_York"
	chi  = "America/Chicago"
	lon  = "Europe/London"
	tok  = "Asia/Tokyo"

//@variable The session string.
selectedSession = input.session("1200-1500", "Session")
//@variable The selected timezone. The input's dropdown contains the fields in the `tz` enum.
selectedTimezone = input.enum(tz.utc, "Session Timezone")

//@variable Is `true` if the current bar's time is in the specified session.
bool inSession = false
if not na(time("", selectedSession, str.tostring(selectedTimezone)))
	inSession := true

// Highlight the background when `inSession` is `true`.
bgcolor(inSession ? color.new(color.green, 90) : na, title = "Active session highlight")
```

## See also

- [input.text_area()](./text_area.md)
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
