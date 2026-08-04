---
title: "map"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_map
---

# map

**Category:** Type

## Description

Keyword used to explicitly declare the "map" type of a variable or a parameter. Map objects (or IDs) can be created with the [map.new<type,type>()](../functions/map/new-type-type.md) function.

## Remarks

Map objects are always of [series](https://www.tradingview.com/pine-script-docs/language/type-system/#series) form.

## Examples

```pinescript
//@version=6
indicator("map", overlay=true)
map<int, float> a = na
a := map.new<int, float>()
a.put(bar_index, close)
label.new(bar_index, a.get(bar_index), "Current close")
```

## See also

- [map.new<type,type>()](../functions/map/new-type-type.md)
