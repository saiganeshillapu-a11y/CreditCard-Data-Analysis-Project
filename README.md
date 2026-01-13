# 💳 CreditCard-Data-Analysis-Project

## 📌 Project Overview
This project implements an **end-to-end Data Analytics pipeline** to process, analyze, and visualize **credit card transaction data** for a financial services organization.  
The system ingests raw transaction data, performs large-scale processing using **Spark, Hive, and Kafka**, and presents actionable insights through **Power BI dashboards**.  

The project demonstrates both **batch and streaming data processing**, converting raw financial data into meaningful business intelligence to support strategic decision-making.

---
## Project Team
- Rajasekharreddy Kamireddy
- Nikhilavaishnavi Katteboina
- Krishnateja Garampalli
- Sai Ganesh Illapu
- Peddabala Anuja

## ❓ Problem Statement
Credit card transactions are generated daily across multiple **cities, card types, and expense categories** for PK&G Finance Company.  
The raw transaction data is **high-volume, unstructured, and difficult to analyze directly**.

Business stakeholders require answers to key questions such as:
- Which cities contribute the highest spending?
- Which months and card types generate maximum revenue?
- How does customer spending vary by gender and expense type?
- What are weekend vs weekday spending patterns?
- How quickly do cumulative spends reach key thresholds?

The challenge is to **process, analyze, and visualize this data efficiently** to extract insights that support better financial and operational decisions.

---

## 🎯 Project Objectives
- Build a **scalable data ingestion pipeline** for batch and streaming data
- Clean and transform raw credit card transaction data
- Perform **advanced analytics** using RDDs, DataFrames, Spark SQL, and HiveQL
- Analyze spending behavior across cities, card types, time periods, and expense categories
- Enable **real-time and batch analytics**
- Deliver interactive **Power BI dashboards** for business users

---

## 📊 Dataset
**Dataset Name:** Credit Card Transaction Dataset  

### 📄 Dataset Description
Each record represents a single credit card transaction with the following attributes:

| Column Name | Description |
|------------|-------------|
| Date | Transaction date (DD-MMM-YY) |
| CardType | Type of credit card (Gold, Silver, Platinum, Signature) |
| ExpenseType | Category of expense (Fuel, Grocery, Travel, Bills, Entertainment, etc.) |
| Gender | Gender of cardholder (M/F) |
| Amount | Transaction amount |

### 📈 Dataset Usage
- Time-based trend analysis (monthly, yearly, seasonal)
- City-wise and card-type spending analysis
- Customer behavior and lifestyle analysis
- Financial insights for business intelligence

---

## 🧰 Tech Stack
- **Programming & Querying:** Python, SQL  
- **Big Data Processing:** Apache Spark (RDD, DataFrame, Spark SQL)  
- **Streaming:** Apache Kafka, Spark Streaming  
- **Data Ingestion & Orchestration:** Apache NiFi  
- **Data Storage:** HDFS (Lakehouse-style Data Lake)  
- **Analytics:** Hive & HiveQL  
- **Visualization:** Power BI  
- **Version Control:** Git & GitHub  

---

## 🏗️ Architecture Overview
1. **Data Source**  
   - Credit card transaction CSV files  

2. **Data Ingestion Layer**  
   - Apache NiFi for file movement and ingestion  
   - Kafka for real-time streaming ingestion  

3. **Storage Layer**  
   - Raw and processed data stored in **HDFS**  

4. **Processing & Analytics Layer**  
   - Spark RDDs & DataFrames  
   - Hive & Spark SQL for analytical queries  
   - Spark Streaming for real-time simulation  

5. **Visualization Layer**  
   - Power BI dashboards for business insights  

---

## 🔄 Data Ingestion

### 🔹 Apache NiFi
- Moves files from source to target directories
- Transfers local files into HDFS
- Pulls data from APIs and lands it into HDFS reliably

### 🔹 Apache Kafka
- Kafka topic creation using CLI
- Kafka producer sends transaction data
- Kafka consumer reads streamed data
- Spark consumes Kafka streams for real-time processing

---

## ⚙️ Data Processing & Analytics

### 🔹 Data Cleaning
- Schema validation and inspection
- Duplicate record removal
- Data type corrections
- Record count verification

### 🔹 PySpark RDD Analytics
- Top 5 cities by total spend
- Highest & lowest expense type per city
- Weekend transaction ratio by city
- Least days to reach 500 transactions per city
- City-wise total and average spend

### 🔹 Hive & HiveQL Analytics
- Rank transactions within each city
- Cities with total spend greater than overall average
- Transaction count by gender and expense type
- Running cumulative spend per card type
- Monthly total spending analysis

### 🔹 Spark SQL Analytics
- Top 5 cities by total spend
- Highest spending month for each card type
- Month-wise spending trends
- Transaction details when cumulative spend reaches 100,000
- City with highest weekend spend-to-transaction ratio
- Highest spending expense type per city

### 🔹 Spark Streaming
- Simulated real-time ingestion using streaming folders
- Schema definition and streaming DataFrame creation
- Aggregations written to console
- Multiple batches added to simulate live data flow

---

## 📈 Power BI Reporting
Interactive dashboards were built to visualize insights:

- **Gold Card Report**  
  - Mid-tier customer spending analysis  
  - City-wise performance  

- **Platinum Card Report**  
  - Premium customer behavior  
  - High-value transactions  

- **Signature Card Report**  
  - High-end spending patterns across cities and time  

- **Overall Insights Dashboard**  
  - Total spend comparison across cities  
  - Top 5 spending cities (tabular & geographical view)  
  - Trend-based insights for stakeholders  

---

## ✅ Conclusion
This project successfully demonstrates a **complete data engineering lifecycle**, from ingestion to visualization.  
By leveraging **NiFi, Kafka, Spark, Hive, and Power BI**, raw credit card transaction data is transformed into **valuable business insights**.


---


