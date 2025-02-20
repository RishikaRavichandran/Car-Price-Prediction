# Car Price Prediction Analysis

## Overview
This project involves analyzing a dataset of car sales to understand factors influencing selling prices. It includes data cleaning, preprocessing, visualization, machine learning modeling, and model evaluation.

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

## Machine Learning Models & Evaluation

### Regression Models:
#### 1. **Linear Regression**
- Mean Squared Error (MSE): 94,596,219,903.38
- R-Squared (R²): 0.5687
- Mean Absolute Error (MAE): 173,245.83

#### 2. **Decision Tree Regressor**
- MSE: 0.1313
- R-Squared (R²): 0.4747
- MAE: 0.1313

#### 3. **Random Forest Regressor** (Best Performing Model)
- MSE: 18,248,431,290.39
- R-Squared (R²): 0.9168
- MAE: 77,372.33

### Classification Models:
#### 1. **Logistic Regression**
- Accuracy: 86.36%
- Precision: 86.94%
- Recall: 85.82%
- F1-Score: 86.37%

#### 2. **Decision Tree Classifier**
- Training Accuracy: 90.94%
- Testing Accuracy: 86.87%
- Precision: 86.24%
- Recall: 87.97%
- F1-Score: 87.09%

### Model Selection:
- **Best Regression Model:** Random Forest Regressor due to higher R² and lower MSE.
- **Best Classification Model:** Logistic Regression for simplicity and generalization.

## Feature Importance Insights
- **Linear Regression**
  - Most influential features: `max_power`, `year`, `engine`
  - Negative influence: `transmission`, `km_driven`, `owner`
  - Newer cars with higher power and engine capacity have higher prices.
  - Cars with manual transmission, higher number of owners, and certain fuel types tend to have lower prices.

- **Random Forest & Decision Tree**
  - Random Forest outperforms Decision Tree due to reduced overfitting.
  - Feature importance follows similar trends but is more refined in Random Forest.

## Files in Repository
- `Analysis Report.docx`: Detailed documentation of analysis and insights.
- `Analysis Report Week - 2.docx`: Model evaluation and feature importance insights.
- `Dataset Analysis.ipynb`: Jupyter Notebook containing data processing, visualization, and modeling.
- `Task 2.ipynb`: Model implementation and evaluation.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/RishikaRavichandran/Car-Price-Prediction.git
   ```
2. Open `Dataset Analysis.ipynb` and `Task 2.ipynb` in Jupyter Notebook.
3. Run the notebooks to explore the analysis, visualization, and model predictions.


## License

This project is open-source and available under the MIT License.

