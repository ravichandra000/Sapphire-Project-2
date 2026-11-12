# Sapphire-Project-2
# Supermart Grocery Sales Dashboard (Excel)

An interactive Excel dashboard that helps management understand sales, profit, products, discounts and geographic performance in one place, without going through the complete dataset.

Built as a data analytics student project during an internship at **Sapphire IQ**.

<img width="872" height="652" alt="Screenshot 2026-11-12 193943" src="https://github.com/user-attachments/assets/70b5a323-0f65-4f1a-8a56-d03ec8994338" />


## Project context

The management team wanted a simple dashboard to answer important business questions about the grocery business. This project analyses the Supermart sales data (9,994 orders) using PivotTables, a calculated field, charts and slicers, and brings the results together on one `Dashboard` sheet.

## Objectives and what the dashboard answers

| Objective | Business question | Tasks covered |
|---|---|---|
| 1. Overall sales performance | How is the overall grocery business performing? | Total sales and profit, category share of sales, sales over time, sales by region |
| 2. Product performance | Which products and categories are driving sales and profit? | Top categories and sub-categories, high-sales but low-profit products |
| 3. Profit and discount | How are discounts and profit related to business performance? | Profit by category and region, relationship between discount and profit |
| 4. Geographic performance | Which locations are contributing most to the business? | Sales by state and city, high-sales but low-profit locations |

## Dashboard contents

The `Dashboard` sheet contains 9 charts and 4 slicers.

| Chart | Type | Answers |
|---|---|---|
| Category over sales | Pie chart | Category share of total sales |
| Sales over profit | Column chart | Sales and profit by category |
| Sales changes over time | Line chart | Sales trend by year |
| Region over sales | Bar chart | Sales by region |
| Sub-category over sales | Bar chart | Top sub-categories by sales |
| Sales vs profit margin by sub-category | Scatter chart | Sub-categories with high sales but low margin |
| Discount vs profit margin | Column chart | Profit margin for each discount band |
| Sales vs profit margin by city | Scatter chart | Cities with high sales but low margin |
| Top 10 cities by sales | Bar chart | Highest-selling cities |

**Slicers:** Year, Region, Category and Sub Category. Use them to filter the dashboard and clear a slicer with its filter icon.

## Workbook structure

| Sheet | Purpose |
|---|---|
| `Dashboard` | Final dashboard with all charts and slicers |
| `Obj_1` | PivotTables for Objective 1: total sales and profit, category, year and region |
| `Obj_2` | PivotTables for Objective 2: category and sub-category sales, profit margin by sub-category |
| `Obj_3` | PivotTables for Objective 3: profit by category and region, category by region table, discount bands |
| `Obj_4` | PivotTables for Objective 4: sales and profit margin by city |
| `Supermart Grocery Sales - Retai...` | Raw data (9,994 rows) plus a helper `Year` column |
| `Sheet2`, `Detail1` to `Detail4` | Helper sheets (the `Detail` sheets are hidden) |

## Key techniques

- **PivotTables** for every summary, with a shared data source
- **Calculated field** `Profit Margin = Profit / Sales`, so margin is always correct for any grouping
- **Helper column** `Year = YEAR(Order Date)` for yearly trends
- **Grouping** of the Discount field into bands (0.10-0.15, 0.15-0.20, 0.20-0.25, 0.25-0.30, 0.30-0.35)
- **Charts** linked to the pivot results, with **slicers** for interactivity

## Key insights

- Total sales are **14,956,982** and total profit is **3,747,121**, a margin of **25.05%**.
- Sales grew every year, from 2.98M in 2015 to 4.98M in 2018 (+67%).
- The seven categories are evenly spread, between 13.6% and 15.2% of sales. Eggs, Meat & Fish leads, and Snacks earns the most profit.
- Health Drinks (1.05M) and Soft Drinks (1.03M) are the top sub-categories. Spices (23.82%) and Masalas (24.23%) have the lowest margins among the high-selling sub-categories.
- Profit margin stays between 24.8% and 25.7% in every discount band, so discount level shows no visible effect on profit in this data.
- West (32.1%) and East (28.4%) bring in about 60% of sales. The top city is Kanyakumari (706,764), but its margin of 24.37% is below the 25.05% average.

## How to use

1. Download or clone this repository.
2. Open `Supermart_Grocery_Sales_-_Dashboard.xlsx` in Microsoft Excel (2013 or later, because slicers are used).
3. Go to the `Dashboard` sheet and use the slicers to filter the charts.
4. To see how a number was built, open the matching `Obj_` sheet and click inside its PivotTable.

## Dataset

Supermart Grocery Sales retail analytics dataset: 9,994 order lines across 24 cities and 23 sub-categories, covering 2015 to 2018.

Columns: Order ID, Customer Name, Category, Sub Category, City, Order Date, Region, Sales, Discount, Profit, State, plus the added `Year` column.

## Notes and limitations

- The **North** region has only one order, so it is not meaningful for comparisons.
- All orders are from **one state** (Tamil Nadu), so the geographic view works at city level.
- **Region** is a sales label and not a geographic area: every city has orders under several regions.
- Margins are close across categories, sub-categories and cities (about 24% to 26%), so the "low profit" items differ from the average by small amounts.
- No effect of discount on profit is unusual for real retail data, so it is reported as what this dataset shows and not as a general rule.

## Project structure

```
Supermart-Grocery-Sales-Dashboard/
|-- README.md
|-- Supermart_Grocery_Sales_-_Dashboard.xlsx
|-- images/
|   `-- dashboard.png
`-- data/
    `-- Supermart_Grocery_Sales_-_Retail_Analytics_Dataset.csv
```

## Built with

- Microsoft Excel: PivotTables, calculated fields, slicers and charts

## Author

RAVI CHANDRA SATTI
Data Analytics Intern, Sapphire IQ
