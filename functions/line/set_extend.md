---
title: "line.set_extend"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.set_extend
---

# line.set_extend

**Category:** Function

## Syntax

```pinescript
line.set_extend(id, extend) → void
```

## Description

Sets extending type of this line object. If extend=[extend.none](../../constants/extend/none.md), draws segment starting at point (x1, y1) and ending at point (x2, y2). If extend is equal to [extend.right](../../constants/extend/right.md) or [extend.left](../../constants/extend/left.md), draws a ray starting at point (x1, y1) or (x2, y2), respectively. If extend=[extend.both](../../constants/extend/both.md), draws a straight line that goes through these points.

## Arguments

- **`id`** `series line` — Line object.
- **`extend`** `series string` — New extending type.

**Return type(s):** `void`

## See also

- [extend.none](../../constants/extend/none.md)
- [extend.right](../../constants/extend/right.md)
- [extend.left](../../constants/extend/left.md)
- [extend.both](../../constants/extend/both.md)
- [line.new()](./new.md)
