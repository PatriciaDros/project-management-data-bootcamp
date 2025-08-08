
Excellent choice. Based on your progress so far and your goal to build toward **project management analytics dashboards**, here’s the next module in your **Excel Learning Plan**:

---

## 📘 Bootcamp Module: **“Data Cleaning & Normalization” in Excel**

> This builds directly on your current work with real inspection data and prepares your dataset for accurate pivot tables, dashboards, and analysis in both Excel and later SQL/Python.

---

### 🎯 Learning Objectives:

By the end of this module, you will be able to:

1. **Identify and correct dirty data** (inconsistent text, dates, duplicate rows, blanks)
2. **Normalize columns** — split/merge cells, extract structured values (e.g., Job ID formats)
3. **Use Excel tools** like `TRIM`, `CLEAN`, `TEXTSPLIT`, `TEXTJOIN`, `TEXTBEFORE/AFTER`, `IFERROR`
4. Set up a “Clean Data Table” to use in **Pivot Tables** and **Dashboards**

---

### 🔨 Mini-Project Task:

> You will clean and normalize your **SAI inspection job tracking sheet** so that:

* Hygienist names are consistent (e.g., no "Vasili" vs. "vasili")
* Date formats are uniform (e.g., all mm/dd/yyyy)
* Job IDs follow consistent patterns (e.g., no “X101X” artifacts)
* A clean summary sheet shows:

  * Total open jobs
  * Open jobs by hygienist
  * Avg. cost per open job

---

### 🧠 Key Concepts & Tools:

| Task                           | Function                                                         |
| ------------------------------ | ---------------------------------------------------------------- |
| Remove leading/trailing spaces | `TRIM()`                                                         |
| Remove non-printing characters | `CLEAN()`                                                        |
| Standardize text case          | `UPPER()`, `LOWER()`, `PROPER()`                                 |
| Fix mixed job ID formats       | `TEXTBEFORE()`, `TEXTAFTER()`, `LEFT()`, `RIGHT()`, `ISNUMBER()` |
| Split one cell into parts      | `TEXTSPLIT()`, `TEXTBEFORE()`, `MID()`                           |
| Combine parts into one         | `TEXTJOIN()`                                                     |
| Handle errors                  | `IFERROR()`                                                      |
| Validate values                | `ISTEXT()`, `ISNUMBER()`, `LEN()`                                |
| Remove Duplicates              | Excel ribbon > Data > Remove Duplicates                          |
| Filter Blank or Missing        | Filter + `COUNTA()`, `IF(ISBLANK())`                             |
| Convert to Table               | `Ctrl + T` or Insert > Table                                     |

---

### 📥 Your Homework Dataset:

Please either:

* Use your **SAI inspection tracking Excel file**, or
* I can generate a **sample messy inspection dataset** for practice.

---

### 📌 Next Steps

Would you like to:

1. ✅ Start with a **guided example** on how to clean a specific column (like Hygienist or Job ID)?
2. 📄 Work with a **sample messy dataset** I provide?
3. 💾 Use your real SAI data — and we’ll build your clean table together?

Let me know how you’d like to proceed — I’ll guide you through it line by line.
