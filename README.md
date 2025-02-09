This project analyzes tourist behavior data and predicts future visitor counts using machine learning. The primary goal is to predict the number of visitors to various tourist destinations for the year 2025 based on historical data from 2018 to 2024.


Requirements:

To run this project, the following libraries are required:

PySpark: For working with large-scale data.
Pandas: For data manipulation and conversion between Pandas and Spark DataFrames.
Scikit-learn: For machine learning models and evaluation.
Matplotlib: For data visualization.
Seaborn: For creating statistical plots.
Openpyxl: For reading and writing Excel files.


You can install the required libraries by running the following commands:

pip install pyspark
pip install openpyxl
pip install seaborn scikit-learn matplotlib pandas


Setup:

Upload the Excel file: The data file needs to be uploaded to the environment.
Install the necessary packages using the commands above.
Run the Python code: The code will load the data, clean it, and perform analysis.
Model Training: The model trains using a Random Forest Regressor to predict visitor counts for 2025.
Output: The predicted visitor counts for 2025 will be saved in an Excel file that can be downloaded.

Steps:


Data Preprocessing:

The code begins by loading an Excel file containing visitor data for various tourist places.

The "Visitors" column is cleaned by removing commas and converting "million" values into numeric data.


Pivot Table Creation:

The data is transformed into a pivot table where the index is the place name, city, type, best visiting months, and description.
The columns represent the years, and the values are the visitor counts.


Feature Preparation:

The columns corresponding to the years (2018-2024) are used as features to predict visitor numbers for 2025.


Model Training:

A Random Forest Regressor is used for training the model, and RandomizedSearchCV is applied to tune the model's hyperparameters.
The model's performance is evaluated using mean absolute error and R-squared score.


Predictions:

Predictions for the year 2025 are generated using the trained model.


Visualization:

A heatmap is generated to show the correlation between the different variables in the dataset.


Output:

The predictions are saved in an Excel file and can be downloaded.


Results
The model's R-squared score indicates how well the model is performing, and if the accuracy is greater than or equal to 90%, the target accuracy is achieved.
The predicted visitor data for 2025 is provided in the Excel file.
