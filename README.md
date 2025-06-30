# JobLogic_Project_01-06-25
 
 Objective
 To develop a machine learning model that can predict whether a company is likely to go bankrupt based on its financial indicators collected
 over 5 years. The task is framed as a binary classification problem (0 = non-bankrupt, 1 = bankrupt).
 Problem-Solving Approach
 1. Understanding the Data The dataset contains 64 numerical financial features per company for each year. After merging all yearly
 datasets, we noticed:
 Class imbalance: Very few bankrupt companies compared to non-bankrupt ones
 Missing data: Some features had significant missing values
 2. Data Preprocessing Dropped columns with more than 40% missing values
 Imputed remaining missing values using the median (to handle outliers better)
 Standardized all features using StandardScaler to normalize the range
 Handled class imbalance using SMOTE, which oversamples the minority class (bankrupt) by synthetically generating new examples
 3. Exploratory Data Analysis Histograms showed that many features were skewed, which is common in financial data
 Correlation heatmap helped understand redundancy and potential multicollinearity
 Applied PCA to visualize class separability in a 2D space
 Model Selection
 Logistic Regression algorithm for linear and binary classification problems. can be readily generalized to multiclass settings, which is known
 as multinomial logistic regression or softmax regression.
 Random Forest A random forest can be considered as an ensemble of decision trees. The idea behind a random forest is to average multiple
 (deep) decision trees that individually suffer from high variance to build a more robust model that has a better generalization performance
 and is less susceptible to overfitting.
 XGBoost Often top performer for structured/tabular data; handles imbalance well. It is essentially a computationally efficient implementation
 of the original gradient boost algorithm
Conclusion
For this task, XGBoost was the most effective model due to its ability to handle imbalance, capture complex patterns, and deliver strong predictive performance. Random Forest was a close second and also helped interpret which financial features were most important.
