---
title: "math.floor"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.floor
---

# math.floor

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.floor(number) → simple int
```

```pinescript
math.floor(number) → input int
```

```pinescript
math.floor(number) → const int
```

```pinescript
math.floor(number) → series int
```

## Description

Rounds the specified `number` down to the largest whole number ("int" value) that is less than or equal to it.

## Arguments

- **`number`** `simple int/float` — The number to round.

## Returns

The largest "int" value that is less than or equal to the `number`.

**Return type(s):** `simple int`

## See also

- [math.ceil()](./ceil.md)
- [math.round()](./round.md)
