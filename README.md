# 📊 Flipkarts Mobile Analysis 

Welcome to the **Flipkarts Mobile Analysis** project! This project involves working with a sample SQL database to analyze mobile phone data typically found on Indian e-commerce platforms like Flipkart.

## 📁 Project Overview

This SQL project explores various insights about mobile phone products, pricing segments, discount trends, and customer ratings/reviews using SQL queries. It was created as a for database and SQL learning.

---

## 🛠️ Technologies Used

* MySQL / SQL
* Flipkart-inspired dataset
* SQL queries for data analysis

---

## 🧾 Dataset Description

The project works on a table named `mobiles` with the following assumed columns:

* `Brand` – Mobile phone brand
* `MRP` – Maximum Retail Price
* `MSP` – Selling Price (after discount)
* `Ratings` / `RatingS` – Customer ratings
* `No_Of_Reviews` – Number of customer reviews
* `Discount` – Discount percentage

---

## 📌 Key SQL Operations Performed

### 🔹 Price Range Segmentation

Classifies brands into price ranges:

* Below ₹10,000
* ₹10,000–₹19,999
* ₹20,000–₹39,999
* ₹40,000 and above

```sql
SELECT Brand,
  SUM(CASE WHEN MRP BETWEEN 0 AND 9999 THEN 1 ELSE 0 END) AS 'Price Below 10k',
  ...
FROM mobiles
GROUP BY Brand;
```

### 🔹 Brand with Highest Discount

Finds the brand offering the highest single product discount.

```sql
SELECT Brand, MAX(MRP - MSP) AS MaxDiscount
FROM mobiles
GROUP BY Brand
ORDER BY MaxDiscount DESC
LIMIT 1;
```

### 🔹 Top 5 Brands by:

* Average Rating
* Total Reviews

### 🔹 Product Filters

* Rating above 4.5 ⭐
* Discount greater than 40%

### 🔹 Additional Analysis

* Average rating and total reviews per brand
* Products with highest discounts
* Unique mobile brands in the dataset

---

## 📈 Learning Outcomes

✅ Understand how to use:

* `CASE` statements
* Aggregate functions (`SUM`, `AVG`, `MAX`)
* `GROUP BY`, `ORDER BY`, and `LIMIT`
* Filtering using `WHERE` clause

---

## 📦 How to Run

1. Import the SQL file into your MySQL database:

   ```sql
   source CLASS-10(FLIPKARTS).sql;
   ```

2. Run queries to explore mobile data insights.

---

## 🧠 Ideal For

* Beginners learning SQL
* School/college-level database projects
* Practicing basic to intermediate SQL queries

---

## 📬 Contact

Have suggestions or questions? Feel free to open an issue or connect monikadoble7@gmail.com 
Name:Monika Doble 
Phone:9890884532
