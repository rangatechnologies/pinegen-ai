---
title: "box.set_text_wrap"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_text_wrap
---

# box.set_text_wrap

**Category:** Function

## Syntax

```pinescript
box.set_text_wrap(id, text_wrap) → void
```

## Description

The function sets the mode of wrapping of the text inside the box.

## Arguments

- **`id`** `series box` — A box object.
- **`text_wrap`** `series string` — Whether to wrap text. Wrapped text starts a new line when it reaches the side of the box. Wrapped text lower than the bottom of the box is not displayed. Unwrapped text stays on a single line and *is displayed* past the width of the box if it is too long. If the `text_size` is 0 or [text.wrap_auto](../../constants/text/wrap_auto.md), this setting has no effect. Possible values: [text.wrap_none](../../constants/text/wrap_none.md), [text.wrap_auto](../../constants/text/wrap_auto.md).

**Return type(s):** `void`

## See also

- [box.set_text()](./set_text.md)
- [box.set_text_size()](./set_text_size.md)
- [box.set_text_valign()](./set_text_valign.md)
- [box.set_text_halign()](./set_text_halign.md)
- [box.set_text_color()](./set_text_color.md)
