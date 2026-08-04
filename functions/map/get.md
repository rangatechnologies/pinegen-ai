---
title: "map.get"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.get
---

# map.get

**Category:** Function

## Syntax

```pinescript
map.get(id, key) → <value_type>
```

## Description

Returns the value associated with the specified `key` in the `id` map.

## Arguments

- **`id`** `any map type` — A map object.
- **`key`** `series <type of the map's elements>` — The key of the value to retrieve.

## Examples

```pinescript
//@version=6
indicator("map.get example")
a = map.new<int, int>()
size = 10
for i = 0 to size
	a.put(i, size-i)
plot(map.get(a, 1))
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.contains()](./contains.md)
