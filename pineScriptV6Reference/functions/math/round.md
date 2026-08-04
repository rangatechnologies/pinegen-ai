---
title: "math.round"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.round
---

# math.round

**Category:** Function

## Syntax

_8 overloaded forms:_

```pinescript
math.round(number) → simple int
```

```pinescript
math.round(number) → input int
```

```pinescript
math.round(number) → const int
```

```pinescript
math.round(number) → series int
```

```pinescript
math.round(number, precision) → simple float
```

```pinescript
math.round(number, precision) → input float
```

```pinescript
math.round(number, precision) → const float
```

```pinescript
math.round(number, precision) → series float
```

## Description

Returns the value of `number` rounded to the nearest integer, with ties rounding up. If the `precision` parameter is used, returns a float value rounded to that amount of decimal places.

## Arguments

- **`number`** `simple int/float` — The value to be rounded.

## Returns

The value of `number` rounded to the nearest integer, or according to precision.

**Return type(s):** `simple int`

## Remarks

Note that for 'na' values function returns 'na'.

## See also

- [math.ceil()](./ceil.md)
- [math.floor()](./floor.md)
