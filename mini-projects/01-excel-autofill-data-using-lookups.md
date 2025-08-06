
Perfect, Tricia — you're building real mastery by applying your Excel skills to live project data from SAI. Let’s dive into **LOOKUP mastery**, especially focusing on:

---

## 🔍 Today's Learning Goals (Excel: Lookup Logic Focus)

### Core Focus:

* Understand and apply `INDEX + MATCH`
* Compare it to `XLOOKUP` (advantages, limitations)
* Practice both on your **SAI project dataset**

---

## 🧠 Step 1: Concept Breakdown — `INDEX + MATCH` vs `XLOOKUP`

### 1️⃣ `INDEX + MATCH` — The Classic Combo

```excel
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```

**Use Case**: More flexible than `VLOOKUP` — allows left-lookups, supports dynamic column targeting.

**Example**:

```excel
=INDEX(D2:D100, MATCH("WA123", A2:A100, 0))
```

This finds the row where `WA123` appears in A2\:A100, then returns the value from D in that same row.

---

### 2️⃣ `XLOOKUP` — Modern Power Tool

```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
```

**Use Case**: Easier to read, no nested functions, supports search modes, and returns error handling.

**Example**:

```excel
=XLOOKUP("WA123", A2:A100, D2:D100, "Not Found")
```

---

## 🔧 Step 2: Real-World Task (Using SAI Dataset)

### 🔍 Scenario:

You want to pull the **Assigned Hygienist** from your SAI dataset based on a given **WA#**.

#### ✅ Try Both Methods:

Assume:

* WA# is in column A
* Assigned Hygienist is in column D

| A (WA#) | B | C | D (Hygienist) |
| ------- | - | - | ------------- |
| WA001   |   |   | John Smith    |
| WA002   |   |   | Mary Jones    |

#### 🧪 Exercise:

| F (Lookup WA#) | G (Hygienist - INDEX+MATCH) | H (Hygienist - XLOOKUP) |
| -------------- | --------------------------- | ----------------------- |
| WA002          |                             |                         |

👉 In **G2**, write the `INDEX + MATCH` formula.
👉 In **H2**, write the `XLOOKUP` formula.

You try it now — I’ll check your logic after.

---

## 🎯 Step 3: Challenge Tasks — Lookup Practice

### 🧩 Challenge #1: Reverse Lookup

> Pull the **WA#** based on **Hygienist name** using `INDEX + MATCH`.

### 🧩 Challenge #2: Two-Way Lookup

> You want to get the **Actual Cost** from a table based on WA# **and** a Service ID.

### 🧩 Challenge #3: Fuzzy Match Alert

> Use `EXACT`, `TRIM`, and `MATCH` to detect if WA# entries from one sheet match another sheet **exactly** (case and spacing included).

---

## ✍️ Step 4: Comprehension Quiz (5 Quick Questions)

> *Don’t peek! Answer first, then I’ll grade you.*

1. What does the `MATCH` function return?
2. Which formula allows left-lookups: `VLOOKUP` or `INDEX + MATCH`?
3. Write a formula to get the “Status” from column F using `XLOOKUP`, based on WA# in A2.
4. True or False: `INDEX + MATCH` is faster than `XLOOKUP` in large datasets.
5. Bonus: What does this return?

   ```excel
   =INDEX(B2:B10, MATCH(TRUE, B2:B10="Open", 0))
   ```

---

## 🧪 Step 5: Mini Project — Lookup Tracker Sheet

**Task**: Build a simple tracker using your real SAI dataset:

* Input: WA#
* Output (auto-filled):

  * Assigned Hygienist
  * Job Status
  * Estimated vs. Actual Cost
  * Over/Under Budget flag

You can use `INDEX + MATCH` or `XLOOKUP` for this.

---

## 🧾 Final Recap + Evaluation

After you're done:

* I’ll **review your formulas**
* Give a **critique**
* Spot any **logic gaps**
* Add to your **Master Notebook** in Markdown format

---

### Ready? Your Turn:

👉 Complete Step 2 (formulas for INDEX+MATCH and XLOOKUP).
👉 Then try the challenge questions and quiz.

Let me know when you're ready to review!
