---
title: "table.set_position"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.set_position
---

# table.set_position

**Category:** Function

## Syntax

```pinescript
table.set_position(table_id, position) → void
```

## Description

The function sets the position of a table.

## Arguments

- **`table_id`** `series table` — A table object.
- **`position`** `series string` — Position of the table. Possible values are: [position.top_left](../../constants/position/top_left.md), [position.top_center](../../constants/position/top_center.md), [position.top_right](../../constants/position/top_right.md), [position.middle_left](../../constants/position/middle_left.md), [position.middle_center](../../constants/position/middle_center.md), [position.middle_right](../../constants/position/middle_right.md), [position.bottom_left](../../constants/position/bottom_left.md), [position.bottom_center](../../constants/position/bottom_center.md), [position.bottom_right](../../constants/position/bottom_right.md).

**Return type(s):** `void`

## See also

- [table.clear()](./clear.md)
- [table.delete()](./delete.md)
- [table.new()](./new.md)
- [table.set_bgcolor()](./set_bgcolor.md)
- [table.set_border_color()](./set_border_color.md)
- [table.set_border_width()](./set_border_width.md)
- [table.set_frame_color()](./set_frame_color.md)
- [table.set_frame_width()](./set_frame_width.md)
