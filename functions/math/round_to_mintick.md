---
title: "math.round_to_mintick"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.round_to_mintick
---

# math.round_to_mintick

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
math.round_to_mintick(number) → simple float
```

```pinescript
math.round_to_mintick(number) → series float
```

## Description

Returns the value rounded to the symbol's mintick, i.e. the nearest value that can be divided by [syminfo.mintick](../../variables/syminfo/mintick.md), without the remainder, with ties rounding up.

## Arguments

- **`number`** `simple int/float` — The value to be rounded.

## Returns

The `number` rounded to tick precision.

**Return type(s):** `simple float`

## Remarks

Note that for 'na' values function returns 'na'.

## See also

- [math.ceil()](./ceil.md)
- [math.floor()](./floor.md)
