# Data Handling

### Resources

1) Numpy documentation -- https://numpy.org/doc/
2) Pandas documentation -- https://pandas.pydata.org/docs/
3) MatplotLib documentation -- https://matplotlib.org/
4) Seaborn Documentation -- https://seaborn.pydata.org/

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
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
    6) Sin and Cos functions

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
<!-- Import libraries -->
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

#### Pickling

All pandas objects are equipped with to_pickle methods which use Python’s cPickle module to save data structures to disk using the pickle format.

```
1) Reading file

df=pd.read_pickle(data)

2) Convert file

df_excel.to_pickle(data)
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# MatplotLib Library

Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like Tkinter, wxPython, Qt, or GTK+.

Some of the major Pros of Matplotlib are:

   1) Generally easy to get started for simple plots
   2) Support for custom labels and texts
   3) Great control of every element in a figure
   4) High-quality output in many formats
   5) Very customizable in general

                
```
import matplotlib.pyplot as plt

%matplotlib inline

```

**Inbuild Functions and Methods**

1) **Plotting x and y points**

It is used to draw points in a diagram. It takes x,y parameters and we also give color parameter.

```
import matplotlib.pyplot as plt
%matplotlib inline
import numpy as np

xpoints = np.array([1, 8])
ypoints = np.array([3, 10])

plt.plot(xpoints, ypoints,c="g")  # c is for color 

```


2) **Markers**

The keyword argument marker to emphasize each point with a specified marker.

**list of Markers**

1) 'o' -- Circle
2) '*' -- Star
3) '.' -- Point
4) ',' -- Pixels
5) 'x' -- X
6) 'X' -- X (filled)
7) '+' -- Plus
8) 'P' -- Plus (filled)
9) 's' -- Square
10) 'D' -- Diamond
11) 'd' -- Diamond (thin)
12) 'p' -- Pentagon
13) 'H' -- hexagon
14) 'h' -- Hexagon
15) 'v' -- Triangle Down
16) '^' -- Triangle Up
17) '<' -- Triangle Left
18) '>' -- Triangle Right
19) '1' -- Tri down
20) '2' -- Tri Up
21) '3' -- Tri Left
22) '4' -- Tri Right
23) '|' -- Vline
24) '_' -- Hline

```
Example

import matplotlib.pyplot as plt
%matplotlib inline

import numpy as np

xpoints = np.array([1, 8])
ypoints = np.array([3, 10])

plt.plot(xpoints, ypoints,marker="*")

```

** Format String FMT**

1) You can use also use the shortcut string notation parameter to specify the marker.
2) This parameter is also called fmt, and is written with this syntax: **marker|line|color**

```
Example 

import matplotlib.pyplot as plt
%matplotlib inline

import numpy as np

ypoints = np.array([3, 8, 1, 10])

plt.plot(ypoints, 'o:r')

```


3) **LineStyle**

The Keyword argument linestyle or shorter ls to change the style of the plotted line

```
Example

plt.plot(ypoints, linestyle = 'dashed')
```

**Shorter Syntax**

1) linestyle can be written as **ls**
2) dotted can be written as **:**
3) dashed can be written as **--**

**List of Styles**

1) 'solid' (dotted) -- **"-"**
2) 'dotted'         -- **":"**
3) 'dashed'         -- **"--"**
4) 'dashdot'        -- **"-."**
5) 'None'           -- **"or"**


**Line Width**

The keyword argument linewidth or the shorter lw to change the width of the line

```
Example

import matplotlib.pyplot as plt
import numpy as np

ypoints = np.array([3, 8, 1, 10])

plt.plot(ypoints, linewidth = '20.5')
plt.show()
```


4) **Labels and Title**

**X-label, Y-label and Title**
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

plt.plot(x, y)

plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")
plt.title("Sports Watch Data")

plt.show()
```

**Set Font Properties for Title and Labels**

The **fontdict** parameter in xlabel() , ylabel() and title() to set font properties for the title and labels.

```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

font1 = {'family':'serif','color':'blue','size':20}
font2 = {'family':'serif','color':'darkred','size':15}

plt.title("Sports Watch Data", fontdict = font1)
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y)
plt.show()
```

**Position the Title**

the **loc** parameter in title() to postion the title.

legal values are: 'left', 'right', and 'center'. Default value is center.

```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

plt.title("Sports Watch Data", loc = 'left')
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)
plt.show()
```


5) **Grid Lines**

The grid() function to add grid lines to the plot

```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

plt.grid()
plt.plot(x, y)
plt.show()
```

**Specify Which Grid Lines to Display**

The axis parameter in the grid() function to specify which grid lines to display.
Legal values are: 'x', 'y' and 'both'. Default value is 'both'.

```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

plt.grid(axis='x')
plt.plot(x, y)
plt.show()
```

**Set Line Properties for the Grid**

The line properties of the grid, like this: grid(color = 'color', linestyle = 'linestyle', linewidth = number).

```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90])
y = np.array([240, 250, 260])

plt.grid(color = 'green', linestyle = '--', linewidth = 0.5)
plt.plot(x, y)
plt.show()
```

6) **Subplots**

With the subplots() function you can draw multiple plots in one figure

