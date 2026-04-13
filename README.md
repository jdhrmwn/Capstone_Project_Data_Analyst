# Quick Commerce Operational Analysis (Astro Case)

This project presents an end-to-end data analysis of a Quick Commerce business model, focusing on operational inefficiencies within dark store fulfillment.

The objective of this analysis is to identify key bottlenecks affecting delivery performance, product quality, and overall operational efficiency, and to provide actionable business recommendations.

---

## Business Context

Quick commerce platforms promise ultra-fast delivery (≤15 minutes), relying on dark stores as micro-fulfillment centers.

However, maintaining both speed and product quality — especially for perishable goods like ice cream and fresh produce — presents significant operational challenges.

---

## Objectives

This analysis aims to:

- Identify bottlenecks in the fulfillment process (especially picking)
- Investigate the root causes of SLA violations
- Analyze product spoilage and its drivers
- Assess data quality and system integrity
- Provide strategic recommendations to improve operations

---

## Dataset Overview

The dataset consists of three main tables:

- **Orders** → transaction-level data (timestamps, delivery duration, status)
- **Products** → product category and characteristics
- **Dark Stores** → store-level operational data (region, picker headcount)

Total records: ~300,000 orders

---

## Key Findings

### 1. Picking Bottleneck (Root Cause)

- Average picking time: ~4 minutes (target: ≤3 minutes)
- ~74.5% of orders exceed picking SLA
- No significant correlation between number of pickers and picking time

Indicates a **systemic inefficiency**, not a manpower issue

---

### 2. Inefficient Warehouse Layout

- Fast-moving items (high-demand products) still have high picking times
- Includes FMCG, fresh produce, and ice cream

Suggests that **warehouse layout is not demand-driven**

---

### 3. Spoilage Occurs Before Delivery

- No significant difference in delivery time between spoiled and non-spoiled orders
- Spoilage affects both perishable and non-perishable products

Indicates that product damage likely occurs **during picking or storage**, not delivery

---

### 4. SLA Miss is Systemic

- No significant difference between day and night performance
- SLA violations occur consistently across time

Confirms issue is **internal (operational), not external (time/weather)**

---

### 5. Data Quality Issues

- ~44% category inconsistency (manual input errors)
- ~3% logical errors (invalid timestamp sequence)
- ~0.67% extreme outliers (negative or unrealistic durations)

Indicates weak **data governance and system validation**

---

## Root Cause Summary

- Inefficient warehouse layout
- Slow picking process
- Increased handling time (especially for perishable goods)
- Higher risk of spoilage
- SLA violations and poor customer experience

---

## Business Impact

- Increased SLA violations (delivery delays)
- Higher product waste and refund rates
- Reduced operational efficiency
- Lower customer satisfaction and trust
- Risk of misleading business decisions due to poor data quality

---

## Recommendations

### 1. Dark Store Optimization
- Implement demand-driven layout
- Place fast-moving items in easily accessible locations
- Introduce zone picking system

---

### 2. Waste Reduction
- Prioritize picking for perishable items
- Improve cold chain handling during picking
- Minimize exposure time outside optimal storage conditions

---

### 3. Data Integrity Improvement
- Enforce logical sequence validation in system
- Automate timestamp recording
- Implement anomaly detection for operational data
  
---

## Tools & Skills

- Python (Pandas, NumPy)
- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Data Visualization (Matplotlib)
- Business Insight & Storytelling

---

## Author

**Jodi Hermawan**
