---
title: "map.clear"
kind: function
namespace: map
source: https://www.tradingview.com/pine-script-reference/v6/#fun_map.clear
---

# map.clear

**Category:** Function

## Syntax

```pinescript
map.clear(id) → void
```

## Description

Clears the map, removing all key-value pairs from it.

## Arguments

- **`id`** `any map type` — A map object.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("map.clear example")
oddMap = map.new<int, bool>()
oddMap.put(1, true)
oddMap.put(2, false)
oddMap.put(3, true)
map.clear(oddMap)
plot(oddMap.size())
```

## See also

- [map.new<type,type>()](./new-type-type.md)
- [map.put_all()](./put_all.md)
- [map.keys()](./keys.md)
- [map.values()](./values.md)
- [map.remove()](./remove.md)
