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






















