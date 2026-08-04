---
title: "label.set_text_font_family"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.set_text_font_family
---

# label.set_text_font_family

**Category:** Function

## Syntax

```pinescript
label.set_text_font_family(id, text_font_family) → void
```

## Description

The function sets the font family of the text inside the label.

## Arguments

- **`id`** `series label` — A label object.
- **`text_font_family`** `series string` — The font family of the text. Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("Example of setting the label font")
if barstate.islastconfirmedhistory
    l = label.new(bar_index, 0, "monospace", yloc=yloc.abovebar)
    label.set_text_font_family(l, font.family_monospace)
```

## See also

- [label.new()](./new.md)
- [font.family_default](../../constants/font/family_default.md)
- [font.family_monospace](../../constants/font/family_monospace.md)
