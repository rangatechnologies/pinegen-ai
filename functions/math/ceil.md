---
title: "math.ceil"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.ceil
---

# math.ceil

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.ceil(number) → simple int
```

```pinescript
math.ceil(number) → input int
```

```pinescript
math.ceil(number) → const int
```

```pinescript
math.ceil(number) → series int
```

## Description

Rounds the specified `number` up to the smallest whole number ("int" value) that is greater than or equal to it.

## Arguments

- **`number`** `simple int/float` — The number to round.

## Returns

The smallest "int" value that is greater than or equal to the `number`.

**Return type(s):** `simple int`

## See also

- [math.floor()](./floor.md)
- [math.round()](./round.md)
