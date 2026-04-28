````markdown
# 📊 Annual Enterprise Survey 2024 — Exploratory Data Analysis

<div align="center">

### Financial Performance Analysis of New Zealand Enterprises

A professional exploratory data analysis (EDA) project using statistics and visualization to uncover patterns in enterprise financial performance across industries.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-lightgrey.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

</div>

---

## 📌 Overview

This project analyzes the **Annual Enterprise Survey: 2024 Financial Year (Provisional)** dataset to identify how financial values vary across industries, variable categories, and reporting units.

The analysis combines:

- 📈 Exploratory Data Analysis (EDA)  
- 📊 Statistical Testing (ANOVA)  
- 📉 Data Visualization  
- 🧹 Data Cleaning & Preprocessing  

---

## 📂 Project Structure

```text
Annual-Enterprise-Survey-EDA/
│
├── Annual_EnterPriese_survey.ipynb
├── annual-enterprise-survey-2024-financial-year-provisional.csv
├── README.md
└── LICENSE
````

---

## 📊 Dataset Summary

| Attribute                | Details                       |
| ------------------------ | ----------------------------- |
| **Dataset Name**         | Annual Enterprise Survey 2024 |
| **Region**               | New Zealand                   |
| **Rows**                 | 55,620                        |
| **Columns (Original)**   | 23                            |
| **Columns (Final Used)** | 10                            |
| **Target Variable**      | `Value`                       |
| **Year**                 | 2024                          |

---

## 🧾 Key Features

| Feature                       | Description                     |
| ----------------------------- | ------------------------------- |
| `Industry_name_NZSIOC`        | Industry classification name    |
| `Industry_aggregation_NZSIOC` | Industry grouping level         |
| `Industry_code_NZSIOC`        | Industry code                   |
| `Units`                       | Dollars / Millions / Percentage |
| `Variable_name`               | Financial metric name           |
| `Variable_category`           | Performance / Position / Ratios |
| `Value`                       | Recorded financial value        |
| `Year`                        | Survey year                     |

---

## 🎯 Objectives

The primary goals of this project are:

* Understand financial value distribution
* Compare industries statistically
* Detect significant group differences
* Identify skewness and outliers
* Present insights visually

---

## 🧹 Data Cleaning & Preparation

| Step               | Action                 |
| ------------------ | ---------------------- |
| Missing Values     | Mean / Mode imputation |
| Null-heavy Columns | Removed                |
| Duplicate Rows     | Checked (none found)   |
| Data Types         | Corrected              |
| Text Fields        | Lowercased & cleaned   |

---

## 📈 Exploratory Data Analysis

### Numerical Variable: `Value`

| Metric       | Observation                   |
| ------------ | ----------------------------- |
| Distribution | Right-skewed                  |
| Variability  | High                          |
| Outliers     | Significant positive outliers |
| Scale        | Highly dispersed              |

### Categorical Variables

| Feature           | Unique Categories |
| ----------------- | ----------------- |
| Industry Name     | 117               |
| Variable Name     | 40                |
| Units             | 3                 |
| Aggregation Level | 3                 |

---

## 📊 Statistical Testing (One-Way ANOVA)

To test whether group means differ significantly:

| Comparison                    | F-Statistic | p-value | Result             |
| ----------------------------- | ----------- | ------- | ------------------ |
| Value vs Industry Aggregation | 41.43       | <0.001  | Significant        |
| Value vs Industry Code        | 5.66        | <0.001  | Significant        |
| Value vs Industry Name        | 6.64        | <0.001  | Significant        |
| Value vs Units                | 1887.23     | <0.001  | Highly Significant |
| Value vs Variable Code        | 69.67       | <0.001  | Significant        |

> All tested categorical variables showed statistically significant differences in `Value`.

---

## 🏆 Top Industries by Mean Value

| Rank | Industry                               | Mean Value |
| ---- | -------------------------------------- | ---------- |
| 1    | Petroleum & Coal Product Manufacturing | 37,547.48  |
| 2    | Primary Metal Manufacturing            | 20,333.45  |
| 3    | Beverage & Tobacco Manufacturing       | 15,308.51  |
| 4    | Transport Equipment Manufacturing      | 9,197.21   |
| 5    | Printing                               | 4,909.65   |

---

## 💡 Key Insights

✅ Financial values are heavily concentrated among a few industries.
✅ Manufacturing sectors dominate high-value reporting.
✅ Units of measurement strongly impact scale interpretation.
✅ Dataset contains substantial skewness and extreme values.
✅ Statistical evidence confirms real differences across groups.

---

## ⚠️ Limitations

* Only one year analyzed
* Provisional dataset may change
* Strong skewness affects raw comparisons
* Large category counts reduce readability

---

## 🚀 Future Enhancements

* Multi-year trend analysis
* Predictive modeling
* Industry clustering
* Dashboard development (Streamlit / Power BI)
* Outlier case investigation

---

## ⚙️ Installation

```bash
pip install pandas numpy scipy seaborn matplotlib jupyter
```

---

## ▶️ Run the Notebook

```bash
git clone https://github.com/your-username/Annual-Enterprise-Survey-EDA.git
cd Annual-Enterprise-Survey-EDA
jupyter notebook Annual_EnterPriese_survey.ipynb
```

---

## 🛠️ Tech Stack

| Tool       | Purpose              |
| ---------- | -------------------- |
| Python     | Core programming     |
| Pandas     | Data manipulation    |
| NumPy      | Numerical operations |
| SciPy      | Statistical testing  |
| Matplotlib | Visualization        |
| Seaborn    | Statistical plots    |
| Jupyter    | Interactive analysis |

---

## 📄 License

Licensed under the **MIT License**.

---

## 👤 Author

**Junaid Ahmed Rupok**

📅 Analysis Date: April 29, 2026
🔗 GitHub: https://github.com/Junaid-Ahmed-Rupok

---

## 🤝 Contributing

Contributions, ideas, and improvements are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push branch
5. Open Pull Request

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star.

**Made with Python, Statistics, and Curiosity**

</div>
```
