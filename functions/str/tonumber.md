---
title: "str.tonumber"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.tonumber
---

# str.tonumber

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
str.tonumber(string) → series float
```

```pinescript
str.tonumber(string) → const float
```

```pinescript
str.tonumber(string) → input float
```

```pinescript
str.tonumber(string) → simple float
```

## Description

Converts a value represented in `string` to its "float" equivalent.

## Arguments

- **`string`** `series string` — String containing the representation of an integer or floating point value.

## Returns

A "float" equivalent of the value in `string`. If the value is not a properly formed integer or floating point value, the function returns [na](../../variables/na.md).

**Return type(s):** `series float`
