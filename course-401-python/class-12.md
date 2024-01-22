# *Course 401 Python, Entry 12: Pandas*




### Explain the purpose and basic functionality of the Pandas library. What are some common operations that can be performed on data using Pandas, and how do they contribute to data analysis and manipulation?

Pandas library works to process spreadsheets. It's like Excel for Python. One of the most common uses is data processing and plotting. This is much like running different Excel functions on data and then creating a graph. However, unlike Excel, Pandas offers the ability to expand upon this data manipulation with ease and no limitations. For example, run a loop on some dataset and then tabulate it and graph it.

Common fucntions:

head() - used to traverse dataset

info() - total number of rows, name of columns, data type, missing values. 

describe - some basic statistic data, like mean and median. Counts missing data cells.

shape - describes the dimensions of the data, columns and rows.

sortvalues - sort by a column

Also, dropduplicates, groupby, and pivotables.

### What are the primary data structures in Pandas, and how do they differ in terms of use cases?

The primary data structures are DataFramd and Series.

**Series (1D)**: A simple array of values.

**Labels**: Can be provided a label via the "index" argument. If none is provided, the values are labeled just using index integers.

**Objects**: Dictionary-like objects can also be created using Series. In this case, the keys are the labels.

**DataFrames (2D)**: Are a multi-dimentional tables, or an array of arrays. The keys likewise act as labels in the these key/value pairs, the values being arrays.

Generally speaking, the two are split as follows:

*Series* - homogenous data type, size-immutable

*DataFrame* - heterogenous, size-mutable

### Describe the process of loading a dataset into a Pandas DataFrame. What are some common file formats that can be used, and which Pandas functions are utilized to read these formats?

First, import pandas, `import pandas as pd`.

Data can be read via:

```
data = pd.read_csv('my_file.csv')
```

And written via:

```
data = pd.to_csv('my_file.csv')
```

This is the most popular, but others include, excel, json, and pickle. The respective functions are .read_excel, .read_json, .read_pickle since, and  .read_csv respectively. The writing functions for these are .to_excel, .to_json, .to_pickle.

## Things I want to know more about

I have a little experience with this in the past actually. I think the best use case is taking data that is processed in ways that can't easily be done in Excel, and then otherwise pushing it to Excel for further work.
