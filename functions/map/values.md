---
title: "map.values"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.values
---

# map.values

**Category:** Function

## Syntax

```pinescript
map.values(id) → array<type>
```

## Description

Returns an array of all the values in the `id` map. The resulting array is a copy and any changes to it are not reflected in the original map.

## Arguments

- **`id`** `any map type` — A map object.

**Return type(s):** `array<>`

## Remarks

Maps maintain insertion order. The elements within the array returned by this function will also be in the insertion order.

## Examples

```pinescript
//@version=6
indicator("map.values example")
a = map.new<string, float>()
a.put("open", open)
a.put("high", high)
a.put("low", low)
a.put("close", close)
values = map.values(a)
ohlc = 0.0
for value in values
	ohlc += value
plot(ohlc/4)
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.get()](./get.md)
- [map.keys()](./keys.md)
- [map.size()](./size.md)
