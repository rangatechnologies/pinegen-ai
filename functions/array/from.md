---
title: "array.from"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.from
---

# array.from

**Category:** Function

## Syntax

_12 overloaded forms:_

```pinescript
array.from(arg0, arg1, ...) → array<type>
```

```pinescript
array.from(arg0, arg1, ...) → array<int>
```

```pinescript
array.from(arg0, arg1, ...) → array<float>
```

```pinescript
array.from(arg0, arg1, ...) → array<bool>
```

```pinescript
array.from(arg0, arg1, ...) → array<string>
```

```pinescript
array.from(arg0, arg1, ...) → array<label>
```

```pinescript
array.from(arg0, arg1, ...) → array<line>
```

```pinescript
array.from(arg0, arg1, ...) → array<color>
```

```pinescript
array.from(arg0, arg1, ...) → array<enum>
```

```pinescript
array.from(arg0, arg1, ...) → array<box>
```

```pinescript
array.from(arg0, arg1, ...) → array<table>
```

```pinescript
array.from(arg0, arg1, ...) → array<linefill>
```

## Description

The function takes a variable number of arguments with one of the types: int, float, bool, string, label, line, color, box, table, linefill, and returns an array of the corresponding type.

## Arguments

- **`arg0, arg1, ...`** `<arg..._type>` — Array arguments.

## Returns

The array element's value.

**Return type(s):** `array<>`

## Remarks

This function can accept up to 4,000 'int', 'float', 'bool', or 'color' arguments. For all other types, including user-defined types, the limit is 999.

## Examples

```pinescript
//@version=6
indicator("array.from_example", overlay = false)
arr = array.from("Hello", "World!") // arr (array<string>) will contain 2 elements: {Hello}, {World!}.
plot(close)
```
