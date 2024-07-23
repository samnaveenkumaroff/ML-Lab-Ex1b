# ML-Lab-Ex1b
DATA PREPROCESSING (To prepare the data suitable for the machine learning model, perform data cleaning, data reduction and data transformation on the given dataset using python implementation.)
Here's the updated README file including the new details for Ex. No: 1b DATA PREPROCESSING:

```
## Ex. No: 1b DATA PREPROCESSING

### AIM
To prepare the data suitable for the machine learning model, perform data cleaning, data reduction, and data transformation on the given dataset using Python implementation.

### DESCRIPTION
Data preprocessing is a process of preparing the raw data and making it suitable for a machine learning model.

- **Data cleaning** can be applied to "clean" the data by filling in missing values, smoothing noisy data, identifying or removing outliers, and resolving inconsistencies.
- **Data reduction** can reduce data size by, for instance, aggregating, eliminating redundant features, or clustering.
- **Data transformations** (e.g., normalization) may be applied, where data are scaled to fall within a smaller range like 0.0 to 1.0.

### DATA CLEANING
Data cleaning is the process of removing incorrect, corrupted, garbage, incorrectly formatted, duplicate, or incomplete data within a dataset. Having wrong or bad quality data can be detrimental to processes and analysis.

- **Check for Missing Values**
  - Data imputation - attribute with 10% missing
  - Replace NaN with a Scalar Value (mean, median, mode, random, KNN etc.)
- **Check for Duplicates**
- **Detect Outliers**

### DATA REDUCTION
Data reduction techniques can be applied to obtain a reduced representation of the data set that is much smaller in volume, yet closely maintains the integrity of the original data.

- Dimensionality reduction, numerosity reduction, data compression.
- Feature selection and Feature extraction
- Drop missing values
- Drop the outliers
- Drop duplicates

### DATA TRANSFORMATION
Data transformation is a technique used to convert the raw data into a suitable format.

- **Normalization** - Data normalization involves converting all data variables into a given range.
  - Min-max - This method implements a linear transformation on the original data.
  - Z-score – This method normalizes the value using the mean and standard deviation.
- **Encoding method** - convert the categorical features into its numeric representation.
  - Label encoding - each label is assigned a unique integer based on alphabetical ordering between 0 and n_classes-1 where n is the number of distinct labels.
  - One-Hot encoding - creates additional features based on the number of unique values in the categorical feature, create dummy variables.

### QUESTIONS
1. Calculate the % of missing values in a column.
2. Replace missing value with mean if the % of missing value is less than 10%.
3. Perform the mode imputation for a categorical data.
4. Perform a KNN Imputer to estimate the missing values.
5. Drop the columns with more than 10% missing values and display the size.
6. Drop the rows with outlier Z-score value > 3 and display the size.
7. Drop the duplicate rows based on more than 50% of columns having the same value.
8. Rescale your data using min-max normalization for a numerical feature. (Python code)
9. Binarize the data by using binarizer class in python (Python Code)
10. Perform the one-hot encoding for a categorical feature. (Python code)

## Contents

- [ML_Lab_Ex_1b.ipynb](ML_Lab_Ex_1b.ipynb): Jupyter notebook for the exercises.
- [ML_Lab_Ex_1b.py](ML_Lab_Ex_1b.py): Python script for the exercises.

## Usage

Clone the repository and run the Jupyter notebook or Python script to perform the machine learning exercises. Make sure to have the required dataset (insurance.csv) in the same directory or update the path accordingly.

### Example

```python
# Load the dataset
import pandas as pd
df = pd.read_csv('insurance.csv')

# Perform Min-Max Normalization
from sklearn.preprocessing import MinMaxScaler
def min_max_normalization(df, column_name):
    scaler = MinMaxScaler()
    df[[column_name]] = scaler.fit_transform(df[[column_name]])
    return df

df = min_max_normalization(df, 'bmi')
print(df['bmi'])
```

## Crafted with Love by Sam Naveenkumar .V

Thank you for visiting the ML-Lab-Ex01 repository. If you have any questions or suggestions, please feel free to raise an issue or contribute to the project.
```
