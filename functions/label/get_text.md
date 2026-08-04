---
title: "label.get_text"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.get_text
---

# label.get_text

**Category:** Function

## Syntax

```pinescript
label.get_text(id) → series string
```

## Description

Returns the text of this label object.

## Arguments

- **`id`** `series label` — Label object.

## Returns

String object containing the text of this label.

**Return type(s):** `series string`

## Examples

```pinescript
//@version=6
indicator("label.get_text")
my_label = label.new(time, open, text="Open bar text", xloc=xloc.bar_time)
a = label.get_text(my_label)
label.new(time, close, text = a + " new", xloc=xloc.bar_time)
```

## See also

- [label.new()](./new.md)
