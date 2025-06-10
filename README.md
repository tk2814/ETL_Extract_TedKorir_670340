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


##  How to Reproduce
git clone https://github.com/tk2814/ETL_Extract_TedKorir_670340.git
cd ETL_Extract_TedKorir_670340
