Great! You’re now working on **project task tracking analysis in Excel**. This will help you apply your skills in:

---

### ✅ Lesson Focus: **Project Task Tracking — Status, Timelines, and Completion**

---

### 🎯 **Objectives**:

By the end of this session, you will be able to:

- Use Excel formulas to analyze task progress
- Calculate overdue tasks and days left
- Visualize task status and completion with Conditional Formatting and PivotTables
- Prepare your first mini dashboard for reporting

---

### 🧠 **Skills You’ll Practice**:

- `IF()`, `TODAY()`, `DATEDIF()`, `TEXT()`, `COUNTIF()`, `AVERAGEIF()`
- Conditional Formatting
- PivotTables (basic)
- Mini Dashboards
- Clear formatting and structure in Excel

---

### 📊 **What You'll Build**:

An Excel tracker that:

- Calculates how many days left (or overdue) each task is
- Highlights overdue or completed tasks
- Summarizes how many tasks each person is handling
- Uses a small dashboard section for visual insight

---

### 📁 Step-by-Step Tasks:

#### 1. **Open Excel** and load this data (from your clipboard or recreate it):

| Task ID  | Task Name | Assigned To | Start Date | Due Date   | Status      | % Complete |
| -------- | --------- | ----------- | ---------- | ---------- | ----------- | ---------- |
| TASK-001 | Task 1    | Charlie     | 2025-07-19 | 2025-08-06 | In Progress | 50%        |
| TASK-002 | Task 2    | Charlie     | 2025-07-18 | 2025-07-22 | Complete    | 100%       |
| TASK-003 | Task 3    | Dana        | 2025-07-20 | 2025-07-24 | Not Started | 0%         |
| TASK-004 | Task 4    | Alice       | 2025-07-17 | 2025-07-26 | Complete    | 100%       |
| TASK-005 | Task 5    | Bob         | 2025-07-18 | 2025-07-26 | In Progress | 30%        |

---

#### 2. **Add New Columns**:

To the right of your table, insert these columns:

- **Days Left** – Formula:
  `=IF([@[Status]]="Complete", "Done", [@[Due Date]] - TODAY())`
- **Overdue?** – Formula:
  `=IF(AND([@[Status]]<>"Complete",[@[Due Date]]<TODAY()),"Yes","No")`

---

#### 3. **Conditional Formatting**:

- Highlight:

  - “Overdue” = Red Fill
  - “Complete” = Green Fill
  - “In Progress” = Yellow Fill

---

#### 4. **Pivot Table**:

- Insert → PivotTable

  - Rows: `Assigned To`
  - Values: `Task ID` (Count), `% Complete` (Average)

---

#### 5. **Mini Dashboard (Optional)**:

- Add a clean table summarizing:

  - Total tasks
  - Tasks overdue
  - % of tasks completed

- Use `COUNTIF()` and `AVERAGEIF()` to calculate

---

### 📝 Let’s Start With:

✅ Step 2: Add those two new columns
👉 Once you do that, paste your formulas here and I’ll check them!

When ready, we’ll move to conditional formatting.
