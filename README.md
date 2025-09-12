# Mental Illnesses Prevalence Analysis

<div align="center">
  
  [![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org)
  [![Pandas](https://img.shields.io/badge/Pandas-2.0.3-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org)
  [![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7.2-11557c?style=flat)](https://matplotlib.org)
  [![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org)
  
  [![Data Source](https://img.shields.io/badge/Data-Kaggle%20Dataset-20BEFF?style=flat&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/imtkaggleteam/mental-health/data)
  [![Years](https://img.shields.io/badge/Years-1990--2019-green?style=flat&logo=calendar&logoColor=white)](https://github.com)
  [![Countries](https://img.shields.io/badge/Countries-204-orange?style=flat&logo=globe&logoColor=white)](https://github.com)
  [![Regions](https://img.shields.io/badge/Regions-5-pink?style=flat&logo=globe&logoColor=white)](https://github.com)
  [![Economic Groups](https://img.shields.io/badge/EconomicGroups-4-purple?style=flat&logo=globe&logoColor=white)](https://github.com)

  [![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat&logo=progress&logoColor=white)](https://github.com)
  [![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat&logo=github&logoColor=white)](https://github.com)

</div>

---

## 📌 Project Overview

This project analyzes **global mental health prevalence** (schizophrenia, depression, anxiety, bipolar disorder, eating disorders) using data from `1-mental-illnesses-prevalence.csv`.  

**Objectives:**

- Clean and preprocess data
- Handle missing values and outliers
- Analyze country, regional, economic, and global trends
- Visualize patterns and correlations between disorders

---

## 📂 Dataset

**Source file:** [Kaggle - Mental Health Dataset](https://www.kaggle.com/datasets/imtkaggleteam/mental-health/data)  

**Main columns(disorders) analyzed:**

| Disorder | Global Average | Range |
|----------|---------------|--------|
| 🔴 Schizophrenia | 0.29 | 0.287 - 0.29 |
| 🔵 Depressive | 3.51 | 3.41 - 3.597 |
| 🟡 Anxiety | 3.79 | 3.746 - 3.846 |
| 🟣 Bipolar | 0.49 | 0.487 - 0.49 |
| 🟢 Eating Disorder | 0.16 | 0.151 - 0.174 |

Other columns include:

- `Entity` (Country / Region / Economic Group)  
- `Code`  
- `Year`  

Dataset Summary:
Countries: 204 | Regions: 5 | Economic Groups: 4 | World: 1
Total Records: 6420

---

## 🛠️ Key Steps

### 1️⃣ Data Cleaning

- Renamed long column names into short, readable ones.  
- Filled missing `Code` values using **region and economic group mapping**.  
- Removed duplicates and reset index.  
- **Outlier handling:** Clipped all mental health columns using **IQR method**.  

### 2️⃣ Data Segmentation

- `df_regions` → regional level  
- `df_economy` → economic group level  
- `df_countries` → country level  
- `df_world` → global level  

### 3️⃣ Exploratory Data Analysis (EDA)

- Calculated **country-level averages**.  
- **Global average prevalence** with min-max range (after outlier clipping).  
- Identified **highest and lowest prevalence countries** in 2019.  
- Analyzed **depression & anxiety averages per country**.  
- Calculated **yearly averages** and correlations between disorders.  
- Tracked **yearly increases/decreases** in prevalence.  

### 4️⃣ Correlation Analysis

- **Depression** shows a strong **negative correlation** with other disorders (~ -0.96).  
- **Schizophrenia** and **Anxiety** / **Eating Disorder** have strong **positive correlations** (~0.8–0.98).  
- **Bipolar disorder** is relatively stable, moderately positively correlated with others.  

### 5️⃣ Visualization

- **Yearly changes** for all disorders (line plots)  
- **Average prevalence** by region and economic group (bar plots)  
- **Correlation matrix** between disorders  

---

## 📊 Example Insights

- Depression and anxiety are **more prevalent globally**.  
- Schizophrenia, bipolar, and eating disorders are **rarer and globally stable**.  
- Outlier clipping ensures that extreme country values **do not distort global averages**.  
- Regional and economic differences are clearly visible in bar charts.  

---

## 📈 Technologies Used

- **Python**  
  - `pandas` → Data manipulation  
  - `matplotlib` → Visualization  
- **Jupyter Notebook** → Analysis and documentation  

---

## 🚀 How to Run

```bash
git clone https://github.com/BuseBoy/Mental-Illnesses-Prevalence-Analysis.git
cd Mental-Illnesses-Prevalence-Analysis
pip install pandas matplotlib
jupyter notebook analysis.ipynb
