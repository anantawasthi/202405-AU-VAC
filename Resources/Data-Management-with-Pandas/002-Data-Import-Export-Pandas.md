Data import and export are fundamental operations in data analysis and manipulation. Pandas provides efficient tools for importing data from various file formats, databases, and sources, as well as exporting data to different formats. Let's discuss these operations in detail along with examples.

### Data Import in Pandas:

#### 1. Importing from CSV Files:

```python
import pandas as pd
# Import data from a CSV file
df = pd.read_csv('data.csv')
```

#### 2. Importing from Excel Files:

```python
import pandas as pd
# Import data from an Excel file
df = pd.read_excel('data.xlsx', sheet_name='Sheet1')
```

#### 3. Importing from SQL Databases:

```python
import pandas as pd
from sqlalchemy import create_engine
# Create a connection to the database
engine = create_engine('sqlite:///example.db')
# Import data from a SQL table
df = pd.read_sql_table('table_name', con=engine)
```

#### 4. Importing from JSON Files:

```python
import pandas as pd
# Import data from a JSON file
df = pd.read_json('data.json')
```

#### 5. Importing from HTML Tables:

```python
import pandas as pd
# Import data from an HTML table
df = pd.read_html('https://example.com/data.html')[0]
```

### Data Export in Pandas:

#### 1. Exporting to CSV Files:

```python
import pandas as pd
# Export data to a CSV file
df.to_csv('output.csv', index=False)
```

#### 2. Exporting to Excel Files:

```python
import pandas as pd
# Export data to an Excel file
df.to_excel('output.xlsx', index=False)
```

#### 3. Exporting to SQL Databases:

```python
import pandas as pd
from sqlalchemy import create_engine
# Create a connection to the database
engine = create_engine('sqlite:///example.db')
# Export data to a SQL table
df.to_sql('table_name', con=engine, index=False, if_exists='replace')
```

#### 4. Exporting to JSON Files:

```python
import pandas as pd
# Export data to a JSON file
df.to_json('output.json', orient='records')
```

#### 5. Exporting to HTML Tables:

```python
import pandas as pd
# Export data to an HTML table
df.to_html('output.html', index=False)
```

These examples demonstrate how Pandas can be used to import data from various sources and export data to different formats, making it a versatile tool for data manipulation and analysis. By leveraging these functionalities, users can easily work with datasets from different sources and share their analysis results in a variety of formats.
