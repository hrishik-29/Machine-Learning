# Exploratory Data Analysis (EDA)

## Objective

This task focused on performing Exploratory Data Analysis (EDA) to understand the characteristics, patterns, and relationships within the dataset using statistical methods and visualizations. This task builds directly upon the data cleaning and preprocessing completed in Task 1.

## Dataset Used

The **Titanic Dataset** was used for this task, utilizing the cleaned and preprocessed version (`cleaned_titanic_after_task1.csv`) from Task 1.

## Tools Used

* **Python:** The core programming language.
* **Pandas:** For data manipulation and generating summary statistics.
* **NumPy:** For numerical operations.
* **Matplotlib:** For creating static, interactive, and animated visualizations.
* **Seaborn:** A high-level data visualization library based on Matplotlib, used for creating informative and attractive statistical graphics.
* **(Optional) Plotly:** (If you chose to use it) For creating interactive plots.

## Steps Performed

The EDA process involved the following steps:

### 1. Generating Summary Statistics
* Calculated descriptive statistics (mean, median, standard deviation, quartiles, etc.) for all numerical features using `df.describe()`.
* Examined value counts for categorical/binary features (like 'Survived' and 'Sex') to understand their distribution.
* **Inferences Made:** [Write down 2-3 key inferences here, e.g., "Observed the distribution of survivors," "Identified average age/fare values," etc.]

### 2. Creating Histograms and Boxplots for Numeric Features
* Generated **histograms** for numerical features (e.g., Age, Fare, Pclass, SibSp, Parch) to visualize their distributions, skewness, and modality.
* Created **boxplots** for the same numerical features to visualize their central tendency, spread, and to confirm the absence of extreme outliers after Task 1's cleaning.
* **Inferences Made:** [Write down 2-3 key inferences here, e.g., "Noted skewed distributions in 'Fare'," "Confirmed the median values," "Observed the range of data points."]

### 3. Using Correlation Matrix for Feature Relationships
* Generated a **correlation matrix** (heatmap) to quantify and visualize the linear relationships between all numerical features. This helped identify correlated features and potential multicollinearity.
* **(Optional):** If you created any specific scatter plots to visualize relationships, mention them here (e.g., "Additionally, created scatter plots for 'Age' vs 'Fare' colored by 'Survived' to visualize specific relationships.")
* **Inferences Made:** [Write down 2-3 key inferences here, e.g., "Identified a positive correlation between 'SibSp' and 'Parch'," "Noted the relationship between 'Fare' and 'Survived'," "Checked for high correlations between independent variables."]

### 4. Identifying Patterns, Trends, or Anomalies & Making Inferences
* Throughout the EDA process, patterns such as the distribution of age, fare, and survival rates were observed. Trends like how certain features correlate with survival were identified.
* The visualizations helped in making basic feature-level inferences about the data's characteristics.
* **Examples of Patterns/Inferences:**
    * [Example 1: e.g., "A higher percentage of females survived compared to males."]
    * [Example 2: e.g., "Passengers in Pclass 1 had a higher survival rate."]
    * [Example 3: e.g., "Age distribution of survivors might differ from non-survivors."]

## Conclusion

This EDA task provided a comprehensive understanding of the cleaned Titanic dataset. By applying statistical summaries and various visualization techniques, valuable insights into feature distributions, relationships, and potential influencing factors for survival were gained. These insights are crucial for subsequent machine learning model building.
