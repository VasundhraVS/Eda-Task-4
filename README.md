# 🏥 Healthcare Data Analysis – Exploratory Data Analysis

## 📌 Project Overview

This project focuses on performing **Exploratory Data Analysis (EDA)** on a healthcare dataset using Python.

The objective of this project is to understand patient-related information, identify missing values, clean and transform the data, and perform statistical and categorical analysis to discover useful patterns in the healthcare dataset.

The analysis was performed using **Pandas, Matplotlib, and Seaborn** in a Python/Jupyter Notebook environment.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Load and understand the healthcare dataset
- Explore the structure and dimensions of the dataset
- Inspect columns and data types
- Identify missing values
- Handle missing values
- Convert date columns into the appropriate datetime format
- Standardize categorical values
- Calculate hospital stay duration
- Analyze admission types
- Analyze medical conditions
- Analyze billing amounts
- Calculate descriptive statistics
- Compare average patient age across medical conditions
- Create a cleaned dataset suitable for further analysis

---

## 📊 Dataset Overview

The dataset contains information about **500 patients** and initially consists of **9 columns**.

### Dataset Columns

| Column | Description |
|---|---|
| `Patient_ID` | Unique identifier assigned to each patient |
| `Gender` | Gender of the patient |
| `Age` | Age of the patient |
| `Medical_Condition` | Medical condition associated with the patient |
| `Admission_Date` | Date on which the patient was admitted |
| `Admission_Type` | Type of hospital admission |
| `Medical_Code` | Medical/diagnostic code associated with the condition |
| `Billing_Amount` | Amount billed for the patient's hospital treatment |
| `Discharge_Date` | Date on which the patient was discharged |

A new calculated column, `Hos_Stay_Days`, is created during the analysis to represent the patient's hospital stay duration.

---

## 🗂️ Project Structure

```text
Healthcare-Data-Analysis/
│
├── EDA-4.ipynb
├── healthcare_raw.csv
└── README.md
