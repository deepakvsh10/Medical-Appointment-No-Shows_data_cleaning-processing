📅 Medical Appointment No Shows - Data Cleaning Project
This repository showcases a practical data cleaning and preprocessing project using a real-world dataset. The project's goal is to transform a raw dataset into a clean, well-structured format, ready for exploratory data analysis, visualization, and machine learning model building.

📂 Dataset
The dataset used is the "Medical Appointment No Shows" dataset, originally from Kaggle. The raw data contains information on over 110,000 medical appointments in Brazil. The data includes patient characteristics such as age, gender, and neighborhood, as well as details about the appointment, such as the scheduled and appointment dates.

🧹 Data Issues Addressed
The raw dataset, like many real-world datasets, contains several issues that need to be addressed before analysis:

Inconsistent Column Names: Column names like No-show, Hipertension, and Handcap contain hyphens, mixed casing, and misspellings, which can be challenging to work with in code.

Invalid Data: The Age column contains at least one invalid value (e.g., age of -1).

Incorrect Data Types: The PatientId column is loaded as a float, and date columns are stored as strings with unnecessary time and timezone information.

Categorical Encoding: The No-show column contains 'Yes' and 'No' values, which are not in a numerical format suitable for most machine learning models.

🚀 Data Cleaning and Preprocessing Workflow
The data_cleaning.py script systematically addresses the issues mentioned above:

Load Data: The script first attempts to load the dataset directly from its public Kaggle URL.

Rename Columns: Column names are standardized to be in snake_case (e.g., No-show becomes no_show), and misspellings like Hipertension and Handcap are corrected.

Handle Invalid Data: Rows with an invalid Age value (less than or equal to zero) are removed from the dataset to ensure data integrity.

Correct Data Types:

The scheduled_day and appointment_day columns are converted from strings to proper datetime objects, and the time components are removed.

The patient_id column is converted to an integer (int64) to handle the large numerical IDs correctly.

Standardize Categorical Data: The no_show column is transformed from Yes/No to a binary numerical representation (1/0), making it ready for machine learning tasks.

💻 How to Run the Script
Prerequisites: Ensure you have Python and the Pandas library installed. You can install Pandas using pip:

pip install pandas

Execute the Script: Run the data_cleaning.py file from your terminal:

python data_cleaning.py

The script will print the head of the raw dataset, followed by its final cleaned state, demonstrating the transformation process.

This project can serve as a foundational piece in a data science portfolio, demonstrating core skills in data manipulation and preprocessing.
