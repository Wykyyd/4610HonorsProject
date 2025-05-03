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

As expected, the curve is upwards sloping in the long-term. This means that investors demand higher yields for longer duration bonds. This curve provides a reference for future comparison of different conditions in subsequent worksheets. 

## Yield Curve at Key Dates
![Image](https://github.com/user-attachments/assets/59f371d2-86a1-4f35-ae02-ef1eba49694f)

**Analysis** 

This chart compares the U.S. Treasury yield curve at four points in time. The selected times are normal times (2016 post Global Financial Crisis), the COVID crash, the curve inversion peak, and recent highs (end of 2024). 

The COVID crash shows a significant drop in short term yields due to aggressive federal policy at the time. The "normal" curve shows a healthy upward sloping yield curve. The curve inversion peak shows an inverted yield curve meaning investors anticipate future economic  slowdown or a recession. We can see that things recovered at recent peaks, but the curve is relatively  flat indicating  there is still market uncertainty. 

## 10 Year Treasury vs Corporate Bond Yields
![Image](https://github.com/user-attachments/assets/6f895310-7d75-4349-b3aa-a75d4c613d79)

**Analysis** 

This chart compares the 10-year U.S. Treasury yield with corporate bond yields across different credit ratings (AAA to BB) over the period from 2015 to 2025. Corporate bond yields follow the yields of the U.S. Treasury, as demonstrated  by the graph. A risk premium is included based on how risky the bond is (AAA - BB, etc). During times of uncertainty such as 2020 
 or 2022, we can seek increased spikes in riskier bonds such as BB or BBB. The consistent gap between each rating shows how credit risk influences borrowing costs across the corporate bond market.

## Corporate Yield Spread Over 10 Year Treasury (2015-2025)
![Image](https://github.com/user-attachments/assets/8d66365a-7dc5-4821-aed6-7719387b2126)

**Analysis** 

This chart shows the average credit spread of corporate bonds over the 10-year U.S. Treasury yield from 2015 to 2025, segmented by credit rating (AAA, A, BBB, and BB). This represents the return investors demand for taking on risk above the risk-free rate. During times of economic stress, the spread widened greatly. This can be seen in 2020 and 2022 especially. High credit rating bonds remained fairly stable. Investors demanded more compensation for companies viewed to have a higher default risk. This reflects risk sentiment regarding lower credit ratings. A particularly interesting point on the graph is the point in which the spread for A bonds dipped the spread for AAA bonds. This is counterintuitive as AAA bonds are considered safer and should have a lower yield. This imbalance indicates a short lived market failure in the bond market. This may be an opportunity for investors to generate excess return or alpha. 

## Credit Spreads by Rating at Key Dates
![Image](https://github.com/user-attachments/assets/b29155b2-4351-477d-810a-84d4ae254bca)

**Analysis** 

This chart compares credit spreads across different bond ratings (AAA, A, BBB, BB) at four points in time. The selected times "normal" times (2016 post Global Financial Crisis), the COVID crash, the curve inversion peak, and recent highs (end of 2024). As anticipated, lower rated bonds have higher spreads for any of the selected times. Investors must be compensated for the risk they take. We can see a trend that the lower credit rating bonds spike much higher during times of market turmoil (2020, 2022). The spread grew past 8% during the COVID crash. The graph clearly exemplifies the shift in investor sentiment during changing economic conditions. 

## Dashboard
![Image](https://github.com/user-attachments/assets/7aa2623c-1770-42f2-a1ab-a3583266ba54)

The dashboard aggregates all the aforementioned charts. This reflects a comprehensive view of U.S. Treasury yields and corporate bond yields from 01/01/2015 to 01/01/2025. These visualizations highlight the impact of monetary policy, market stress, and credit risk on bond yields. 

## Tableau Packaged Workbook

[Download 4610HonorsProject.twbx](https://github.com/wykyyd/4610HonorsProject/raw/main/4610HonorsProject.twbx)

