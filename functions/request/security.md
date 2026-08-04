---
title: "request.security"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.security
---

# request.security

**Category:** Function

## Syntax

```pinescript
request.security(symbol, timeframe, expression, gaps, lookahead, ignore_invalid_symbol, currency, calc_bars_count) → series <type>
```

## Description

Requests the result of an expression from a specified context (symbol and timeframe).

## Arguments

- **`symbol`** `series string` — Symbol or ticker identifier of the requested data. Use an empty string or [syminfo.tickerid](../../variables/syminfo/tickerid.md) to request data using the chart's symbol. To retrieve data with additional modifiers (extended sessions, dividend adjustments, non-standard chart types like Heikin Ashi and Renko, etc.), create a custom ticker ID for the request using the functions in the `ticker.*` namespace.
- **`timeframe`** `series string` — Timeframe of the requested data. Use an empty string or [timeframe.period](../../variables/timeframe/period.md) to request data from the chart's timeframe or the `timeframe` specified in the [indicator()](../indicator.md) function. To request data from a different timeframe, supply a valid timeframe string. See [here](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications) to learn about specifying timeframe strings.
- **`expression`** `variable, function, object, array, matrix, or map of series int/float/bool/string/color/enum, or a tuple of these` — The expression to calculate and return from the requested context. It can accept a built-in variable like [close](../../variables/close.md), a user-defined variable, an expression such as `ta.change(close) / (high - low)`, a function call that does not use Pine Script® drawings, an [object](https://www.tradingview.com/pine-script-docs/language/objects/), a [collection](https://www.tradingview.com/pine-script-docs/language/type-system/#collections), or a tuple of expressions.
- **`gaps`** `simple barmerge_gaps` (optional) — Specifies how the returned values are merged on chart bars. Possible values: [barmerge.gaps_on](../../constants/barmerge/gaps_on.md), [barmerge.gaps_off](../../constants/barmerge/gaps_off.md). With [barmerge.gaps_on](../../constants/barmerge/gaps_on.md) a value only appears on the current chart bar when it first becomes available from the function's context, otherwise [na](../../variables/na.md) is returned (thus a "gap" occurs). With [barmerge.gaps_off](../../constants/barmerge/gaps_off.md) what would otherwise be gaps are filled with the latest known value returned, avoiding [na](../../variables/na.md) values. Optional. The default is [barmerge.gaps_off](../../constants/barmerge/gaps_off.md).
- **`lookahead`** `simple barmerge_lookahead` (optional) — On historical bars only, returns data from the timeframe before it elapses. Possible values: [barmerge.lookahead_on](../../constants/barmerge/lookahead_on.md), [barmerge.lookahead_off](../../constants/barmerge/lookahead_off.md). Has no effect on realtime values. Optional. The default is [barmerge.lookahead_off](../../constants/barmerge/lookahead_off.md) starting from Pine Script® v3. The default is [barmerge.lookahead_on](../../constants/barmerge/lookahead_on.md) in v1 and v2. WARNING: Using [barmerge.lookahead_on](../../constants/barmerge/lookahead_on.md) at timeframes higher than the chart's without offsetting the `expression` argument like in `close[1]` will introduce future leak in scripts, as the function will then return the `close` price before it is actually known in the current context. As is explained in the User Manual's page on [Repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/#future-leak-with-request-security) this will produce misleading results.
- **`ignore_invalid_symbol`** `input bool` (optional) — Determines the behavior of the function if the specified symbol is not found: if [false](../../constants/false.md), the script will halt and throw a runtime error; if [true](../../constants/true.md), the function will return [na](../../variables/na.md) and execution will continue. Optional. The default is [false](../../constants/false.md).
- **`currency`** `series string` (optional) — Optional. Specifies the target currency for converting values expressed in currency units (e.g., [open](../../variables/open.md), [high](../../variables/high.md), [low](../../variables/low.md), [close](../../variables/close.md)) or expressions involving such values. Literal values such as `200` are not converted. The conversion rate for monetary values depends on the previous daily value of a corresponding currency pair from the most popular exchange. A spread symbol is used if no exchange provides the rate directly. Possible values: a "string" representing a valid currency code (e.g., "USD" or "USDT") or a constant from the `currency.*` namespace (e.g., [currency.USD](../../constants/currency/usd.md) or [currency.USDT](../../constants/currency/usdt.md)). The default is [syminfo.currency](../../variables/syminfo/currency.md).
- **`calc_bars_count`** `simple int` (optional) — Optional. Determines the maximum number of recent historical bars that the function can request. If specified, the function evaluates the `expression` argument starting from that number of bars behind the last historical bar in the requested dataset, treating those bars as the only available data. Limiting the number of historical bars in a request can help improve calculation efficiency in some cases. The default is the same as the number of [chart bars](https://www.tradingview.com/pine-script-docs/writing/limitations/#chart-bars) available for the symbol and timeframe. The maximum number of bars that the function can attempt to retrieve depends on the [intrabar limit](https://www.tradingview.com/pine-script-docs/writing/limitations/#intrabars) of the user's plan. However, the request cannot retrieve more bars than are available in the dataset.

## Returns

A result determined by `expression`.

## Remarks

Scripts using this function might calculate differently on historical and realtime bars, leading to [repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

A single script can contain no more than 40 unique `request.*()` function calls. A call is unique only if it does not call the same function with the same arguments.

When using two calls to a `request.*()` function to evaluate the same expression from the same context with different `calc_bars_count` values, the second call requests the same number of historical bars as the first. For example, if a script calls `request.security("AAPL", "", close, calc_bars_count = 3)` after it calls `request.security("AAPL", "", close, calc_bars_count = 5)`, the second call also uses five bars of historical data, not three.

The symbol of a `request.()` call can be *inherited* if it is not specified precisely, i.e., if the `symbol` argument is an empty string or [syminfo.tickerid](../../variables/syminfo/tickerid.md). Similarly, the timeframe of a `request.()` call can be inherited if the `timeframe` argument is an empty string or [timeframe.period](../../variables/timeframe/period.md). These values are normally taken from the chart on which the script is running. However, if `request.*()` function A is called from within the expression of `request.*()` function B, then function A can inherit the values from function B. See [here](https://www.tradingview.com/pine-script-docs/concepts/other-timeframes-and-data/#nested-requests) for more information.

## Detailed Description



```pinescript
//@version=6
indicator("Simple `request.security()` calls")
// Returns 1D close of the current symbol.
dailyClose = request.security(syminfo.tickerid, "1D", close)
plot(dailyClose)

// Returns the close of "AAPL" from the same timeframe as currently open on the chart.
aaplClose = request.security("AAPL", timeframe.period, close)
plot(aaplClose)
```

---



```pinescript
//@version=6
indicator("Advanced `request.security()` calls")
// This calculates a 10-period moving average on the active chart.
sma = ta.sma(close, 10)
// This sends the `sma` calculation for execution in the context of the "AAPL" symbol at a "240" (4 hours) timeframe.
aaplSma = request.security("AAPL", "240", sma)
plot(aaplSma)

// To avoid differences on historical and realtime bars, you can use this technique, which only returns a value from the higher timeframe on the bar after it completes:
indexHighTF = barstate.isrealtime ? 1 : 0
indexCurrTF = barstate.isrealtime ? 0 : 1
nonRepaintingClose = request.security(syminfo.tickerid, "1D", close[indexHighTF])[indexCurrTF]
plot(nonRepaintingClose, "Non-repainting close")

// Returns the 1H close of "AAPL", extended session included. The value is dividend-adjusted.
extendedTicker = ticker.modify("NASDAQ:AAPL", session = session.extended, adjustment = adjustment.dividends)
aaplExtAdj = request.security(extendedTicker, "60", close)
plot(aaplExtAdj)

// Returns the result of a user-defined function.
// The `max` variable is mutable, but we can pass it to `request.security()` because it is wrapped in a function.
allTimeHigh(source) =>
	var max = source
	max := math.max(max, source)
allTimeHigh1D = request.security(syminfo.tickerid, "1D", allTimeHigh(high))

// By using a tuple `expression`, we obtain several values with only one `request.security()` call.
[open1D, high1D, low1D, close1D, ema1D] = request.security(syminfo.tickerid, "1D", [open, high, low, close, ta.ema(close, 10)])
plotcandle(open1D, high1D, low1D, close1D)
plot(ema1D)

// Returns an array containing the OHLC values of the chart's symbol from the 1D timeframe.
ohlcArray = request.security(syminfo.tickerid, "1D", array.from(open, high, low, close))
plotcandle(array.get(ohlcArray, 0), array.get(ohlcArray, 1), array.get(ohlcArray, 2), array.get(ohlcArray, 3))
```

## See also

- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [timeframe.period](../../variables/timeframe/period.md)
- [ticker.new()](../ticker/new.md)
- [ticker.modify()](../ticker/modify.md)
- [request.security_lower_tf()](./security_lower_tf.md)
- [request.dividends()](./dividends.md)
- [request.earnings()](./earnings.md)
- [request.splits()](./splits.md)
- [request.financial()](./financial.md)
