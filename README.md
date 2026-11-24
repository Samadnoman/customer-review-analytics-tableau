# Flipkart Product Review Analysis: Data Cleaning, EDA and Tableau Dashboard

An analysis of 9,374 customer reviews of Bluetooth headsets from boAt, OnePlus, Realme and U&I, sold on the Flipkart online store. The project covers data cleaning in Excel, exploratory data analysis, choosing key performance indicators (KPIs), and an interactive two-page dashboard in Tableau.

Built for the Relational Database module of my MSc in Data Analytics and completed in April 2026.

## Project at a glance

| | |
|---|---|
| **Data** | Flipkart product reviews from Kaggle: 9 variables, 9,374 rows (9,205 after cleaning) |
| **Products** | 9 headset models from 4 brands: boAt, OnePlus, Realme and U&I |
| **Review period** | Mainly 2019 to 2020 |
| **Tools** | Microsoft Excel (cleaning and statistics), Tableau (dashboard) |
| **KPIs** | Average Rating, Total Number of Reviews, Positive Review Rate, Brand Popularity Index |
| **Completed** | April 2026 (uploaded to GitHub in November 2026) |

## What I did

1. **Planned the analysis.** Chose rating as the outcome variable, with brand, product model, location and review date as explanatory variables. Defined the KPIs and sketched the dashboard before building it ([Planned Analysis](docs/Planned_Analysis.pdf)).
2. **Cleaned the data in Excel.** Removed duplicate reviews (9,374 down to 9,205 rows), dealt with missing values, fixed incorrect formats and formatted the columns ([EDA and Data Cleaning](docs/Exploratory_Data_Analysis_and_Data_Cleaning.pdf)).
3. **Explored the data.** Calculated descriptive statistics for ratings and votes, and wrote a data dictionary for all 9 variables.
4. **Built the Tableau dashboard.**
   - **Page 1, overall product analysis:** KPI cards, brand popularity, average rating by brand, number of reviews by product model and review trend over time.
   - **Page 2, brand-level analysis:** filters for brand, product model, rating and review date, plus a rating-threshold parameter for what-if analysis of the Positive Review Rate.

## Key figures (cleaned data)

| Brand | Reviews | Average rating | Rated 4 or 5 stars |
|---|---|---|---|
| boAt | 3,737 | 4.07 | 77.1% |
| Realme | 2,777 | 4.03 | 77.1% |
| OnePlus | 1,876 | 4.27 | 83.7% |
| U&I | 815 | 4.10 | 78.4% |
| **All brands** | **9,205** | **4.10** | **78.6%** |

boAt has the most reviews, so it's the most popular brand by engagement, while OnePlus has the highest average rating and the highest share of positive reviews.

## Repository structure

```
data/
  raw/flipkart_product_reviews_raw.csv            Original Kaggle data, 9,374 rows
  cleaned/flipkart_product_reviews_cleaned.xlsx   Cleaned data used in Tableau, 9,205 rows
tableau/
  flipkart_product_review_dashboard.twbx          Packaged Tableau workbook (opens in Tableau Desktop or Tableau Public)
docs/
  Planned_Analysis (.docx and .pdf)               Planned analysis, KPIs and dashboard sketch
  Exploratory_Data_Analysis_and_Data_Cleaning     Data dictionary, cleaning steps and descriptive statistics
```

## How to view the dashboard

Download `tableau/flipkart_product_review_dashboard.twbx` and open it in Tableau Desktop or the free Tableau Public app. The data is packaged inside the workbook, so you don't need to connect anything.

## Related project

The [Sports Hall Event MongoDB project](https://github.com/Samadnoman/sports-hall-events-mongodb-part1) was completed for the same module.

## Data source and licence

The review data is the public Flipkart product reviews dataset from Kaggle. My code, documents and workbook are released under the [MIT Licence](LICENSE).
