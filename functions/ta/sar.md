---
title: "ta.sar"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.sar
---

# ta.sar

**Category:** Function

## Syntax

```pinescript
ta.sar(start, inc, max) → series float
```

## Description

Parabolic SAR (parabolic stop and reverse) is a method devised by J. Welles Wilder, Jr., to find potential reversals in the market price direction of traded goods.

## Arguments

- **`start`** `simple int/float` — Start.
- **`inc`** `simple int/float` — Increment.
- **`max`** `simple int/float` — Maximum.

## Returns

Parabolic SAR.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("ta.sar")
plot(ta.sar(0.02, 0.02, 0.2), style=plot.style_cross, linewidth=3)

// The same on Pine Script®
pine_sar(start, inc, max) =>
	var float result = na
	var float maxMin = na
	var float acceleration = na
	var bool isBelow = false
	bool isFirstTrendBar = false

	if bar_index == 1
		if close > close[1]
			isBelow := true
			maxMin := high
			result := low[1]
		else
			isBelow := false
			maxMin := low
			result := high[1]
		isFirstTrendBar := true
		acceleration := start

	result := result + acceleration * (maxMin - result)

	if isBelow
		if result > low
			isFirstTrendBar := true
			isBelow := false
			result := math.max(high, maxMin)
			maxMin := low
			acceleration := start
	else
		if result < high
			isFirstTrendBar := true
			isBelow := true
			result := math.min(low, maxMin)
			maxMin := high
			acceleration := start
			
	if not isFirstTrendBar
		if isBelow
			if high > maxMin
				maxMin := high
				acceleration := math.min(acceleration + inc, max)
		else
			if low < maxMin
				maxMin := low
				acceleration := math.min(acceleration + inc, max)

	if isBelow
		result := math.min(result, low[1])
		if bar_index > 1
			result := math.min(result, low[2])
		
	else
		result := math.max(result, high[1])
		if bar_index > 1
			result := math.max(result, high[2])

	result

plot(pine_sar(0.02, 0.02, 0.2), style=plot.style_cross, linewidth=3)
```
