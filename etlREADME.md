# ETL Extract and Transform Lab

## Description
This project implements a basic ETL (Extract, Transform, Load) process focused on extraction and transformation of synthetic sales dataset, as part of a data warehousing assignment. 

It includes:
1. Full Extraction: Loads the entire `custom_data.csv` sales dataset and displays basic stats.
2. Incremental Extraction: Extracts only new or updated records since the last extraction, tracked via `last_extraction.txt`.
3. Transformation: Applies data cleaning, enrichment, and categorization to both full and incremental datasets.
4. A synthetic dataset of 100 sales transactions (transaction ID, date, product, quantity, price).

## Transformation Techniques Applied
1. Cleaning: Removed duplicate rows from datasets.
2. Enrichment: Added `total_price` column (`quantity * price`).
3. Categorization: Created `price_category` column to label items as "Low", "Medium", or "High" based on price.

## Load (`etl_load.ipynb`)-LAB 5
- Loaded the transformed data
- Saved it to efficient Parquet format using `pandas.to_parquet()`
- Previewed results using `pd.read_parquet().head()`
- sample code `python `: full_data.to_parquet('loaded_data/full_data.parquet', index=False)

## Saved files into `loaded_data/` folder as:
- `full_data.parquet`
- `incremental_data.parquet`

## Tools Used
. Python 3
. pandas (for data handling)
. Jupyter Notebook (for implementation and documentation)
. parquet via pyrraw

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
   - 


