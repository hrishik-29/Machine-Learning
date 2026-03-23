# Decision Trees and Random Forests

## Objective
This task focused on understanding and implementing tree-based models (Decision Trees and Random Forests) for classification, including concepts like overfitting, feature importance, and cross-validation.
## Dataset
Heart Disease Dataset (`heart.csv`)

## Tools Used
- Python 3
- Libraries: pandas, scikit-learn, matplotlib, graphviz

## Steps Performed

1.  **Dataset Loading and Initial Inspection:**
    - The `heart.csv` dataset was loaded using pandas.
    - Inspected for missing values and data types. (No significant missing values were found for this dataset.)

2.  **Data Preprocessing:**
    - Categorical features (`sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca`, `thal`) were one-hot encoded to convert them into a numerical format suitable for modeling.

3.  **Data Splitting:**
    - The dataset was split into training (80%) and testing (20%) sets using `train_test_split` to evaluate model generalization.

4.  **Decision Tree Classifier:**
    - A `DecisionTreeClassifier` was trained on the preprocessed training data.
    - Initial training and test accuracies were recorded.

5.  **Decision Tree Visualization:**
    - The trained Decision Tree was visualized using `export_graphviz` and Graphviz, showing the decision rules learned by the model.

6.  **Overfitting Analysis and Tree Depth Control:**
    - The initial Decision Tree showed signs of overfitting (high training accuracy, lower test accuracy).
    - The `max_depth` parameter was experimented with (`max_depth=3, 5, 7, 10`) to find an optimal depth that balanced training and testing performance and mitigated overfitting.

7.  **Random Forest Classifier:**
    - A `RandomForestClassifier` (with 100 estimators) was trained.
    - Its training and test accuracies were calculated.

8.  **Model Comparison and Feature Importance:**
    - The Random Forest's performance was compared to the best-performing Decision Tree. Random Forest generally yielded better generalization.
    - Feature importances from the Random Forest model were extracted and visualized, identifying the most influential features in predicting heart disease.

9.  **Cross-Validation:**
    - 5-fold cross-validation was performed on the Random Forest model to obtain a more robust estimate of its performance across different data partitions.

## Results and Insights
- The initial Decision Tree tended to overfit the training data.
- Limiting `max_depth` improved the generalization of the Decision Tree.
- Random Forests generally provided higher and more stable accuracy compared to a single Decision Tree, effectively reducing overfitting.
- The feature importance analysis revealed which factors (e.g., `cp_1.0`, `thall_fixed`, `oldpeak`, `thalach`) were most indicative of heart disease according to the Random Forest model.
- Cross-validation confirmed the consistent performance of the Random Forest model.
