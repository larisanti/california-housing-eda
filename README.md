# California Housing Exploratory Data Analysis

This project performs an **exploratory data analysis (EDA)** of the California Housing dataset, which contains information about housing prices in various districts of California.

Using Pandas, NumPy, Matplotlib, and Seaborn, the analysis focuses on understanding the dataset's characteristics, identifying relationships between features, and uncovering insights for predicting housing values. Key steps included data loading and initial exploration, univariate and bivariate analysis, feature engineering, and correlation analysis.


##  Data Exploration Workflow

The EDA is structured into five sections for a clear and logical flow:

### 1. Data Loading and Initial Exploration
This section covers the initial steps of loading the California Housing dataset into a pandas DataFrame. It includes displaying the first and last few rows to get a glimpse of the data structure, checking data types and non-null counts using `.info()`, identifying missing values with `.isnull().sum()`, and calculating descriptive statistics using `.describe()` to understand the central tendency, spread, and potential outliers of the numerical features.

---

### 2. Exploring Individual Features (Univariate Analysis)
This section focuses on analyzing each feature independently. Visualizations such as box plots and histograms are used to understand the distribution of individual variables like Median Income, House Age, Average Rooms, Average Bedrooms, Population, Average Occupancy, and Median House Value. This helps in identifying the shape of distributions, potential skewness, and the presence of outliers.

![Univariate Analysis](https://github.com/larisanti/california-housing-eda/blob/main/images/images%20for%20README.md/1-univariate.jpg)

---

### 3. Exploring Relationships Between Features (Bivariate Analysis)
This section investigates the relationships between pairs of features, particularly focusing on how other features relate to the target variable, Median House Value. Scatter plots and KDE plots are used to visualize these relationships, helping to identify potential correlations and dependencies that could be important for predictive modeling. Key relationships explored include Median Income vs. Median House Value and Average Rooms vs. Median House Value.

![Bivariate Analysis](https://github.com/larisanti/california-housing-eda/blob/main/images/images%20for%20README.md/2-bivariate.jpg)

---


### 4. Feature Engineering
This section involves creating new features or transforming existing ones to potentially enhance the dataset's predictive power. Examples include categorizing House Age into distinct groups and creating per-person metrics like Estimated Median Income per Person and Bedrooms per Person by leveraging existing features like Average Occupancy. The distributions of these newly engineered features are also visualized.

![Feature Engineering](https://github.com/larisanti/california-housing-eda/blob/main/images/images%20for%20README.md/3-features.jpg)

---

### 5. Correlation Analysis
This section quantifies the linear relationships between all numerical features in the dataset. A correlation matrix is calculated, and a heatmap is generated to visualize these correlations. This provides a clear overview of which features have strong linear relationships with each other and, importantly, with the target variable, Median House Value. This analysis helps in understanding the degree and direction of linear associations.

![Correlation](https://github.com/larisanti/california-housing-eda/blob/main/images/images%20for%20README.md/4-correlation.jpg)

---

## Key Findings

*   **Data Overview:** The dataset contains 20,640 entries with no missing values. All features are numerical (float64 data type).
*   **Potential Outliers:** Initial descriptive statistics and visualizations (e.g., box plots for MedInc, AveRooms, AveBedrms, Population, and AveOccup) indicated the presence of potential outliers with significantly high values in these features.
*   **Feature Distributions:**
    *   `MedInc` (Median Income) and `MedHouseVal` (Median House Value) distributions are skewed right, with the majority of block groups having lower to middle values. A notable peak in `MedHouseVal` at the maximum value suggests potential capping of higher values.
    *   `HouseAge` distribution shows that most block groups have a mix of older and newer houses, with significant counts in the '25-40' and '40+' age categories after categorization.
    *   `AveRooms` and `AveBedrms` distributions are also skewed right, with most block groups having a small average number of rooms and bedrooms per household.
    *   `Population` and `AveOccup` distributions are heavily skewed right, with most block groups having relatively low populations and average household occupancy.
*   **Relationships Between Features:**
    *   There is a **strong positive linear relationship** between `MedInc` and `MedHouseVal`. Block groups with higher median incomes tend to have higher median house values.
    *   `AveRooms` shows a positive but weaker relationship with `MedHouseVal` compared to `MedInc`.
    *   Geographical location (`Latitude` and `Longitude`) also shows notable linear correlations with `MedHouseVal`, indicating that location is an important factor.
    *   `Population` and `AveOccup` have very weak linear correlations with `MedHouseVal`.
*   **Feature Engineering:**
    *   Creating `HouseAgeCategory` helps in understanding the distribution of housing age in discrete groups.
    *   Engineering `MedIncPerPersonEstimate` and `BedrmsPerPerson` provides per-capita perspectives on income and living space, which could potentially be more informative predictors than the aggregate metrics.
*   **Overall Correlation:** The correlation heatmap confirms that `MedInc`, `Latitude`, and `Longitude` are the features most strongly linearly correlated with `MedHouseVal`.

---
For a complete look at the analysis, including all detailed plots and code, please refer to the Jupyter Notebook file: [california\_housing\_eda.ipynb](https://github.com/larisanti/california-housing-eda/blob/main/california_housing_eda.ipynb)
---
