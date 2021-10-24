
# Data Analysis

## **JupyterLab**:

**JupyterLab is a next-generation web-based user interface for Project Jupyter.**

JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. 

For a demonstration of JupyterLab and its features, you can view this video:


***
**[Video](https://www.youtube.com/watch?v=A5YyoCKxEOU)**
****

***
**To know more please[visit this page](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)**
****

----------------
## **NumPy**:

**NumPy** is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

```bash
import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))

print(wines[:3])

output--> 

[['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], ['7.4', '0.7', '0', '1.9', '0.076', '11', '34', '0.9978', '3.51', '0.56', '9.4', '5'], ['7.8', '0.88', '0', '2.6', '0.098', '25', '67', '0.9968', '3.2', '0.68', '9.8', '5']]

```

***
**To know more please [visit this page](https://www.dataquest.io/blog/numpy-tutorial-python/)**
****