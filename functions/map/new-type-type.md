---
title: "map.new<type,type>"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.new<type,type>
---

# map.new<type,type>

**Category:** Function

## Syntax

```pinescript
map.new<keyType, valueType>() → map<keyType, valueType>
```

## Description

Creates a new map object: a collection that consists of key-value pairs, where all keys are of the `keyType`, and all values are of the `valueType`.

`keyType` can be a primitive type or enum. For example: [int](../../types/int.md), [float](../../types/float.md), [bool](../../types/bool.md), [string](../../types/string.md), [color](../../types/color.md).

`valueType` can be of any type except `array<>`, `matrix<>`, and `map<>`. User-defined types are allowed, even if they have `array<>`, `matrix<>`, or `map<>` as one of their fields.

## Returns

The ID of a map object which may be used in other map.*() functions.

## Remarks

Each key is unique and can only appear once. When adding a new value with a key that the map already contains, that value replaces the old value associated with the key.

Maps maintain insertion order. Note that the order does not change when inserting a pair with a `key` that's already in the map. The new pair replaces the existing pair with the `key` in such cases.

## Examples

```pinescript
//@version=6
indicator("map.new<string, int> example")
a = map.new<string, int>()
a.put("example", 1)
label.new(bar_index, close, str.tostring(a.get("example")))
```

## See also

- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.get()](./get.md)
- [array.new<type>()](../array/new-type.md)
