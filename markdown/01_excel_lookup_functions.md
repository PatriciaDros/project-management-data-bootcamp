# 🔥 Lesson: Excel Lookup Functions & Error Handling

## 📅 Date

July 28, 2025

## 🤖 Environment Setup

- Github Desktop and, of course, Github
- Excel (Microsoft365)
- MySQL Workbench
- Python (Jupyter notebook)
- VSCode (XCode)
- Tableau
- Markdown Live Preview

## 🎯 Learning Objectives

- Understand how to use `VLOOKUP`, `XLOOKUP`,
- Identify common Excel errors such as `#VALUE!`, `#NAME!`, and `#N/A!`
- Use `IFERROR()` and `IFNA()` to clean up error messages in formulas

---

## ✅ Key Concepts

### VLOOKUP

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])

```

- Looks for a value in the first column or a range and returns a value from a specified **column**
- Use `FALSE` for exact match

### XLOOKUP

```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found])
```

- Replaces VLOOKUP with easier syntax
- Handles left-to-right and right-to-left lookups

### Error Types and Fixes

| Error     | Meaning                  | Fix                                      |
| --------- | ------------------------ | ---------------------------------------- |
| `#VALUE!` | Wrong Data Type          | Check for text where a nuber is expected |
| `#NAME?`  | Misspelled function Name | Double-check formula spelling            |
| `#N/A`    | Value not found          | Double-check formula spelling            |

### ✅ Drill Summary

- Learned `VLOOKUP` and `XLOOKUP`
- Practiced formula troubleshooting
- Applied `IFERROR()` and `IFNA()`
- Understood Excel error types and when to use which fix

### 📌 Next Steps

- Practice with custom Excel data
- Learn conditional formatting
- Start working with Pivot Tables

You can also check this Markdown Previewer:  
👉 [https://markdownlivepreview.com](https://markdownlivepreview.com)
