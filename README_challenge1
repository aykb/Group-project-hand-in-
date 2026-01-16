## Overview
This challenge focuses on cleaning and exploring a real smart-city energy dataset. The primary goal is to use k-means clustering to detect atypical days (potential outliers) for several buildings based on their energy consumption patterns.

## Dataset
We are utilizing the *Household Data* package from **Open Power System Data** (OPSD), specifically the 60-minute resolution data.

- **Package Page**: https://data.open-power-system-data.org/household_data/2020-04-15/
- **Direct CSV (60-minute, single index)**: `https://data.open-power-system-data.org/household_data/2020-04-15/household_data_60min_singleindex.csv`

## Challenge Steps
The following steps are covered in this notebook:

1.  **Load the OPSD Household Data**: The 60-minute household data is loaded into a pandas DataFrame, with `utc_timestamp` parsed as datetime and set as the DataFrame index.
2.  **Data-Quality Checks & Missing Values**: Missing values are computed, and a strategy is applied to handle them. Columns with more than 50% missing values are dropped, and remaining NaNs are filled using forward-fill and backward-fill methods.
3.  **Build a Daily Dataset for Several Buildings**: Specific `grid_import` columns for selected residential and public buildings are chosen. The hourly data is resampled to daily sums. The data is then transformed into a tidy long format, including `date`, `building_id`, `daily_grid_import_kwh`, `building_type`, and `location`.
4.  **k-means Clustering to Detect Atypical Days**: Feature vectors are created using `daily_grid_import_kwh` and `day_of_week`. These features are standardized with `StandardScaler`, and k-means clustering with `k=3` is applied. The resulting cluster labels are assigned back to the daily energy data.
5.  **Inspect Clusters and Outliers**: The size of each cluster is computed, and the smallest cluster is identified as the 
