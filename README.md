# California Housing Exploratory Data Analysis

This project performs an **exploratory data analysis (EDA)** of the California Housing dataset, which contains information about housing prices in various districts of California.

Using **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**, the analysis focuses on understanding the dataset's characteristics, identifying relationships between features, and uncovering insights for predicting housing values. Key steps included data loading and initial exploration, univariate and bivariate analysis, feature engineering, and correlation analysis.

## The key findings are:

*   **Data Overview:** The dataset contains 20,640 entries with no missing values. All features are numerical (float64 data type).
*   **Potential Outliers:** Initial descriptive statistics and visualizations (e.g., box plots for MedInc, AveRooms, AveBedrms, Population, and AveOccup) indicated the presence of potential outliers with significantly high values in these features.

![Median Income](https://github.com/larisanti/california-housing-eda/blob/main/images/1-median-income.png)


*   **Feature Distributions:**
    *   `MedInc` (Median Income) and `MedHouseVal` (Median House Value) distributions are skewed right, with the majority of block groups having lower to middle values. A notable peak in `MedHouseVal` at the maximum value suggests potential capping of higher values.
    *   `AveRooms` and `AveBedrms` distributions are also skewed right, with most block groups having a small average number of rooms and bedrooms per household.
    *   `Population` and `AveOccup` distributions are heavily skewed right, with most block groups having relatively low populations and average household occupancy.
    *  `HouseAge` distribution shows that most block groups have a mix of older and newer houses, with significant counts in the '25-40' and '40+' age categories after categorization.
    ![House Age - Feature](https://github.com/larisanti/california-housing-eda/blob/main/images/9-house-age-feature.png)


*   **Relationships Between Features:**
    *   There is a **strong positive linear relationship** between `MedInc` and `MedHouseVal`. Block groups with higher median incomes tend to have higher median house values.
![Median Income - Bivariate](https://github.com/larisanti/california-housing-eda/blob/main/images/7-median-income-bivariate.png)

    *   `AveRooms` shows a positive but weaker relationship with `MedHouseVal` compared to `MedInc`.
    *   Geographical location (`Latitude` and `Longitude`) also shows notable linear correlations with `MedHouseVal`, indicating that location is an important factor.
    *   `Population` and `AveOccup` have very weak linear correlations with `MedHouseVal`.


*   **Feature Engineering:**
    *   Creating `HouseAgeCategory` helps in understanding the distribution of housing age in discrete groups.
    *   Engineering `MedIncPerPersonEstimate` and `BedrmsPerPerson` provides per-capita perspectives on income and living space, which could potentially be more informative predictors than the aggregate metrics.
![Bedrooms - Feature](https://github.com/larisanti/california-housing-eda/blob/main/images/11-bedrooms-feature.png)


*   **Overall Correlation:** The correlation heatmap confirms that `MedInc`, `Latitude`, and `Longitude` are the features most strongly linearly correlated with `MedHouseVal`.
![Correlation Matrix](https://github.com/larisanti/california-housing-eda/blob/main/images/12-correlation-matrix.png)

---

## To visualize the complete analysis, including all plots and code, refer to the **Jupyter Notebook** file: [california\_housing\_eda.ipynb](https://github.com/larisanti/california-housing-eda/blob/main/california_housing_eda.ipynb)
