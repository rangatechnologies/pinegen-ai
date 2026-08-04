---
title: "array.reverse"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.reverse
---

# array.reverse

**Category:** Function

## Syntax

```pinescript
array.reverse(id) → void
```

## Description

The function reverses an array. The first array element becomes the last, and the last array element becomes the first.

## Arguments

- **`id`** `any array type` — An array object.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.reverse example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.get(a, 0))
array.reverse(a)
plot(array.get(a, 0))
```

## See also

- [array.new_float()](./new_float.md)
- [array.sort()](./sort.md)
- [array.push()](./push.md)
- [array.set()](./set.md)
- [array.avg()](./avg.md)
