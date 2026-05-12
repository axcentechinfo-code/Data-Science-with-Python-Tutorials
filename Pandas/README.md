# Pandas Day 1: Introduction to Pandas DataFrames

## Overview
This Jupyter notebook provides a beginner-friendly introduction to working with Pandas DataFrames in Python. We'll explore basic operations such as loading data from a CSV file, inspecting the data, and understanding its structure. The dataset used is a sample student records file containing information about students' academic performance, placements, and other details.

## Prerequisites
- Python 3.x
- Pandas library (`pip install pandas`)
- Jupyter Notebook or JupyterLab

## Dataset
The dataset (`Dataset/student.csv`) contains the following columns:
- **Student_ID**: Unique identifier for each student
- **Name**: Student's name
- **Gender**: Male/Female
- **Age**: Student's age
- **Department**: Academic department (Data Science, AI & ML, Cyber Security, Cloud Computing)
- **City**: City of residence
- **Attendance_Percentage**: Percentage of classes attended
- **Math_Marks, Science_Marks, English_Marks, Python_Marks**: Marks in respective subjects
- **Projects_Completed**: Number of projects completed
- **Internship**: Whether the student has done an internship (Yes/No)
- **Placement_Status**: Whether placed (Placed/Not Placed)
- **Study_Hours_Per_Day**: Daily study hours
- **Backlogs**: Number of backlogs
- **CGPA**: Cumulative Grade Point Average
- **Scholarship**: Whether receiving scholarship (Yes/No)
- **Joining_Date**: Date of joining the institution

## Code Explanation

### 1. Importing Pandas
```python
import pandas as pd
```
This cell imports the Pandas library and assigns it the alias `pd`. Pandas is a powerful data manipulation library in Python that provides data structures like DataFrames for handling tabular data.

### 2. Specifying the Data File Path
```python
data = 'Dataset/student.csv'
```
Here, we define the path to our CSV file. The file is located in the `Dataset` subdirectory relative to the notebook.

### 3. Loading the Data into a DataFrame
```python
df = pd.read_csv(data)
df
```
- `pd.read_csv(data)` reads the CSV file and creates a DataFrame object.
- `df` is the variable name we assign to our DataFrame.
- Displaying `df` shows the entire DataFrame in the output.

### 4. Viewing the First Few Rows
```python
df.head()
```
The `head()` method displays the first 5 rows of the DataFrame by default. This is useful for quickly inspecting the data structure and content.

### 5. Viewing the Last Few Rows
```python
df.tail()
```
The `tail()` method displays the last 5 rows of the DataFrame. This helps in understanding the end of the dataset.

### 6. Getting the Total Number of Elements
```python
df.size
```
`size` returns the total number of elements in the DataFrame (rows × columns). It's equivalent to `df.shape[0] * df.shape[1]`.

### 7. Getting the Shape of the DataFrame
```python
df.shape
```
`shape` returns a tuple representing the dimensions of the DataFrame: (number_of_rows, number_of_columns).

### 8. Getting Column Names
```python
df.columns
```
`columns` returns an Index object containing the column names of the DataFrame.

### 9. Unpacking Shape Information
```python
rows, columns = df.shape
print(f'Number of rows: {rows}')
print(f'Number of columns: {columns}')
```
This unpacks the tuple returned by `df.shape` into separate variables and prints them in a formatted string.

### 10. Getting DataFrame Information
```python
df.info()
```
`info()` provides a concise summary of the DataFrame, including:
- Number of entries (rows)
- Column names and data types
- Number of non-null values per column
- Memory usage

### 11. Statistical Summary (Numeric Columns)
```python
df.describe()
```
`describe()` generates descriptive statistics for numeric columns, including:
- Count
- Mean
- Standard deviation
- Minimum, 25th percentile, median (50%), 75th percentile, maximum

### 12. Data Types of Columns
```python
df.dtypes
```
`dtypes` returns the data type of each column in the DataFrame.

### 13. Statistical Summary (All Columns)
```python
df.describe(include='all')
```
This provides descriptive statistics for all columns, including categorical data. For non-numeric columns, it shows:
- Count
- Unique values
- Top (most frequent value)
- Frequency of top value

## Key Concepts Learned
1. **DataFrame Creation**: Loading data from CSV files
2. **Data Inspection**: Using `head()`, `tail()`, `shape`, `size`, `columns`
3. **Data Types**: Understanding column data types with `dtypes`
4. **Summary Statistics**: Generating insights with `describe()`
5. **DataFrame Info**: Getting overview with `info()`

## Next Steps
- Data cleaning and preprocessing
- Data manipulation (filtering, sorting, grouping)
- Data visualization
- Advanced Pandas operations

## Running the Notebook
1. Ensure you have the required dependencies installed
2. Make sure the `Dataset/student.csv` file is in the correct location
3. Run the cells in order from top to bottom
4. Observe the outputs to understand each operation

## Exercises
1. Try loading a different CSV file
2. Experiment with `df.head(10)` to see more rows
3. Use `df.describe()` on specific columns
4. Explore other DataFrame methods like `df.sample()` or `df.isnull().sum()`