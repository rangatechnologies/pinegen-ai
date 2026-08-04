---
title: "str.match"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.match
---

# str.match

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
str.match(source, regex) → simple string
```

```pinescript
str.match(source, regex) → series string
```

## Description

Returns the new substring of the `source` string if it matches a `regex` regular expression, an empty string otherwise.

## Arguments

- **`source`** `simple string` — Source string.
- **`regex`** `simple string` — The regular expression to which this string is to be matched.

## Returns

The new substring of the `source` string if it matches a `regex` regular expression, an empty string otherwise.

**Return type(s):** `simple string`

## Remarks

Function returns first occurrence of the [regular expression](https://en.wikipedia.org/wiki/Regular_expression#Perl_and_PCRE) in the `source` string.

The backslash "&#92;" symbol in the`regex` string needs to be escaped with additional backslash, e.g. "&#92;&#92;d" stands for regular expression "&#92;d".

## Examples

```pinescript
//@version=6
indicator("str.match")

s = input.string("It's time to sell some NASDAQ:AAPL!")

// finding first substring that matches regular expression "[\w]+:[\w]+"
var string tickerid = str.match(s, "[\\w]+:[\\w]+")

if barstate.islastconfirmedhistory
	label.new(bar_index, high, text = tickerid) // "NASDAQ:AAPL"
```

## See also

- [str.contains()](./contains.md)
- [str.substring()](./substring.md)
