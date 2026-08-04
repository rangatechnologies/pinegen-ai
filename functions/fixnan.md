---
title: "fixnan"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_fixnan
---

# fixnan

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
fixnan(source) → series float
```

```pinescript
fixnan(source) → series int
```

```pinescript
fixnan(source) → series color
```

## Description

For a given series replaces NaN values with previous nearest non-NaN value.

## Arguments

- **`source`** `series int/float` — Source used for the calculation.

## Returns

Series without na gaps.

**Return type(s):** `series float`

## See also

- [na()](./na.md)
- [na](../variables/na.md)
- [nz()](./nz.md)
