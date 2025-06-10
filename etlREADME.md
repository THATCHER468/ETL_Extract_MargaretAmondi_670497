# ETL Extract Lab

## Description
This project implements a basic ETL (Extract, Transform, Load) process focused on extraction for a data warehousing assignment. It includes:
1.Full Extraction: Loads the entire `custom_data.csv` sales dataset and displays basic stats.
2.Incremental Extraction: Extracts only new or updated records since the last extraction, tracked via `last_extraction.txt`.
3.A synthetic dataset of 100 sales transactions (transaction ID, date, product, quantity, price).

## Tools Used
. Python 3
. pandas (for data handling)
. Jupyter Notebook (for implementation and documentation)

## How to Reproduce
1. Setup:
   - Clone this repository: `git clone https://github.com/THATCHER468/ETL_Extract_MargaretAmondi_670497.git`
   - Ensure Python 3 and pandas are installed (`pip install pandas`)
2. Dataset:
   - The dataset `custom_data.csv` is a synthetic sales dataset generated with Python.
   - It contains 100 records with columns: transaction_id, sale_date, product, quantity, price.
3. Run the Notebook:
   - Open `etl_extract.ipynb` in Jupyter Notebook: `jupyter notebook etl_extract.ipynb`
   - Run all cells to perform full and incremental extractions.
   - The notebook will read `custom_data.csv`, extract data, and update `last_extraction.txt`.
4. Expected Output:
   - Full extraction shows stats for all 100 rows.
   - Incremental extraction filters records after the timestamp in `last_extraction.txt`.

