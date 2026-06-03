# Sales Analysis with Pandas

## Overview

This project analyzes a year's worth of sales data from an electronics store. Using Python, Pandas, and Matplotlib, the dataset is cleaned, processed, and analyzed to uncover valuable business insights such as top-performing months, cities, products, and customer purchasing patterns.

## Dataset

The dataset contains monthly sales records with the following fields:

- Order ID
- Product
- Quantity Ordered
- Price Each
- Order Date
- Purchase Address

Twelve monthly CSV files were merged into a single dataset for analysis.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## Data Cleaning

The following preprocessing steps were performed:

- Merged all monthly CSV files into one dataset
- Removed missing values
- Removed duplicate header rows
- Converted columns to appropriate data types
- Created new columns for analysis

## Feature Engineering

Additional columns were created to improve analysis:

### Month

Extracted the month from the order date.

### Sales

Calculated total sales for each order.

```python
all_data['Sales'] = all_data['Quantity Ordered'] * all_data['Price Each']
```

### City

Extracted city and state information from the purchase address.

### Hour

Extracted the purchase hour from the order timestamp.

## Business Questions Answered

### 1. What was the best month for sales?

**Answer:** December

**Total Sales:** $4,613,443.34

**Insight:** Holiday shopping and year-end promotions contributed significantly to increased sales.

---

### 2. Which city generated the most revenue?

**Answer:** San Francisco, CA

**Total Sales:** $8,262,203.91

**Insight:** San Francisco generated the highest revenue, likely due to its large customer base and strong technology market.

---

### 3. What time should advertisements be displayed?

**Peak Purchase Hours:**

- 11:00 AM
- 7:00 PM

**Recommendation:**

Run advertisements during:

- 10:00 AM – 12:00 PM
- 6:00 PM – 8:00 PM

These periods correspond to the highest customer activity.

---

### 4. What products are most often sold together?

Top product combinations:

| Product Combination | Count |
|--------------------|--------|
| iPhone + Lightning Charging Cable | 1005 |
| Google Phone + USB-C Charging Cable | 987 |
| iPhone + Wired Headphones | 447 |

**Insight:** Customers frequently purchase accessories together with smartphones, creating opportunities for cross-selling and product bundles.

---

### 5. What product sold the most?

**Answer:** AAA Batteries (4-pack)

**Insight:**

- Low-cost products sell in higher volumes.
- Batteries and charging accessories are frequently replaced and purchased repeatedly.
- Product price appears to have an inverse relationship with quantity sold.

## Visualizations

The project includes visualizations for:

- Monthly sales trends
- Revenue by city
- Customer activity by hour
- Frequently purchased product combinations
- Product sales versus product price

## Key Findings

- December had the highest sales revenue.
- San Francisco was the top-performing city.
- Customer purchasing activity peaks around midday and evening.
- Smartphones are commonly purchased with charging accessories.
- Batteries and charging cables are among the highest-selling products.

## Project Structure

```
SalesAnalysis/
│
├── Sales_Data/
│   ├── Sales_January_2019.csv
│   ├── Sales_February_2019.csv
│   ├── ...
│
├── Sales_Analysis.ipynb
├── all_data.csv
├── README.md
│
└── images/
    ├── monthly_sales.png
    ├── city_sales.png
    ├── hourly_orders.png
    └── product_sales.png
```

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/SalesAnalysis.git
```

Install required packages:

```bash
pip install pandas numpy matplotlib
```

Run the Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Sales_Analysis.ipynb
```

and run all cells.

## Future Improvements

- Profit analysis
- Weekly and seasonal sales trends
- Customer segmentation
- Product category analysis
- Interactive dashboards using Plotly or Streamlit
- Sales forecasting using Machine Learning

## Author

Lucky

A data analysis project demonstrating data cleaning, feature engineering, exploratory data analysis, and business insight generation using Python and Pandas.
