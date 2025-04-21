# 📊 Netflix Dataset Cleaning and Preprocessing Project

Welcome to my Netflix Data Cleaning Project!  
This project is focused on **cleaning, transforming, and preparing** the Netflix dataset to make it analysis-ready using Python and the Pandas library. The dataset contains metadata about TV shows and movies available on Netflix, including titles, countries, genres, release years, ratings, and more.

---

## 📁 Dataset Overview

- **Source**: [Kaggle Netflix Titles Dataset]
- **File**: `netflix_titles.csv`
- **Rows**: ~6,000
- **Original Columns**: 12
- **Context**: This dataset includes information like show ID, type (Movie/TV Show), title, country of production, release year, rating, duration, genres, etc.

---

## 🏯 Project Objective

The primary objective of this project is to:
> **Clean and prepare a dataset (without nulls, duplicates, and inconsistent formats) to make it suitable for analysis and business insights.**

---

## 🛠️ Step-by-Step Work Done

### 1. ✅ **Data Loading & Initial Exploration**
- Loaded the dataset using `pd.read_csv()`
- Inspected first 10 rows using `.head()`
- Checked data types, non-null values, and column names using `.info()`

---

### 2. 🧹 **Removing Unnecessary Columns**
- Dropped the following columns:
  - `cast`
  - `director`
  - `description`
- **Reason**: These fields contain long text and sparse data that are not required for this phase of analysis.

---

### 3. 🔍 **Checking & Handling Missing Values**
- Used `.isnull().sum()` to check nulls in each column.
- Found missing values in:
  - `country`
  - `date_added`
  - `rating`
  - `duration`

#### ➔ Treatment:
- **`country`**: Filled missing values with the **most frequently occurring country** (`United States`).
- **`date_added`, `rating`, `duration`**: Filled missing values using **forward fill method (`ffill`)**.

---

### 4. ♻️ **Handling Duplicates**
- Iterated through each column and counted duplicated values using `.duplicated().sum()`
- Checked and reported duplicates per column.

---

### 5. 📅 **Date Format Cleaning**
- Converted `date_added` to **datetime format** using `format='mixed'`.
- Ensured `release_year` is treated as a proper integer year using `.dt.year`.

---

### 6. ✂️ **Whitespace Removal in Text Columns**
- Removed unnecessary whitespaces from string-based columns using `applymap()` with a lambda function.
- This step ensures consistency in values for future analysis.

---
## 7. Saved the cleaned data in the desktop
- Saved the file in the desktop using '.to_csv()' 

---
## ✅ Final Output

After cleaning, the dataset is now:
- **Free of null values** in critical columns
- **Free from redundant/unnecessary columns**
- **Uniform in text formatting**
- **Properly formatted datetime fields**
- **Checked for duplicates**
- **Consistent and analysis-ready**
- **Saved the cleaned data in Desktop**
---

## 📌 Tools & Technologies Used

| Tool        | Purpose                                |
|-------------|----------------------------------------|
| Python      | Programming language                   |
| Pandas      | Data manipulation & cleaning           |
| Jupyter / PyCharm | IDE for writing and executing code |
| NumPy       | (Implicitly used via Pandas)           |

---

## 📊 Next Steps (Future Scope)

Now that the dataset is clean, the next steps could include:
- Performing **Exploratory Data Analysis (EDA)**
- Creating **visualizations** using Matplotlib / Seaborn
- Extracting business insights (e.g., most popular content type, country-wise distribution)
- Building **dashboards** or using in **machine learning pipelines**

---

## 👩‍💼 About Me

I’m currently pursuing my **Bachelor’s degree** and learning **Business Analytics**.  
This project is a part of my learning journey to improve my skills in data cleaning and real-world data handling.

I am always open to feedback, collaboration, or internship opportunities in data analytics. Feel free to connect!

---

## 📂 Project Structure

```
netflix_data_cleaning/
│
├── netflix_titles.csv            # Raw dataset
├── netflix_cleaned.csv           # Cleaned dataset (output)
├── netflix_cleaning_script.py    # Python script used for cleaning
└── README.md                     # This file
```

---

## 📬 Contact

- 📧 Email: anuragsharma200078690@gmail.com
