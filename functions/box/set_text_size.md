---
title: "box.set_text_size"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_text_size
---

# box.set_text_size

**Category:** Function

## Syntax

```pinescript
box.set_text_size(id, text_size) → void
```

## Description

The function sets the size of the box's text.

## Arguments

- **`id`** `series box` — A box object.
- **`text_size`** `series int/string` — Size of the box's text. The size can be any positive integer, or one of the `size.*` built-in constant strings. The constant strings and their equivalent integer values are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (8), [size.small](../../constants/size/small.md) (10), [size.normal](../../constants/size/normal.md) (14), [size.large](../../constants/size/large.md) (20), [size.huge](../../constants/size/huge.md) (36).

**Return type(s):** `void`

## See also

- [box.set_text()](./set_text.md)
- [box.set_text_color()](./set_text_color.md)
- [box.set_text_valign()](./set_text_valign.md)
- [box.set_text_halign()](./set_text_halign.md)
