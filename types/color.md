---
title: "color"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_color
---

# color

**Category:** Type

## Description

Keyword used to explicitly declare the "color" type of a variable or a parameter.

## Remarks

Color literals have the following format: #RRGGBB or #RRGGBBAA. The letter pairs represent 00 to FF hexadecimal values (0 to 255 in decimal) where RR, GG and BB pairs are the values for the color's red, green and blue components. AA is an optional value for the color's transparency (or alpha component) where 00 is invisible and FF opaque. When no AA pair is supplied, FF is used. The hexadecimal letters can be upper or lower case.

Explicitly mentioning the type in a variable declaration is optional, except when it is initialized with [na](../variables/na.md). Learn more about Pine Script® types in the User Manual page on the [Type System](https://www.tradingview.com/pine-script-docs/language/type-system/).

## Examples

```pinescript
//@version=6
indicator("color", overlay = true)

color textColor = color.green
color labelColor = #FF000080 // Red color (FF0000) with 50% transparency (80 which is half of FF).
if barstate.islastconfirmedhistory
	label.new(bar_index, high, text = "Label", color = labelColor, textcolor = textColor)

// When declaring variables with color literals, built-in constants(color.green) or functions (color.new(), color.rgb()), the "color" keyword for the type can be omitted.
c = color.rgb(0,255,0,0)
plot(close, color = c)
```

## See also

- [var](../keywords/var.md)
- [varip](../keywords/varip.md)
- [int](./int.md)
- [float](./float.md)
- [string](./string.md)
- [color.rgb()](../functions/color/rgb.md)
- [color.new()](../functions/color/new.md)
