# California Housing Exploratory Data Analysis

This project performs an **exploratory data analysis (EDA)** of the California Housing dataset, which contains information about housing prices in various districts of California.

Using **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**, the analysis focuses on understanding the dataset's characteristics, identifying relationships between features, and uncovering insights for predicting housing values. Key steps included data loading and initial exploration, univariate and bivariate analysis, feature engineering, and correlation analysis.

The key findings are:

* **Median Income (MedInc):** Shows a strong positive linear correlation with Median House Value (MedHouseVal). This suggests that areas with higher median incomes tend to have higher median house values.
* **Geographical Location (Latitude and Longitude):** Also exhibits a notable linear relationship with MedHouseVal, indicating that location significantly influences housing prices.
* **Average Rooms (AveRooms) and House Age (HouseAge):** Have weaker linear relationships with MedHouseVal compared to income and location.
* **Population and Average Occupancy (Population and AveOccup):** Show very little linear correlation with MedHouseVal, suggesting a minimal linear impact on median house value in this dataset.

---

To visualize the complete analysis, including all plots and code, refer to the **Jupyter Notebook** file:

[california\_housing\_eda.ipynb](https://github.com/larisanti/california-housing-eda/blob/main/california_housing_eda.ipynb)
