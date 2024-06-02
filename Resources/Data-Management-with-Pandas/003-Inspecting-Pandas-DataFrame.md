Inspecting a Pandas DataFrame is an essential step in data analysis, as it allows you to understand the structure, content, and properties of your dataset. In this detailed write-up, we'll explore various methods and attributes provided by Pandas to inspect a DataFrame, along with examples.

### 1. Viewing the DataFrame:

#### `.head()` and `.tail()`:

These methods allow you to preview the first few or last few rows of the DataFrame.

```python
import pandas as pd

# Create a DataFrame
data = {'Name': ['John', 'Anna', 'Peter', 'Linda', 'Bob'],
        'Age': [25, 35, 30, 28, 40],
        'Salary': [50000, 60000, 55000, 52000, 70000]}
df = pd.DataFrame(data)

print(df.head())  # View the first 5 rows
print(df.tail(3))  # View the last 3 rows
```

### 2. Checking DataFrame Information:

#### `.info()`:

Provides a concise summary of the DataFrame, including column data types and non-null counts.

```python
print(df.info())
```

#### `.shape`:

Returns a tuple representing the dimensions of the DataFrame (rows, columns).

```python
print(df.shape)
```

#### `.columns`:

Returns a list of column names in the DataFrame.

```python
print(df.columns)
```

### 3. Descriptive Statistics:

#### `.describe()`:

Generates descriptive statistics for numerical columns, including count, mean, min, max, and percentiles.

```python
print(df.describe())
```

### 4. Data Types and Missing Values:

#### `.dtypes`:

Returns the data types of each column in the DataFrame.

```python
print(df.dtypes)
```

#### `.isnull()` and `.notnull()`:

These methods return a boolean DataFrame indicating missing (null) or non-missing values.

```python
print(df.isnull())   # True for missing values, False otherwise
print(df.notnull())  # False for missing values, True otherwise
```

### 5. Checking for Duplicates:

#### `.duplicated()`:

Returns a boolean Series indicating duplicate rows.

```python
print(df.duplicated())
```

#### `.drop_duplicates()`:

Removes duplicate rows from the DataFrame.

```python
df.drop_duplicates(inplace=True)
```

### Conclusion:

Inspecting a Pandas DataFrame allows you to gain insights into the structure, content, and quality of your data. By utilizing the methods and attributes discussed above, you can effectively understand, explore, and clean your dataset, paving the way for meaningful analysis and decision-making in your data science projects.
