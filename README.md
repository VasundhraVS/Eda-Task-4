# Healthcare Data Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project focuses on **Exploratory Data Analysis (EDA)** and data preprocessing using a healthcare dataset.

The analysis was performed using **Python, Pandas, Matplotlib, and Seaborn**. The dataset was explored to understand its structure, identify missing values, clean the data, convert date columns, standardize categorical values, and derive new information such as hospital stay duration.

## 🎯 Objectives

* Understand the structure of the healthcare dataset
* Explore columns, data types, and dataset dimensions
* Identify and handle missing values
* Convert date columns into the appropriate datetime format
* Clean and standardize categorical data
* Calculate hospital stay duration
* Analyze billing amounts
* Explore medical conditions and admission types
* Perform basic statistical analysis
* Compare admission types with medical conditions
* Analyze the average age for different medical conditions

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook / Google Colab**

## 📂 Dataset

The project uses a healthcare dataset named:

`healthcare_raw.csv`

The dataset contains healthcare-related information including:

* Medical Code
* Admission Date
* Discharge Date
* Admission Type
* Medical Condition
* Age
* Billing Amount
* Other healthcare-related attributes

## 🔍 Data Analysis Process

### 1. Importing Libraries

The following Python libraries were used:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Loading the Dataset

The healthcare CSV file was loaded using Pandas:

```python
df = pd.read_csv("healthcare_raw.csv")
```

### 3. Dataset Exploration

The dataset was explored using:

* `df.head()`
* `df.tail()`
* `df.shape`
* `df.columns`
* `df.info()`
* `df.dtypes`
* `df.describe()`

These operations helped understand the dataset structure, dimensions, data types, and statistical summary.

### 4. Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

The `Medical_Code` column was specifically checked for missing values.

Missing medical codes were replaced with `"Unknown"`:

```python
df['Medical_Code'] = df['Medical_Code'].fillna('Unknown')
```

### 5. Date Conversion

The admission and discharge date columns were converted into datetime format:

```python
df['Admission_Date'] = pd.to_datetime(df['Admission_Date'])
df['Discharge_Date'] = pd.to_datetime(df['Discharge_Date'])
```

This makes the date columns suitable for further date-based analysis.

### 6. Categorical Data Cleaning

Admission types were standardized by removing unnecessary spaces and converting values to lowercase:

```python
df['Admission_Type'] = (
    df['Admission_Type']
    .str.strip()
    .str.lower()
)
```

### 7. Calculating Hospital Stay

A new column called `Hos_Stay_Days` was created to calculate the number of days a patient stayed in the hospital.

```python
df["Hos_Stay_Days"] = (
    df['Discharge_Date'] - df['Admission_Date']
).dt.days
```

### 8. Statistical Analysis

Statistical summaries were performed for:

* Billing Amount
* Hospital Stay Days
* Age

For example:

```python
df['Billing_Amount'].describe()
```

and

```python
df['Hos_Stay_Days'].describe()
```

### 9. Medical Condition Analysis

The frequency of different medical conditions was analyzed using:

```python
df["Medical_Condition"].value_counts()
```

### 10. Admission Type vs Medical Condition

A cross-tabulation was created to examine the relationship between admission types and medical conditions:

```python
pd.crosstab(
    df['Admission_Type'],
    df['Medical_Condition']
)
```

### 11. Average Age by Medical Condition

The average age for each medical condition was calculated using:

```python
df.groupby('Medical_Condition')['Age'].mean()
```

## 📊 Key EDA Areas

The notebook covers:

* Dataset structure exploration
* Missing-value detection and handling
* Data type conversion
* Categorical data cleaning
* Date preprocessing
* Feature creation
* Statistical summaries
* Medical condition distribution
* Admission type analysis
* Hospital stay analysis
* Age analysis

## 📁 Project Structure

```text
EDA-4/
│
├── EDA-4(1).ipynb
├── healthcare_raw.csv
└── README.md
```

## 🚀 How to Run

1. Clone or download this repository.
2. Open `EDA-4(1).ipynb` using **Jupyter Notebook** or **Google Colab**.
3. Make sure `healthcare_raw.csv` is available in the required location.
4. Install the required libraries if necessary:

```bash
pip install pandas matplotlib seaborn
```

5. Run the notebook cells sequentially.

## 📌 Conclusion

This project demonstrates the basic **data preprocessing and exploratory data analysis workflow** using a healthcare dataset.

The analysis includes identifying missing data, cleaning categorical values, converting dates, creating a new hospital-stay feature, and performing statistical and categorical analysis. These preprocessing steps help prepare healthcare data for further analysis, visualization, and potential machine learning applications.

## 👩‍💻 Author

**Vasundhra**

BCA Student | Aspiring Data Analyst / Full Stack Developer
