# Customer Segmentation Project

## Overview
This project performs customer segmentation analysis using clustering techniques on Ulabox (online grocery delivery service) order data from 2017. The goal is to identify distinct customer groups based on their purchasing behavior and product preferences to enable targeted marketing strategies.

## Dataset
**File:** `ulabox_orders_with_categories_partials_2017.csv`

The dataset contains 14 columns with customer order information:

### Column Descriptions
- **customer**: Unique customer identifier
- **order**: Unique order identifier
- **total_items**: Number of products purchased in the order
- **discount%**: Discount/fee amount (negative values indicate delivery charges or fees)
- **weekday**: Day of the week the order was placed
- **hour**: Time of day the order was placed
- **Food%**: Percentage of spending on non-fresh food (grocery products like sugar, coffee, oats)
- **Fresh%**: Percentage of spending on fresh food (milk, fruits, vegetables)
- **Drinks%**: Percentage of spending on beverages (wine, vodka, scotch, soft drinks)
- **Home%**: Percentage of spending on home accessories
- **Beauty%**: Percentage of spending on beauty products
- **Health%**: Percentage of spending on health products (supplements, medicines)
- **Baby%**: Percentage of spending on baby products
- **Pets%**: Percentage of spending on pet products

## Data Preprocessing

### Steps Performed:
1. **Data Loading & Exploration**
   - Loaded CSV file and performed initial data inspection
   - Verified data types (all numerical)
   - Checked for null values and duplicates (none found)

2. **Customer-Level Aggregation**
   - Aggregated individual orders to customer level (34.13% unique customers)
   - Dropped order-specific columns:  `weekday`, `hour`, `discount%`

3. **Feature Engineering**
   - Recalculated percentages at customer level based on total items purchased

4. **Final Features**
   - `total_orders`: Number of orders placed by customer
   - `total_items`: Total items purchased across all orders
   - `Food%`, `Fresh%`, `Drinks%`, `Home%`, `Beauty%`, `Health%`, `Baby%`, `Pets%`: Percentage breakdown by product category

## Methodology

### Correlation Analysis
- Analyzed relationships between features to identify patterns and potential data leakage

### Clustering
- **Algorithm**: K-Means Clustering
- Identifies distinct customer segments based on purchasing behavior
- Enables customer profiling 

