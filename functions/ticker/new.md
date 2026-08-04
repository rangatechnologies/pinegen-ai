---
title: "ticker.new"
kind: function
namespace: ticker
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ticker.new
---

# ticker.new

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ticker.new(prefix, ticker, session, adjustment, backadjustment, settlement_as_close) → simple string
```

```pinescript
ticker.new(prefix, ticker, session, adjustment, backadjustment, settlement_as_close) → series string
```

## Description

Creates a ticker identifier for requesting additional data for the script.

## Arguments

- **`prefix`** `simple string` — Exchange prefix. For example: 'BATS', 'NYSE', 'NASDAQ'. Exchange prefix of main series is [syminfo.prefix](../../variables/syminfo/prefix.md).
- **`ticker`** `simple string` — Ticker name. For example 'AAPL', 'MSFT', 'EURUSD'. Ticker name of the main series is [syminfo.ticker](../../variables/syminfo/ticker.md).
- **`session`** `simple string` (optional) — Session type. Optional argument. Possible values: [session.regular](../../constants/session/regular.md), [session.extended](../../constants/session/extended.md). Session type of the current chart is [syminfo.session](../../variables/syminfo/session.md). If session is not given, then [syminfo.session](../../variables/syminfo/session.md) value is used.
- **`adjustment`** `simple string` (optional) — Adjustment type. Optional argument. Possible values: [adjustment.none](../../constants/adjustment/none.md), [adjustment.splits](../../constants/adjustment/splits.md), [adjustment.dividends](../../constants/adjustment/dividends.md). If adjustment is not given, then default adjustment value is used (can be different depending on particular instrument).
- **`backadjustment`** `simple backadjustment` (optional) — Specifies whether past contract data on continuous futures symbols is back-adjusted. This setting only affects the data from symbols with this option available on their charts. Optional. The default is [backadjustment.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.inherit), meaning that the new ticker ID inherits the symbol's default setting. Possible values: [backadjustment.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.inherit), [backadjustment.on](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.on), [backadjustment.off](https://www.tradingview.com/pine-script-reference/v6/#var_backadjustment.off).
- **`settlement_as_close`** `simple settlement` (optional) — Specifies whether a futures symbol's [close](../../variables/close.md) value represents the actual closing price or the settlement price on "1D" and higher timeframes. This setting only affects the data from symbols with this option available on their charts. Optional. The default is [settlement_as_close.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.inherit), meaning that the new ticker ID inherits the chart symbol's default setting. Possible values: [settlement_as_close.inherit](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.inherit), [settlement_as_close.on](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.on), [settlement_as_close.off](https://www.tradingview.com/pine-script-reference/v6/#var_settlement_as_close.off).

## Returns

String value of ticker id, that can be supplied to [request.security()](../request/security.md) function.

**Return type(s):** `simple string`

## Remarks

You may use return value of [ticker.new()](./new.md) function as input argument for [ticker.heikinashi()](./heikinashi.md), [ticker.renko()](./renko.md), [ticker.linebreak()](./linebreak.md), [ticker.kagi()](./kagi.md), [ticker.pointfigure()](./pointfigure.md) functions.

## Examples

```pinescript
//@version=6
indicator("ticker.new", overlay=true)
t = ticker.new(syminfo.prefix, syminfo.ticker, session.regular, adjustment.splits)
t2 = ticker.heikinashi(t)
c = request.security(t2, timeframe.period, low, barmerge.gaps_on)
plot(c, style=plot.style_linebr)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [syminfo.session](../../variables/syminfo/session.md)
- [session.extended](../../constants/session/extended.md)
- [session.regular](../../constants/session/regular.md)
- [ticker.heikinashi()](./heikinashi.md)
- [adjustment.none](https://www.tradingview.com/pine-script-reference/v6/#var_adjustment.none)
- [adjustment.splits](https://www.tradingview.com/pine-script-reference/v6/#var_adjustment.splits)
- [adjustment.dividends](https://www.tradingview.com/pine-script-reference/v6/#var_adjustment.dividends)
- [backadjustment.inherit](../../constants/backadjustment/inherit.md)
- [backadjustment.on](../../constants/backadjustment/on.md)
- [backadjustment.off](../../constants/backadjustment/off.md)
- [settlement_as_close.inherit](../../constants/settlement_as_close/inherit.md)
- [settlement_as_close.on](../../constants/settlement_as_close/on.md)
- [settlement_as_close.off](../../constants/settlement_as_close/off.md)
