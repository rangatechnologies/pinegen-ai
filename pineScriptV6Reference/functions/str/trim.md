---
title: "str.trim"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.trim
---

# str.trim

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
str.trim(source) → const string
```

```pinescript
str.trim(source) → input string
```

```pinescript
str.trim(source) → simple string
```

```pinescript
str.trim(source) → series string
```

## Description

Constructs a new string with all consecutive whitespaces and other control characters (e.g., “\n”, “\t”, etc.) removed from the left and right of the `source`.

## Arguments

- **`source`** `const string` — String to trim.

**Return type(s):** `const string`

## Remarks

Returns an empty string ("") if the result is empty after the trim or if the `source` is [na](../../variables/na.md).

## Examples

```pinescript
//@version=6
indicator("str.trim")
trim = str.trim("    abc    ") // Returns "abc"
label.new(bar_index,close,trim)
```
