# ETL Midterm Project 

## 1. Project Overview

This ETL (Extract, Transform, Load) mini-project demonstrates a practical pipeline for handling sales-related datasets. The project involves extracting raw and incremental data, applying meaningful transformations to clean and enrich the datasets, and finally loading the processed data into structured storage formats (Parquet files).

The project is organized into three main phases, each handled in separate Jupyter notebooks.

---

## 2. ETL Phases

### 📘 `EXTRACT – etl_extract.ipynb` – Extract Phase
- Loads the `raw_data.csv` and `incremental_data.csv` files from the `data/` folder.
- Displays `.head()`, `.info()`, and checks for missing values and duplicates.
- Observations are noted and raw files are saved in the appropriate directory.

### 🧹 `TRANSFORM – etl_transform.ipynb` – Transform Phase
- Applies at least four meaningful transformations:
  - Removed duplicate rows
  - Handled missing values using appropriate methods (e.g., median imputation)
  - Created new columns such as `total_price` (quantity × unit_price)
  - Converted date columns to datetime format
- Transformed datasets are saved in `transformed/` as:
  - `transformed_full.csv`
  - `transformed_incremental.csv`
  - Images
  ![Chart](images\Screenshot 2025-06-24 182617.png)
  ![Chart](images\Screenshot 2025-06-24 182644.png)
  ![Chart](images\Screenshot 2025-06-24 182657.png)
  

### 💾 `LOAD – etl_load.ipynb` – Load Phase
- Loads the transformed CSVs into Parquet format using `pandas.to_parquet()`.
- Files are saved to `loaded/` as:
  - `full_data.parquet`
  - `incremental_data.parquet`
- Previews the stored data using `pd.read_parquet().head()`.

---

## 3. Tools Used

- Python 3.x
- Jupyter Notebook
- pandas
- Parquet (`.parquet` files for optimized storage)

---

## 4. How to Run the Project

Follow the steps below to run this ETL (Extract → Transform → Load) project on your local machine.

---

### 🧰 Requirements

You will need the following:

- Python 3.x installed
- Jupyter Notebook or JupyterLab
- Python libraries:
  - `pandas`
  - `pyarrow` (for Parquet support)
  - `matplotlib` and `seaborn` (for optional data visualization)

You can install the required libraries using:

```bash
pip install pandas pyarrow matplotlib seaborn

- clone the repository to your local machine and run all the files
