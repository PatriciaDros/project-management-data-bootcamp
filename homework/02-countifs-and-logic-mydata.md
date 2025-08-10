
Perfect! Let’s dig into `COUNTIFS` using your **Monthly Status** sheet.

---

## 🧮 COUNTIFS in Your Project Data: Real-World Use Cases

We'll build some **insight-generating formulas** based on your data. First, here’s a refresher of your relevant columns:

| Column Name                       | Notes                                                          |
| --------------------------------- | -------------------------------------------------------------- |
| `WA Status`                       | e.g., *Closed*, *NEW* — use this to filter completed projects. |
| `PAID / UNPAID`                   | e.g., *PAID*, *UNPAID* — helps us track financial status.      |
| `Actual Date of Completion (RFP)` | Can be used to filter by year.                                 |
| `Primary Hygienist`               | Use to drill into individual performance.                      |
| `Estimated Cost (WA)`             | Can be used for cost-based conditions.                         |

---

## ✅ Formula #1: Count all **Closed + PAID** Projects

```excel
=COUNTIFS(F:F, "Closed", G:G, "PAID")
```

➡️ **Replace F\:F and G\:G** with the correct columns based on:

* F\:F → your `WA Status` column
* G\:G → your `PAID / UNPAID` column

---

## ✅ Formula #2: Count projects by a specific Hygienist (e.g., *Bracamonte, Jesus*) in 2025

You’ll need to use a **helper column** to extract the year from `Actual Date of Completion (RFP)`.

### Step 1: Create a new column `Completion Year` with:

```excel
=YEAR([@[Actual Date of Completion (RFP)]])
```

### Step 2: Use `COUNTIFS` like this:

```excel
=COUNTIFS([Primary Hygienist], "Bracamonte, Jesus", [Completion Year], 2025)
```

---

## ✅ Formula #3: Count UNPAID projects with Estimated Cost > \$4,000

This requires a bit more:

### Step 1: Create a helper column `Est > 4000`:

```excel
=IF([@[Estimated Cost (WA)]] > 4000, "YES", "NO")
```

### Step 2: COUNTIFS:

```excel
=COUNTIFS([Est > 4000], "YES", [PAID / UNPAID], "UNPAID")
```

---

## 🔁 Optional Summary Tiles

Later today, we’ll turn these formulas into dashboard-style KPIs:

| Metric                     | Formula          |
| -------------------------- | ---------------- |
| Total Closed + PAID        | `=COUNTIFS(...)` |
| Bracamonte 2025 Projects   | `=COUNTIFS(...)` |
| Unpaid High-Value Projects | `=COUNTIFS(...)` |

---

### ⚙️ Next Steps:

1. Insert formulas in a new section of the **Monthly Status** tab (label each metric).
2. Let me know once you’ve tried one — I’ll help troubleshoot and verify!
3. I’ll guide you through building visuals next if you’re up for it.

Ready? Let’s start with **Formula #1** and walk through together?
