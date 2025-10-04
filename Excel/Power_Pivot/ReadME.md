# Power Pivot – Loan Data Analysis

This folder contains exercises from my Data Analytics Bootcamp using **Power Pivot in Excel**.  
The goal was to understand **calculated columns, RELATED(), measures, and dashboarding** in DAX for analyzing loan data.

---

## Step 1: Calculated Columns – It's Math, Not Magic
- Created calculated columns for **Borrower Equity** (Property Value – Loan Amount).  
- Helps banks assess how much property value is left after lending (down payment equity).  

✅ Key takeaway: Power Pivot makes it easy to apply these calculations across datasets.

---

## Step 2: Using the `RELATED()` Function
- Used `RELATED()` to pull in **Banker Name** and **Closing Month** from a related table.  
- Found the number of loans closed by each banker (e.g., *Del closed 5 loans in December 2021*).  

✅ Key takeaway: Relationships in Power Pivot simplify cross-table lookups compared to Excel’s VLOOKUP.

---

## Step 3: Measures – The Real Power of DAX
- Introduced **Measures** for calculations like `COUNT()`, `SUM()`, and `AVERAGE()` to summarize data.  
- Example: `average_loan_amount = AVERAGE(loan_data[loan_amount])`  
- Measures dynamically update with filters (e.g., city, banker, or time period).  

✅ Key takeaway: Measures add powerful *filter context* automatically, enabling deeper analytics without editing the underlying data.

---

## Step 4: Data Stories with Dashboards
- Built PivotTables to visualize measures across **sales teams**.  
- Compared performance by office:
  - San Francisco closed **$100M more in loans** than New York.  
  - But their **average loan sizes were nearly identical** ($279,342 vs. $279,329).  

✅ Key takeaway: PivotTables make it easy to tell a *data-driven story* with aggregated insights.

---

## What I Learned So Far
- Difference between **calculated columns** and **measures** in Power Pivot.  
- How relationships (`RELATED()`) connect datasets smoothly.  
- How filter context shapes results in DAX.  
- How PivotTables can be used for storytelling with business data.

---

📊 *Next steps*: Learn more advanced DAX functions (FILTER, CALCULATE) and design a professional dashboard summarizing loan risk and banker performance.
