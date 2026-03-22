# Linear Regression

## Objective
The objective of this task was to implement and understand both simple and multiple linear regression models. This involved hands-on experience with data preprocessing, model training, evaluation, and interpretation using Python libraries.

## Tools Used
* **Scikit-learn:** For implementing linear regression models, splitting data, and evaluation metrics.
* **Pandas:** For data loading, manipulation, and preprocessing.
* **Matplotlib:** For data visualization, especially plotting the actual vs. predicted values.
* **NumPy:** Implicitly used by Pandas and Scikit-learn, often explicitly imported for numerical operations.

## Dataset
The dataset used for this task is the **House Price Prediction Dataset**, which was suggested for this task. This dataset contains various features related to houses and their corresponding sale prices, making it suitable for a regression task.

## Steps Performed

1.  **Data Loading and Initial Exploration:**
    * The `house_price_prediction.csv` dataset was loaded into a Pandas DataFrame.
    * Initial exploration included checking the first few rows (`df.head()`), reviewing data types and non-null counts (`df.info()`), and generating descriptive statistics (`df.describe()`).

2.  **Data Preprocessing:**
    * Missing values in numerical columns were handled by filling them with the mean of their respective columns to maintain data integrity.
    * Features (all columns except the target) and the target variable (e.g., 'Price' or 'SalePrice') were separated into `X` and `y` respectively.

3.  **Data Splitting:**
    * The dataset was split into training and testing sets using `train_test_split` from `sklearn.model_selection`. A test size of 20% and a `random_state` were used to ensure reproducibility.

4.  **Model Training (Multiple Linear Regression):**
    * A `LinearRegression` model from `sklearn.linear_model` was initialized and trained on the `X_train` and `y_train` data.

5.  **Model Evaluation:**
    * Predictions (`y_pred`) were made on the test set (`X_test`).
    * The model's performance was evaluated using the following metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), and $R^{2}$ score.
        * **Mean Absolute Error (MAE):** The average magnitude of the errors in a set of predictions, without considering their direction.
        * **Mean Squared Error (MSE):** The average of the squares of the errors. It gives higher weight to larger errors.
        * **Root Mean Squared Error (RMSE):** The square root of the MSE, representing the standard deviation of the residuals.
        * **R-squared ($R^{2}$) Score:** A statistical measure that represents the proportion of the variance for a dependent variable that's explained by independent variables in a regression model.

6.  **Visualization (Actual vs. Predicted Prices):**
    * A scatter plot was generated to visualize the relationship between the actual house prices (`y_test`) and the predicted house prices (`y_pred`).
    * A diagonal line (`y=x`) was added to the plot. This line represents the ideal scenario where predicted values exactly match actual values. Points closer to this line indicate higher accuracy of the model.

## What I Learned
* Gained practical experience in implementing simple and multiple linear regression models.
* Understood the importance of data preprocessing steps.
* Learned how to split data effectively for training and testing machine learning models.
* Deepened understanding of key regression evaluation metrics and their interpretation.
* Practiced visualizing model performance through actual vs. predicted plots.
* Learned about regression modeling, evaluation metrics, and model interpretation.
