---
title: "str.replace"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.replace
---

# str.replace

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.replace(source, target, replacement, occurrence) → const string
```

```pinescript
str.replace(source, target, replacement, occurrence) → simple string
```

```pinescript
str.replace(source, target, replacement, occurrence) → series string
```

## Description

Returns a new string with the Nth occurrence of the `target` string replaced by the `replacement` string, where N is specified in `occurrence`.

## Arguments

- **`source`** `const string` — Source string.
- **`target`** `const string` — String to be replaced.
- **`replacement`** `const string` — String to be inserted instead of the target string.
- **`occurrence`** `const int` (optional) — N-th occurrence of the target string to replace. Indexing starts at 0 for the first match. Optional. Default value is 0.

## Returns

Processed string.

**Return type(s):** `const string`

## Examples

```pinescript
//@version=6
indicator("str.replace")
var source = "FTX:BTCUSD / FTX:BTCEUR"

// Replace first occurrence of "FTX" with "BINANCE" replacement string
var newSource = str.replace(source, "FTX", "BINANCE", 0)

if barstate.islastconfirmedhistory
	// Display "BINANCE:BTCUSD / FTX:BTCEUR"
	label.new(bar_index, high, text = newSource)
```

## See also

- [str.replace_all()](./replace_all.md)
- [str.match()](./match.md)
