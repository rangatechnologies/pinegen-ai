---
title: "box.set_text_formatting"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_text_formatting
---

# box.set_text_formatting

**Category:** Function

## Syntax

```pinescript
box.set_text_formatting(id, text_formatting) → void
```

## Description

Sets the formatting attributes the drawing applies to displayed text.

## Arguments

- **`id`** `series box` — A box object.
- **`text_formatting`** `series text_format` — The formatting of the displayed text. Formatting options support addition. For example, `text.format_bold + text.format_italic` will make the text both bold and italicized. Possible values: [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none), [text.format_bold](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_bold), [text.format_italic](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_italic). Optional. The default is [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none).

**Return type(s):** `void`

## See also

- [box.set_text_color()](./set_text_color.md)
- [box.set_text_size()](./set_text_size.md)
- [box.set_text_valign()](./set_text_valign.md)
- [box.set_text_halign()](./set_text_halign.md)
- [box.set_text()](./set_text.md)
