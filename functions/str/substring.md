---
title: "str.substring"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.substring
---

# str.substring

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.substring(source, begin_pos, end_pos) → const string
```

```pinescript
str.substring(source, begin_pos, end_pos) → simple string
```

```pinescript
str.substring(source, begin_pos, end_pos) → series string
```

## Description

Returns a new string that is a substring of the `source` string. The substring begins with the character at the index specified by `begin_pos` and extends to 'end_pos - 1' of the `source` string.

## Arguments

- **`source`** `const string` — Source string from which to extract the substring.
- **`begin_pos`** `const int` — The beginning position of the extracted substring. It is inclusive (the extracted substring includes the character at that position).
- **`end_pos`** `const int` — The ending position. It is exclusive (the extracted string does NOT include that position's character). Optional. The default is the length of the `source` string.

## Returns

The substring extracted from the source string.

**Return type(s):** `const string`

## Remarks

Strings indexing starts from 0. If `begin_pos` is equal to `end_pos`, the function returns an empty string.

## Examples

```pinescript
//@version=6
indicator("str.substring", overlay = true)
sym= input.symbol("NASDAQ:AAPL")
pos = str.pos(sym, ":") // Get position of ":" character
tkr= str.substring(sym, pos+1) // "AAPL"
if barstate.islastconfirmedhistory
	label.new(bar_index, high, text = tkr)
```

## See also

- [str.contains()](./contains.md)
- [str.pos()](./pos.md)
- [str.match()](./match.md)
