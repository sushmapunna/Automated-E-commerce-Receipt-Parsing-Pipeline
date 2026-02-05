# Automated-E-commerce-Receipt-Parsing-Pipeline
eveloped a Python ETL pipeline using Regex to transform unstructured receipt data into structured, SQL-ready datasets.  Automated merchant and date normalization to reduce manual data cleaning effort.
**Goal:** Transform unstructured, multi-format e-commerce receipt logs into structured, SQL-ready datasets.

### 🔹 The Challenge
Raw transaction logs from vendors like **Amazon**, **Uber**, and **Swiggy** often come in inconsistent text formats:
* *Amazon:* "Order #123 paid Rs. 500 on 12-Jan-2025"
* *Uber:* "Trip on 15 Jan cost 500" (Missing year, different structure)
* *Flipkart:* "id FK-999 sent 450 INR. Date: 2025/01/13"

### 🔹 The Solution (`cleaner.py`)
I built a Python pipeline using **Pandas** and **Regular Expressions (Regex)** to:
1.  **Parse Unstructured Text:** Engineered complex Regex patterns to extract Merchant, Amount, Date, and Order ID from diverse strings.
2.  **Normalize Data:** Implemented logic to standardize disparate date formats (e.g., converting '15 Jan' to '2025-01-15') and vendor names.
3.  **Automated QA:** Designed a validation layer that flags invalid records (e.g., missing amounts, future dates) and segregates them into a `qa_report.csv` for root cause analysis.
## 🛠 Tech Stack & Skills
* **Languages:** Python 3.x, SQL.
* **Libraries:** Pandas, NumPy, Re (Regex), SQLite.
* **Concepts:** ETL Pipelines, Data Cleaning, Window Functions (LAG, OVER), Root Cause Analysis (RCA), Anomaly Detection.

---
