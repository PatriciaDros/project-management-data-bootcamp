
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

👉 Would you like me to make a **small Excel demo file with these examples and formulas built in**, so you can open it and play around tonight?
