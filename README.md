# README: Weekly U.S. Diesel Retail Prices Dataset

## Overview
This dataset contains **weekly retail prices for U.S. No. 2 Diesel fuel** in **dollars per gallon**. The data spans from **March 21, 1994** to **November 2, 1998**, recording the weekly average price of diesel fuel across the United States. It serves as a valuable resource for analyzing trends in fuel prices, evaluating historical economic conditions, and building time-series forecasting models.

---

## Dataset Information
- **File Name:** `Weekly_U.S.Diesel_Retail_Prices.csv`
- **Number of Records:** 1425 rows (one row per week)
- **File Size:** ~28.3 KB
- **Columns:**
  1. **`Week of`**: The date (in `YYYY-MM-DD` format) representing the start of the week.
  2. **`Weekly U.S. No 2 Diesel Retail Prices Dollars per Gallon`**: The average diesel price for that week in dollars per gallon.

---

## Column Descriptions

1. **`Week of`**:
   - Represents the **start date of the week** when the fuel price was recorded.
   - Format: `YYYY-MM-DD`

2. **`Weekly U.S. No 2 Diesel Retail Prices Dollars per Gallon`**:
   - The **average retail price of No. 2 Diesel fuel** across the U.S. for that particular week.
   - Unit: **Dollars per gallon**.
   - Some values may show floating-point precision (e.g., `1.1159999999999999`), which can be rounded to 2-3 decimal places if needed for further analysis.

---

## Sample Data

| Week of     | Weekly U.S. No 2 Diesel Retail Prices Dollars per Gallon |
|-------------|----------------------------------------------------------|
| 1994-03-21  | 1.106                                                    |
| 1994-03-28  | 1.107                                                    |
| 1994-04-04  | 1.109                                                    |
| 1994-04-11  | 1.108                                                    |
| 1994-04-18  | 1.105                                                    |

---

## Usage Suggestions
This dataset can be used for:
1. **Time-Series Forecasting:** Build predictive models to forecast diesel prices for future weeks.
2. **Trend Analysis:** Analyze long-term trends and seasonality in U.S. diesel prices.
3. **Economic Impact Studies:** Study the relationship between fuel prices and economic indicators during the given timeframe.
4. **Anomaly Detection:** Detect significant fluctuations in fuel prices over time.

---

## How to Use the Dataset
1. **Loading the Dataset** (using Python and Pandas):
   ```python
   import pandas as pd

   # Load the dataset
   df = pd.read_csv("Weekly_U.S.Diesel_Retail_Prices.csv")

   # Display the first few rows
   print(df.head())
   ```

2. **Data Preprocessing:**
   - Handle any floating-point precision if needed (e.g., `round()` function in Python).
   - Convert the `Week of` column to **datetime format** for time-series analysis:
     ```python
     df['Week of'] = pd.to_datetime(df['Week of'])
     ```

3. **Visualization Example** (using Matplotlib):
   ```python
   import matplotlib.pyplot as plt

   # Plot diesel prices over time
   plt.figure(figsize=(10, 5))
   plt.plot(df['Week of'], df['Weekly U.S. No 2 Diesel Retail Prices Dollars per Gallon'], label='Diesel Price')
   plt.xlabel('Date')
   plt.ylabel('Price (Dollars per Gallon)')
   plt.title('Weekly U.S. Diesel Retail Prices (1994-1998)')
   plt.legend()
   plt.show()
   ```

---

## License
Refer to the **LICENSE.txt** file in the repository for licensing information.

---

## Acknowledgments
This dataset is part of the **Weekly_US_Diesel_Retail_Prices_Prediction** project by **Duo-Keyboard-Koalition**.

---

## Contact
If you encounter any issues or have questions about this dataset, feel free to open an issue in the [GitHub repository](https://github.com/Duo-Keyboard-Koalition/Weekly_US_Diesel_Retail_Prices_Prediction).