---
title: "session.isfirstbar"
kind: variable
namespace: session
source: https://www.tradingview.com/pine-script-reference/v6/#var_session.isfirstbar
---

# session.isfirstbar

**Category:** Variable

**Type:** `series bool`

## Description

Returns [true](../../constants/true.md) if the current bar is the first bar of the day's session, [false](../../constants/false.md) otherwise. If extended session information is used, only returns `true` on the first bar of the pre-market bars.

## Examples

```pinescript
//@version=6
strategy("`session.isfirstbar` Example", overlay = true)
longCondition = year >= 2022
// Place a long order at the `close` of the trading session's first bar.
if session.isfirstbar and longCondition
    strategy.entry("Long", strategy.long)

// Close the long position at the `close` of the trading session's last bar.
if session.islastbar and barstate.isconfirmed
    strategy.close("Long", immediately = true)
```

## See also

- [session.isfirstbar_regular](./isfirstbar_regular.md)
- [session.islastbar](./islastbar.md)
- [session.islastbar_regular](./islastbar_regular.md)
