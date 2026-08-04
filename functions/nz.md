---
title: "nz"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_nz
---

# nz

**Category:** Function

## Syntax

_6 overloaded forms:_

```pinescript
nz(source, replacement) → simple int
```

```pinescript
nz(source, replacement) → simple float
```

```pinescript
nz(source, replacement) → simple color
```

```pinescript
nz(source, replacement) → series int
```

```pinescript
nz(source, replacement) → series float
```

```pinescript
nz(source, replacement) → series color
```

## Description

Replaces [na](../variables/na.md) (undefined) values with either a type-specific default value or a specified replacement.

## Arguments

- **`source`** `simple int` — The source series to process.
- **`replacement`** `simple int` — Optional. The value the function uses to replace [na](../variables/na.md) values in the `source` series. The default depends on the `source` type: `0` for "int", `0.0` for "float", or `#00000000` for "color".

## Returns

The value of `source` if it is not `na`. If the value of `source` is `na`, returns zero, or the `replacement` argument when one is used.

**Return type(s):** `simple int`

## Examples

```pinescript
//@version=6
indicator("nz", overlay=true)
plot(nz(ta.sma(close, 100)))
```

## See also

- [na](../variables/na.md)
- [na()](./na.md)
- [fixnan()](./fixnan.md)
