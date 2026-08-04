---
title: "session.islastbar_regular"
kind: variable
namespace: session
source: https://www.tradingview.com/pine-script-reference/v6/#var_session.islastbar_regular
---

# session.islastbar_regular

**Category:** Variable

**Type:** `series bool`

## Description

Returns [true](../../constants/true.md) on the last regular session bar of the day, [false](../../constants/false.md) otherwise. The result is the same whether extended session information is used or not.

## Remarks

This variable is not guaranteed to return [true](../../constants/true.md) once in every session because the last bar of the session might not exist if no trades occur during what should be the session's last bar.

This variable is not guaranteed to work as expected on non-standard chart types, e.g., Renko.

## Examples

```pinescript
//@version=6
strategy("`session.islastbar_regular` Example", overlay = true)
longCondition = year >= 2022
// Place a long order at the `close` of the trading session's first bar.
if session.isfirstbar and longCondition
    strategy.entry("Long", strategy.long)
// Close the long position at the `close` of the trading session's last bar.
if session.islastbar_regular and barstate.isconfirmed
    strategy.close("Long", immediately = true)
```

## See also

- [session.isfirstbar](./isfirstbar.md)
- [session.islastbar](./islastbar.md)
- [session.isfirstbar_regular](./isfirstbar_regular.md)
