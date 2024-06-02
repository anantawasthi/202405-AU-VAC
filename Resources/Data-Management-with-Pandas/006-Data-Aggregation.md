Data aggregation in Pandas involves computing summary statistics or aggregating data based on specific criteria. Let's explore detailed examples of data aggregation:

### Example 1: Computing Summary Statistics for Numeric Columns

```python
import pandas as pd

# Sample DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Age': [25, 30, 35, 40],
        'Salary': [50000, 60000, 70000, 80000]}
df = pd.DataFrame(data)

# Compute summary statistics for numeric columns
summary_stats = df.describe()

print("Summary Statistics for Numeric Columns:")
print(summary_stats)
```

### Example 2: Grouping and Aggregating Data by a Categorical Column

```python
# Group data by 'Gender' column and compute average age and salary
grouped_data = df.groupby('Gender').agg({'Age': 'mean', 'Salary': 'mean'})

print("\nGrouped Data and Aggregated Statistics:")
print(grouped_data)
```

### Example 3: Applying Custom Aggregation Functions

```python
# Define custom aggregation function
def range_func(x):
    return x.max() - x.min()

# Apply custom aggregation function to 'Salary' column
custom_agg = df['Salary'].agg(range_func)

print("\nCustom Aggregation Result:")
print(custom_agg)
```

### Example 4: Aggregating Data Using Pivot Tables

```python
# Create a pivot table to compute mean salary by gender and age group
pivot_table = df.pivot_table(index='Gender', columns=pd.cut(df['Age'], bins=[20, 30, 40, 50]), values='Salary', aggfunc='mean')

print("\nPivot Table with Aggregated Data:")
print(pivot_table)
```

### Example 5: Aggregating Data with GroupBy and Multiple Functions

```python
# Group data by 'Gender' column and apply multiple aggregation functions
grouped_data = df.groupby('Gender').agg({'Age': ['mean', 'median'], 'Salary': ['min', 'max']})

print("\nGrouped Data with Multiple Aggregation Functions:")
print(grouped_data)
```

### Example 6: Rolling Aggregations for Time Series Data

```python
# Sample DataFrame with time series data
date_range = pd.date_range(start='2022-01-01', end='2022-12-31')
time_series_data = pd.DataFrame({'Date': date_range, 'Value': range(len(date_range))})

# Compute rolling mean over a window of 30 days
rolling_mean = time_series_data.rolling(window=30, on='Date').mean()

print("\nRolling Mean for Time Series Data:")
print(rolling_mean)
```

These examples demonstrate various techniques for aggregating data in Pandas, including computing summary statistics, grouping and aggregating data by categorical columns, applying custom aggregation functions, using pivot tables, performing rolling aggregations for time series data, and more. By leveraging these aggregation capabilities, users can gain valuable insights from their datasets and perform advanced data analysis tasks efficiently.
