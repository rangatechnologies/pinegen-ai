---
title: "ticker.modify"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.modify
---

# ticker.modify

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.modify(tickerid, session, adjustment, backadjustment, settlement_as_close) → simple string
```

```pinescript
ticker.modify(tickerid, session, adjustment, backadjustment, settlement_as_close) → series string
```

## Description

Creates a ticker identifier for requesting additional data for the script.

## Arguments

- **`tickerid`** `simple string` — Symbol name with exchange prefix, e.g. 'BATS:MSFT', 'NASDAQ:MSFT' or tickerid with session and adjustment from the [ticker.new()](./new.md) function.
- **`session`** `simple string` (optional) — Session type. Optional argument. Possible values: [session.regular](../../constants/session/regular.md), [session.extended](../../constants/session/extended.md). Session type of the current chart is [syminfo.session](../../variables/syminfo/session.md). If session is not given, then [syminfo.session](../../variables/syminfo/session.md) value is used.
- **`adjustment`** `simple string` (optional) — Adjustment type. Optional argument. Possible values: [adjustment.none](../../constants/adjustment/none.md), [adjustment.splits](../../constants/adjustment/splits.md), [adjustment.dividends](../../constants/adjustment/dividends.md). If adjustment is not given, then default adjustment value is used (can be different depending on particular instrument).
- **`backadjustment`** `simple backadjustment` (optional) — Specifies whether past contract data on continuous futures symbols is back-adjusted. This setting only affects the data from symbols with this option available on their charts. Optional. The default is [backadjustment.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.inherit), meaning that the modified ticker ID inherits the setting from the ticker ID passed to the `tickerid` parameter, or it inherits the symbol's default if the `tickerid` does not specify this setting. Possible values: [backadjustment.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.inherit), [backadjustment.on](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.on), [backadjustment.off](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.off).
- **`settlement_as_close`** `simple settlement` (optional) — Specifies whether a futures symbol's [close](../../variables/close.md) value represents the actual closing price or the settlement price on "1D" and higher timeframes. This setting only affects the data from symbols with this option available on their charts. Optional. The default is [settlement_as_close.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.inherit), meaning that the modified ticker ID inherits the setting from the `tickerid` passed into the function, or it inherits the chart symbol's default if the `tickerid` does not specify this setting. Possible values: [settlement_as_close.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.inherit), [settlement_as_close.on](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.on), [settlement_as_close.off](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.off).

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Examples

```pinescript
//@version=6
indicator("ticker_modify", overlay=true)
t1 = ticker.new(syminfo.prefix, syminfo.ticker, session.regular, adjustment.splits)
c1 = request.security(t1, "D", close)
t2 = ticker.modify(t1, session.extended)
c2 = request.security(t2, "2D", close)
plot(c1)
plot(c2)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [syminfo.session](../../variables/syminfo/session.md)
- [session.extended](../../constants/session/extended.md)
- [session.regular](../../constants/session/regular.md)
- [ticker.heikinashi()](./heikinashi.md)
- [adjustment.none](../../constants/adjustment/none.md)
- [adjustment.splits](../../constants/adjustment/splits.md)
- [adjustment.dividends](../../constants/adjustment/dividends.md)
- [backadjustment.inherit](../../constants/backadjustment/inherit.md)
- [backadjustment.on](../../constants/backadjustment/on.md)
- [backadjustment.off](../../constants/backadjustment/off.md)
- [settlement_as_close.inherit](../../constants/settlement_as_close/inherit.md)
- [settlement_as_close.on](../../constants/settlement_as_close/on.md)
- [settlement_as_close.off](../../constants/settlement_as_close/off.md)
