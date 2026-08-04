---
title: "map.remove"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.remove
---

# map.remove

**Category:** Function

## Syntax

```pinescript
map.remove(id, key) → <value_type>
```

## Description

Removes a key-value pair from the `id` map.

## Arguments

- **`id`** `any map type` — A map object.
- **`key`** `series <type of the map's elements>` — The key of the pair to remove from the map.

## Returns

The previous value associated with `key` if the key was present in the map, or [na](../../variables/na.md) if there was no such key.

## Examples

```pinescript
//@version=6
indicator("map.remove example")
a = map.new<string, color>()
a.put("firstColor", color.green)
oldColorValue = map.remove(a, "firstColor")
plot(close, color = oldColorValue)
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.clear()](./clear.md)
