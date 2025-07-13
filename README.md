# ETL Extract Lab

Name: Alfred Gakinya  
Student ID: 671579

## 🧾 Description
This project demonstrates the **extraction** phase of an ETL pipeline using Python and Jupyter. It includes full and incremental data extraction from a realistic dataset.

##⚙️ Tools Used
- Python
- pandas
- Jupyter Notebook

## 🔁 How to Reproduce
1. Clone the repo
2. Run `etl_extract.ipynb` in Jupyter
3. Dataset used: `custom_data.csv` (synthetic sales data with timestamps)
4. The notebook extracts and prints:
   - Full dataset
   - New records since the last timestamp
   - Updates `last_extraction.txt`

## Lab 5 – Load

### ✅ Loading Method Used:
We used **Pandas DataFrames** and saved the data as **Parquet files** – an efficient, columnar storage format.

### 🗂️ Output Files:
- `loaded_data/full_data.parquet`
- `loaded_data/incremental_data.parquet`

### 🔢 Sample Code:
```python
import pandas as pd

df = pd.read_csv("transformed_full.csv")
df.to_parquet("loaded_data/full_data.parquet", index=False)


