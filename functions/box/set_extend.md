---
title: "box.set_extend"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_extend
---

# box.set_extend

**Category:** Function

## Syntax

```pinescript
box.set_extend(id, extend) → void
```

## Description

Sets extending type of the border of this box object. When [extend.none](../../constants/extend/none.md) is used, the horizontal borders start at the left border and end at the right border. With [extend.left](../../constants/extend/left.md) or [extend.right](../../constants/extend/right.md), the horizontal borders are extended indefinitely to the left or right of the box, respectively. With [extend.both](../../constants/extend/both.md), the horizontal borders are extended on both sides.

## Arguments

- **`id`** `series box` — A box object.
- **`extend`** `series string` — New extending type.

**Return type(s):** `void`

## See also

- [box.new()](./new.md)
- [extend.none](../../constants/extend/none.md)
- [extend.right](../../constants/extend/right.md)
- [extend.left](../../constants/extend/left.md)
- [extend.both](../../constants/extend/both.md)
