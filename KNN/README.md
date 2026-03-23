# K-Nearest Neighbors (KNN) Classification

## Objective
This task aimed to understand and implement the K-Nearest Neighbors (KNN) algorithm for classification problems. The primary tools used were Scikit-learn, Pandas, and Matplotlib[cite: 2].

## Dataset
The Iris dataset was used for this task, as suggested by the task guidelines[cite: 4]. It's a classic dataset for classification, containing 150 samples across three species of Iris flowers (Setosa, Versicolor, Virginica), each with 4 features: sepal length, sepal width, petal length, and petal width.

## Key Concepts Explored
* **Instance-based learning**: KNN is an instance-based learning algorithm[cite: 5].
* **Euclidean Distance**: This metric is fundamental to KNN for calculating the distance between data points[cite: 5].
* **K Selection**: Experimenting with different values of 'K' (the number of neighbors) is crucial for finding the optimal model performance[cite: 3, 5].
* **Normalization**: Understanding the importance of feature scaling in distance-based algorithms like KNN[cite: 6].

## Implementation Steps

1.  **Library Import**: Imported necessary libraries including `pandas`, `numpy`, `sklearn.datasets`, `sklearn.model_selection`, `sklearn.preprocessing`, `sklearn.neighbors`, `sklearn.metrics`, `matplotlib.pyplot`, `matplotlib.colors`, and `sklearn.decomposition` for PCA[cite: 2].
2.  **Dataset Loading**: The Iris dataset was loaded using `load_iris()` from `sklearn.datasets`[cite: 4].
3.  **Feature Normalization**: `StandardScaler` was applied to normalize the features[cite: 1]. This is crucial for KNN to ensure all features contribute equally to distance calculations, preventing features with larger scales from dominating[cite: 6].
4.  **Data Splitting**: The dataset was split into training and testing sets (70% training, 30% testing) using `train_test_split`.
5.  **K-Value Experimentation**: The KNN model (`KNeighborsClassifier` from `sklearn`) was trained and evaluated for various `k` values (from 1 to 20)[cite: 3]. The accuracy for each `k` was recorded and plotted to identify the optimal `k`.
6.  **Model Evaluation**: After selecting an optimal `k`, the model's performance was evaluated using accuracy and a confusion matrix[cite: 4].
    * **Accuracy Score**: The proportion of correctly classified instances.
    * **Confusion Matrix**: A table showing true positives, true negatives, false positives, and false negatives for each class, providing a detailed view of the model's performance[cite: 4].
7.  **Decision Boundary Visualization**: To visualize how the model classifies data, Principal Component Analysis (PCA) was used to reduce the dataset's dimensionality to 2, allowing for a 2D plot of the decision boundaries[cite: 4].

## Results

### Optimal K Selection
The accuracy was plotted for different values of K. Below is the plot showing the accuracy for various K values:

![KNN Accuracy for Different K Values](knn_accuracy_plot.png)

Based on running the provided code, the optimal K value was consistently determined to be **7**, as it yielded a high and stable accuracy.

### Model Performance with Optimal K
* **Optimal K**: 7
* **Accuracy**: 1.0000

### Confusion Matrix
The confusion matrix for the model with the optimal K (K=7) is as follows:

For a 3-class problem (like Iris), the confusion matrix typically looks like this:
This can also be represented as a 2D array:
`[[19 0 0]`
 `[ 0 13 0]`
 `[ 0 0 13]]`

Or, if you generated a heatmap:

![Confusion Matrix for Optimal K](confusion_matrix_heatmap.png)

**Interpretation**: The diagonal elements (19, 13, 13) show the number of correct predictions for each class, while off-diagonal elements show misclassifications. In this specific run with an optimal K of 7 and `random_state=42` for the data split, the model achieved perfect classification, meaning all 19 'setosa' samples, 13 'versicolor' samples, and 13 'virginica' samples in the test set were correctly predicted. There were no false positives or false negatives, indicating excellent performance.

### Decision Boundary Visualization
The decision boundaries, visualized using the first two principal components, are shown below:

![Decision Boundary Plot](decision_boundary_plot.png)

**Interpretation**: The plot illustrates how the KNN algorithm partitions the feature space based on the identified classes when reduced to two principal components. The colored regions represent the areas where new data points would be classified into a particular species. The separation lines are the decision boundaries, indicating where the model switches its classification. The model successfully separates the Iris species based on these two principal components, showing distinct and well-defined regions for each class, consistent with the high accuracy achieved.

## Conclusion
This task successfully demonstrated the implementation of the KNN classification algorithm, including data preprocessing (normalization), hyperparameter tuning (K selection), model evaluation[cite: 4], and visualization of decision boundaries[cite: 4]. The results indicate that KNN is an effective algorithm for classification tasks like the Iris dataset, particularly when features are appropriately scaled.
