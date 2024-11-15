# data_cleaning

for raw data: https://www.kaggle.com/datasets/kushsheth/los-angeles-police-department-lapd-crime-data

This Python script performs data cleaning and manipulation on a dataset of crime incidents in Los Angeles. The key steps are as follows:

1-Loading the Dataset:

The dataset is loaded from a CSV file located in the directory specified by the path variable. The data is copied to a new DataFrame df for further processing.

2-Renaming of Variables:

The column names of the dataset are renamed to more readable and consistent names, such as "id", "reported", "occurred", "area", "code", etc.

3-Date Transformations:

The "reported" and "occurred" date columns are cleaned and standardized into the format "DD.MM.YYYY". Invalid date formats are handled using try-except blocks.

4-Time Format Correction:

The "time" column is reformatted to the standard "HH
" time format by padding zeros where necessary.

5-Adding Descent Information:

A new column, descent_info, is added based on a predefined dictionary of descent/ethnic codes. These codes are mapped to more descriptive information about the ancestry or ethnic origin.

6-Crime Code Generalization:

The code variable is generalized into 9 main crime categories (e.g., "Violent Crimes", "Sexual Crimes", "Property Crimes") by matching crime descriptions with keywords.

7-Gender Code Generalization:

The "sex" variable is cleaned, and unknown or ambiguous gender codes ("X", "H", "-") are replaced with "other". Missing values are also filled with "other".

8-Weapon Classification:

The "weapon" variable is analyzed and grouped into 6 main categories (e.g., "Firearms", "Cutting Weapons", "Blunt Objects"). A new column, weapon_info, is added to reflect these classifications.

9-Status Transformation:

The "status" variable is standardized by replacing abbreviations with more descriptive labels (e.g., "Invest Cont" becomes "Investigation Continued").

10-Age Data Correction:

Observations with zero or negative values in the "age" variable are replaced with the trimmed mean to handle outliers.

11-Exporting the Final Data:

The cleaned and transformed dataset is saved as a new CSV file, final_data.csv.
