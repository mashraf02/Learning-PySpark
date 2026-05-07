# Airbnb Data Analysis with Apache Spark

A beginner-friendly big data analytics project built using **PySpark** to analyze Airbnb listing, review, and calendar datasets. This project demonstrates how Apache Spark can be used for large-scale data processing, cleaning, transformation, aggregation, and exploratory data analysis.

---

# Project Overview

This notebook-based project focuses on learning and practicing core Apache Spark concepts using real-world Airbnb datasets.

The analysis includes:

- Loading large CSV datasets with PySpark
- Creating and configuring Spark sessions
- Exploring DataFrame schemas and structures
- Cleaning and preprocessing data
- Handling duplicate column names
- Aggregations and statistical analysis
- GroupBy operations
- Working with Spark SQL functions
- Understanding data distributions and trends

The project is designed mainly for:

- Beginners learning Apache Spark
- Students practicing PySpark DataFrames
- Data engineering and analytics learners
- Big data enthusiasts exploring real-world datasets

---

# Technologies Used

- Python
- Apache Spark (PySpark)
- Jupyter Notebook
- Spark SQL Functions

---

# Dataset

The project uses Airbnb datasets containing:

- Listings information
- Reviews data
- Calendar availability data

Dataset files used:

```bash
Data/listings.csv.gz
Data/reviews.csv.gz
Data/calendar.csv.gz
```

---

# Key Learning Topics

## Spark Session Creation

Learned how to:

- Configure Spark
- Set shuffle partitions
- Control logging levels
- Initialize SparkSession properly

## Data Loading

Used:

```python
spark.read.csv()
```

with:

- `header=True`
- `inferSchema=True`
- `multiLine=True`
- `escape='"'`

## Data Exploration

Performed:

- Schema inspection
- Row/column counting
- Data previews
- Statistical summaries

## Data Cleaning

Implemented:

- Duplicate column handling
- Null checking
- Column renaming
- Data formatting

## Aggregations & Analytics

Used:

- `groupBy()`
- `agg()`
- `avg()`
- `min()`
- `max()`
- `count()`
- `orderBy()`

Example:

```python
listings_clean.groupBy("room_type") \
    .agg(
        F.count("id").alias("total_listings"),
        F.round(F.avg("price_usd"), 2).alias("avg_price")
    )
```

---

# Project Structure

```bash
├── practise-apache-spark.ipynb
├── Data/
│   ├── listings.csv.gz
│   ├── reviews.csv.gz
│   └── calendar.csv.gz
└── README.md
```

---

# How to Run

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

## 2. Move into the Project Folder

```bash
cd your-repository-name
```

## 3. Install Dependencies

```bash
pip install pyspark jupyter
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

## 5. Open the Notebook

```bash
practise-apache-spark.ipynb
```

---

# Skills Demonstrated

- Big Data Processing
- PySpark DataFrames
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Spark SQL Functions
- Distributed Data Processing Basics
- Data Aggregation Techniques

---

# Future Improvements

Possible future enhancements:

- Data visualization with Matplotlib or Plotly
- Spark SQL queries
- Machine learning with Spark MLlib
- Airbnb price prediction model
- Dashboard integration
- Kafka streaming integration
- Data pipeline automation using Airflow

---

# Why This Project?

This project was created as part of a learning journey into:

- Apache Spark
- Big data analytics
- Distributed computing
- PySpark-based data engineering workflows

It focuses on understanding Spark fundamentals through hands-on experimentation with real-world datasets.

---

# Author

**Mashraful Islam**

Computer Science & Engineering Student

Interested in:

- Big Data
- Data Engineering
- Machine Learning
- Distributed Systems
- Apache Spark Ecosystem

---

# License

This project is for educational and learning purposes.
