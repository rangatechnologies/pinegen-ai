---
title: "bar_index"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_bar_index
---

# bar_index

**Category:** Variable

**Type:** `series int`

## Description

Current bar index. Numbering is zero-based, index of the first bar is 0.

## Remarks

Note that **bar_index** has replaced **n** variable in version 4.

Note that bar indexing starts from 0 on the first historical bar.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## Examples

```pinescript
//@version=6
indicator("bar_index")
plot(bar_index)
plot(bar_index > 5000 ? close : 0)
```

## See also

- [last_bar_index](./last_bar_index.md)
- [barstate.isfirst](./barstate/isfirst.md)
- [barstate.islast](./barstate/islast.md)
- [barstate.isrealtime](./barstate/isrealtime.md)
