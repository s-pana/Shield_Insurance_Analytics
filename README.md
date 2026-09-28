
# Shield Insurance – Customer & Revenue Analytics

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Data%20Analysis%20Expressions-blue?style=for-the-badge)](#)
[![Star Schema](https://img.shields.io/badge/Data%20Model-Star%20Schema-success?style=for-the-badge)](#)

An interactive, multi-page business intelligence solution developed for Shield Insurance to replace spreadsheet silos with data-driven decision-making. This project tracks top-line revenue velocity, customer demographics, multi-channel distribution efficiency, and portfolio claim exposure across 5 metropolitan operating markets.

---

## 🔗 Live Interactive Dashboard
Experience the live, interactive Power BI report directly in your browser:
👉 **[View Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOTdkNjMwOGItZjYwYy00NTdmLTk3ZDAtOTM4ZGRlMmU0Njk0IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)**
<br/>
Watch the complete project presentation and walkthrough on LinkedIn:
👉 **[View Project Presentation on LinkedIn](https://lnkd.in/p/dgZ6MXS7)**
---

## 📌 Executive Summary & Operational Scale
* **Total Portfolio Revenue:** ₹989.3M across ~26.8K (27K) active customers
* **Revenue Run-Rate:** Daily Revenue Growth (DRG) of ₹5.47M
* **Customer Acquisition Run-Rate:** Daily Customer Growth (DCG) of 148.29/day
* **Seasonal Peak:** March 2023 surge reaching ₹263.8M and 7,081 customer acquisitions (driven by year-end tax planning)

---

## 📊 Dashboard Architecture & Views

### 1. Home View (Operational Pulse & Trends)
* **High-Level KPIs:** Instant monitoring of Total Revenue, Total Customers, DRG, and DCG.
* **Dynamic Bookmark Switcher:** Interactive toggle button to switch between Revenue and Customer growth trends across the same visual without leaving the page.
* **Demographic Matrix:** Revenue matrix crossing all 5 cities against 6 age brackets.

### 2. Sales Mode View (Distribution & Affinity)
* **Channel Distribution:** Donut and area charts breaking down sales across `Offline-Agent`, `Online-App`, `Offline-Direct`, and `Online-Website`.
* **Policy Performance Matrix:** Cross-tabulation of product revenues across sales channels to evaluate channel-level policy affinity.

### 3. Customer Demographics & Risk Analysis View
* **Demographic Cohorts:** Customer share analysis across age brackets (`18–24`, `25–30`, `31–40`, `41–50`, `51–65`, and `65+`).
* **Expected Settlement Reserves:** Visualizes liability exposure per demographic cohort to identify high-risk segments and guide underwriting policy.

---

## 🔍 Key Business Insights

| Category | Finding | Strategic Implication |
| :--- | :--- | :--- |
| **Metro Dominance** | **Delhi NCR** (₹401.6M / 40.6%) and **Mumbai** (₹239.5M / 24.2%) generate **64.8%** of total revenue. | Consolidate corporate agency teams in Tier-1 metros while expanding digitally in emerging hubs (Indore: ₹81.3M). |
| **Core Demographic** | The **31–40 age cohort** is the top revenue engine portfolio-wide, contributing **₹293.6M (29.7%)**. | Middle-aged professionals (31–50) generate >53% of revenue; launch targeted family health bundles. |
| **Channel Dynamics** | **Offline Agents** drive 55.7% (₹550.8M), while digital channels (App + Website) account for **~29%**. | Accelerate app renewals to lower intermediary broker commissions by 12–18%. |
| **Flagship Policy** | **POL2005HEL** dominates every sales mode, contributing **₹324.3M** (roughly 33% of revenue). | Anchor go-to-market strategies and product marketing around POL2005HEL. |
| **Settlement Liability** | Policyholders aged **65+** carry **~₹7.0B** in expected claims across a small customer base. | Introduce tiered deductibles and co-pay structures for senior renewals to safeguard reserves. |

---

## 🛠️ Data Architecture & Modeling

The project employs an optimized **Star Schema** to ensure high performance and clean relationship filtering:

* **Fact Tables:**
  * `fact_premiums`: Captures transactional policy sales (`customer_code`, `date`, `policy_id`, `sales_mode`, `final_premium_amt`).
  * `fact_settlements`: Auxiliary table providing historical claim settlement risk percentages by age cohort.
* **Dimension Tables:**
  * `dim_customer`: Customer demographics (`customer_code`, `Age`, `Age Segment`, `city`, `dob`, `Map_Latitude`, `Map_Longitude`).
  * `dim_policies`: Product metadata (`policy_id`, `base_coverage_amt`, `base_premium_amt`).
  * `dim_date`: Calendar lookup (`date`, `Day_no`, `day_type`, `mmm_yy`).

---

## 💡 Strategic Recommendations
1. **Tier-1 Metro Expansion:** Allocate senior relationship managers in Delhi NCR and Mumbai targeting high-earning corporate employees (ages 31–40).
2. **Digital Migration Strategy:** Provide renewal discounts on the Shield Mobile App to shift recurring transactions from brokers to direct digital channels.
3. **Underwriting Calibration:** Recalibrate premium rates and copay policies for `POL2005HEL` among seniors (65+) to buffer against elevated settlement risk.
