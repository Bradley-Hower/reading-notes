# *Course 401 Python, Entry 11: Data Analysis*

## Jupyter Navigation shortcuts

+ a - Add above
+ b - Add below
+ c - Copy
+ x - Cut
+ v - Paste

--

+ dd - Delete
+ z - Undo
+ shift z - Redo
+ y - Code
+ m - Markdown

---

+ Enter - Enter cell
+ Shift enter - Run cell

Frame equations with `$` to mark code.

Execution order appears to the left. All code runs as one file.

Selective run code by looing at `run`  menu.

## Numpy Tutorial - Table of Contents

[https://www.dataquest.io/blog/numpy-tutorial-python/](https://www.dataquest.io/blog/numpy-tutorial-python/)

- Numpy 2-Dimensional Arrays
  - Creating A NumPy Array
  - Alternative NumPy Array Creation Methods
  - Using NumPy To Read In Files
  - Indexing NumPy Arrays
  - Slicing NumPy Arrays
  - Assigning Values To NumPy Arrays
- 1-Dimensional NumPy Arrays
- N-Dimensional NumPy Arrays
  - NumPy Data Types
  - Converting Data Types
- NumPy Array Operations
  - Single Array Math
  - Multiple Array Math
  - Broadcasting
- NumPy Array Methods
- NumPy Array Comparisons
  - Subsetting
- Reshaping NumPy Arrays
  -Combining NumPy Arrays

**What are the key features and benefits of Jupyter Lab, and how does it differ from Jupyter Notebook?**

Jupyter Notebooks has the great ability to allow for note taking and to run code within the same document. Jupyter supports many file formats. This allows for a great level of integration with other work and code.

**What are the main functionalities provided by the NumPy library, and how can it be useful in Python programming, particularly for scientific computing and data manipulation tasks?**

The main functionalities is its ability to build and manipulate multi-dimentional arrays. In additon, there is a lot of high-level mathematical function support. This allows for massive data computations.

**Explain the basic structure and properties of NumPy arrays, and provide examples of how to create, manipulate, and perform operations on them.**

Structures of arrays that are supported are 1-D, 2-D, and N-D (multi-dimentional). The syntax is as follows to set the dimentions:

1D - shape: (4,) - Columns four cells
2D - shape: (2,3) - Rows two cells, Columns three cells
3D - shape: (4, 3, 2) - Rows four cells, Columns three cells, Slices two cells

Data is stored as matrixes, array of arrays.

### Create a Numpy Array

`import numpy as np`

```
a = np.array([1, 2, 3])           # 1D array
b = np.array([[1, 2, 3], [4, 5, 6]])  # 2D array
```

### Manipulating Arrays

```
g = np.reshape(a, (3, 1))  # Reshape 'a' to a 3x1 array
h = np.concatenate((a, e))  # Concatenate arrays 'a' and 'e'
```

### Operations

Some operations include "random", "genfromtxt", "sum", and more.

## Things I want to know more about

Some more solid use cases for Numpy.
