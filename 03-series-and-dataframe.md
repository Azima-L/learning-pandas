## Series & DataFrame
Pandas organizes data through two fundamental data structures: **Series** and **DataFrames**, which form the foundation for working with and analyzing data in the library.

<br>

---

### What is Series?

A Series in Pandas is a one-dimensional, labeled data structure. It contains a single column of data, where each value is associated with an index or row label.

Example:
```python
import pandas as pd

data = ["Apple", "Banana", "Orange"]
s = pd.Series(data, index=['a','b','c'])

print(s)
```

Output:
```text
        s
a   Apple
b  Banana
c  Orange
dtype: str
```

<br>

---

### How about DataFrame?

A DataFrame in Pandas is a two-dimensional, labeled data structure. It consists of rows and multiple columns, with each column can be of different types of data. Think of DataFrame as an Excel or Google Sheets spreadsheet, but inside Python.

Example:
```python
import pandas as pd

data = {
    'Name': ["Ali", "Sarah", "Bob", "John"],
    'Age': [30, 23, 20, 25],
    'Department': ["Engineer", "HR", "Marketing", "Engineer"]
    }
df = pd.DataFrame(data)

print(df)
```

Output:
```text
    Name  Age  Department
0    Ali   30    Engineer
1  Sarah   23          HR
2    Bob   20   Marketing
3   John   25    Engineer
```

<br>

---

*Note: Homogeneous vs. Heterogeneous:*

*Series are Homogeneous: Think of a Series as one column where all values share the same data type, such as numbers or text. Mixed types are allowed, but pandas converts the column to `object`, reducing performance and disrupting mathematical operations.*

*DataFrames are Heterogeneous: A DataFrame is the whole spreadsheet. It connects multiple columns together, meaning different columns can hold completely different data types side by side.*