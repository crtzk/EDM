# Midterm Lab Task 2 – Data Cleaning and Transformation Using Power Query Editor
For this task, we are provided with an Uncleaned_DS_jobs.csv dataset (from Kaggle) and tasked with performing data cleaning and transformation using Power Query Editor in Excel to generate meaningful insights.
## STEP 1 – Data Cleaning Process
- Load the raw file
- Fit Column and row width and height
- TRIM extra spaces
- Remove NULL values
- Remove Duplicates
## STEP 2 – Data Transformation
- Salary Estimate Column:
- In Power Query, select the Salary Estimate column.
- Use Transform > Extract > Text Before Delimiter to remove any characters after the open parenthesis.
- Create Min and Max Salary Columns:
- Use Add Column > Column from Examples to generate the Min Sal and Max Sal columns from the Salary Estimate column.
- Add Role Type Column.
- Go to Add Column > Custom Column and use the formula to categorize job titles into roles like Data Scientist, Data Analyst, Data Engineer, etc.
- Split Location Column:
- Select the Location column and use Transform > Split Column by Delimiter (Comma) to split location into separate columns.
- Location Correction:
- Create a custom column to correct location values, replacing certain locations (e.g., "New Jersey" to ", NJ", "California" to ", CA").
- Handle Negative Values:
- Filter out negative values in Competitors and Industry columns.
- Clean Company Name:
- Remove any unwanted text from the Company Name column using Transform > Replace Values or Remove Text.
## STEP 3 – Screenshots
- Before Data Cleaning: (See screenshot of raw data before any transformations were made.)
![Screenshot]
- After Data Cleaning: (See screenshot of cleaned data post-transformation.)
![Screenshot]
## STEP 4 – Final Output Queries
![Screenshot]
Physical Data Model
