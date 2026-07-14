# Python-Case-Study
# Automobile Data Analysis & Statistical Modeling Case Study

This repository contains a comprehensive data analysis case study conducted in Python using a Google Colab notebook environment. The project spans across Exploratory Data Analysis (EDA), data visualization, hypothesis testing ($t$-test), and probability modeling using statistical distributions.

## 📊 Dataset Overview
The analysis is performed on a custom dataset (`CarFeatures.csv`) consisting of 25 unique car observations and 18 specifications, bridging both categorical attributes and continuous performance metrics.

Key features include:
* **Categorical:** `Make`, `Fuel Type`, `Aspiration`, `Number of Doors`, `Body Style`, `Number of Cylinders`, etc.
* **Numerical:** `Wheel Base`, `Curb Weight`, `Engine Size`, `Horsepower`, `City MPG`, `Highway MPG`, `Price`.

---

## 🚀 Key Analysis & Features

### 1. Exploratory Data Analysis (EDA) & Visualization
* **Univariate Analysis:** Generated distribution plots (`sns.histplot`/`kde`) and horizontal box plots to analyze continuous numerical spreads and detect potential outliers.
* **Categorical Plotting:** Created customized, colorful `sns.countplot` visualizations utilizing distinct palettes mapping out frequency spreads (e.g., `Body Style`, `Make`).
* **Correlation & Pairwise Relationships:** Visualized feature interactions and multicollinearity matrices via annotated Seaborn heatmaps (`sns.heatmap`) and relational pairplots (`sns.pairplot`).

### 2. Descriptive & Aggregation Insights
* Segmented average pricing structures by car manufacturer (`Make`) to isolate the costliest brand (**Chevrolet** at \$40,450.00) and the cheapest brand (**Ford** at \$8,246.50).
* Compared average pricing between regular and alternative fuel networks, demonstrating that **Gas** vehicles held a higher mean baseline over **Diesel** variations in this specific sample pool.
* Constructed descriptive contingency tables/cross-tabulations (`pd.crosstab`) cross-referencing brand configurations against categorical metrics like `Body Style` and `Number of Cylinders`.

### 3. Hypothesis Testing ($t$-Test)
Conducted an **Independent Two-Sample $t$-Test** to mathematically confirm if the price difference between Gas cars ($\mu_{\text{Gas}}$) and Diesel cars ($\mu_{\text{Diesel}}$) was statistically significant:
* **Null Hypothesis ($H_0$):** $\mu_{\text{Gas}} - \mu_{\text{Diesel}} = 0$ (No significant difference in average price)
* **Alternative Hypothesis ($H_1$):** $\mu_{\text{Gas}} - \mu_{\text{Diesel}} \neq 0$ (A significant difference exists)
* **Result:** Calculated a $p$-value of `0.2728`. Since $p > 0.05$, the study **failed to reject the null hypothesis**, indicating no statistically significant price disparity given the sample size.

### 4. Advanced Probability & Sampling Distributions
* **Conditional Probability:** Leveraged categorical multi-indexing frameworks to calculate conditional outcomes (e.g., assessing the exact odds of a randomly selected 8-cylinder vehicle belonging to a specific manufacturer).
* **Hypergeometric Sampling Logic:** Modeled probability scenarios involving finite population sampling without replacement using `scipy.stats.hypergeom` (e.g., surveying a subset group to isolate specific mechanical traits like `Turbo` engine aspiration).

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Environment:** Jupyter Notebook / Google Colab
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Operations:** `scipy.stats` (specifically `ttest_ind`, `hypergeom`, and `binom`)

---

## 📁 Repository Structure
```text
├── Data/
│   └── CarFeatures.csv             # Raw structured dataset used for the case study
├── Python_Case_Study.ipynb         # Complete executed Google Colab source code
└── README.md                       # Documentation overview
