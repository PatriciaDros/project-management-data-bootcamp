
Perfect 🎯 — yes, you nailed it: we just wrapped up **Week 3 (Date & Time)**, so now we roll into **Week 4: Logical Functions & Error Handling**.

Here’s how I suggest we structure **this week’s lessons**:

---

# 📘 Week 4: Logical Functions & Error Handling

### 🎯 Learning Objectives

* Use logical tests to create rules for project data (flags, warnings, categories).
* Combine multiple conditions (AND, OR, NOT).
* Build decision trees with nested IF/IFS.
* Handle messy data with IFERROR & IFNA.

---

## **Step 1: Intro to IF (refresher + expansion)**

* Formula:
  `=IF(logical_test, value_if_true, value_if_false)`
* Use case: Flag projects as **Paid** vs **Unpaid**.

**Lab 4.1:**

> Create a helper column: If `Paid Amount = Actual Cost`, return “Closed”, else “Open”.

---

## **Step 2: Multiple Conditions**

* `=IF(AND(...), "Yes", "No")`
* `=IF(OR(...), "Yes", "No")`
* `=NOT(...)`

**Lab 4.2:**

> Flag projects where:
>
> * Status = “Open” **AND** Days Open > 30 → “Overdue”
> * Otherwise → “On Track”

---

## **Step 3: Nested IF & IFS**

* Nested IF = multiple layers of decision rules.
* IFS = cleaner syntax in newer Excel.

**Lab 4.3:**

> Categorize jobs by Actual Cost:
>
> * < \$500 → “Small”
> * \$500–\$2000 → “Medium”
> * > \$2000 → “Large”

---

## **Step 4: Error Handling**

* IFERROR: `=IFERROR(formula, "Custom Message")`
* IFNA: handles `#N/A`.

**Lab 4.4:**

> Wrap your VLOOKUP/XLOOKUP with IFERROR so missing WA#s show “Not Found” instead of `#N/A`.

---

## **Step 5: Real-World Integration**

* Build **status flags** into your project tracker:

  * Paid? (Yes/No)
  * Overdue? (Yes/No)
  * Risk Category (Low/Med/High based on cost + time).

This sets us up perfectly for **Week 5: PivotTables & Summaries**, since logical columns make grouping much more powerful.

---

📌 Next step:
Do you want me to build you a **Week 4 Lab Sheet (Markdown with exercises + answer key hidden at the bottom)** so you can drop it straight into your repo like the DateTime one?
