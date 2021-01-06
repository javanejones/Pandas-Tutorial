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

Concat= combine all worksheets into one dataframe exmple below:

- df = pd.concat(pd.read_excel('filename.xlsx', sheet_name=None, ignore_index=True))

Individual work sheets use for best results!! exmple below:

- df = pd.read_excel('filename.xlsx', sheet_name='sheetname')

#### or

- df = pd.read_excel('filename.xlsx', sheet_name=0)

- 0 represents sheet 1. 

View all worksheets in the file exmple below:

- df = pd.read_excel('filename.xlsx', sheet_name=None)

## Data Types

### object: str or mixed,	Usage =	Text or mixed numeric and non-numeric values

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

## <br><br>Data aggregation

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

## <br><br>Saving your changed DataFrame

### Excel vs. CSV(Comma Seperated Values)

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

