# ETL_Extract_TedKorir_670340

##  Student Info
**Full Name:** Ted Korir 
**Student ID:** 670340

---

##  Project Description
This project demonstrates a basic ETL (Extract, Transform, Load) pipeline using Python. The focus is on data **extraction**, specifically:
- Full extraction of all data records
- Incremental extraction based on timestamp
- Simulating and storing the last extraction time

The notebook reads a dataset containing 50  sales and transaction data, filters records based on timestamps, and updates that were self generated on vs code.

---

##  Tools Used
- Python 
- pandas
- Jupyter Notebook
- Git + GitHub
  
## How to run the notebook
Open etl_extract.ipynb in Jupyter Notebook or VS Code

Run the notebook cells step-by-step

The notebook will:

Load and display full dataset

Read last_extraction.txt to simulate previous run

Extract only new records based on timestamp

Update the last_extraction.txt file with the latest timestamp

##  Transformations Applied

The following data transformations were performed on both the full and incremental datasets:

1. **Cleaning**
   - Removed rows with missing (NaN) values using `dropna()`.
   - Removed duplicate records using `drop_duplicates()`.

2. **Enrichment**
   - Added a new column `total_price`, calculated as:
     ```
     total_price = quantity × unit_price
     ```

3. **Structural Changes**
   - Standardized column names: converted to lowercase, replaced spaces with underscores.
   - Converted `order_date` column to datetime format using `pd.to_datetime()`.


  ## Lab 5 – Load

### Loading Method Used:
- Used Parquet for both the full and incremental transformed datasets.

### Output Location:
- Both Parquet files are saved inside the `loaded_data/` directory:
  - `loaded_data/full_data.parquet`
  - `loaded_data/incremental_data.parquet`

### Example Python Load Code:
```python
import pandas as pd

# Load CSV
df = pd.read_csv('transformed_full.csv')

# Save as Parquet
df.to_parquet('loaded_data/full_data.parquet', index=False)





##  How to Reproduce
git clone https://github.com/tk2814/ETL_Extract_TedKorir_670340.git
cd ETL_Extract_TedKorir_670340
