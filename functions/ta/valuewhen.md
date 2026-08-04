---
title: "ta.valuewhen"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.valuewhen
---

# ta.valuewhen

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
ta.valuewhen(condition, source, occurrence) → series float
```

```pinescript
ta.valuewhen(condition, source, occurrence) → series int
```

```pinescript
ta.valuewhen(condition, source, occurrence) → series bool
```

```pinescript
ta.valuewhen(condition, source, occurrence) → series color
```

## Description

Returns the value of the `source` series on the bar where the `condition` was true on the nth most recent occurrence.

## Arguments

- **`condition`** `series bool` — The condition to search for.
- **`source`** `series int/float` — The value to be returned from the bar where the condition is met.
- **`occurrence`** `simple int` — The occurrence of the condition. The numbering starts from 0 and goes back in time, so '0' is the most recent occurrence of `condition`, '1' is the second most recent and so forth. Must be an integer >= 0.

**Return type(s):** `series float`

## Remarks

This function requires execution on every bar. It is not recommended to use it inside a [for](../../keywords/for.md) or [while](../../keywords/while.md) loop structure, where its behavior can be unexpected. Please note that using this function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## Examples

```pinescript
//@version=6
indicator("ta.valuewhen")
slow = ta.sma(close, 7)
fast = ta.sma(close, 14)
// Get value of `close` on second most recent cross
plot(ta.valuewhen(ta.cross(slow, fast), close, 1))
```

## See also

- [ta.lowestbars()](./lowestbars.md)
- [ta.highestbars()](./highestbars.md)
- [ta.barssince()](./barssince.md)
- [ta.highest()](./highest.md)
- [ta.lowest()](./lowest.md)
