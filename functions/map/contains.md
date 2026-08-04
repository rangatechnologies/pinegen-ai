---
title: "map.contains"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.contains
---

# map.contains

**Category:** Function

## Syntax

```pinescript
map.contains(id, key) → series bool
```

## Description

Returns [true](../../constants/true.md) if the `key` was found in the `id` map, [false](../../constants/false.md) otherwise.

## Arguments

- **`id`** `any map type` — A map object.
- **`key`** `series <type of the map's elements>` — The key to search in the map.

**Return type(s):** `series bool`

## Examples

```pinescript
//@version=6
indicator("map.includes example")
a = map.new<string, float>()
a.put("open", open)
p = close
if map.contains(a, "open")
	p := a.get("open")
plot(p)
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.size()](./size.md)
