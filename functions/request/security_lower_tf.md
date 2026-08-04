---
title: "request.security_lower_tf"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.security_lower_tf
---

# request.security_lower_tf

**Category:** Function

## Syntax

```pinescript
request.security_lower_tf(symbol, timeframe, expression, ignore_invalid_symbol, currency, ignore_invalid_timeframe, calc_bars_count) → array<type>
```

## Description

Requests the results of an expression from a specified symbol on a timeframe lower than or equal to the chart's timeframe. It returns an [array](../../types/array.md) containing one element for each lower-timeframe bar within the chart bar. On a 5-minute chart, requesting data using a `timeframe` argument of "1" typically returns an array with five elements representing the value of the `expression` on each 1-minute bar, ordered by time with the earliest value first.

## Arguments

- **`symbol`** `series string` — Symbol or ticker identifier of the requested data. Use an empty string or [syminfo.tickerid](../../variables/syminfo/tickerid.md) to request data using the chart's symbol. To retrieve data with additional modifiers (extended sessions, dividend adjustments, non-standard chart types like Heikin Ashi and Renko, etc.), create a custom ticker ID for the request using the functions in the `ticker.*` namespace.
- **`timeframe`** `series string` — Timeframe of the requested data. Use an empty string or [timeframe.period](../../variables/timeframe/period.md) to request data from the chart's timeframe or the `timeframe` specified in the [indicator()](../indicator.md) function. To request data from a different timeframe, supply a valid timeframe string. See [here](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications) to learn about specifying timeframe strings.
- **`expression`** `variable, object or function of series int/float/bool/string/color/enum, or a tuple of these` — The expression to calculate and return from the requested context. It can accept a built-in variable like [close](../../variables/close.md), a user-defined variable, an expression such as `ta.change(close) / (high - low)`, a function call that does not use Pine Script® drawings, an [object](https://www.tradingview.com/pine-script-docs/language/objects/), or a tuple of expressions. [Collections](https://www.tradingview.com/pine-script-docs/language/type-system/#collections) are not allowed unless they are within the fields of an object
- **`ignore_invalid_symbol`** `series bool` (optional) — Determines the behavior of the function if the specified symbol is not found: if [false](../../constants/false.md), the script will halt and throw a runtime error; if [true](../../constants/true.md), the function will return [na](../../variables/na.md) and execution will continue. Optional. The default is [false](../../constants/false.md).
- **`currency`** `series string` (optional) — Optional. Specifies the target currency for converting values expressed in currency units (e.g., [open](../../variables/open.md), [high](../../variables/high.md), [low](../../variables/low.md), [close](../../variables/close.md)) or expressions involving such values. Literal values such as `200` are not converted. The conversion rate for monetary values depends on the previous daily value of a corresponding currency pair from the most popular exchange. A spread symbol is used if no exchange provides the rate directly. Possible values: a "string" representing a valid currency code (e.g., "USD" or "USDT") or a constant from the `currency.*` namespace (e.g., [currency.USD](../../constants/currency/usd.md) or [currency.USDT](../../constants/currency/usdt.md)). The default is [syminfo.currency](../../variables/syminfo/currency.md).
- **`ignore_invalid_timeframe`** `series bool` (optional) — Determines the behavior of the function when the chart's timeframe is smaller than the `timeframe` used in the function call. If [false](../../constants/false.md), the script will halt and throw a runtime error. If [true](../../constants/true.md), the function will return [na](../../variables/na.md) and execution will continue. Optional. The default is [false](../../constants/false.md).
- **`calc_bars_count`** `simple int` (optional) — Optional. Determines the maximum number of recent historical bars that the function can request. If specified, the function evaluates the `expression` argument starting from that number of bars behind the last historical bar in the requested dataset, treating those bars as the only available data. Limiting the number of historical bars in a request can help improve calculation efficiency in some cases. The default is the same as the number of [chart bars](https://www.tradingview.com/pine-script-docs/writing/limitations/#chart-bars) available for the symbol and timeframe. The maximum number of bars that the function can attempt to retrieve depends on the [intrabar limit](https://www.tradingview.com/pine-script-docs/writing/limitations/#intrabars) of the user's plan. However, the request cannot retrieve more bars than are available in the dataset.

## Returns

An array of a type determined by `expression`, or a tuple of these.

## Remarks

Scripts using this function might calculate differently on historical and realtime bars, leading to [repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

Please note that spreads (e.g., "AAPL+MSFT*TSLA") do not always return reliable data with this function.

A single script can contain no more than 40 unique `request.*()` function calls. A call is unique only if it does not call the same function with the same arguments.

When using two calls to a `request.*()` function to evaluate the same expression from the same context with different `calc_bars_count` values, the second call requests the same number of historical bars as the first. For example, if a script calls `request.security("AAPL", "", close, calc_bars_count = 3)` after it calls `request.security("AAPL", "", close, calc_bars_count = 5)`, the second call also uses five bars of historical data, not three.

The symbol of a `request.()` call can be *inherited* if it is not specified precisely, i.e., if the `symbol` argument is an empty string or [syminfo.tickerid](../../variables/syminfo/tickerid.md). Similarly, the timeframe of a `request.()` call can be inherited if the `timeframe` argument is an empty string or [timeframe.period](../../variables/timeframe/period.md). These values are normally taken from the chart that the script is running on. However, if `request.*()` function A is called from within the expression of `request.*()` function B, then function A can inherit the values from function B. See [here](https://www.tradingview.com/pine-script-docs/concepts/other-timeframes-and-data/#nested-requests) for more information.

## Examples

```pinescript
//@version=6
indicator("`request.security_lower_tf()` Example", overlay = true)

// If the current chart timeframe is set to 120 minutes, then the `arrayClose` array will contain two 'close' values from the 60 minute timeframe for each bar.
arrClose = request.security_lower_tf(syminfo.tickerid, "60", close)

if bar_index == last_bar_index - 1
    label.new(bar_index, high, str.tostring(arrClose))
```

## See also

- [request.security()](./security.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [timeframe.period](../../variables/timeframe/period.md)
- [ticker.new()](../ticker/new.md)
- [request.dividends()](./dividends.md)
- [request.earnings()](./earnings.md)
- [request.splits()](./splits.md)
- [request.financial()](./financial.md)
