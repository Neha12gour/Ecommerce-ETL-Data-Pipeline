# 🚀 End-to-End E-commerce ETL Pipeline & Power BI Dashboard

## 📌 Project Overview
This project demonstrates a complete **ETL (Extract, Transform, Load) pipeline** built using e-commerce data from an API.  
The pipeline processes raw JSON data, transforms it into structured format, stores it in a SQL database, and visualizes insights using Power BI.

---

## 🏢 Business Problem
E-commerce businesses generate large volumes of raw, unstructured data.  
The challenge is to convert this data into **meaningful insights** to support decision-making.

This project answers:
- What is the total revenue?
- Which products and categories drive sales?
- Who are the most valuable customers?
- How does revenue vary across regions and time?

---

## 🔄 Project Architecture

API → Python (ETL) → MySQL → Power BI Dashboard

---

## 🛠️ Tech Stack

- **Python** (Pandas, Requests)
- **MySQL**
- **SQLAlchemy**
- **Power BI**
- **DummyJSON API**

---

## ⚙️ ETL Pipeline

### 🔹 1. Extract
- Fetched data from API endpoints:
  - Products
  - Users
  - Carts

- Used `requests` to retrieve JSON data  
- Converted JSON into Pandas DataFrames  

---

### 🔹 2. Transform

#### Data Cleaning
- Removed duplicates  
- Selected relevant columns  
- Renamed columns for consistency  

#### Data Transformation
- Flattened nested JSON (cart → products) using `explode()`  
- Extracted:
  - product_id  
  - quantity  

#### Feature Engineering
- Created key metrics:
  - **Revenue = price × quantity**
  - Extracted **month & year from date**
- Merged datasets to enrich data:
  - carts + products → for price  

---

### 🔹 3. Load
- Loaded cleaned data into MySQL using SQLAlchemy  
- Created structured tables:
  - `products`
  - `users`
  - `orders`

---

## 🗄️ Database Schema

### 📦 products
- product_id  
- title  
- price  
- category  

### 👤 users
- user_id  
- full_name  
- city  

### 🧾 orders
- cart_id  
- user_id  
- product_id  
- quantity  
- revenue  
- date  

---

## 📊 Power BI Dashboard

### 🔹 KPIs
- Total Revenue  
- Total Orders  
- Average Order Value (AOV)  
- Total Customers  

---

### 🔹 Visualizations
- Revenue by Category  
- Revenue by City  
- Top Products  
- Revenue by Gender  
- Average Rating by Category  
- Sales Trend (Time-based)

---

## 📈 Key Insights

- 🪑 Furniture category contributes majority of revenue (~87%)  
- 🌍 Certain cities dominate revenue generation  
- 💳 High AOV indicates strong purchasing power  
- 👩 Customer base heavily skewed towards one segment  
- 📦 Few products contribute most revenue (Pareto principle)

---

## 🚀 Key Learnings

- Built a real-world **ETL pipeline from scratch**  
- Worked with **API-based data ingestion**  
- Performed **data transformation & feature engineering**  
- Integrated **SQL with Power BI**  
- Translated raw data into **business insights**

---

## 🔮 Future Improvements

- Automate pipeline (Airflow / Scheduler)  
- Implement incremental loading  
- Deploy on cloud (AWS / Azure)  

---

## 🤝 Let's Connect

I’m actively looking for **Data Analyst / Business Analyst roles**.  
Feel free to connect and discuss data, analytics, or opportunities!

---
