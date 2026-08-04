---
title: "syminfo.target_price_estimates"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.target_price_estimates
---

# syminfo.target_price_estimates

**Category:** Variable

**Type:** `series float`

## Description

The latest total number of price target predictions for the current symbol.

## Remarks

If analysts supply the targets when the market is closed, the variable can return [na](../na.md) until the market opens.

## Examples

```pinescript
//@version=6
indicator("syminfo target_price")
if barstate.islastconfirmedhistory
	//@variable The time value one year from the date of the last analyst recommendations.
	int YTD = syminfo.target_price_date + timeframe.in_seconds("12M") * 1000
	//@variable A line connecting the current `close` to the highest yearly price estimate.
	highLine = line.new(time, close, YTD, syminfo.target_price_high, color = color.green, xloc = xloc.bar_time)
	//@variable A line connecting the current `close` to the lowest yearly price estimate.
	lowLine = line.new(time, close, YTD, syminfo.target_price_low, color = color.red, xloc = xloc.bar_time)
	//@variable A line connecting the current `close` to the median yearly price estimate.
	medianLine = line.new(time, close, YTD, syminfo.target_price_median, color = color.gray, xloc = xloc.bar_time)
	//@variable A line connecting the current `close` to the average yearly price estimate.
	averageLine = line.new(time, close, YTD, syminfo.target_price_average, color = color.orange, xloc = xloc.bar_time)
	// Fill the space between targets
	linefill.new(lowLine, medianLine, color.new(color.red, 90))
	linefill.new(medianLine, highLine, color.new(color.green, 90))
	// Create a label displaying the total number of analyst estimates.
	string estimatesText = str.format("Number of estimates: {0}", syminfo.target_price_estimates)
	label.new(bar_index, close, estimatesText, textcolor = color.white, size = size.large)
```

## See also

- [syminfo.target_price_average](./target_price_average.md)
- [syminfo.target_price_date](./target_price_date.md)
- [syminfo.target_price_high](./target_price_high.md)
- [syminfo.target_price_low](./target_price_low.md)
- [syminfo.target_price_median](./target_price_median.md)
