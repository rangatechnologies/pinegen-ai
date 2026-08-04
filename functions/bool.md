---
title: "bool"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_bool
---

# bool

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
bool(x) → const bool
```

```pinescript
bool(x) → input bool
```

```pinescript
bool(x) → simple bool
```

```pinescript
bool(x) → series bool
```

## Description

Converts the `x` value to a [bool](../types/bool.md) value. Returns [false](../constants/false.md) if `x` is [na](../variables/na.md), [false](../constants/false.md), or an [int](../types/int.md)/[float](../types/float.md) value equal to 0. Returns [true](../constants/true.md) for all other possible values.

## Arguments

- **`x`** `simple int/float/bool` — The value to convert to the specified type, usually [na](../variables/na.md).

## Returns

The value of the argument after casting to bool.

**Return type(s):** `const bool`

## See also

- [float()](./float.md)
- [int()](./int.md)
- [color()](./color.md)
- [string()](./string.md)
- [line()](./line.md)
- [label()](./label.md)
