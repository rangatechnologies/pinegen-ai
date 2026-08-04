---
title: "array.sort"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.sort
---

# array.sort

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.sort(id, order) → void
```

```pinescript
array.sort(id, order, sort_field) → void
```

## Description

The function sorts the elements of an array.

## Arguments

- **`id`** `array<int/float/string>` — An array object.
- **`order`** `series sort_order` (optional) — The sort order: order.ascending (default) or order.descending.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.sort example")
a = array.new_float(0,0)
for i = 0 to 5
	array.push(a, high[i])
array.sort(a, order.descending)
if barstate.islast
	label.new(bar_index, close, str.tostring(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
- [array.reverse()](./reverse.md)
- [order.ascending](../../constants/order/ascending.md)
- [order.descending](../../constants/order/descending.md)
