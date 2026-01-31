# Food Delivery Market Analysis

## 📌 Project Overview

This project presents an end-to-end **data integration and analysis** of a food delivery platform using data from multiple real-world sources and formats. The goal is to combine heterogeneous datasets into a single analytical view and extract meaningful business insights related to orders, users, restaurants, revenue, and customer behavior.

The analysis focuses on understanding **order trends, user behavior, restaurant performance, membership impact, and revenue seasonality**.

---

## 📂 Datasets Used

The project integrates three different datasets, each representing a real-world system:

| Dataset           | Format | Description                                       |
| ----------------- | ------ | ------------------------------------------------- |
| `orders.csv`      | CSV    | Transaction-level order data                      |
| `users.json`      | JSON   | User profile and membership details               |
| `restaurants.sql` | SQL    | Restaurant metadata including cuisine and ratings |

---

## 🔗 Data Integration (ETL Process)

### Step 1: Load Data

* Orders loaded from CSV
* Users loaded from JSON
* Restaurants loaded by executing SQL into a database

### Step 2: Join Logic

The datasets were merged using **LEFT JOINs** to ensure all orders are retained:

* `orders.user_id` → `users.user_id`
* `orders.restaurant_id` → `restaurants.restaurant_id`

### Step 3: Final Dataset

The final merged dataset contains:

* Order details (order ID, date, amount)
* User information (city, membership type)
* Restaurant information (name, cuisine, rating)

Output file:

```
final_food_delivery_dataset.csv
```

---

## 📊 Analysis Performed

### 1️⃣ Order Trends Over Time

* Monthly order volume analysis
* Identification of growth and decline periods

### 2️⃣ User Behavior Patterns

* Orders per user
* Repeat customer behavior
* Spending trends

### 3️⃣ City-wise & Cuisine-wise Performance

* Top-performing cities by revenue
* Most popular and profitable cuisines

### 4️⃣ Membership Impact (Gold vs Regular)

* Order count comparison
* Revenue contribution by membership type
* Average order value (AOV) analysis

### 5️⃣ Revenue Distribution & Seasonality

* Monthly revenue trends
* Detection of seasonal spikes
* Revenue concentration insights

---

## 🛠 Tools & Technologies

* **Python**
* **Pandas** – data manipulation and joins
* **SQLite** – SQL execution
* **Jupyter Notebook** – analysis and visualization

---

## 📈 Key Outcomes

* Successfully integrated multi-format datasets into a single analytical view
* Demonstrated real-world ETL and data wrangling skills
* Generated actionable business insights for a food delivery platform

---

## 📁 Project Structure

```
├── orders.csv
├── users.json
├── restaurants.sql
├── final_food_delivery_dataset.csv
├── Food Delivery Market Analysis.ipynb
└── README.md
```

---

## 🚀 Future Improvements

* Add predictive modeling for demand forecasting
* Perform customer segmentation
* Build dashboards using Power BI / Tableau
* Automate the ETL pipeline

---

## ⚠️ Disclaimer

This project is created for **learning and demonstration purposes only**. The datasets are simulated and do not represent real customer or business data.

---

## 👤 Author

**Om Shah**

---

⭐ If you find this project useful, feel free to star the repository!
