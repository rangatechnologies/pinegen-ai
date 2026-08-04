---
title: "label.get_x"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.get_x
---

# label.get_x

**Category:** Function

## Syntax

```pinescript
label.get_x(id) → series int
```

## Description

Returns UNIX time or bar index (depending on the last xloc value set) of this label's position.

## Arguments

- **`id`** `series label` — Label object.

## Returns

UNIX timestamp (in milliseconds) or bar index.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("label.get_x")
my_label = label.new(time, open, text="Open bar text", xloc=xloc.bar_time)
a = label.get_x(my_label)
plot(time - label.get_x(my_label)) //draws zero plot
```

## See also

- [label.new()](./new.md)
