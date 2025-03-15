# [Midterm Lab Task 2](https://github.com/user-attachments/files/19111495/Midterm.Lab.Task.2.xlsx)
This task shows the process of data cleaning and preparation using Power Query.
## Step-by-Step Process
### Step 1: Download and Load Data  
- Download the dataset (Uncleaned_DS_jobs.csv)
- Open Excel
- Go to Data, New Query, Open File, Text/CSV
- Click Load and then Edit using Power Query Editor  

### Step 2: Duplicate Raw Data  
- Right-click the dataset in the Queries pane
- Select Duplicate  

### Step 3: Clean Salary Data  
- Select the Salary Estimate column
-  Go to Transform Menu, Extract, Text Before Delimiter
- Type "(" and click OK
- Create two new columns: Min Salary and Max Salary  
   - Select Salary Estimate column, Add Column Menu, Column from Examples, From Selections  
   - Type the first min salary value and press Enter (all rows will auto-fill)  
   - Rename column to "Min Sal"  
   - Repeat process for Max Salary  

### Step 4: Add Role Type Column  
- Go to Add Column Menu then Custom Column
- Rename the column to "Role Type"
- Use this logic:  
   - If Job Title contains "Data Scientist" to Assign "Data Scientist"  
   - If Job Title contains "Data Analyst" to Assign "Data Analyst"  
   - If Job Title contains "Data Engineer" to Assign "Data Engineer"  
   - If Job Title contains "Machine Learning" to Assign "Machine Learning Engineer"  
   - Otherwise, assign "Other" 
- Change the column type to Text  

### Step 5: Split Location Column  
- Select the Location column  
- Add a Custom Column with corrections:  
   - If Location = "New Jersey" then Assign ", NJ"  
   - If Location = "Remote" or "United States" to Assign ", Other"  
   - If Location = "Texas" then Assign ", TX"  
   - If Location = "California" Assign ", CA" 
- Click OK, then select the new column  
- Go to Transform, Split Column, By Delimiter (comma ",")  
- Click OK  
- Rename the second split column to "State Abbreviations"  
- Check and replace incorrect values (e.g., "Anne Rundell" → "MA")  

### Step 6: Split Size Column  
- Create two new columns: MinCompanySize and MaxCompanySize
- Use the same method as Salary Estimate to split values  

### Step 7: Handle Negative Values  
- Filter out -1s from the Competitors column
- Filter out 0s from the Revenues column
- Remove -1s from the Industry column  

### Step 8: Clean Company Names  
- Remove any extra characters or ratings after company names  

### Step 9: Copy Cleaning Steps as Proof  
- Go to Home Menu, Click Advanced Editor
- Copy and save the code in your portfolio  



### Step 10: Reshape and Group Data  
#### Group by Role Type  
- Duplicate the raw data then rename it as "Sal By Role Type dup"
- Select only Role Type, Min Salary, and Max Salary columns
- Change Min and Max Salary type to currency
- Multiply values by 1000 (Numbers Column, Standard, Multiply, Type 1000)
- Group rows by Role Type and get the average for Min and Max Salary  

#### Group by Company Size  
- Create a reference of raw data then rename it as "Sal By Role Size ref"
-  Select only Size, Min Salary, and Max Salary columns
-   Change Min and Max Salary type to currency
-  Multiply values by 1000
-  Group rows by Size and get the average for Min and Max Salary  


### Step 11: Merge State Mapping  
- Click Unclean DS Jobs
- Right-click in the Queries pane, New Query, Open Workbook State Mapping
- Select the columns and click OK  
-  Select Uncleaned DS Jobs query
- Choose the State Abbreviation column in both queries
-  Click Merge then Click OK
-  Rename the merged column as "State Full Name"
-  Remove nulls and blanks
### Step 12: Group by State  
- Create a reference of raw data → Rename it as "Sal By State ref"  
- Select only State Full Name, Min Salary, and Max Salary columns
- Change Min and Max Salary type to currency
- Multiply values by 1000
- Group rows by State Full Name and get the average for Min and Max Salary  



### Step 13: View Query Dependencies  
- Go to View Menu → Click Dependencies
- Check if all queries are correctly linked  

## Here are the screenshots showcasing the table transformation process
### Here's the screenshot of my output before I started data cleaning (see screenshot)
![Image](https://github.com/user-attachments/assets/38ea140c-bb3b-44c1-b2cb-a25601ea8467)
## Here's the screenshot of the Advanced Editor
![Image](https://github.com/user-attachments/assets/363e27b5-76d2-4561-8907-6718216a3d45)
### Here's the screenshot of my output after I started data cleaning (see screenshot)
![Image](https://github.com/user-attachments/assets/dd368a40-ad15-4159-a5dd-3ab372efe33d)


### Here's the screenshot of Sal By Role type (see screenshot)
![Image](https://github.com/user-attachments/assets/4a2b5298-8a0b-4440-8e83-de4f0810d89d)
### Here's the screenshot of Sal By Role Size (see screenshot)
![Image](https://github.com/user-attachments/assets/f193001b-6da3-46fa-aa36-877f20cefc81)
### Here's the screenshot of Sal By State (see screenshot)
![Image](https://github.com/user-attachments/assets/d6e69440-32be-4cbf-af2c-5d8a99dfdcbc)
### Here's the screenshot of States (see screenshot)
![Image](https://github.com/user-attachments/assets/8c402690-1e7a-4253-899d-e0f74b6e302a)
### Here's the screenshot of the Query Dependencies
![Image](https://github.com/user-attachments/assets/e964092b-b535-4357-86aa-13795196b172)
