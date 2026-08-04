---
title: "map.put_all"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.put_all
---

# map.put_all

**Category:** Function

## Syntax

```pinescript
map.put_all(id, id2) → void
```

## Description

Puts all key-value pairs from the `id2` map into the `id` map.

## Arguments

- **`id`** `any map type` — A map object to append to.
- **`id2`** `any map type` — A map object to be appended.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("map.put_all example")
a = map.new<string, float>()
b = map.new<string, float>()
a.put("first", 10)
a.put("second", 15)
b.put("third", 20)
map.put_all(a, b)
plot(a.get("third"))
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put()](./put.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.remove()](./remove.md)
