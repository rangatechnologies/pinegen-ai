---
title: "map.put"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.put
---

# map.put

**Category:** Function

## Syntax

```pinescript
map.put(id, key, value) → <value_type>
```

## Description

Puts a new key-value pair into the `id` map.

## Arguments

- **`id`** `any map type` — A map object.
- **`key`** `series <type of the map's elements>` — The key to put into the map.
- **`value`** `series <type of the map's elements>` — The key value to put into the map.

## Returns

The previous value associated with `key` if the key was already present in the map, or [na](../../variables/na.md) if the key is new.

## Remarks

Maps maintain insertion order. Note that the order does not change when inserting a pair with a `key` that's already in the map. The new pair replaces the existing pair with the `key` in such cases.

## Examples

```pinescript
//@version=6
indicator("map.put example")
a = map.new<string, float>()
map.put(a, "first", 10)
map.put(a, "second", 15)
prevFirst = map.put(a, "first", 20)
currFirst = a.get("first")
plot(prevFirst)
plot(currFirst)
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put_all()](./put_all.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.remove()](./remove.md)
