# Dendrite.ai
This repository created for the answer of screening test of dendrite.ai

I have used Jupyter Notebook to run the command because it is fast and reliable.

It follows following steps:

**Importing Libraries:** The script begins by importing the necessary Python libraries and modules, such as pandas, numpy, and various modules from sklearn for machine learning tasks like regression and feature selection.

**read_file Function:** This function reads data from a CSV file specified by the path_data variable and processes the contents of an RTF (Rich Text Format) file specified by the path_json variable. It extracts information from the RTF file using the striprtf module, converts the extracted text into a Python object using JSON parsing, and returns the data, parsed object, and target column.

**Imputation and Data Handling:** The script iterates through columns of the dataset and handles missing values and categorical variables. For numerical columns, it imputes missing values based on the method specified in the JSON object. For categorical columns, it performs text handling based on the method specified in the JSON object, such as using hashing or other techniques. It also renames columns according to the JSON object.

**Splitting Data:** The split_data function splits the data into training and testing sets for model building. It separates the target column from the features.

**Feature Reduction:** The feature_reduction function reduces the dimensionality of the feature set using methods specified in the JSON object. It can perform feature selection using tree-based importance, perform Principal Component Analysis (PCA), or remove highly correlated features.

**Model Building:** The model_build function builds and evaluates regression models based on the algorithm specified in the JSON object. It uses various regression algorithms like Random Forest Regressor, Decision Tree Regressor, Gradient Boosting Regressor, ElasticNet, Lasso, and Ridge. It uses GridSearchCV for hyperparameter tuning and evaluates the models using Root Mean Squared Error (RMSE).

**Main Execution:** The main part of the script reads data from the CSV and RTF files, processes the data using the functions defined earlier, and then performs feature reduction and model building for selected regression algorithms. It prints out the RMSE for each algorithm.
