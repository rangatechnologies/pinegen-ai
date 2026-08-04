---
title: "map.copy"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.copy
---

# map.copy

**Category:** Function

## Syntax

```pinescript
map.copy(id) → map<keyType, valueType>
```

## Description

Creates a copy of an existing map.

## Arguments

- **`id`** `any map type` — A map object to copy.

## Returns

A copy of the `id` map.

## Examples

```pinescript
//@version=6
indicator("map.copy example")
a = map.new<string, int>()
a.put("example", 1)
b = map.copy(a)
a := map.new<string, int>()
a.put("example", 2)
plot(a.get("example"))
plot(b.get("example"))
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.get()](./get.md)
- [map.size()](./size.md)
