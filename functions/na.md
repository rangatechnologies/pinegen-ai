---
title: "na"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_na
---

# na

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
na(x) → simple bool
```

```pinescript
na(x) → series bool
```

## Description

Tests if `x` is [na](../variables/na.md).

## Arguments

- **`x`** `simple int/float` — Value to be tested.

## Returns

Returns [true](../constants/true.md) if `x` is [na](../variables/na.md), [false](../constants/false.md) otherwise.

**Return type(s):** `simple bool`

## Examples

```pinescript
//@version=6
indicator("na")
// Use the `na()` function to test for `na`.
plot(na(close[1]) ? close : close[1])
// ALTERNATIVE
// `nz()` also tests `close[1]` for `na`. It returns `close[1]` if it is not `na`, and `close` if it is.
plot(nz(close[1], close))
```

## See also

- [na](../variables/na.md)
- [fixnan()](./fixnan.md)
- [nz()](./nz.md)
