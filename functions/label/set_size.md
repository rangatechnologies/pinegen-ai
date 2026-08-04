---
title: "label.set_size"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.set_size
---

# label.set_size

**Category:** Function

## Syntax

```pinescript
label.set_size(id, size) → void
```

## Description

Sets arrow and text size of the specified label object.

## Arguments

- **`id`** `series label` — Label object.
- **`size`** `series int/string` — Size of the label. Accepts a positive [int](../../types/int.md) value or one of the built-in `size.*` constants. The constants and their equivalent numeric sizes are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (\~7), [size.small](../../constants/size/small.md) (\~10), [size.normal](../../constants/size/normal.md) (12), [size.large](../../constants/size/large.md) (18), [size.huge](../../constants/size/huge.md) (24). The default value is [size.normal](../../constants/size/normal.md), which represents the numeric size of 12.

**Return type(s):** `void`

## See also

- [size.auto](../../constants/size/auto.md)
- [size.tiny](../../constants/size/tiny.md)
- [size.small](../../constants/size/small.md)
- [size.normal](../../constants/size/normal.md)
- [size.large](../../constants/size/large.md)
- [size.huge](../../constants/size/huge.md)
- [label.new()](./new.md)
