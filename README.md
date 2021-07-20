# Data Handling

### Practice And Resources

1) Hackerrank -- https://www.hackerrank.com/domains/python?filters%5Bsubdomains%5D%5B%5D=numpy
2) Numpy documentation -- https://numpy.org/doc/


### Numpy -- Array Processing Library 

<b>Inbuilt Functions</b>

1) **Shape** -- It specifies how many no of rows and columns are there in array.
2) **Reshape** -- It takes no of rows and columns as a values and convert arr into that rows and columns.
3) **Arange** -- It create 1-D array and It takes range from lower value to upper value and take also take step value in that.
4) **Copy** -- Copy function helps that it will not change original array after copy.
5) **Ones** -- It will create array of values with 1 and it also take datatype.
6) **Zeroes** -- It will create array of values with 0 and it also take datatype.
7) **Transpose** -- We can generate the transpostion of an array using this and it will not affect the original array but it will create a new array.
8) **Flattern** -- The Tool flatten creates a copy of the input array flattened to one dimension.
9) **Concatenate** -- Two or more arrays can be concatenated together using the concatenate functions with a tuple of the array to be joined and for 2-D array we can also specify the axis .
10) **Identity** -- It returns an identity array.
11) **eye** -- it returns a 2-D array with 1's as the diagonal and 0's elsewhere.
12) **Mathematics functions** --  

    1) Add, Subtract, Divide, Multiply, Power, Mod, Rint
    2) Min , Max 
    3) Mean , Variance , Standard Deviation
    4) Dot and Cross product of two arrays
    5) Inner and Outer product of two arrays

13) **Polynomials functions** --
    
    1) Poly -- It returns the coefficient of a polynomial with the given sequence of roots.
    2) Roots -- It returns the roots of a polynomial with the given coefficient.
    3) Polyint -- It returns the derivative of the specified order of a polynomial.
    4) Polyder -- It returns the derivative of the specified order of a polynomail.
    5) Polyval -- It evalutes the ploynomail at specific value.
    6) Polyfit -- It fits a polynomial of a specified order to a set of data using a least-squares approach.

14) **Linear Algebra** --
    
    1) Linalg.det -- It computes the determinant of an array.
    2) Linalg.eig -- It computes the eigenvalues and right eigenvectors of a square array.
    3) Linalg.inv -- It computes the (multiplicative) inverse of a matrix.
    
   
    
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Pandas Library 

Pandas is an open source, BSD-licensed library providing high-performance, easy-to-use data structure and data analysis tools for the python programming language.

```
<!-- Import libraries              -->
             import pandas as pd
             import numpy as np
```

#### Data Frames 

1) A two-dimensional labeled data structure with columns of potentially different types.
2) It Take 3 parameters -- data , Index , Columns.

``` 
Syntax

df = pd.DataFrame(data,Index,Column)

```

#### Data Series 

1) Pandas Series is a one-dimensional labeled array capable of holding data of any type (integer, string, float, python objects, etc.).
2) It take two parameter -- data , index.

```
Syntax

df = pd.Series(data,index)

```


Inbulid Functions and Methods

1) **.head()** -- It will give the top rows values.
2) **.loc** -- It is label-based, which means that you have to specify rows and columns based on their row and column labels.
3) **.iloc** -- It is integer position-based, so you have to specify rows and columns by their integer position values (0-based integer position).
4) **.value** -- It will convert data Frame into array.
5) **.isnull** -- It will check null values in data.
6) **sum()** -- It will give sum of specific data values.
7) **.value_counts()** -- returns object containing counts of unique values.
8) **.unique()** -- It is used to get unique values of Series object.
9) **.info()** -- It will give information about data like rows , columns etc.
10) **.describe()** -- is used for calculating some statistical data like percentile, mean and std of the numerical values of the Series or DataFrame. It analyzes both numeric and object series and also the DataFrame column sets of mixed data types.
11) **.corr()** -- It is used to find the pairwise correlation of all columns in the dataframe.
12) **.dropna(axis = 0 or 1)** -- It is used to remove missing values.
13) **.reindex()** -- It will replace index with new index values.
14) **.isna()** -- It is used to detect missing values.
15) **.fillna()** -- It is used to fill NA/NaN values using the specified method.
16) **.notna()** -- It detects existing/ non-missing values in the dataframe.


#### Reading different data Sources with the help of pandas

##### **CSV** 

It contains comma seperated values in the file.

```
<!-- import  -->
from io import StringIO, BytesIO
```

1) Reading CSV file

      StringIO and ByteIO --  module an in-memory file-like object. This object can be used as input or output to the most function that would expect a standard file object.
     
```
pd.read_csv(StringIO(data))
```

2) Read from specific columns 

```
df = pd.read_csv( StringIo(data) , usecols = None)
```

3) Convert data into CSV

```
df.to_csv(file)
```

4) Datatype of CSV data

```
df=pd.read_csv(StringIO(data),dtype=object)
```

5) Escapechar helps to remove a characters from data

```
pd.read_csv(StringIO(data),escapechar='\\')
```


##### **JSON** 

File contains key-value pair type data.

1) Reading JSON file

```
pf.read_json(data)
```

2) Convert Json to different json format

```
orient -- string, Indication of expected JSON string format

df.to_json(orient="index")

df.to_json(orient="records")
```

3) Convert data into json

```
df.to_json(data)
```


##### **HTML Content**

1) Reading file

```
df = pd.read_html(data)
```

2) Matching value

```
dfs = pd.read_html(url_mcc, match='')
```

3) Convert data into html content

```
df.to_html(data)
```


##### **EXCEL File**

1) Reading File

```
df = pd.read_excel(data)
```

2) Convert data into Excel format

```
df.to_excel(data)
```





















