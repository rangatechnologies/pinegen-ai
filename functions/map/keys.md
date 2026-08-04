---
title: "map.keys"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.keys
---

# map.keys

**Category:** Function

## Syntax

```pinescript
map.keys(id) → array<type>
```

## Description

Returns an array of all the keys in the `id` map. The resulting array is a copy and any changes to it are not reflected in the original map.

## Arguments

- **`id`** `any map type` — A map object.

**Return type(s):** `array<>`

## Remarks

Maps maintain insertion order. The elements within the array returned by this function will also be in the insertion order.

## Examples

```pinescript
//@version=6
indicator("map.keys example")
a = map.new<string, float>()
a.put("open", open)
a.put("high", high)
a.put("low", low)
a.put("close", close)
keys = map.keys(a)
ohlc = 0.0
for key in keys
	ohlc += a.get(key)
plot(ohlc/4)
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.get()](./get.md)
- [map.values()](./values.md)
- [map.size()](./size.md)
