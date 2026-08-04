---
title: "syminfo.shares_outstanding_float"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.shares_outstanding_float
---

# syminfo.shares_outstanding_float

**Category:** Variable

**Type:** `simple float`

## Description

The total number of shares outstanding a company has available, excluding any of its restricted shares.

## Examples

```pinescript
//@version=6
indicator("syminfo simple")
//@variable A table containing information about a company's employees, shareholders, and shares.
var result_table = table.new(position = position.top_right, columns = 2, rows = 5, border_width = 1)
if barstate.islastconfirmedhistory
	// Add header cells
	table.cell(table_id = result_table, column = 0, row = 0, text = "name")
	table.cell(table_id = result_table, column = 1, row = 0, text = "value")
	// Add employee info cells.
	table.cell(table_id = result_table, column = 0, row = 1, text = "employees")
	table.cell(table_id = result_table, column = 1, row = 1, text = str.tostring(syminfo.employees))
	// Add shareholder cells.
	table.cell(table_id = result_table, column = 0, row = 2, text = "shareholders")
	table.cell(table_id = result_table, column = 1, row = 2, text = str.tostring(syminfo.shareholders))
	// Add float shares outstanding cells.
	table.cell(table_id = result_table, column = 0, row = 3, text = "shares_outstanding_float")
	table.cell(table_id = result_table, column = 1, row = 3, text = str.tostring(syminfo.shares_outstanding_float))
	// Add total shares outstanding cells.
	table.cell(table_id = result_table, column = 0, row = 4, text = "shares_outstanding_total")
	table.cell(table_id = result_table, column = 1, row = 4, text = str.tostring(syminfo.shares_outstanding_total))
```

## See also

- [syminfo.employees](./employees.md)
- [syminfo.shareholders](./shareholders.md)
- [syminfo.shares_outstanding_total](./shares_outstanding_total.md)
