# Data Cleaning & Preprocessing

## Objective

This task focused on learning how to clean and prepare raw datasets for machine learning models. The core objective was to perform essential preprocessing steps to ensure data quality and suitability for subsequent analysis and model training.

## Dataset Used

For this task, I used the **Titanic Dataset**, a classic dataset often used for introductory machine learning projects. It contains information about passengers on the Titanic, including their demographics, travel details, and survival status.

## Tools Used

* **Python:** The primary programming language for data manipulation and analysis.
* **Pandas:** A powerful library used for data loading, manipulation, and analysis of tabular data.
* **NumPy:** Essential for numerical operations, especially when working with arrays and mathematical functions.
* **Matplotlib/Seaborn:** Libraries used for data visualization, particularly for identifying outliers through boxplots.

## Steps Performed

The following steps were executed to clean and preprocess the Titanic dataset:

### 1. Dataset Import and Initial Exploration

* The `titanic.csv` dataset was imported into a Pandas DataFrame.
* Basic information such as data types (`.info()`), descriptive statistics (`.describe()`), and the number of missing values (`.isnull().sum()`) were explored to understand the dataset's structure and identify initial cleaning requirements.

### 2. Handling Missing Values

* **'Age' Column:** Missing values in the 'Age' column (numerical) were imputed using the **median** of the column, as the median is more robust to outliers compared to the mean.
* **'Embarked' Column:** Missing values in the 'Embarked' column (categorical) were filled with the **mode** (most frequent value) of the column.
* **'Cabin' Column:** The 'Cabin' column had a very high percentage of missing values. Given its limited utility without extensive feature engineering and the high missing rate, this column was **dropped** from the dataset.

### 3. Converting Categorical Features into Numerical (Encoding)

* **'Sex' Column:** The 'Sex' column, being a binary categorical feature ('male', 'female'), was converted into numerical representation using **Label Encoding**.
* **'Embarked' Column:** The 'Embarked' column, a multi-class categorical feature ('S', 'C', 'Q'), was converted using **One-Hot Encoding** (`pd.get_dummies()`) to avoid implying an ordinal relationship between categories. One of the generated columns was dropped to prevent multicollinearity.
* **Irrelevant Columns:** Columns like 'Name', 'Ticket', and 'PassengerId' were dropped as they are unique identifiers or textual data not directly relevant for training a predictive model in their raw form.

### 4. Normalization/Standardization of Numerical Features

* Numerical features such as 'Age', 'Fare', 'Pclass', 'SibSp', and 'Parch' were scaled using **Standardization (Z-score normalization)**. This process transforms the data to have a mean of 0 and a standard deviation of 1, which helps various machine learning algorithms perform better, especially those sensitive to the scale of features.

### 5. Outlier Visualization and Handling

* **Boxplots** were used to visualize outliers in numerical features, particularly in the 'Fare' column where significant outliers are often present.
* Outliers in the 'Fare' column were identified and removed using the **Interquartile Range (IQR) method**. This involved filtering out data points that fell outside the range of `Q1 - 1.5 * IQR` and `Q3 + 1.5 * IQR`.

## Conclusion

This task provided hands-on experience in essential data preprocessing steps. By performing these operations, the raw Titanic dataset was transformed into a clean, numerical, and scaled format, making it suitable for training machine learning models. Understanding these steps is fundamental for building robust and accurate predictive models.
