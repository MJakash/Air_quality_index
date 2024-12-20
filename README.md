
Description of the Process
Data Loading and Initial Exploration:

The dataset was loaded using pandas from an Excel file named AirQualityUCI.xlsx.
Missing values in the dataset were checked. Additionally, any occurrences of the placeholder value -200 (indicating missing or invalid data) were replaced with NaN.
Handling Missing Data:

Numeric columns were identified, and missing values were imputed by replacing them with the respective column means.
Data Cleaning:

Non-relevant columns like Date and Time were removed to focus on the core features for modeling.
A heatmap of the correlation matrix was generated using seaborn to visualize relationships among features.
Feature Scaling:

The features were standardized using StandardScaler to ensure all variables have a mean of 0 and a standard deviation of 1. This helps the model converge more efficiently.
Train-Validation-Test Split:

The dataset was split into training, validation, and testing sets using an 80-10-10 ratio. This ensures proper evaluation and tuning of the model.
Model Selection and Training:

A Random Forest Regressor was chosen as the model for predicting the target variable CO(GT).
The model was trained on the training set using default hyperparameters.
Model Evaluation:

Predictions were made on both the validation and test sets.
Performance metrics such as Root Mean Squared Error (RMSE) and R-squared values were computed to evaluate the model's accuracy.
Model Performance
Validation Set:

RMSE: 0.5065
R-squared: 0.8526
The model showed good accuracy on the validation set, with low error and a high R-squared value indicating that 85.26% of the variance in the target variable was explained.
Test Set:

RMSE: 0.4828
R-squared: 0.8812
On the unseen test data, the model performed even better, achieving a lower error and explaining 88.12% of the variance in the target variable.
Conclusion
The Random Forest Regressor demonstrated strong predictive capabilities for the CO(GT) target variable. The low RMSE and high R-squared values on both validation and test sets indicate that the model effectively captured the underlying patterns in the data. These results suggest that the model generalizes well to unseen data.
