# Airline Delay Analysis

## Project Overview

This project explores U.S. airline flight records to understand flight operations, delays, cancellations, and diversions. Three Jupyter notebooks document data inspection, cleaning and preprocessing, and exploratory data analysis (EDA). The analysis uses Python and prepared CSV files stored in the repository.

## Objectives

- Inspect the flight dataset and select fields relevant to delay analysis.
- Prepare the selected data for analysis by handling missing values and data types.
- Explore flight status, airline and airport activity, delay patterns and causes, cancellations, and time-based trends.

## Dataset Used

The repository includes a raw CSV with 2,000,000 flight records and 109 columns, along with selected and cleaned versions. The selected dataset contains 27 fields covering flight dates, airlines, origin and destination, delays and delay causes, cancellation and diversion status, and distance. The cleaned dataset contains 1,998,955 records after rows missing origin or destination state were removed.

## Tools & Technologies

- Python 3.12
- Jupyter Notebook
- pandas and NumPy
- Matplotlib and Seaborn
- CSV

## Project Workflow

1. **Data loading and understanding:** Load the raw CSV, inspect its shape, columns, data types, missing values, duplicates, and descriptive statistics.
2. **Feature selection:** Keep 27 fields related to dates, airlines, airports, delays, flight status, and distance.
3. **Cleaning and preprocessing:** Remove rows missing origin or destination state; fill missing delay-cause values with zero; convert `FlightDate` to datetime and selected text fields to categorical types; save the cleaned CSV.
4. **Exploratory analysis:** Summarize and visualize flight status, airline and airport activity, delay distributions and causes, cancellations, and monthly and weekly delay patterns.

## Files in the Repository

- `dataset/raw/airline_delay.csv`: Raw flight records (2,000,000 rows, 109 columns).
- `dataset/processed/airline_delay_selected.csv`: Selected 27 analysis fields before cleaning.
- `dataset/processed/airline_delay_cleaned.csv`: Cleaned selected data used by the EDA notebook.
- `notebooks/1. Data_Understanding.ipynb`: Inspects the raw data and creates the selected dataset.
- `notebooks/2. Data Cleaning & Preprocessing.ipynb`: Cleans the selected dataset and saves the cleaned file.
- `notebooks/3. Exploratory Data Analysis (EDA).ipynb`: Performs summary analysis and creates charts.
- `.gitignore`: Lists files and folders excluded from version control.

## Key Insights

The EDA notebook reports that most flights were completed, delay distributions are right-skewed, and NAS delays affect the most flights. Late aircraft delays contribute the most total delay minutes. The notebook also identifies variation in delays by airline, airport, month, and day of week.

## How to Run/View the Project

1. Install Python 3.12 and Jupyter Notebook, plus `pandas`, `numpy`, `matplotlib`, and `seaborn`.
2. Open the notebooks in order from the `notebooks` folder.
3. Run each notebook's cells from top to bottom. The first notebook reads the raw CSV and writes the selected CSV; the second reads that selected file and writes the cleaned CSV; the EDA notebook reads the cleaned CSV.

The project contains no SQL scripts or Power BI (`.pbix`) file.
