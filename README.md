# SmartCleaner 🧹

SmartCleaner is a Python library that **automatically cleans Pandas DataFrames**.

## Features
- Remove duplicate rows
- Fill missing values (mean/median/mode/zero)
- Standardize column names
- Convert date-like strings to datetime (planned)
- Optional outlier removal

## Installation
```bash
pip install smartcleaner
```

## Usage
```python
import pandas as pd
from smartcleaner import SmartCleaner

df = pd.DataFrame({
    "Name": ["Alice", "Bob", "Alice", None],
    "Age": [25, None, 25, 30],
    "Salary": [50000, 60000, 50000, None]
})

sc = SmartCleaner(df)
print(sc.remove_duplicates())
print(sc.fill_missing("mean"))
print(sc.standardize_columns())
print(sc.remove_outliers("zscore"))
print(sc.get_cleaned_data())
```
