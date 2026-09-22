# Healthcare Data Analysis – Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project focuses on performing **Exploratory Data Analysis (EDA)** on a healthcare dataset using Python. The dataset contains patient information such as age, gender, medical condition, admission type, medical code, billing amount, admission date, and discharge date.

The project involves understanding the dataset, cleaning missing and inconsistent data, converting date columns, creating new features, and analyzing healthcare-related patterns.

---

## 🎯 Objectives

- Understand the structure and characteristics of the healthcare dataset
- Perform basic data exploration
- Identify and handle missing values
- Convert date columns into the appropriate format
- Standardize categorical data
- Calculate hospital stay duration
- Analyze medical conditions and admission types
- Analyze billing amounts and patient ages
- Identify relationships between different healthcare attributes

---

## 📊 Dataset

The dataset contains **500 patient records** and **9 columns**.

### Dataset Columns

| Column | Description |
|---|---|
| Patient_ID | Unique identifier for each patient |
| Gender | Gender of the patient |
| Age | Age of the patient |
| Medical_Condition | Medical condition diagnosed |
| Admission_Date | Date of hospital admission |
| Admission_Type | Type of hospital admission |
| Medical_Code | Medical/diagnostic code |
| Billing_Amount | Hospital billing amount |
| Discharge_Date | Date of hospital discharge |

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## 🔍 Data Analysis Process

### 1. Data Loading

The healthcare dataset was loaded using Pandas.

```python
import pandas as pd

df = pd.read_csv("healthcare_raw.csv")
