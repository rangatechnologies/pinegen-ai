---
title: "request.quandl"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.quandl
---

# request.quandl

**Category:** Function

## Syntax

```pinescript
request.quandl(ticker, gaps, index, ignore_invalid_symbol) → series float
```

## Description

**Note:** This function has been deprecated due to the API change from NASDAQ Data Link. Requests for "QUANDL" symbols are no longer valid and requests for them return a runtime error.

Some of the data previously provided by this function is available on TradingView through other feeds, such as "BCHAIN" or "FRED". Use Symbol Search to look for such data based on its description. Commitment of Traders (COT) data can be requested using the official [LibraryCOT](https://www.tradingview.com/v/ysFf2OTq/) library.

Requests [Nasdaq Data Link](https://data.nasdaq.com/) (formerly Quandl) data for a symbol.

## Arguments

- **`ticker`** `series string` — Symbol. Note that the name of a time series and Quandl data feed should be divided by a forward slash. For example: "CFTC/SB_FO_ALL".
- **`gaps`** `simple barmerge_gaps` (optional) — Merge strategy for the requested data (requested data automatically merges with the main series: OHLC data). Possible values include: [barmerge.gaps_on](../../constants/barmerge/gaps_on.md), [barmerge.gaps_off](../../constants/barmerge/gaps_off.md). [barmerge.gaps_on](../../constants/barmerge/gaps_on.md) - requested data is merged with possible gaps ([na](../../variables/na.md) values). [barmerge.gaps_off](../../constants/barmerge/gaps_off.md) - requested data is merged continuously without gaps, all the gaps are filled with the previous, nearest existing values. Default value is [barmerge.gaps_off](../../constants/barmerge/gaps_off.md).
- **`index`** `series int` (optional) — A Quandl time-series column index.
- **`ignore_invalid_symbol`** `input bool` (optional) — An optional parameter. Determines the behavior of the function if the specified symbol is not found: if false, the script will halt and return a runtime error; if true, the function will return na and execution will continue. The default value is false.

## Returns

Requested series.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("request.quandl")
f = request.quandl("CFTC/SB_FO_ALL", barmerge.gaps_off, 0)
plot(f)
```

## See also

- [request.security()](./security.md)
- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
