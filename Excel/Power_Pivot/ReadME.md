# 🧮 Power Pivot – Loan Data Analysis

This project contains exercises from my **Data Analytics Bootcamp** using **Power Pivot in Excel**.  
The goal was to understand **calculated columns**, the **RELATED() function**, **measures**, and **interactive dashboards** using **DAX** for analyzing loan data.

---

## 🧩 Step 1: Calculated Columns – *It's Math, Not Magic*
Created calculated columns for **Borrower Equity**:

```DAX
Borrower Equity = [Property Value] - [Loan Amount]
```

This helps banks assess how much property value is left after lending (down payment equity).

✅ **Key takeaway:** Power Pivot makes it easy to apply these calculations across large datasets dynamically.

---

## 🔗 Step 2: Using the `RELATED()` Function
Used `RELATED()` to pull in **Banker Name** and **Closing Month** from a related table.

```DAX
Banker Name = RELATED(Bankers[Name])
Closing Month = RELATED(Calendar[Month])
```

Found the number of loans closed by each banker  
➡️ Example: *Del closed 5 loans in December 2021.*

✅ **Key takeaway:** Relationships in Power Pivot simplify cross-table lookups compared to Excel’s VLOOKUP.

---

## ⚙️ Step 3: Measures – *The Real Power of DAX*
Introduced **Measures** for dynamic calculations such as `COUNT()`, `SUM()`, and `AVERAGE()`.

Example:

```DAX
average_loan_amount = AVERAGE(loan_data[loan_amount])
```

Measures automatically update with filters (e.g., city, banker, or time period).

✅ **Key takeaway:** Measures add powerful **filter context**, enabling deeper analytics without editing the base data.

---

## 📊 Step 4: Data Stories with Dashboards
Built **PivotTables** and **PivotCharts** to visualize measures across **Sales Teams**.

### Highlights:
- Compared performance by **office**  
  → *San Francisco closed $100M more in loans than New York.*
- Average loan sizes were nearly identical:  
  → *$279,342 vs. $279,329*

✅ **Key takeaway:** PivotTables make it easy to tell a **data-driven story** with aggregated business insights.

---

## 🎛️ Step 5: Adding Timeline & Interactive Dashboard
Enhanced the dashboard by adding **Timeline slicers** and linking visuals together.

### Process:
1. Added a **Timeline slicer** on the *Loan Volume Over Time* PivotChart.  
   → This slicer references the **Date** field from the **Calendar** table.
2. Connected this slicer to the **Sales Team Volume** PivotChart.  
   → Initially, the pie chart didn’t respond because it wasn’t connected.
3. Linked both visuals so that time-based filtering now dynamically updates **all charts**.

📅 **Insight Example:**  
The sales volume for **New York in Q2** was **$84,420,000**.

✅ **Final Result:**  
The **CRO dashboard** is now interactive and allows dynamic exploration by **date, department, heads, and offices**.

---

## 🧠 What I Learned So Far
- Difference between **Calculated Columns** and **Measures** in Power Pivot.  
- How **RELATED()** connects data models seamlessly.  
- How **filter context** shapes DAX results.  
- How to design **interactive dashboards** for storytelling.

---


## 📸 Dashboard Preview
 
<img width="1366" height="768" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/4bb091ac-0661-4556-a26e-a4132e681120" />

---

### 🏁 Summary
This project transformed raw loan data into a professional, interactive Power Pivot dashboard — empowering business leaders to **analyze performance** and **make data-driven decisions** efficiently.
