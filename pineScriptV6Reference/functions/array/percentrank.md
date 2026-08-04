---
title: "array.percentrank"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.percentrank
---

# array.percentrank

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.percentrank(id, index) → series float
```

```pinescript
array.percentrank(id, index) → series int
```

## Description

Returns the percentile rank of the element at the specified `index`.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`index`** `series int` — The index of the element for which the percentile rank should be calculated.

**Return type(s):** `series float`

## Remarks

Percentile rank is the number of elements in the array that are less than or equal to the reference value, expressed as a percentage.

Returns [na](../../variables/na.md) if the `id` array is empty.

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
- [array.reverse()](./reverse.md)
- [order.ascending](../../constants/order/ascending.md)
- [order.descending](../../constants/order/descending.md)
