---
title: "str.repeat"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.repeat
---

# str.repeat

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
str.repeat(source, repeat, separator) → const string
```

```pinescript
str.repeat(source, repeat, separator) → input string
```

```pinescript
str.repeat(source, repeat, separator) → simple string
```

```pinescript
str.repeat(source, repeat, separator) → series string
```

## Description

Constructs a new string containing the `source` string repeated `repeat` times with the `separator` injected between each repeated instance.

## Arguments

- **`source`** `const string` — String to repeat.
- **`repeat`** `const int` — Number of times to repeat the `source` string. Must be greater than or equal to 0.
- **`separator`** `const string` (optional) — String to inject between repeated values. Optional. The default is empty string.

**Return type(s):** `const string`

## Remarks

Returns [na](../../variables/na.md) if the `source` is [na](../../variables/na.md).

## Examples

```pinescript
//@version=6
indicator("str.repeat")
repeat = str.repeat("?", 3, ",") // Returns "?,?,?"
label.new(bar_index,close,repeat)
```
