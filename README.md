
# Feature Engineering

Feature engineering is a crucial step in the data preprocessing pipeline that involves transforming raw data into a format suitable for machine learning models. It primarily deals with three factors:

1) **Outliers:**
   Outliers are extreme values that deviate significantly from other observations in the dataset. They can adversely affect model performance. Outliers can be handled using two main methods:

   1.1) **Percentile Method:**
      Identify and remove outliers by setting a threshold based on percentiles manually.

   1.2) **Standard Deviation or Z-score Method:**
      Define a threshold based on the mean plus a certain number of standard deviations, and then eliminate observations beyond this threshold.

2) **Handling Null Values:**
   Null values, also known as missing values, are common in datasets and need to be addressed effectively. There are different types of null values, including MCAR (Missing Completely at Random), MAR (Missing at Random), and MNAR (Missing Not at Random). Techniques to handle null values include:

   2.1) **Handling Null in Continuous Data:**
      - 2.1.1) Mean/Median Imputation: Replace missing values with the mean or median of the respective feature.
      - 2.1.2) Random Sample Imputation: Replace missing values with non-missing values randomly sampled from the same column. This method preserves the distribution of data better than mean/median imputation.
      - 2.1.3) Capturing New Features: Introduce a new binary feature indicating the presence of missing values and then replace missing values using mean/median imputation or random sample imputation.
      - 2.1.4) End of Distribution Imputation: Replace missing values with a value at the end of the distribution, such as mean plus a multiple of standard deviation.

   2.2) **Handling Null in Categorical Data:**
      - 2.2.1) Create new features to indicate the presence of missing values and then replace missing values with the most frequent class in each category.
      - 2.2.2) Replace missing values with a new category label, such as 'missing,' treating missing values as a separate class.

3) **Handling Categorical Features:**
   Categorical features represent qualitative variables with discrete categories. Effective handling of categorical features is essential for model performance. Common approaches include:

   3.1) **Direct One-Hot Encoding:**
      Create binary features for each category using one-hot encoding. However, this method can lead to the curse of dimensionality, especially when dealing with a large number of categories.
   
   3.2) **Use Top-K Classes:**
      Select the top-K most frequent classes in each categorical feature and encode them into binary features. This reduces the dimensionality of the feature space while retaining important information about the most significant categories.

Proper feature engineering can significantly impact the performance and interpretability of machine learning models, making it a critical step in the data preprocessing pipeline.
