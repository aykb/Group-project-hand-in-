This notebook addresses Challenge 3 which focuses on building a machine learning model to predict daily energy consumption for smart-city buildings and evaluating its fairness across different building groups.

Goals:
Predict daily_grid_import_kwh using calendar features and simple lag features for each building.
Compare linear and non-linear models.
Evaluate the fairness of prediction errors across building types and and locations.
Key Steps:
Load the Daily Energy Dataset: The energy_daily_features.csv dataset (generated in Challenge 1) is loaded and inspected.
Feature Engineering:
Calendar features (day_of_week, month, is_weekend) are extracted from the date column.
Lag features (lag1, lag7) representing previous days' energy consumption are created per building.
Rows with missing lag features are dropped.
Train/Test Split: The data is split into training (80%) and testing (20%) sets. Features include calendar and lag features, as well as one-hot encoded building_type and location.
Baseline Model & Evaluation (Linear Regression):
A LinearRegression model is trained.
Its performance is evaluated using RMSE and R² score.
A plot of predicted vs actual values is generated.
Non-linear Model & Feature Importance (Random Forest):
A RandomForestRegressor model is trained.
Its RMSE and R² score are compared to the linear model.
Feature importances from the Random Forest model are displayed for interpretability.
Fairness of Prediction Errors across Building Groups:
A test_results DataFrame is created to store true values, predictions, and absolute errors for both models.
Mean Absolute Error (MAE) is computed for both models, grouped by building_type and location, to identify systematic errors.
Short Discussion: A markdown cell discusses model performance, feature importance, fairness findings, and potential strategies for fairer energy management policies.
Optional – Design a simple regression fairness metric: (Not yet implemented) This optional section suggests defining a custom fairness metric for regression problems, similar to those in AIF360, and applying it to the models.
