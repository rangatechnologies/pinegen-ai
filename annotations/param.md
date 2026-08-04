---
title: "@param"
kind: annotation
source: https://www.tradingview.com/pine-script-reference/v6/#an_@param
---

# @param

**Category:** Annotation

## Description

If placed above a function declaration, it adds a custom description for a function parameter. After the annotation, users should specify the parameter name, then its description.

The Pine Editor's autosuggest uses this description and displays it when a user hovers over the function name. When used in [library()](../functions/library.md) scripts, the descriptions of all functions using the [export](../keywords/export.md) keyword will pre-fill the "Description" field in the publication dialogue.

## Examples

```pinescript
//@version=6
// @description Provides a tool to quickly output a label on the chart.
library("MyLibrary")

// @function Outputs a label with `labelText` on the bar's high.
// @param labelText (series string) The text to display on the label.
// @returns Drawn label.
export drawLabel(string labelText) =>
	label.new(bar_index, high, text = labelText)
```
