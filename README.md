# 🎵 Chinook Music Store: Data Warehouse & BI Project

![Dashboard Preview](mining/output/dashboard_preview.png)
## 📌 Project Overview
This project implements a complete **Business Intelligence** solution for Chinook Music Store, focusing on the **Financial Perspective**. The goal is to analyze revenue trends, customer segments, and forecast future sales to assist executive decision-making.

**Key Objectives:**
1.  Design a **Star Schema** Data Warehouse.
2.  Perform **ETL** (Extract, Transform, Load) processes.
3.  Implement **Data Mining** (Clustering & Regression) for predictive insights.
4.  Develop an interactive **Dashboard** for KPI monitoring.

---

## 🏗️ Architecture & Tech Stack

| Component | Tool Used | Description |
| :--- | :--- | :--- |
| **Database** | MySQL / CSV | Source operational data. |
| **ETL** | Pentaho (PDI) | Data integration & cleaning. |
| **Data Mining** | Python (Pandas, Scikit-Learn) | Customer Segmentation (RFM) & Sales Forecasting. |
| **Dashboard** | Google Looker Studio | Visualizing KPIs (Revenue, Growth, ARPC). |

---

## 📊 1. Data Warehouse Design
We transformed the transactional database (3NF) into a **Star Schema** optimized for OLAP queries.

- **Fact Table:** `Fact_Sales` (Measures: Quantity, Amount, LineTotal).
- **Dimension Tables:**
  - `Dim_Customer` (Geography, Email).
  - `Dim_Time` (Year, Quarter, Month, Day).
  - `Dim_Music` (Track, Genre, Album, Artist).

---

## 🧠 2. Data Mining Implementation

### A. Customer Segmentation (Clustering)
**Algorithm:** K-Means Clustering
**Goal:** Group customers based on RFM (Recency, Frequency, Monetary) to identify high-value clients.

| Cluster | Label | Insight |
| :--- | :--- | :--- |
| **0** | Standard | Regular customers with average spending. |
| **1** | Dormant | Inactive customers (>1.5 years), high churn risk. |
| **2** | **Premium** | **High ARPC ($44.8)**, recent activity. Priority for loyalty programs. |

### B. Sales Forecasting (Regression)
**Algorithm:** Linear Regression
**Goal:** Predict Monthly Revenue for the next 6 months.
**Result:**
- **Slope:** `-0.01` (Indicates Stagnant/Slightly Declining Trend).
- **Recommendation:** Requires immediate marketing intervention or catalog expansion.

![Regression Result](mining/output/regression_result.png)

---

## 📈 3. Dashboard Visualization
The Executive Dashboard visualizes the following KPIs:
- **Total Revenue:** Real-time financial position.
- **ARPC (Avg Revenue Per Customer):** Monitoring customer value.
- **Sales Trend:** Historical vs. Forecasted data.

🔗 **[View Live Dashboard](LINK_DASHBOARD_LOOKER_KAMU_DISINI)**

---

## 🚀 How to Run

### Prerequisites
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `scikit-learn`

### Steps
1. **Clone the repository**
   ```bash
   git clone [https://github.com/username/chinook-dwh-project.git](https://github.com/username/chinook-dwh-project.git)
