---
title: "array.percentile_linear_interpolation"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.percentile_linear_interpolation
---

# array.percentile_linear_interpolation

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.percentile_linear_interpolation(id, percentage) → series float
```

```pinescript
array.percentile_linear_interpolation(id, percentage) → series int
```

## Description

Returns the value for which the specified percentage of array values (percentile) are less than or equal to it, using linear interpolation.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`percentage`** `series int/float` — The percentage of values that must be equal or less than the returned value.

**Return type(s):** `series float`

## Remarks

In statistics, the percentile is the percent of ranking items that appear at or below a certain score. This measurement shows the percentage of scores within a standard frequency distribution that is lower than the percentile rank being measured. Linear interpolation estimates the value between two ranks.

Returns [na](../../variables/na.md) if the `id` array is empty.

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
- [array.reverse()](./reverse.md)
- [order.ascending](../../constants/order/ascending.md)
- [order.descending](../../constants/order/descending.md)
