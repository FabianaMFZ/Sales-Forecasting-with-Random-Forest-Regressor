## Sales Forecasting Project

### Overview
This project focuses on building a machine learning model for accurate sales forecasting. It involves data preprocessing, feature engineering, and exploratory analysis to uncover patterns, by adhering to best practices in time series analysis, such as preserving temporal order in data splits and engineering lag-based features to capture trends and seasonality. By predicting future sales, the model helps businesses optimize inventory, allocate resources efficiently, and plan strategic promotions, ultimately driving revenue growth and improving operational decision-making.

**This project uses Python to:**
  - Explore and preprocess historical sales data.
  - Engineer features to capture temporal patterns and improve model performance.
  - Build, evaluate, and optimize machine learning models.
  - Apply the best model to predict sales for production data.

**Features**
  - Data cleaning and preprocessing.
  - Feature engineering for lag variables, rolling averages, and temporal patterns.
  - Model training using Decision Tree Regressor and Gradient Boosting Regressor.
  - Model evaluation with metrics like RMSE, R², and MAE.
  - Predictions for future sales applied to production data.

### Workflow

**Data Exploration**
  - Cleaned and transformed the dataset.
  - Visualized key trends, such as:
     - Sales distribution per store.
     - Patterns during promotional periods.
     - Monthly trends of average sales across all stores.
  - Analyzed feature correlations to guide feature selection.

**Feature Engineering**
  - Created lag features (e.g., weekly and monthly sales changes) and rolling averages to capture trends and seasonality.
  - Addressed outliers by capping sales values.
  - Evaluated multicollinearity to refine feature selection and reduce noise.

**Model Development**
  - Decision Tree Regressor:
     - Explored tree depths to optimize complexity.
     - Analyzed feature importance to identify key variables.
  - Gradient Boosting Regressor:
     - Used TimeSeriesSplit for cross-validation.
     - Performed hyperparameter tuning using RandomizedSearchCV.
     - Achieved improved performance over the Decision Tree model.

**Production Deployment**
  - Applied the best model to production data.
  - Evaluated performance using RMSE, R², and MAE.
  - Saved predictions alongside actual values for both training and test sets.

### Key Findings
  - Temporal features (e.g., rolling averages, lag values) had the highest predictive power.
  - Proper handling of outliers and time-based splits significantly improved model reliability.
  - Gradient Boosting outperformed the Decision Tree model, achieving lower RMSE and better generalization.

### Results
  - Best Model: Gradient Boosting Regressor.
  - Metrics:
      - RMSE: Significantly lower for Gradient Boosting compared to the Decision Tree.
      - R²: High, indicating strong explanatory power.
      - MAE: Low, reflecting accurate predictions.

### Requirements
    Required libraries:
        pandas
        numpy
        matplotlib
        seaborn
        scikit-learn
        joblib
