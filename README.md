# Medical-Appointment-No-Shows_data_cleaning-processing
📊 Data Cleaning and Preprocessing Project
This repository contains a simple Python script to demonstrate a typical data cleaning and preprocessing workflow using the Pandas library. The process is crucial for preparing raw data for subsequent analysis, visualization, or machine learning tasks.

📂 Dataset
The script uses a simulated dataset inspired by the "Medical Appointment No Shows" data from Kaggle. The raw data includes common issues such as:

Missing values (NaN)

Duplicate rows

Inconsistent text formatting

Inconsistent date formats

Incorrect data types (e.g., age as a float, negative age)

Poorly named columns (e.g., No-show with a hyphen)

🚀 How to Run the Script
Prerequisites: Ensure you have Python and the Pandas library installed. You can install Pandas using pip:

pip install pandas

Execute the Script: Run the data_cleaning.py file from your terminal:

python data_cleaning.py

The script will print the state of the data at various stages of the cleaning process, showing the raw data, and then the final, clean output.

🧹 Data Cleaning Steps Performed
The data_cleaning.py script follows a structured approach to clean the dataset:

Column Renaming: Renamed columns to a uniform, clean format (e.g., no-show became no_show).

Duplicate Removal: Identified and removed duplicate rows based on the patient and appointment IDs.

Missing Value Handling:

Missing gender values were filled with the most common gender (M or F).

Missing age values were filled with the median age.

Data Validation: Handled invalid data points, such as a negative age, by filtering them out or correcting them.

Data Type Conversion:

Converted age from a float to an integer.

Converted date columns from strings to proper datetime objects.

Data Standardization:

Standardized the gender column to all uppercase (M, F).

Converted the no_show column from 'Yes'/'No' to a binary 1/0 format for easier analysis.

📦 Output
After running the script, the final output will be a cleaned DataFrame printed to the console. In a real-world application, you would typically save this cleaned data to a new CSV file, for example, cleaned_data.csv.
