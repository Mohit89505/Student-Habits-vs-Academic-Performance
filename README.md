# Student-Habits-vs-Academic-Performance
This notebook analyzes the relationship between student habits and academic performance using the "student-habits-vs-academic-performance" dataset from Kaggle.

Here's a summary of the steps performed:

Load Libraries: Necessary libraries for data manipulation, visualisation, and machine learning are imported (pandas, numpy, matplotlib, seaborn, sklearn).
Download Dataanalyses.
Load Data: The CSV file (student_habits_performance.csv) from the downloaded directory is loaded into a pandas DataFrame df. The first few rows are displayed.
Explore Data Shape: The shape of the DataFrame (number of rows and columns) is checked.
Check for Missing Values: Missing values in the DataFrame are identified and summed up per column.
Handle Missing Values: Missing values in the 'parental_education_level' column are filled with the mode of the column.
Identify Categorical and Numerical Columns: Columns are separated into categorical and numerical types for further processing.
Visualize Categorical Data: Histograms are plotted to visualize the distribution of values in categorical columns.
Visualize Numerical Data: Histograms are plotted to visualize the distribution of values in numerical columns.
Drop Student ID: The 'student_id' column is dropped as it's not relevant for the analysis.
Encode Categorical Data:
Ordinal categorical columns ('diet_quality', 'parental_education_level', 'internet_quality') are mapped to numerical values.
Nominal categorical columns ('gender', 'part_time_job', 'extracurricular_participation') are one-hot encoded using pd.get_dummies.
Combine DataFrames: The encoded categorical columns are concatenated with the numerical and mapped ordinal columns.
Drop Original Categorical Columns: The original categorical columns are dropped from the combined DataFrame.
Correlation Analysis: A correlation matrix is calculated and visualized using a heatmap to understand the relationships between variables, particularly with the target variable 'exam_score'.
Prepare Data for Modeling:
The features (X) and target variable (y) are separated.
The features are scaled using StandardScaler.
The data is split into training and testing sets using train_test_split.
Train and Evaluate Models:
Several regression models (Linear Regression, Ridge, Lasso, Random Forest) are trained on the scaled training data.
Predictions are made on the test data.
The performance of each model is evaluated using R² score and Root Mean Squared Error (RMSE).
This notebook provides a foundational analysis and modeling approach to predict student exam scores based on their habits and other factors.
