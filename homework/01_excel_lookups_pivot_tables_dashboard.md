# 📘 Day Summary: Excel Dashboard & Pivot Table Mastery

## ✅ End-of-Day Recap

### Topics Covered Today

- Excel lookup formulas: `VLOOKUP`, `XLOOKUP`, `IFERROR`, `IFNA`
- Date logic formulas: `Days Left`, `Overdue`
- Conditional formatting by task status
- Pivot tables with:
  - Row grouping (e.g., Assigned To)
  - Calculated values (Count, Averages)
- Dashboard creation:
  - KPI cards
  - Pie chart & bar chart visuals
- `GETPIVOTDATA` usage for dynamic referencing
- GitHub Desktop: Screenshot management, project commits

---

## 📝 Homework

### Task 1: Add a New Task

- Add `TASK-006` to your Excel tracker.
- Include dummy values for:
  - Task Name
  - Assigned To
  - Start Date
  - Due Date
  - Status
  - % Complete
- Ensure all dependent formulas (`Days Left`, `Overdue`, Pivot Table) update correctly.

### Task 2: New KPI Card

- Create a new card titled `In Progress Tasks`.
- Count how many tasks are currently marked as "In Progress".
- Use helper columns and/or `GETPIVOTDATA` if needed.

### Optional Challenge

- Add slicers to your pivot table/dashboard:
  - Slicer 1: `Assigned To`
  - Slicer 2: `Status`

### Task 3: Reflection in Markdown

Write a short reflection (you can call the file `2025-07-27-reflection.md`) with:

- What did I learn today?
- What challenged me?
- How could I apply this in a real-world project management environment?

---

## ❓ Comprehension Q&A Check

Answer these in your own words (in your reflection file or a new file called `2025-07-27-qa.md`):

1. What does this formula do: `=IF(F2="Complete", "Done", E2-TODAY())`?  
   When might it give a result you didn’t expect?

2. What is the benefit of using `GETPIVOTDATA()` instead of a simple cell reference?

3. You wanted to assign numerical values to status labels. What workaround did you use to simulate a calculated field in the pivot table?

4. When using conditional formatting to color-code statuses, how could that potentially create confusion?

5. What’s the relationship between the pivot table and your dashboard visuals? Why is this connection powerful?

---

## ✅ Submission Tip

Once completed, commit and push your updated Excel file, dashboard screenshots, and Markdown files (`reflection.md`, `qa.md`) to your GitHub repo under your `homework` folder.
