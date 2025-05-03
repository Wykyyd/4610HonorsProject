# 4610 Honors Project

## Datasets

This project utilizes historical bond yield data from multiple sources, with a focus on U.S. Treasury securities and corporate bonds. All datasets were cleaned, transformed, and combined using Power Query and Tableau to enable yield curve analysis, credit risk comparisons, and time-series trend evaluation. 

### 1. Bank of America ICE Corporate Bond Indices (via FRED)
- **Source**: Federal Reserve Economic Data (FRED)
- **Ratings Used**: AAA, AA, BBB, BB
- **Frequency**: Daily
- **Date Range**: 01/01/2015 – 01/01/2025

### 2. U.S. Treasury Constant Maturity Yield Curve (via FRED)
- **Source**: U.S. Department of the Treasury via FRED
- **Maturities**: 1M, 3M, 6M, 1Y, 2Y, 3Y, 5Y, 7Y, 10Y, 20Y, 30Y
- **Frequency**: Daily
- **Date Range**: 01/01/2015 – 01/01/2025

### 3. 10-Year Treasury Yield (Single Maturity) – DGS10
- **Source**: FRED (Series ID: DGS10)
- **Description**: Market yield on U.S. Treasury securities at 10-Year constant maturity
- **Frequency**: Daily
- **Date Range**: 01/01/2015 – 01/01/2025

### 4. Corporate Yields + 10Y Treasury Dataset (Merged in Power Query)
- **Description**: Combined the Bank of America corporate bond yield data (AAA, AA, BBB, BB) with the 10-Year Treasury constant maturity yield (`DGS10`) using `Date` as the key
- **Purpose**: Enabled credit spread analysis directly in Tableau by calculating differences such as:
  - BB – AAA Yield
  - BB – 10Y Treasury Yield
- **Note**: Spread calculations were performed inside Tableau, not pre-processed in Power Query

## Average Yield Curve
![Image](https://github.com/user-attachments/assets/3853d26a-799a-431c-9584-831b0942add6)

**Analysis** 

This chart shows the average U.S. Treasury yield curve from 01/01/2015 to 01/01/2025. The yield curve was calculated across all maturities ranging from 1 month to 30 years. The curve reflects interest rate expectations over time. 

As expected, the curve is upwards sloping in the long-term. This means that investors demand higher yields for longer duration bonds. This curve provides a reference for future comparison of different coniditons in subsequent worksheets. 

## Yield Curve at Key Dates
![Image](https://github.com/user-attachments/assets/59f371d2-86a1-4f35-ae02-ef1eba49694f)

**Analysis** 

This chart compares the U.S. Treasury yield curve at four points in time. The selected times are the normal times (2016 post Global Financial Crisis), the COVID crash, the curve inversion peak, and recent highs. 



## 10 Year Treasury vs Corporate Bond Yields
![Image](https://github.com/user-attachments/assets/6f895310-7d75-4349-b3aa-a75d4c613d79)

**Analysis** 

## Corporate Yield Spread Over 10 Year Treasury (2015-2025)
![Image](https://github.com/user-attachments/assets/8d66365a-7dc5-4821-aed6-7719387b2126)

**Analysis** 

## Credit Spreads by Rating at Key Dates
![Image](https://github.com/user-attachments/assets/b29155b2-4351-477d-810a-84d4ae254bca)

**Analysis** 

## Dashboard
![Image](https://github.com/user-attachments/assets/7aa2623c-1770-42f2-a1ab-a3583266ba54)

The dashboard aggregates all the aforementioned charts. This reflects a comprehensive view of U.S. Treasury yields and corporate bond yields from 01/01/2015 to 01/01/2025. These visualizations highlight the impact of monetary policy, market stress, and credit risk on bond yields. 

## Tableau Packaged Workbook

[Download 4610HonorsProject.twbx](https://github.com/wykyyd/4610HonorsProject/raw/main/4610HonorsProject.twbx)

