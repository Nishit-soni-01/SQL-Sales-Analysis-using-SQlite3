## 📊 SQL-Powered Interactive Sales Data Analysis Dashboard

### Project Repository for Data Science Training

This project demonstrates a full-stack data analysis workflow using Python and SQLite. It serves as a practical showcase of database management, advanced SQL querying, data wrangling, and generating business insights through visualization—all key skills for a Data Scientist.

## ✨ Key Features Demonstrated

As a 3rd-year B.Tech student and Data Science trainee, this project highlights the following core competencies:

* **Database Management (SQLite):** Efficient setup and connection to a serverless, file-based database (`sales_analysis.db`).
* **Data Ingestion & Wrangling:** Utilizing the `pandas` library to generate realistic synthetic data and leveraging `pandas.to_sql()` for fast, clean data loading into the database.
* **Advanced SQL Querying:** Execution of complex analytical queries directly on the SQLite database, including:
    * **Aggregation:** Using `SUM()` and `GROUP BY` to calculate Total Sales and Total Profit by category.
    * **Date Functionality:** Employing `strftime` to extract and group data by month for time-series trend analysis.
    * **Ranking & Filtering:** Using `ORDER BY` and `LIMIT` to identify top-performing regions.
* **Business Intelligence (Visualization):** Converting query results into actionable visualizations using `matplotlib` and `seaborn`.

## 🛠️ Technologies Used

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Database** | **SQLite3** (via Python's built-in module) | Backend data storage and relational management. |
| **Data Processing** | **Pandas** & **NumPy** | Data generation, manipulation, and SQL query execution (`pd.read_sql_query`). |
| **Visualization** | **Matplotlib** & **Seaborn** | Creating bar charts, line plots, and pie charts for insight presentation. |
| **Workflow** | **Jupyter Notebook** | Interactive development, documentation, and result presentation. |

## 🚀 Getting Started

### Prerequisites

* Python 3.x
* The required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`).


The notebook will:
* Generate 150 dummy sales records.
<img width="842" height="197" alt="Screenshot 2025-12-14 174256" src="https://github.com/user-attachments/assets/d6d5e139-f2cc-4908-b43d-7ea2bb442d12" />

* Create and populate the `sales_analysis.db` file.
* Execute all analytical SQL queries and print the results.
* Display the visualizations inline.
<img width="946" height="581" alt="Screenshot 2025-12-14 174309" src="https://github.com/user-attachments/assets/7c655db9-12a2-413d-b23b-c5723f9f2091" />



## 📈 Key Analytical Insights

The project focuses on three main business questions answered entirely through SQL queries:

### 1. Product Performance Analysis

* **SQL Query Concept:** `SELECT Product, SUM(Sales), SUM(Profit) FROM sales GROUP BY Product...`
* **Insight:** Identifies the most profitable and highest-grossing products, informing inventory strategy and marketing spend allocation.

<img width="1244" height="745" alt="Screenshot 2025-12-14 174333" src="https://github.com/user-attachments/assets/a7419f80-e495-4d65-9208-fe141c5bc6f7" />


### 2. Monthly Sales Trend

* **SQL Query Concept:** `SELECT strftime('%Y-%m', Date) AS Sale_Month, SUM(Sales) FROM sales GROUP BY Sale_Month...`
* **Insight:** Visualizes the sales volume over time, helping to detect seasonality, growth momentum, or periods requiring promotional intervention.

<img width="1467" height="793" alt="Screenshot 2025-12-14 174353" src="https://github.com/user-attachments/assets/b65810b4-6e9b-4d27-bc9a-89ccd7d19fe2" />


### 3. Regional Sales Contribution

* **SQL Query Concept:** `SELECT Region, SUM(Quantity) FROM sales GROUP BY Region ORDER BY SUM(Quantity) DESC LIMIT 3;`
* **Insight:** Pinpoints the top-performing geographic regions, providing critical information for optimizing distribution and sales team focus.


<img width="1001" height="845" alt="Screenshot 2025-12-14 174411" src="https://github.com/user-attachments/assets/a3cabb07-a2fa-4dfd-8cba-651c34c66759" />

---
*Created by Nishit soni as part of Data Science Training.*
---
