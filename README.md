# 📊 Annual Enterprise Survey 2024 — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

**Financial Performance Analysis of New Zealand Enterprises**  
*Uncovering patterns in enterprise financial data through statistical testing and visualization*

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Dataset Summary](#-dataset-summary)
- [Key Features](#-key-features)
- [Project Objectives](#-project-objectives)
- [Data Cleaning](#-data-cleaning--preparation)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Statistical Testing](#-statistical-testing)
- [Top Industries](#-top-industries-by-mean-value)
- [Key Insights](#-key-insights)
- [Limitations](#-limitations)
- [Future Enhancements](#-future-enhancements)
- [Installation & Usage](#-installation--usage)
- [Tech Stack](#-tech-stack)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 📋 Overview

This project presents a **comprehensive exploratory data analysis (EDA)** of the **Annual Enterprise Survey: 2024 Financial Year (Provisional)** dataset from New Zealand. The analysis leverages statistical testing (ANOVA), data visualization, and rigorous data cleaning to uncover how financial values vary across:

- 🏭 **Industries** (117 categories)
- 📊 **Financial Variables** (40 metrics)
- 📐 **Units of Measurement** (dollars, millions, percentages)
- 🏷️ **Industry Aggregation Levels** (Levels 1, 3, 4)

### Quick Stats

| Metric | Value |
|--------|-------|
| **Total Records** | 55,620 |
| **Industries Analyzed** | 117 |
| **Financial Variables** | 40 |
| **Measurement Units** | 3 |
| **Rows (Original)** | 23 columns |
| **Rows (Cleaned)** | 10 columns |

---

## 📊 Dataset Summary

| Attribute | Details |
|-----------|---------|
| **Dataset Name** | Annual Enterprise Survey 2024 |
| **Region** | New Zealand 🌏 |
| **Total Rows** | 55,620 |
| **Columns (Original)** | 23 |
| **Columns (Final)** | 10 |
| **Target Variable** | `Value` |
| **Year** | 2024 (Provisional) |
| **Data Status** | Ready for Analysis ✅ |

---

## 🧾 Key Features

| Feature | Description | Unique Values |
|---------|-------------|----------------|
| `Industry_name_NZSIOC` | Industry classification name | 117 |
| `Industry_aggregation_NZSIOC` | Industry grouping level (1, 3, 4) | 3 |
| `Industry_code_NZSIOC` | Industry classification code | 139 |
| `Industry_code_ANZSIC06` | ANZSIC06 industry code | 119 |
| `Units` | Dollars / Millions / Percentage | 3 |
| `Variable_name` | Financial metric name | 40 |
| `Variable_code` | Financial metric code | 39 |
| `Variable_category` | Performance / Position / Ratios | 3 |
| **`Value`** | 🎯 **Recorded financial value** | Continuous |
| `Year` | Survey reference year | — |

---

## 🎯 Project Objectives

Our analysis aims to achieve the following goals:

### 1. Understand Value Distribution
- Create histograms and box plots to visualize data spread
- Analyze skewness and kurtosis
- Identify distribution patterns

### 2. Compare Industries Statistically
- Perform One-way ANOVA testing across industry groups
- Test significance at α = 0.05 level
- Validate group differences

### 3. Detect Significant Differences
- Calculate p-values for all comparisons
- Identify meaningful group distinctions
- Validate statistical significance

### 4. Identify Outliers & Anomalies
- Detect extreme values using log-scaled box plots
- Calculate coefficient of variation (CV)
- Flag unusual data patterns

### 5. Present Insights Visually
- Create professional Seaborn visualizations
- Develop Matplotlib charts
- Generate comprehensive data summaries

---

## 🧹 Data Cleaning & Preparation

Our data underwent a rigorous 5-step cleaning process:

### Step 1: Handle Missing Values
- Applied mean/mode imputation for missing data
- Preserved data integrity and distribution
- Documented imputation decisions

### Step 2: Remove Null Columns
- Identified columns with ≥50% null values
- Removed redundant or incomplete features
- Retained data richness

### Step 3: Check for Duplicates
- Scanned for duplicate records
- No duplicates found (0 removed)
- Verified data uniqueness

### Step 4: Standardize Data Types
- Corrected inconsistent data types
- Ensured type consistency across columns
- Optimized memory usage

### Step 5: Clean Text Data
- Lowercased all text fields
- Stripped leading/trailing whitespace
- Standardized formatting

**Result:** Clean, analysis-ready dataset with 55,620 records and 10 key features ✅

---

## 📈 Exploratory Data Analysis

### Numerical Variable Analysis: `Value`

| Characteristic | Finding |
|---|---|
| **Distribution** | Right-skewed 📈 |
| **Variability** | High (CV > 1) — substantial spread |
| **Outliers** | Significant positive outliers present |
| **Scale** | Highly dispersed across different units |
| **Concentration** | Values concentrated in specific industries |

### Categorical Variables Overview

```
Industry Name     ████████████████████████ 117 unique
Variable Name     ████████ 40 unique
Units             ██ 3 unique
Aggregation Level ██ 3 unique
```

### Key Observations

- **Right-skewed distribution** indicates most values cluster at lower end with long tail of high values
- **High coefficient of variation** suggests diverse financial performance across enterprises
- **Unit-specific patterns** emerge when segmenting by measurement type
- **Industry variation** shows clear differences between sectors

---

## 📊 Statistical Testing

### Methodology
- **Test Type:** One-Way ANOVA (Analysis of Variance)
- **Significance Level:** α = 0.05
- **Notation:** ★★★ = p < 0.001 (Highly Significant)

### Test Results

| Comparison | F-Statistic | p-value | Significance |
|-----------|------------|---------|--------------|
| Value vs Industry Aggregation | **41.43** | < 0.001 | ★★★ Highly Significant |
| Value vs Industry Code | **5.66** | < 0.001 | ★★★ Highly Significant |
| Value vs Industry Name | **6.64** | < 0.001 | ★★★ Highly Significant |
| Value vs Units | **1,887.23** | < 0.001 | ★★★ Highly Significant |
| Value vs Variable Code | **69.67** | < 0.001 | ★★★ Highly Significant |

### Conclusion

✅ **All tested categorical variables showed statistically significant differences in financial values (p < 0.001).**

This provides strong evidence that:
- Industry classification impacts financial metrics
- Measurement units significantly affect value scales
- Variable types create meaningful distinctions
- Group differences are real and measurable

---

## 🏆 Top Industries by Mean Value

Ranking of industries by average financial value:

| Rank | Industry | Mean Value | Sector |
|------|----------|-----------|--------|
| 🥇 **1st** | Petroleum & Coal Product Manufacturing | **$37,547.48** | Manufacturing |
| 🥈 **2nd** | Primary Metal Manufacturing | **$20,333.45** | Manufacturing |
| 🥉 **3rd** | Beverage & Tobacco Manufacturing | **$15,308.51** | Manufacturing |
| **4th** | Transport Equipment Manufacturing | **$9,197.21** | Manufacturing |
| **5th** | Printing | **$4,909.65** | Manufacturing |

### Key Observation
The top 5 industries are dominated by **manufacturing sectors**, particularly resource-intensive and capital-heavy industries. This suggests:
- Manufacturing requires substantial financial investment
- Resource extraction industries report highest values
- Capital intensity correlates with financial metrics

---

## 💡 Key Insights

### 💰 Financial Concentration
Financial values are **heavily concentrated** among a few industries, indicating market dominance and economic inequality across sectors.

### 🏭 Manufacturing Dominance  
**Manufacturing sectors** consistently rank highest in financial metrics, suggesting:
- Capital-intensive operations
- High investment requirements
- Significant economic contribution

### 📐 Units Impact Scale Interpretation
Different **units of measurement** (dollars, millions, percentages) strongly impact scale interpretation, requiring careful normalization and comparison.

### 📈 Substantial Skewness
Dataset contains **significant skewness and extreme values**, affecting:
- Traditional statistical assumptions
- Outlier detection methods
- Comparative analysis approaches

### 🧪 Validated Statistical Significance
All tested categorical variables demonstrate **real, meaningful differences** in financial values, validated through rigorous ANOVA testing with p < 0.001.

### 📊 Distribution Patterns
- **Right-skewed** distribution common across metrics
- **Outliers** primarily on positive (high value) end
- **Coefficient of variation** exceeds 1.0 in most categories

---

## ⚠️ Limitations

### Current Analysis Scope
- ⚠️ **Single Year Only** — Analysis covers 2024 only; multi-year trends not examined
- ⚠️ **Provisional Dataset** — Data may be subject to revision or updates
- ⚠️ **High Skewness** — Extreme skewness affects raw value comparisons
- ⚠️ **Large Category Count** — 117 industries reduce visualization readability
- ⚠️ **Unit Scaling** — Different measurement units complicate direct comparison

### Recommendations for Future Work
- Normalize values by unit type before comparison
- Consider log-transformation for skewed distributions
- Aggregate similar industries for clearer patterns
- Incorporate multiple years for trend analysis

---

## 🚀 Future Enhancements

We plan to expand this analysis with:

- [ ] **Multi-Year Trend Analysis** — Incorporate historical data and identify temporal patterns
- [ ] **Predictive Modeling** — Develop forecasts for enterprise performance metrics
- [ ] **Industry Clustering** — Group similar industries using unsupervised learning
- [ ] **Interactive Dashboard** — Build Streamlit or Power BI visualization tools
- [ ] **Outlier Case Studies** — Deep-dive analysis into extreme value records
- [ ] **Segmentation Analysis** — Identify enterprise size and performance tiers
- [ ] **Correlation Studies** — Analyze relationships between financial variables
- [ ] **Benchmarking** — Compare against historical baselines and sector averages

---

## ⚙️ Installation & Usage

### Prerequisites

Ensure you have Python 3.x installed with the following packages:

```bash
pip install pandas numpy scipy seaborn matplotlib jupyter
```

### Quick Start

1. **Clone the Repository**
```bash
git clone https://github.com/Junaid-Ahmed-Rupok/Annual-Enterprise-Survey-EDA.git
cd Annual-Enterprise-Survey-EDA
```

2. **Install Dependencies**
```bash
pip install -r requirements.txt
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook Annual_EnterPriese_survey.ipynb
```

4. **Run Analysis**
- Open the notebook in your browser
- Execute cells sequentially
- Review visualizations and statistical outputs

### Dataset Access

The dataset is included in the repository:
```
📊 annual-enterprise-survey-2024-...csv
```

---

## 🛠️ Tech Stack

| Tool | Purpose | Version |
|------|---------|---------|
| **Python** | Core programming language | 3.x |
| **Pandas** | Data manipulation & analysis | Latest |
| **NumPy** | Numerical operations & arrays | Latest |
| **SciPy** | Statistical testing & functions | Latest |
| **Matplotlib** | Data visualization & plotting | Latest |
| **Seaborn** | Statistical graphics & plots | Latest |
| **Jupyter** | Interactive notebook environment | Latest |

### Why These Tools?

- **Pandas** — Powerful for data cleaning and transformation
- **NumPy** — Efficient numerical computations
- **SciPy** — Advanced statistical testing (ANOVA, etc.)
- **Matplotlib/Seaborn** — Professional visualizations
- **Jupyter** — Interactive and reproducible analysis

---

## 📂 Project Structure

```
📦 Annual-Enterprise-Survey-EDA
│
├── 📓 Annual_EnterPriese_survey.ipynb    # Main analysis notebook
├── 📄 README.md                          # Project documentation
├── 📜 LICENSE                            # MIT License
├── 📊 annual-enterprise-survey-2024.csv  # Dataset
└── 📋 requirements.txt                   # Python dependencies
```

---

## 🤝 Contributing

We welcome contributions! Here's how to contribute:

1. **Fork** the repository
2. Create a **feature branch** 
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit** your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push** to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a **Pull Request**

### Areas for Contribution
- Additional statistical analyses
- Enhanced visualizations
- Documentation improvements
- Bug fixes and optimizations
- New insights and findings

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

**You are free to:**
- Use this project for personal and commercial purposes
- Modify the code
- Distribute the work
- Include it in proprietary applications

**With the conditions:**
- Include the original license
- Include copyright notice
- State significant changes

---

## 👤 Author

**Junaid Ahmed Rupok**

- 📅 **Analysis Date:** April 29, 2026
- 🔗 **GitHub:** [@Junaid-Ahmed-Rupok](https://github.com/Junaid-Ahmed-Rupok)
- 💼 **Focus:** Data Analysis, Statistical Testing, Data Visualization

---

## ⭐ Support

If you found this project useful and learned something from it, please consider:

- ⭐ **Star** this repository to show your appreciation
- 🐛 **Report issues** if you find any bugs
- 💡 **Suggest improvements** for future enhancements
- 🤝 **Share** with others who might benefit

---

## 📞 Questions & Feedback

Have questions or suggestions? Feel free to:
- Open an issue on GitHub
- Contact the author directly
- Suggest improvements via pull requests

---

<div align="center">

**Made with ❤️, Python, Statistics, and endless curiosity**

*Transforming data into insights, one analysis at a time.*

</div>
