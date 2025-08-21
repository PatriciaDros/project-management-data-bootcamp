
Perfect — we’ll treat this like a **lecture module** instead of a quiz. You’ll get an overview, real-world examples tied to your dataset, and a few **end-of-topic questions** to check your understanding (but no heavy drills yet).

---

# 📅 Excel Bootcamp — DATE & TIME Functions (Lecture)

## 1. Why Dates Matter in Project Analytics

In project management (like your asbestos/mold inspections), dates help you answer:

* How long did a job take from start to finish?
* Is a payment overdue?
* How many business days are left before a deadline?
* What month/quarter had the most work?

Excel has **serial numbers** behind the scenes for dates (e.g., Jan 1, 1900 = 1). This means you can calculate with them just like numbers.

---

## 2. Core Date Functions

### 🟢 TODAY() & NOW()

* `=TODAY()` → Returns today’s date.
* `=NOW()` → Returns current date *and* time.
  **Use case:** Auto-fill report dates without typing.

---

### 🟢 YEAR(), MONTH(), DAY()

* `=YEAR(A2)` → Extracts the year from a date.
* `=MONTH(A2)` → Extracts the month (1–12).
* `=DAY(A2)` → Extracts the day (1–31).
  **Use case:** Split invoice date into Year/Month for reporting.

---

### 🟢 DATEDIF(start, end, "unit")

* `"d"` = days, `"m"` = months, `"y"` = years
* `=DATEDIF(Start_Date, End_Date, "d")` → Days between two dates.
  **Use case:** How many days did a job take from start to finish?

---

### 🟢 NETWORKDAYS(start, end, \[holidays])

* Excludes weekends, and optionally holidays.
* `=NETWORKDAYS(A2, B2)` → Business days between two dates.
  **Use case:** Time to complete inspection *excluding weekends*.

---

### 🟢 WORKDAY(start, days, \[holidays])

* Adds business days to a start date.
* `=WORKDAY(A2, 10)` → Returns the date 10 business days after A2.
  **Use case:** Calculate due dates based on standard turnaround.

---

## 3. Real-World Example (Your Dataset Style)

Imagine columns:

| WA # | Start Date | End Date | Invoice Date | Payment Date |
| ---- | ---------- | -------- | ------------ | ------------ |
| 101  | 7/1/2025   | 7/7/2025 | 7/10/2025    | 7/25/2025    |

Possible formulas:

* **Job Duration (calendar days):**
  `=DATEDIF(B2, C2, "d")` → 6 days
* **Business Days Duration:**
  `=NETWORKDAYS(B2, C2)` → 5 days
* **Days Until Payment:**
  `=DATEDIF(D2, E2, "d")` → 15 days
* **Overdue Flag:**
  `=IF(E2="", IF(TODAY()>D2+30, "Overdue","Pending"), "Paid")`

---

## 4. End-of-Topic Questions (light check-in)

1. What’s the difference between `TODAY()` and `NOW()`?
2. If Start Date = 8/1/2025 and End Date = 8/19/2025, what would `=DATEDIF(Start, End, "d")` return?
3. Why might `NETWORKDAYS` be better than `DATEDIF` in project tracking?
4. Write a formula to return just the **month number** from an invoice date in cell C2.
5. Suppose your invoices are due **30 business days** after Invoice Date. How could you calculate the **due date**?

---
---
### TODAY() and NOW() Functions

Yes! 👍

* **`TODAY()`** → Returns the current date (no time).
* **`NOW()`** → Returns the current date **and** time.

✅ Both are **volatile functions**, which means they **automatically update** every time Excel recalculates.

That can happen when:

* You open the workbook.
* You enter or edit data anywhere.
* You press **F9** (force recalculation).

⚠️ One thing to keep in mind: if you send the file to someone else tomorrow, the values will update to *their* current system date/time, not stay “frozen” on yours.

👉 Would you like me to also show you a trick for making TODAY or NOW *static* (so the value doesn’t keep changing)?

---

Perfect! Here are the **static date/time tricks** you can use in Excel:

---

### 🗓 Insert Static Date

* Shortcut: **Ctrl + ;**
* This inserts today’s date as a fixed value.
  (e.g., `8/19/2025`)

---

### ⏰ Insert Static Time

* Shortcut: **Ctrl + Shift + ;**
* This inserts the current time as a fixed value.
  (e.g., `2:37 PM`)

---

### 📌 Insert Static Date & Time Together

1. Press **Ctrl + ;** (date)
2. Press **Space**
3. Press **Ctrl + Shift + ;** (time)
   👉 You’ll get something like: `8/19/2025 2:37 PM`

---

### 🔒 Make TODAY() or NOW() Static

If you already have `=TODAY()` or `=NOW()` and want to freeze it:

1. Select the cell(s).
2. Copy (**Ctrl + C**).
3. Paste Values (**Ctrl + Alt + V → V**) or right-click → **Paste Values**.
   → That replaces the formula with the actual date/time number.

---

⚡ Pro tip: use **TODAY()** and **NOW()** for rolling dashboards/reports (always up to date), and use **static shortcuts** for logs, timestamps, or records where you don’t want the value to change.

👉 Want me to cook up a mini “date/time drill” for you to practice both dynamic and static versions?

---

Awesome 🙌 Here’s your **Excel Date & Time Drill**. It’s short and practical — you can do it on your lunch break:

---

# 📅 Excel Date & Time Mastery Drill

### Dataset (mock project log)

| Project | Status   | Start Date | Completed Date | Logged By | Timestamp |
| ------- | -------- | ---------- | -------------- | --------- | --------- |
| A101    | Started  |            |                | Alice     |           |
| B205    | Finished |            |                | Bob       |           |
| C309    | Started  |            |                | Charlie   |           |
| D404    | Finished |            |                | Alice     |           |

---

### Tasks

1. **Static Date Entry**
   In the *Start Date* column, insert **today’s date as static** for the “Started” jobs.

2. **Dynamic Date**
   In *Completed Date*, enter a formula that always shows today’s date **if status = "Finished"**, otherwise leave it blank.

   > Hint: `=IF(B2="Finished",TODAY(),"")`

3. **Static Timestamp**
   In the *Timestamp* column, enter the **date + time (static)** for when you log Alice’s job on row 1.

   > Use `Ctrl + ;` + space + `Ctrl + Shift + ;`

4. **NOW() for Log System**
   In the *Timestamp* column for Bob’s job, use `NOW()` so that it updates every time the sheet refreshes.

5. **Elapsed Days**
   Add a helper column called **Days Since Start**: calculate how many days have passed since the Start Date until today.

   > Hint: `=TODAY()-C2`

---

### End-of-Drill Reflection

* Which cells should stay **static** (permanent record)?
* Which cells benefit from being **dynamic** (always updating)?

---

⚡ When you’re done, you’ll have a clear sense of when to use `TODAY()` / `NOW()` vs. static entries.

Want me to also make this into a **ready-to-use Excel file** like I did for COUNTIFS/SUMIFS?

