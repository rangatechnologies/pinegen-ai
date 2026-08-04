---
title: "map.size"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.size
---

# map.size

**Category:** Function

## Syntax

```pinescript
map.size(id) → series int
```

## Description

Returns the number of key-value pairs in the `id` map.

## Arguments

- **`id`** `any map type` — A map object.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("map.size example")
a = map.new<int, int>()
size = 10
for i = 0 to size
	a.put(i, size-i)
plot(map.size(a))
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.get()](./get.md)
