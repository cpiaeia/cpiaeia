<div align="center">
  
# Data Visualization

<br>
</div>

# 1. Why visualize?
* ## Computers are better than humans at crunching numbers, but humans are better at identifying visual patterns.
* ## Visualizations allow us to understand lots of data quickly – they make it easier to spot trends and communicate our results with others
* ## There are many types of visualizations: scatter plots, line plot, bar charts, etc.
* ## The right choice depends on the type of data.

# 2. Terminology
## Individual (row): Person/place/thing for which data is recorded.
## Variable (column): Something that is recorded for each individual, a.k.a. a "feature".
* ### Numerical: It makes sense to do arithmetic with the values.
* ### Categorical: Values fall into categories.
# 3. Classification of Data
* ## Cross-sectional / Time series / Panel data
* ## Quantitative vs Qualitative Data
# 4. Types of Visualization
* ## Scatter Plot: numerical vs. numerical.
* ## Line Plot: sequential numerical (time) vs. numerical.
* ## Bar Chart: categorical vs. numerical.
* ## Histogram: distribution of numerical.
* ## Response variable (dependent)- Y-axis the variable we wish to explain mapped to the vertical axis
* ## Explanatory (independent)- X-axis helps to explain changes in the response variable placed on the horizontal axis
-------------
## Libraries import:
  ``` Python
  import pandas as pd
  import numpy as np
  import matplotlib.pyplot as plt
  import matplotlib as mpl
  ```
# 5. Scatter Plots
## Basic code:
  ``` Python
  df.plot(kind='scatter',x=x_column_for-horizontal,y=y_column_for_vertical)
  ```
> Tip: If you add a semicolon (;) after a call to .plot, it will hide the weird output 
# 6. Line Plots
## Basic code:
  ``` Python
  df.plot(kind='line',x=x_column_for-horizontal,y=y_column_for_vertical)
  ```
> Tip: if you want the x-axis to be the index, omit the x=argument!
# 7. Bar Charts
## Basic code:
  ``` Python
  df.plot(kind='barh',x=x_column_for-horizontal,y=y_column_for_vertical)
  ```
* ### Bar charts visualize a single numerical variable.
* ### In a bar chart,t he thickness and spacing of bars is arbitrary.
* ### Order of the categorical labels doesn't matter.
* ### The “h” in “barh” stands for "horizontal".
* ### Easier to read labels this way.
* ### In the previous chart, we set y='Streams' even though streams are measured by x-axis length
> Additional function: .str.contains('Searching_string') . It can return strings with 'Searching_string'
