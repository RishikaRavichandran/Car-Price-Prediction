# Car-Price-Prediction

## Overview

This project involves analyzing a dataset of car sales to understand factors influencing selling prices. It includes data cleaning, preprocessing, visualization, and a feasibility study for machine learning models.

## Dataset

- **Rows**: 8128
- **Columns**: 12
- **Features**:
  - Categorical: `fuel`, `seller_type`, `transmission`, `owner`
  - Numerical: `year`, `selling_price`, `km_driven`, `mileage`, `engine`, `seats`, `max_power`
  - Derived Feature: `car_age` (calculated from `year`)

## Data Preprocessing

- **Handling Missing Values**:
  - `mileage`, `engine`, `seats`, and `max_power` had missing values.
  - `max_power` (mixed data type) was first replaced by mode, converted to numeric, and then missing values were filled with the median.
- **Encoding**:
  - Categorical features were label-encoded.
- **Feature Engineering**:
  - `car_age` was derived to enhance visualization and analysis.

## Data Visualization Insights

- **Price Trends**:
  - Selling prices are skewed to the right, with most cars priced lower and a few expensive outliers.
  - Newer cars tend to have higher prices.
  - Car prices decrease as the car's age increases.
  - Prices initially remain stable with increasing kilometers driven but drop after a threshold.
  - Higher mileage generally leads to lower prices, with some exceptions.
- **Feature Correlations**:
  - Moderate positive correlation between `year` and `selling_price`.
  - `engine` and `max_power` show a moderate positive correlation with `selling_price`.
  - Diesel cars tend to have higher prices than petrol, LPG, or CNG cars.
  - Automatic cars are priced higher than manual ones.
  - First-owner cars have higher prices than second-owner ones.

## Machine Learning Feasibility

- **Problem Type**: Regression
  - Target variable: `selling_price`
  - Regression models such as Linear Regression and others can be used.
- **Supervised Learning**:
  - The dataset contains labeled data, where input features are used to train models for predicting selling prices.

## Files in Repository

- `Analysis Report.docx`: Detailed documentation of analysis and insights.
- `Dataset Analysis.ipynb`: Jupyter Notebook containing data processing, visualization, and modeling.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/RishikaRavichandran/Car-Price-Prediction.git
   ```
2. [Open](https://github.com/your-repo.gitOpen) `Dataset Analysis.ipynb` in Jupyter Notebook.
3. Run the notebook to explore the analysis and model predictions.

## License

This project is open-source and available under the MIT License.

