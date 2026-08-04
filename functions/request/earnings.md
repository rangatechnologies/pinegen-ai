---
title: "request.earnings"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.earnings
---

# request.earnings

**Category:** Function

## Syntax

```pinescript
request.earnings(ticker, field, gaps, lookahead, ignore_invalid_symbol, currency) → series float
```

## Description

Requests earnings data for the specified symbol.

## Arguments

- **`ticker`** `series string` — Symbol. Note that the symbol should be passed with a prefix. For example: "NASDAQ:AAPL" instead of "AAPL". Using [syminfo.ticker](../../variables/syminfo/ticker.md) will cause an error. Use [syminfo.tickerid](../../variables/syminfo/tickerid.md) instead.
- **`field`** `series string` (optional) — Input string. Possible values include: [earnings.actual](../../constants/earnings/actual.md), [earnings.estimate](../../constants/earnings/estimate.md), [earnings.standardized](../../constants/earnings/standardized.md). Default value is [earnings.actual](../../constants/earnings/actual.md).
- **`gaps`** `simple barmerge_gaps` (optional) — Merge strategy for the requested data (requested data automatically merges with the main series OHLC data). Possible values: [barmerge.gaps_on](../../constants/barmerge/gaps_on.md), [barmerge.gaps_off](../../constants/barmerge/gaps_off.md). [barmerge.gaps_on](../../constants/barmerge/gaps_on.md) - requested data is merged with possible gaps ([na](../../variables/na.md) values). [barmerge.gaps_off](../../constants/barmerge/gaps_off.md) - requested data is merged continuously without gaps, all the gaps are filled with the previous nearest existing values. Default value is [barmerge.gaps_off](../../constants/barmerge/gaps_off.md).
- **`lookahead`** `simple barmerge_lookahead` (optional) — Merge strategy for the requested data position. Possible values: [barmerge.lookahead_on](../../constants/barmerge/lookahead_on.md), [barmerge.lookahead_off](../../constants/barmerge/lookahead_off.md). Default value is [barmerge.lookahead_off](../../constants/barmerge/lookahead_off.md) starting from version 3. Note that behavour is the same on real-time, and differs only on history.
- **`ignore_invalid_symbol`** `input bool` (optional) — An optional parameter. Determines the behavior of the function if the specified symbol is not found: if false, the script will halt and return a runtime error; if true, the function will return na and execution will continue. The default value is false.
- **`currency`** `series string` (optional) — Currency into which the symbol's currency-related earnings values (e.g. [earnings.actual](../../constants/earnings/actual.md)) are to be converted. The conversion rate depends on the previous daily value of a corresponding currency pair from the most popular exchange. A spread symbol is used if no exchange provides the rate directly. Possible values: a "string" representing a valid currency code (e.g., "USD" or "USDT") or a constant from the `currency.*` namespace (e.g., [currency.USD](../../constants/currency/usd.md) or [currency.USDT](../../constants/currency/usdt.md)). The default is [syminfo.currency](../../variables/syminfo/currency.md).

## Returns

Requested series, or n/a if there is no earnings data for the specified symbol.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("request.earnings")
s1 = request.earnings("NASDAQ:BELFA")
plot(s1)
s2 = request.earnings("NASDAQ:BELFA", earnings.actual, gaps=barmerge.gaps_on, lookahead=barmerge.lookahead_on)
plot(s2)
```

## See also

- [request.dividends()](./dividends.md)
- [request.splits()](./splits.md)
- [request.security()](./security.md)
- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
