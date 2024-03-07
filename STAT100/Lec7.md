<div align="center">

# Data Visualization, Part II

</div>

# 1. Histogram and Overlaid Plots
## Displaying a Categorical Distribution
* ### The distribution of a variable (a column) describes the frequencies of its different values
* ### The group method counts the number of rows for each value in the column (e.g. the number of top movies released by each studio)
* ### Bar charts can display the distribution of a categorical variable (e.g. studios):
  * ### One bar for each category
  * ### Length of bar is the count of individuals in that category
  * ### You can choose the order of the bars
## Two types of distribution
* ### Bar Chart: Categorical vs. numerical
* ### Histogram: distribution of numerical
## Binning Numerical Balues
### Binning is counting the number of numerical values that lie within ranges, called bins.
* ### Bins are defined by their lower bounds (inclusive)
* ### The upper bound is the lower bound of the next bin
------------
# 2. How do we visualize the distribution of the number of streams?
## Basic code:
  ``` Python
  import pandas as pd
  import numpy as np
  import matplotlib.pyplot as plt
  import matplotlib as mpl
  df.plot(kind='hist',y=column_name)
  ```
  > The height of a bar is the number of values in the corresponding bin.
  > Optional: specify the number of bins with bins=. Use ec='w' to see where bins start and end more clearly.
  ``` Python
  df.plot(kind='hist', y='Streams', bins=20, ec='w');
  ```
## Custom bins
* ### We can specify our own bins with an array or list.
* ### It's good to do this, so that we know where the bins start and end.
* ### bins=np.arange(1, 9) creates the bins [1, 2), [2, 3), [3, 4), [4, 5), [5, 6), [6, 7), [7, 8].
> Note: last bin is inclusive!
> Warning: Data points not in any bin will not be included in the histogram.
