# Pandas-Tutorial

## Welcome to quick tutorial of python pandas

- Pandas is one of the most commonly used Python packages/libraries for data science.<br><br>
- Pandas is Python's answer for making two dimensional tables (ala Excel and SQL).<br><br>
- Pandas calls a table a "DataFrame".<br><br>
- Pandas DataFrames are used by Python's other packages for statistical analysis, data manipulation, and data visualization <br><br>
- Pandas DataFrames can be exported as .csv and other files.<br><br>

## Core components of pandas: Series and DataFrames

- The primary two components of pandas are the Series and DataFrame.

- A Series is essentially a column, and a DataFrame is a multi-dimensional table made up of a collection of Series.

### Loading files into python

Below are a few examples of reading files into python

- pd.read_csv()
- pd.read_excel()
- pd.read_html()
- and many more

## Loading excel into python

### Excel Work Sheets

Concat= combine all worksheets into one dataframe example below:

- df = pd.concat(pd.read_excel('filename.xlsx', sheet_name=None, ignore_index=True))

Individual work sheets use for best results!! Example below:

- df = pd.read_excel('filename.xlsx', sheet_name='sheetname')

#### Or

- df = pd.read_excel('filename.xlsx', sheet_name=0)

- 0 represents sheet 1. 

View all worksheets in the file example below:

- df = pd.read_excel('filename.xlsx', sheet_name=None)

## Data Types

### object: str or mixed,   Usage = Text or mixed numeric and non-numeric values

#### Examples: 
- x = John
- y = 52x
- z = John##

### int64: int, Usage= Integer numbers 

#### Examples: 
- x = 1
- y = 35656222554887711
- z = -3255522

### float64: float, Usage= Floating point numbers

#### Examples:
- x = 1.10 or x = 35e3
- y = 1.0 or y = 12E4
- z = -35.59 or z = -87.7e100

### bool: bool Usage= True/False values

#### Examples:

- print(10 > 9) True      > greater than
- print(10 == 9) False    == equal
- print(10 < 9) False     < - less than

### datetime64: Usage= Date and time values

#### Examples: 
- x = 2020-01-01
- y = 01-05-2020

## <br><br> Data aggregation

Data aggregation means taking many data points and reducing them to one number, whether it's a count, sum, mean, or other single statistic. Here are some DataFrame method functions:

- [`.count()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.count.html)
- [`.sum()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sum.html)
- [`.mean()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.mean.html)
- [`.median()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.median.html)
- [`.min()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.min.html)
- [`.max()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.max.html)
- [`.unique()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.unique.html)
- [`.nunique()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.nunique.html)
- [`.std()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.std.html)   #Standard error
- [`.var()`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.var.html)   #Variance
- And more!

## Function   Description

- index()     Method returns index (row labels) of the DataFrame

- insert()    Method inserts a column into a DataFrame

- add()   Method returns addition of dataframe and other, element-wise (binary operator add)

- sub()   Method returns subtraction of dataframe and other, element-wise (binary operator sub)

- mul()   Method returns multiplication of dataframe and other, element-wise (binary operator mul)

- div()   Method returns floating division of dataframe and other, element-wise (binary operator truediv)

- unique()    Method extracts the unique values in the dataframe

- nunique()   Method returns count of the unique values in the dataframe

- value_counts()  Method counts the number of times each unique value occurs within the Series

- columns()   Method returns the column labels of the DataFrame

- axes()  Method returns a list representing the axes of the DataFrame

- isnull()    Method creates a Boolean Series for extracting rows with null values

- notnull()   Method creates a Boolean Series for extracting rows with non-null values

- between()   Method extracts rows where a column value falls in between a predefined range

- isin()  Method extracts rows from a DataFrame where a column value exists in a predefined collection

- dtypes()    Method returns a Series with the data type of each column. The result’s index is the original DataFrame’s columns

- astype()    Method converts the data types in a Series

- values()    Method returns a Numpy representation of the DataFrame i.e. only the values in the DataFrame will be returned, the axes labels will be removed

- sort_values()- Set1, Set2   Method sorts a data frame in Ascending or Descending order of passed Column

- sort_index()    Method sorts the values in a DataFrame based on their index positions or labels instead of their values but sometimes a data frame is made out of two or more data frames and hence later index can be changed using this method

- loc[]   Method retrieves rows based on index label

- iloc[]  Method retrieves rows based on index position

- ix[]    Method retrieves DataFrame rows based on either index label or index position. This method combines the best features of the .loc[] and .iloc[] methods

- rename()    Method is called on a DataFrame to change the names of the index labels or column names

- columns()   Method is an alternative attribute to change the coloumn name

- drop()  Method is used to delete rows or columns from a DataFrame

- pop()   Method is used to delete rows or columns from a DataFrame

- sample()    Method pulls out a random sample of rows or columns from a DataFrame

- nsmallest()     Method pulls out the rows with the smallest values in a column

- nlargest()  Method pulls out the rows with the largest values in a column

- shape()     Method returns a tuple representing the dimensionality of the DataFrame

- ndim()  Method returns an ‘int’ representing the number of axes / array dimensions.
Returns 1 if Series, otherwise returns 2 if DataFrame

- dropna()    Method allows the user to analyze and drop Rows/Columns with Null values in different ways

- fillna()    Method manages and let the user replace NaN values with some value of their own

- rank()  Values in a Series can be ranked in order with this method

- query()     Method is an alternate string-based syntax for extracting a subset from a DataFrame

- copy()  Method creates an independent copy of a pandas object

- duplicated()    Method creates a Boolean Series and uses it to extract rows that have duplicate values

- drop_duplicates()   Method is an alternative option to identifying duplicate rows and removing them through filtering

- set_index()     Method sets the DataFrame index (row labels) using one or more existing columns

- reset_index()   Method resets index of a Data Frame. This method sets a list of integer ranging from 0 to length of data as index

- where()     Method is used to check a Data Frame for one or more condition and return the result accordingly. By default, the 
rows not satisfying the condition are filled with NaN value

## <br><br> Saving your changed DataFrame

### Excel vs. CSV (Comma Separated Values)

### Excel
- It is a binary file that holds information about all the worksheets in a workbook
- Files saved in excel cannot be opened or edited by text editors
- Excel consumes more memory while importing data
- As a developer, it's difficult to programmatically manipulate Excel files since the Excel is proprietary.

### CSV 
- CSV stands for Comma Separated Values. It is a plain text format with a series of values separated by commas
- CSV files can be opened or edited by text editors like notepad
- Importing CSV files can be much faster, and it also consumes less memory
- As a developer it's easy to programmatically manipulate CSV since, after all, they are simple text files.
