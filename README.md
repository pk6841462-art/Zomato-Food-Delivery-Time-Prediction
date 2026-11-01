# Zomato Food Delivery Time Prediction

A Machine Learning project that predicts food delivery time based on factors such as delivery distance, traffic conditions, weather, delivery partner ratings, and vehicle conditions.

The project uses historical food delivery data to build and evaluate predictive models, with Random Forest Regressor selected as the final model.
## Objectives

* Analyze food delivery data to identify important patterns.
* Perform data cleaning and exploratory data analysis.
* Engineer relevant features for prediction.
* Build and optimize Machine Learning models.
* Evaluate model performance.
* Understand feature contributions using SHAP explainability.
## Dataset

* **Records:** 45,584
* **Original Features:** 20
* **Target Variable:** `Time_taken (min)`
* **Task:** Regression

The dataset contains information about delivery partners, order details, weather, traffic, vehicle conditions, and geographical coordinates.
## Technologies Used

* **Python** – Programming language
* **Pandas & NumPy** – Data manipulation
* **Matplotlib & Seaborn** – Data visualization
* **Scikit-learn** – Machine Learning and model evaluation
* **SHAP** – Model explainability
* **Joblib** – Model saving
* **Jupyter Notebook** – Development environment
## Data Preprocessing

* Handled missing values and checked duplicate records.
* Converted date and time information into numerical features.
* Calculated delivery distance using the Haversine formula.
* Removed unnecessary identifier columns.
* Applied One-Hot Encoding to categorical features.
* Used StandardScaler for numerical feature scaling.
* Split the dataset into 80% training and 20% testing data.
## Exploratory Data Analysis (EDA)

Performed data analysis and visualization to understand delivery time patterns and relationships between delivery time and factors such as distance, traffic, weather, ratings, vehicle conditions, and multiple deliveries.
## Feature Engineering

Created additional features, including delivery distance using geographical coordinates and numerical representations of order date and time, to improve the model's predictive capability.
##Model Development

Implemented Linear Regression and Random Forest Regressor models. Used RandomizedSearchCV for hyperparameter tuning and selected the optimized Random Forest model.

Model Performance
Metric	Linear Regression	Tuned Random Forest
MAE	4.80 min	3.21 min
RMSE	6.05 min	4.08 min
R² Score	0.5848	0.8115

The tuned Random Forest model achieved an R² score of 81.15% with a Mean Absolute Error of approximately 3.21 minutes.

Cross-Validation

Performed 5-fold cross-validation to evaluate model consistency.

Average CV MAE: 3.23 minutes
Standard Deviation: 0.0322
Model Explainability

Used SHAP (SHapley Additive exPlanations) to understand feature contributions and explain individual model predictions.

Future Improvements
Develop an interactive prediction interface using Streamlit.
Explore advanced regression algorithms.
Improve prediction accuracy using additional delivery-related features.
