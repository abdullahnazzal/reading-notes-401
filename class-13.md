
# Linear Regressions

## **How to run Linear regression in Python scikit-Learn**:

**Exploring Boston Housing Data Set**

The first step is to import the required Python libraries into Ipython Notebook.

```py
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
```
**To convert boston.data into a pandas data frame.**

```py
data_frame.head()
```
***

**Create a model and fit it**

```py
model = LinearRegression()
model.fit(x, y)
model = LinearRegression().fit(x, y)

```
***

**Get results**

```py
r_sq = model.score(x, y)
print('coefficient of determination:', r_sq)

==> coefficient of determination: 0.715875613747954

print('intercept:', model.intercept_)

==> intercept: 5.633333333333329

print('slope:', model.coef_)

==> slope: [0.54]

```
**Predict response**

```py
y_pred = model.predict(x)
print('predicted response:', y_pred, sep='\n')

==> predicted response:
[ 8.33333333 13.73333333 19.13333333 24.53333333 29.93333333 35.33333333]
```
***
**To know more please [visit this page](https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/)**
****

