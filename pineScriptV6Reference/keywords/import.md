---
title: "import"
kind: keyword
source: https://www.tradingview.com/pine-script-reference/v6/#kw_import
---

# import

**Category:** Keyword

## Syntax

```pinescript
import {username}/{libraryName}/{libraryVersion} as {alias}
```

## Description

Used to load an external [library()](../functions/library.md) into a script and bind its functions to a namespace. The importing script can be an indicator, a strategy, or another library. A library must be published (privately or publicly) before it can be imported.

## Arguments

- **`username`** `literal string` (optional) — User name of the library's author.
- **`libraryName`** `literal string` (optional) — Name of the imported library, which corresponds to the `title` argument used by the author in his library script.
- **`libraryVersion`** `literal int` (optional) — Version number of the imported library.
- **`alias`** `literal string` (optional) — A non-numeric identifier used as a namespace to refer to the library's functions. Optional. The default is the `libraryName` string.

## Remarks

Using an alias that replaces a built-in namespace such as math.* or strategy.* is allowed, but if the library contains function names that shadow Pine Script®'s built-in functions, the built-ins will become unavailable. The same version of a library can only be imported once. Aliases must be distinct for each imported library. When calling library functions, casting their arguments to types other than their declared type is not allowed. An import statement cannot use 'as' or 'import' as `username`, `libraryName`, or `alias` identifiers.

## Examples

```pinescript
//@version=6
indicator("num_methods import")
// Import the first version of the username’s "num_methods" library and assign it to the "m" namespace",
import username/num_methods/1 as m
// Call the “sinh()” function from the imported library
y = m.sinh(3.14)
// Plot value returned by the "sinh()" function",
plot(y)
```

## See also

- [library()](../functions/library.md)
- [export](./export.md)
