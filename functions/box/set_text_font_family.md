---
title: "box.set_text_font_family"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_text_font_family
---

# box.set_text_font_family

**Category:** Function

## Syntax

```pinescript
box.set_text_font_family(id, text_font_family) → void
```

## Description

The function sets the font family of the text inside the box.

## Arguments

- **`id`** `series box` — A box object.
- **`text_font_family`** `series string` — The font family of the text. Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("Example of setting the box font")
if barstate.islastconfirmedhistory
    b = box.new(bar_index, open-ta.tr, bar_index-50, open-ta.tr*5, text="monospace")
    box.set_text_font_family(b, font.family_monospace)
```

## See also

- [box.new()](./new.md)
- [font.family_default](../../constants/font/family_default.md)
- [font.family_monospace](../../constants/font/family_monospace.md)