1) The subplots() function takes three arguments that describes the layout of the figure.
2) The layout is organized in rows and columns, which are represented by the first and second argument.
3) The third argument represents the index of the current plot.

```
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)

plt.show()
```

**Super Title**

Add a title to the entire figure with the suptitle() function.

```
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)

plt.suptitle("My Graph")
plt.show()
```

## Scatter

1) **Creating Scatter plots**
The scatter() function plots one dot for each observation. It needs two arrays of the same length, one for the values of the x-axis, and one for values on the y-axis

```
import matplotlib.pyplot as plt
import numpy as np

x = np.array([5,7,8])
y = np.array([99,86,87])

plt.scatter(x, y , c ='g')
plt.show()
```

2) **ColorMap**

A colormap is like a list of colors, where each color has a value that ranges from 0 to 100.

There are many colorbar are available.

```
import matplotlib.pyplot as plt
import numpy as np

x = np.array([5,7,8])
y = np.array([99,86,87])
colors = np.array([0, 10, 20])

plt.scatter(x, y, c=colors, cmap='viridis')

plt.colorbar()
plt.show()
```

3) **Size**

change the size of the dots with the s argument

```
import matplotlib.pyplot as plt
import numpy as np

x = np.array([5,7,8])
y = np.array([99,86,87])
sizes = np.array([10, 20,30])

plt.scatter(x, y, s = sizes)

plt.colorbar()
plt.show()
```

4) **Alpha**

adjust the transparency of the dots with the alpha argument.

```
import matplotlib.pyplot as plt
import numpy as np

x = np.array([5,7,8])
y = np.array([99,86,87])
sizes = np.array([10, 20,30])

plt.scatter(x, y, s = sizes , alpha=0.5)

plt.colorbar()
plt.show()
```


## Bars Charts

The bar() function takes arguments that describes the layout of the bars.
The categories and their values represented by the first and second argument as arrays.

```
x = ["APPLES", "BANANAS"]
y = [400, 350]
plt.bar(x, y)
```

1) **Horizontal Bars**

The bars to be displayed horizontally instead of vertically, use the barh() function.

```
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.barh(x, y)
plt.show()
```

2) **Color, Width and Height**

```
<!-- For horizontal bars, use height instead of width -->

import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.barh(x, y,color='red', width=0.1, height=0.1)
plt.show()
```

## **Histograms**

A histogram is a graph showing frequency distributions.
It is a graph showing the number of observations within each given interval.

The hist() function will use an array of numbers to create a histogram, the array is sent into the function as an argument.

```
import matplotlib.pyplot as plt
import numpy as np

x = np.random.normal(170, 10, 250)

plt.hist(x)
plt.show() 
```


## **Pie Charts**

1) **Creating Chart**

pie() function to draw pie charts

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])

plt.pie(y)
plt.show()
```

2) **Labels and Colors**

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
mycolors = ["black", "hotpink", "b", "#4CAF50"]

plt.pie(y, labels = mylabels, colors = mycolors)
plt.show()
```

3) **Start Angle**

The default start angle is at the x-axis, but you can change the start angle by specifying a startangle parameter.

The startangle parameter is defined with an angle in degrees, default angle is 0.

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels, startangle = 90)
plt.show() 
```

4) **Explode**

The explode parameter, if specified, and not None, must be an array with one value for each wedge.
Each value represents how far from the center each wedge is displayed.

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
myexplode = [0.2, 0, 0, 0]

plt.pie(y, labels = mylabels, explode = myexplode)
plt.show() 
```

5) **Shadow** 

Add a shadow to the pie chart by setting the shadows parameter to True.

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
myexplode = [0.2, 0, 0, 0]

plt.pie(y, labels = mylabels, explode = myexplode, shadow = True)
plt.show()
```

6) **Legend and With Header**

To add a list of explanation for each wedge, use the legend() function.

```
import matplotlib.pyplot as plt
import numpy as np

y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)
plt.legend(title="Four Fruits")
plt.show() 
```

## **Box Plot**

A Box Plot is also known as Whisker plot is created to display the summary of the set of data values having properties like minimum, first quartile, median, third quartile and maximum.

1) **Creating Box Plot

```
matplotlib.pyplot.boxplot(data, notch=None, vert=None, patch_artist=None, widths=None)

```

2) Attributes and Values

      1) Data -- array or sequence of array to be plotted
      2) notch -- optional parameter accepts boolean values
      3) vert -- optional parameter accepts boolean values false and true for horizontal and vertical plot respectively
      4) bootstrap -- optional parameter accepts int specifies intervals around notched boxplots
      5) usermedians -- optional parameter accepts array or sequence of array dimension compatible with data
      6) position -- optional parameter accepts array and sets the position of boxes
      7) widths -- optional parameter accepts array and sets the width of boxes
      8) patch_artist -- optional parameter having boolean value
      9) Labels -- sequence of strings sets label for each dataset
      10) meanline -- optional having boolean value try to render meanline as full width of box
      11) order -- optional parameter sets the order of the boxplot

```
data = [np.random.normal(0, std, 100) for std in range(1, 4)]

# rectangular box plot
plt.boxplot(data,vert=True,patch_artist=False);
```



















