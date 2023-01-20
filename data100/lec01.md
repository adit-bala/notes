## EDA (Exploratory Data Analysis)

-> Process of transforming, visualizing, and summarizing data to 
    - Build/confirm understanding of data and its provenance (origin of data, methodology by which data is produced)
    - Identify and address potential issues in the data
    - Inform the subsequent analysis
    - Discover potential hypotheses

**EDA** is an *open-ended* analysis:
    - Informal, no specific idea to look for
    - understand where data is coming from

**Data Cleaning**:
    - Process of transforming **raw data** to facilitate subsequent analysis

## Intro to Pandas

**What is it**: Data analysis library (similar to NumPy)

### Series, DataFrames, and Indices

#### Series
**Definition**: 1D labeled array data, containing sequence of values of same type and **index**

```python
# Initializing
s = pd.Series([-1, 10, 2]) -> (index, value) -> [(0, -1), (1, 10), (2, 2)]

# Changing index - done during initialization or afterwards
s = pd.Series([4, -2, 0, 6]), index = ["a", "b", "c", "d"]

# Accessing by index -> returns `value`
s["a"] 
# rv -> 4, type: int

# Accessing multiple items 
s[["a", "c"]] 
# rv ->  [("a", 4), ("c", 0)], type: Series

# Filtering condition -> apply vectorized boolean operation to our Series
s[s > 0]
# rv -> [("a", 4), ("d", 6)], type: Series


```

#### DataFrame

**Definition**: 2D tabular data with both row and column labels, can be thought of as a dictionary of Series all sharing the same index

```python
# Initiliazing DataFrame
elections = pd.read_csv("elections.csv")
```

A (statistical) population from which we draw **samples**. Each sample has certain **features**

##### DataFrame API

```python
# Syntax: pandas.DataFrame(data, infex, columns)

# From list and column names
pd.DataFrame([1,2,3], columns=["Numbers"])

# multiple columns
pd.DataFrame([[1,"one"], [2, "two"]], columns=["Numbers", "Description"])

# From dictionary
pd.DataFrame({'Fruit': ['Strawberry', 'Orange'], 'Price': [5.49, 3.99]})

# From Series
pd.DataFrame({"A-column":<SERIES>})

pd.DataFrame(<SERIES>)
<SERIES>.to_frame()

```

#### Index

**Definition**: Sequence of row/column labels, can also be non-numeric (ex. String)

```python
elections.set_index("Candidate", in_place=True)
# in_place -> override
```

**Notes on Index**:
    - Index: numbers, non-numeric
    - Column Names: unique



### Slicing with loc, iloc, and []

#### loc

**Definition**: Operator used to select 

```python
# get first five heads
elections.head(5)

# equivalent syntax to above
elections.loc[0:4]

# get last five heads
elections.tail(5)

# equivalent to above
elections.loc[-5:]

# get specific rows and columns
# Syntax : _.loc[[<INDEX>], [<COLUMN>]], if <COLUMN> is not a list, then we return Series
elections.loc[[87], ["Year"]]
# rv -> row 87 with column Year
```

#### iloc

**Definition**: Select items by **number**

```python
# same as loc but columns as index
elections.iloc[[1, 2, 3], [0, 1, 2]]

# columns as range
elections.iloc[[1, 2, 3], 0:3]

# selecting all
elections.iloc[:, 0:3]
```

#### []

**Definition**: could be slice of row numbers, list of column numbers, or a single column label















