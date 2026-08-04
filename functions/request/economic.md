---
title: "request.economic"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.economic
---

# request.economic

**Category:** Function

## Syntax

```pinescript
request.economic(country_code, field, gaps, ignore_invalid_symbol) → series float
```

## Description

Requests economic data for a symbol. Economic data includes information such as the state of a country's economy (GDP, inflation rate, etc.) or of a particular industry (steel production, ICU beds, etc.).

## Arguments

- **`country_code`** `series string` — The code of the country (e.g. "US") or the region (e.g. "EU") for which the economic data is requested. The [Help Center article](https://www.tradingview.com/chart/?solution=43000665359) lists the countries and their codes. The countries for which information is available vary with metrics. The [Help Center article for each metric](https://www.tradingview.com/support/folders/43000581956-list-of-available-economic-indicators/) lists the countries for which the metric is available.
- **`field`** `series string` — The code of the requested economic metric (e.g., "GDP"). The [Help Center article](https://www.tradingview.com/chart/?solution=43000665359) lists the metrics and their codes.
- **`gaps`** `simple barmerge_gaps` (optional) — Specifies how the returned values are merged on chart bars. Possible values: [barmerge.gaps_off](../../constants/barmerge/gaps_off.md), [barmerge.gaps_on](../../constants/barmerge/gaps_on.md). With [barmerge.gaps_on](../../constants/barmerge/gaps_on.md), a value only appears on the current chart bar when it first becomes available from the function's context, otherwise [na](../../variables/na.md) is returned (thus a "gap" occurs). With [barmerge.gaps_off](../../constants/barmerge/gaps_off.md), what would otherwise be gaps are filled with the latest known value returned, avoiding [na](../../variables/na.md) values. Optional. The default is [barmerge.gaps_off](../../constants/barmerge/gaps_off.md).
- **`ignore_invalid_symbol`** `input bool` (optional) — Determines the behavior of the function if the specified symbol is not found: if [false](../../constants/false.md), the script will halt and return a runtime error; if [true](../../constants/true.md), the function will return [na](../../variables/na.md) and execution will continue. Optional. The default is [false](../../constants/false.md).

## Returns

Requested series.

**Return type(s):** `series float`

## Remarks

Economic data can also be accessed from charts, just like a regular symbol. Use "ECONOMIC" as the exchange name and `{country_code}{field}` as the ticker. The name of US GDP data is thus "ECONOMIC:USGDP".

## Examples

```pinescript
//@version=6
indicator("US GDP")
e = request.economic("US", "GDP")
plot(e)
```

## See also

- [request.financial()](./financial.md)
