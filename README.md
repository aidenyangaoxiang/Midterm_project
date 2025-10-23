# 🏘️ Housing Price Analysis

This project analyzes housing price determinants in **Taipei** and **Boston** using hedonic pricing models. The goal is to understand how different structural, environmental, and accessibility-related factors influence property values across these two urban contexts.

---

## 🎯 Research Objectives

- Compare structural attribute premiums (e.g., number of rooms, house age) between Taipei and Boston
- Analyze spatial price variations within Taipei using grid-based fixed effects
- Examine the relationship between accessibility (e.g., distance to jobs, MRT proximity) and housing prices
- Identify other contextual factors that drive differences in housing values

---

## 📦 Datasets

### 🏙️ Taipei Real Estate Data
- Price per unit area
- Age of the house
- Distance to the nearest MRT station
- Number of nearby convenience stores
- Latitude and longitude (location)

### 🏡 Boston Housing Data (UCI Housing Dataset)
- Median value of homes (MEDV)
- Crime rate (CRIM)
- Air pollution index (NOX)
- Distance to employment centers (DIS)
- Number of rooms (RM)
- Age of house
- Pupil-teacher ratio (PTRATIO)
- Percent lower status population (LSTAT)
- Proximity to the Charles River (CHAS)

---

## 🧪 Methodology

This project uses a unified and modular **hedonic regression pipeline** to model housing prices:

### 1. **Data Preprocessing**
- Load Taipei and Boston datasets
- Normalize variables
- Apply log-transformations to prices and distance metrics for linearization

### 2. **Exploratory Data Analysis (EDA)**
- Correlation heatmaps to understand feature interactions
- Scatter plots and histograms for feature distributions
- Partial dependence plots to explore variable-price relationships

### 3. **Regression Modeling**
- Use **Ordinary Least Squares (OLS)** to regress price on housing and location variables
- Fit models for both cities independently
- Evaluate statistical significance and fit metrics (R², RMSE)

### 4. **Fixed Effects in Taipei**
- Divide the Taipei city space into spatial grids
- Include grid-based fixed effects to control for unobserved location heterogeneity

### 5. **Cross-City Comparison**
- Compare coefficient estimates across cities
- Highlight variables that show consistent or divergent effects (e.g., accessibility vs. environmental quality)

---

## 🔍 Code Structure & Workflow

All logic is implemented in the `Midterm_project.ipynb` notebook, with the following structure:

- **Data Loading & Cleaning**
  - `pd.read_csv()` and basic transformations
- **EDA**
  - Seaborn and Matplotlib visualizations
- **Modeling**
  - Statsmodels OLS fitting and summary interpretation
  - Log-linear models for more interpretable elasticities
- **Visualization**
  - Partial dependence plots
  - Grid-fixed effect surface maps (Taipei only)
- **Comparison**
  - Tables of coefficient estimates
  - Insights drawn from regression results

---

## 📈 Sample Insights

- **Taipei**: Distance to MRT stations has a strong negative effect on price; convenience store count has a positive association.
- **Boston**: Air quality (NOX) and socioeconomic status (LSTAT) are significant negative predictors of price; more rooms (RM) significantly increases value.
- Accessibility premiums are more spatially concentrated in Taipei than Boston.

---

## 🧰 Dependencies

- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- statsmodels

---

## ✍️ Run the code

- run the Midterm_project.ipynb step by step
- You can install required packages via:

```bash
pip install -r requirements.txt


