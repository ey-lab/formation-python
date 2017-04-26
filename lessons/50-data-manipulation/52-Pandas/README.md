# Pandas
Pandas is a Python package providing high-performance, easy-to-use data structures and data analysis tools. It is mainly used in high level programming and is based on NumPy. Among other things, it contains

- A fast and efficient DataFrame object for data manipulation based on NumPy
- Highly optimized for performance, with critical code paths written in Cython or C
- Tools for reading and writing data between in-memory data structures and different formats: CSV and text files, Microsoft Excel, SQL databases, and the fast HDF5 format
- Flexible reshaping and pivoting of data sets
- Intelligent label-based slicing, fancy indexing, and subsetting of large data sets
- Aggregating or transforming data with a powerful group by engine allowing split-apply-combine operations on data sets
- High performance merging and joining of data sets
- Hierarchical axis indexing provides an intuitive way of working with high-dimensional data in a lower-dimensional data structure
- Time series-functionality: date range generation and frequency conversion, moving window statistics, moving window linear regressions, date shifting and lagging

## Install Pandas
### Mac / Linux
Pre-built binary package can be installed using pip.
```
pip install pandas
```

### Windows
For Windows users consider using a free Python distribution such as Anaconda. Pandas comes installed with it.


## Pandas types

DataFrame is a container for Series, and Panel is a container for DataFrame objects.

| Dimensions  | Name  | Description |
|----------|------|---|
| 1 | Series  | 1D labeled homogeneously-typed array |
| 2 | DataFrame | General 2D labeled, size-mutable tabular structure with potentially heterogeneously-typed columns |
| 3 | Panel | General 3D labeled, also size-mutable array |

## Mutability and copying of data

All pandas data structures are value-mutable (the values they contain can be altered) but not always size-mutable. The length of a Series cannot be changed, but, for example, columns can be inserted into a DataFrame. However, the vast majority of methods produce new objects and leave the input data untouched. In general, though, we like to favor immutability where sensible.

