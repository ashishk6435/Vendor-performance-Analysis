# 📊 Vendor Performance & Profitability Analysis

## 🔍 Business Problem
The organization works with a **large vendor base (8,000+ vendors)** supplying multiple brands and products.  
Despite strong overall revenue, management lacked clarity on:

- Which vendors **actually drive profitability** (not just revenue)
- Whether the business is **over-dependent on a small set of vendors**
- Which vendors and brands are **eroding margins or locking capital in inventory**
- How inventory inefficiencies impact **cash flow and working capital**

Procurement and inventory decisions were being made **without a consolidated, data-driven performance view**.

---

## 🎯 Project Objectives
- Evaluate vendor performance using **sales, purchase cost, profit margin, and inventory efficiency**
- Identify **top-performing and low-performing vendors**
- Detect **vendor concentration risk** using Pareto analysis
- Identify **low-sales but high-margin brands** for pricing or promotional optimization
- Highlight **unsold inventory and slow-moving stock risks**
- Provide **actionable business recommendations** for procurement and management

---

## 🧾 Data Overview
- **Dataset**: Vendor-level sales summary  
- **Granularity**: Vendor × Brand × Product  
- **Vendors**: 8,000+  
- **Key Metrics**:
  - Total Sales & Total Purchase
  - Gross Profit & Profit Margin
  - Stock Turnover
  - Unsold Inventory Capital
- **Limitation**: No time dimension available  
  → Analysis is **cross-sectional**, not trend-based

---

## 🔬 Exploratory Data Analysis (EDA) – Key Findings

### Data Quality & Distribution
- **Negative Gross Profit** observed (min: -52,002), indicating loss-making transactions
- **Profit Margin** includes extreme negative values due to zero or low revenue cases
- Several products show **zero sales but positive purchase quantity**, indicating unsold inventory

### Outliers & Variability
- Purchase and sales prices show **significant right-skew**, indicating premium products
- Freight cost varies widely, suggesting **logistics inefficiencies**
- Stock turnover ranges from **0 to 274**, highlighting uneven inventory movement

### Correlation Insights
- Purchase quantity vs sales quantity shows **very strong correlation (0.999)**
- Profit margin shows **weak correlation** with sales price and stock turnover
- Faster inventory turnover does **not necessarily translate to higher margins**

--- 
<p align="center">
  <img src="images/dashboard_overview.png" width="800"/>
</p>

<p align="center"><i>Vendor Performance Dashboard – Executive Overview</i></p>


## 📈 Key Analytical Insights

### 1️⃣ Vendor Concentration Risk 
- **Top 10 vendors contribute ~65.7% of total purchase value**
- Remaining vendors contribute only ~34.3%

**Impact**:  
High dependency on a small vendor group increases **supply-chain and negotiation risk**.

---



---

### 3️⃣ Low-Sales, High-Margin Brands
- **198 brands** exhibit **low sales volume but high profit margins**

**Opportunity**:  
Targeted promotions or pricing optimization can increase volume **without sacrificing profitability**.

---

### 4️⃣ Inventory & Unsold Capital Risk
- **$2.71M tied up in unsold inventory**
- Several vendors show **low stock turnover and high unsold inventory value**

**Impact**:  
Capital lock-in reduces cash-flow efficiency and increases holding costs.

---

### 5️⃣ Bulk Purchasing Advantage
- Large purchase orders achieve **~72% lower unit cost**
- Indicates clear economies of scale

**Impact**:  
Bulk purchasing can improve margins if aligned with actual sales demand.

---

## 📊 Dashboard Overview (Power BI)

### Key Features
- Executive KPI summary (Sales, Purchase, Profit, Margin, Unsold Capital)
- Top vendors by **Sales vs Profit**
- Pareto chart for **purchase contribution**
- Margin category distribution
- Low-performing vendors identification
- Inventory risk analysis



---

## 💡 Business Recommendations

- **Segment vendors** into strategic, tactical, and non-core categories
- **Diversify suppliers** to reduce dependency on top vendors
- **Renegotiate pricing and freight costs** with high-volume, low-margin vendors
- Promote **low-sales, high-margin brands** to improve volume efficiently
- Optimize procurement quantities for **slow-moving inventory**
- Leverage **bulk purchasing benefits** while avoiding overstocking

---

## 🛠 Tools & Technologies
- **Python**: Pandas, Matplotlib, Seaborn (EDA & analysis)
- **Power BI**: Interactive dashboards & reporting
- **Analytical Techniques**: vendor segmentation, performance scoring


