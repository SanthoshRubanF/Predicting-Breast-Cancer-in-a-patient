Predicting-Breast-Cancer-in-a-patient
Import Libraries
	pandas: For data manipulation and analysis. 
	numpy: For numerical operations. 
	seaborn: For statistical data visualization. 
	matplotlib: For plotting graphs. 
	sklearn.preprocessing: For encoding labels and scaling features. 
	sklearn.svm: For Support Vector Machine classifier. 
	sklearn.model_selection: For splitting data and hyperparameter tuning. 
	sklearn.metrics: For evaluating model performance. 
	sklearn.linear_model: For Logistic Regression model.

Data Loading and Initial Exploration
	Load Data: Read the CSV file into a DataFrame. 
	Data Information: Display info about the DataFrame including column types and non-null counts. Missing Values: Check for missing values in each column. 
	Data Shape: Check the number of rows and columns. 
	Class Distribution: Check the distribution of the target variable 'diagnosis'.

Data Cleaning and Transformation
	Drop Columns: Remove columns with missing values and the 'id' column. 
	Encode Target: Map 'diagnosis' from 'B'/'M' to 0/1. 
	Check Data: Display the first few rows, updated shape, info, missing values, and summary statistics.

Encoding and Visualization
	Encode Target Again: Ensure 'diagnosis' is properly encoded. 
	Visualization: Plot the count of each diagnosis class.

Feature Exploration
	Boxplots: Create boxplots for each feature to visualize their distributions and detect outliers.

Correlation Matrix
	Heatmap: Show the correlation between features using a heatmap.

Splitting and Scaling Data
	Feature and Target Separation: Separate features (X) and target (y). 
	Train-Test Split: Split data into training and testing sets. 
	Standardize Features: Scale features for better model performance.

SVM Classifier Training and Evaluation
	Train SVM: Train a Support Vector Machine classifier. 
	Predictions: Predict on test data. 
	Metrics: Calculate and print accuracy, precision, recall, specificity, and AUC-ROC.

Hyperparameter Tuning with GridSearchCV

	Define Grid: Set up a grid of hyperparameters for tuning. 
	Grid Search: Perform grid search with cross-validation to find the best parameters. 
	Best Model: Get the best model and evaluate it on the test set.

Logistic Regression Model
	Train Logistic Regression: Train a Logistic Regression model.
	Evaluate: Predict on test data and calculate accuracy.

Confusion Matrix
	Confusion Matrix: Compute and print the confusion matrix. 
	Extract Values: Extract TP, TN, FP, and FN from the confusion matrix. 
	Print Accuracy: Print the confusion matrix and the accuracy.
