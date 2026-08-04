---
title: "str.tostring"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.tostring
---

# str.tostring

**Category:** Function

## Syntax

_5 overloaded forms:_

```pinescript
str.tostring(value) → series string
```

```pinescript
str.tostring(value) → simple string
```

```pinescript
str.tostring(value) → const string
```

```pinescript
str.tostring(value, format) → series string
```

```pinescript
str.tostring(value, format) → simple string
```

## Arguments

- **`value`** `series int/float/bool/string/enum/array<int/float/bool/string>/matrix<int/float/bool/string>` — Value or array ID whose elements are converted to a string.

## Returns

The string representation of the `value` argument.

If the `value` argument is a string, it is returned as is.

When the `value` is na, the function returns the string "NaN".

**Return type(s):** `series string`

## Remarks

The formatting of float values will also round those values when necessary, e.g. str.tostring(3.99, '#') will return "4".

To display trailing zeros, use '0' instead of '#'. For example, '#.000'.

When using [format.mintick](../../constants/format/mintick.md), the value will be rounded to the nearest number that can be divided by [syminfo.mintick](../../variables/syminfo/mintick.md) without the remainder. The string is returned with trailing zeros.

If the x argument is a string, the same string value will be returned.

Bool type arguments return "true" or "false".

When x is na, the function returns "NaN".
