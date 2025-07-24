# Big Data Recommender System

A scalable collaborative filtering recommender system for Amazon Electronics product ratings using Apache Spark.

## 📁 Repository Name
**BigData**

## 🛠 Tech Stack
- PySpark (Apache Spark MLlib)
- ALS (Alternating Least Squares)

---

## 📌 Project Description

This project demonstrates the power of distributed data processing and collaborative filtering at scale. We built a recommender system on **Amazon Electronics** product data using Spark’s ALS algorithm to handle **millions of real-world product ratings** efficiently.

---

## 🚀 Features

- 💾 Managed over **7.8 million** product ratings from real-world Amazon data.
- 🔍 Applied **5-core filtering** (users and items with ≥ 5 ratings) for denser interactions.
- ⚙️ Trained an **ALS collaborative filtering model** to generate personalized recommendations.
- 🎯 Generated **Top-5 recommendations** per user and product.
- 📉 Achieved **RMSE ≈ 3.10** on a robust 10% test sample.
- ⚡ Developed using an **optimized Spark setup** with tuned parallelism, partitioning, and memory management.

---

## 🧪 Sample Workflow

```python
from pyspark.ml.recommendation import ALS

# Initialize ALS model
als = ALS(
    userCol="userIndex",
    itemCol="productIndex",
    ratingCol="rating"
)

# Fit model to training data
model = als.fit(train_data)
