# Superstore Performance Dashboard - Tableau

## Project Overview

This project is an interactive 2-page Tableau dashboard built on the Sample Superstore dataset from 2014 to 2017. It analyzes sales, profitability, customer performance, returns, discounting, and shipping to identify areas where revenue and profitability diverge.

The dashboard uses parameter-driven KPIs, hover-based drill-downs, and cross-filtering to support detailed exploration of business performance.

## Objectives

- Analyze sales, profit, orders, margin, and average order value.
- Compare sales and profit trends over time.
- Identify differences between revenue and profitability across categories and regions.
- Analyze the impact of discounting on profitability.
- Evaluate returns and their potential impact on profit.
- Examine whether shipping speed contributes to returns or profitability.
- Provide customer-level performance details.

## Dataset

- **Source:** Sample Superstore Dataset
- **Tables:** `Orders_Clean` and `Returns_Clean`
- **Period:** 2014-2017
- **Size:** Approximately 10,000 order line items
- **Categories:** Furniture, Office Supplies, and Technology
- **Returns:** Presence-based return data using Order ID. There is no explicit Yes/No return field.

## Tools & Technologies

| Tool / Technique | Purpose |
|------|---------|
| Tableau Desktop | Dashboard development and visualization |
| Tableau Parameters | Dynamic year selection and KPI comparisons |
| Calculated Fields | Business metrics and comparisons |
| Viz-in-Tooltip | Category to Sub-Category drill-down |
| Dual-Axis Charts | Sales and profit trend analysis |
| Dashboard Filters | Interactive data exploration |
| Navigation Objects | Navigation between dashboard pages |

## Data Cleaning & Transformation

The dataset was prepared using cleaned Orders and Returns tables.

- Used `Orders_Clean` and `Returns_Clean` as the primary data sources.
- Prepared order, sales, profit, discount, quantity, and customer fields for analysis.
- Used Order ID presence in the Returns table to identify returned orders.
- Calculated AOV directly in Tableau because the source `AOV` column was empty.
- Created calculated fields for current-year and previous-year comparisons.
- Created margin calculations for profitability analysis.

## Data Analysis

The analysis focuses on the relationship between revenue and profitability.

Key analyses include:

- Sales and profit trends over time.
- Sales and profit performance by state.
- Category and sub-category profitability.
- Regional and segment profitability.
- Impact of discount levels on profit.
- Returns volume and profit exposure.
- Average fulfillment time by category and region.
- Customer-level sales, quantity, profit, and discount performance.

## Dashboard

### Page 1 - Sales & Profitability Overview

The first dashboard page includes:

- **KPI Row:** Total Sales, Total Profit, Total Orders, Margin %, and AOV.
- **YoY Comparison:** Dynamic year selection using a `SELECT YEAR` parameter.
- **Sales & Profit Over Time:** Dual-axis bar and line chart showing monthly sales and profit trends.
- **Sales & Profit by State:** Geographic view using Sales for circle size and Profit/Margin for color.
- **Category Performance:** Category-level sales and profit composition.
- **Sub-Category Drill-Down:** Viz-in-Tooltip for detailed sub-category analysis.
- **Returns Analysis:** Return volume by category and region.
- **Shipping Analysis:** Average fulfillment time by category and region.

### Page 2 - Customer Records

The second dashboard provides a customer-level detail table containing:

- Region
- City
- Country
- Sales
- Quantity
- Profit
- Discount

Tableau Navigation objects are used to move between the two dashboard pages.

## Key Insights

- **Margin does not always follow Sales.** Furniture generates approximately $720K to $836K in revenue but operates at around a 2.5% margin compared with approximately 17% for Office Supplies and Technology.
- **Regional profitability varies significantly.** The Central region has the weakest overall margin, with Consumer performance being a key contributor to the gap.
- **Higher discounting reduces profitability.** Discount bands above 20% are unprofitable in aggregate despite the intention of increasing sales volume.
- **Returns risk differs from returns volume.** Technology has fewer returned items than Office Supplies but represents a larger share of profit dollars exposed to returns because of its higher-value products.
- **Shipping speed does not explain performance differences.** The analysis did not find a clear relationship between fulfillment time, returns, and profitability.

## Dashboard Screenshots
PAGE 1
<img width="1642" height="606" alt="image" src="https://github.com/user-attachments/assets/d0ec8569-549c-4ff7-ba69-477954a8a0f9" />
<img width="1637" height="567" alt="image" src="https://github.com/user-attachments/assets/58550ddd-3343-46e8-a612-efe882b5abb9" />

PAGE 2 
<img width="1645" height="838" alt="image" src="https://github.com/user-attachments/assets/58f09153-8c21-49ea-a290-76b7e66e0139" />


## Conclusion

The Superstore Performance Dashboard uses Tableau to analyze the relationship between sales, profitability, discounts, returns, shipping, and customer performance. The analysis shows that high revenue does not necessarily translate into strong profitability. By combining interactive visualizations, parameters, calculated fields, drill-downs, and detailed customer records, the dashboard provides a structured view of the factors influencing retail performance.
