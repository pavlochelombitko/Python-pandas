# Retail sales analysis: your business brief

You are a junior analyst for BrightDesk, a fictional Slovak retailer selling accessories, stationery, home goods and electronics. The manager is planning next quarter's promotions and wants evidence from the previous quarter.

This is synthetic practice data, not real company sales. File: `DB/retail_business_sales.csv`. It contains 600 sales from 1 July to 30 September 2026. There are 20 products, four regions and two channels (Online and Store). All monetary values are EUR excluding VAT. Every row is one sale of one product, potentially multiple units. Each sale has a unique ID. There are no returns or missing values in this exercise.

## What the columns mean

| Column | Meaning |
|---|---|
| sale_id | Unique sale identifier. Count these to count sales, not units. |
| date | Sale date in YYYY-MM-DD format. |
| product | Product name. The same product appears in many sales. |
| category | Accessories, Stationery, Home or Electronics. |
| region | Customer region, represented by Bratislava, Kosice, Zilina or Nitra. |
| channel | Online or Store. |
| price | Selling price per unit before discount, in EUR. |
| unit_cost | Purchase cost to the retailer per unit, in EUR. |
| quantity | Units sold in this sale. |
| discount_pct | Percentage discount: 10 means 10%, not 0.10. Applies to every unit in the row. |

## The business calculations

Create your own columns for these calculations. Use `revenue` to mean revenue AFTER discounts throughout this project.

- Revenue before discount = price multiplied by quantity.
- Revenue = price multiplied by quantity multiplied by (1 minus discount_pct divided by 100).
- Cost of goods sold = unit_cost multiplied by quantity.
- Gross profit = revenue minus cost of goods sold.
- Gross margin (%) = gross profit divided by revenue, multiplied by 100.

For a category, region or channel margin, divide its TOTAL gross profit by its TOTAL revenue. Do not average the individual sale margins. Gross profit excludes rent, wages, shipping and marketing, so it is not net profit. Round money to two decimal places when displaying it.

## Your assignments

Work one assignment at a time. Send your code, graph where requested, and a short business conclusion. No need to build a dashboard or learn every new method at once.

### 1. Give the manager a quarterly snapshot

Calculate total revenue after discounts, total gross profit, total units sold and number of sales. Identify the product with the largest individual sale by revenue and report that sale's ID. Explain the difference between number of sales and number of units. No graph required yet.

### 2. Decide which category deserves attention

Compare total revenue and total gross profit by category. Make one bar chart for each. Does the revenue leader also lead on gross profit? Report the gross margin for each category. Write two sentences explaining which category you would investigate further and why.

### 3. Select products for a promotion

Find the top five products by TOTAL gross profit and plot a bar chart. Compare them with the top five by TOTAL revenue. Recommend two products for the manager to review, supporting each choice with numbers. The data does not include stock or marketing costs, so treat this as a shortlist.

### 4. Review regional performance

Compare total revenue, total gross profit and number of sales by region. Plot total gross profit by region. Calculate average revenue per sale for each region. Is the largest region also the one with the highest average revenue per sale?

### 5. Compare Online and Store

For each channel, calculate total revenue, total gross profit, number of sales and gross margin. Plot gross profit by channel. Explain whether the channel with more sales also has the higher margin. Propose one follow-up question before allocating more budget.

### 6. Explain the quarter's trend

Calculate revenue for July, August and September and draw a LINE chart in chronological order. Identify the strongest month and calculate its growth versus the previous month. Explore which category contributed most to that change. Date handling is new: ask for a small hint when you reach this task.

### 7. Investigate discounts

Use a scatter plot with discount_pct on the horizontal axis and quantity on the vertical axis. Add a trend line and show Pearson's correlation in the title. Then compare gross margin across discount levels. Write what you observe; a correlation alone does not prove that discounts caused customers to buy more because products and channels also differ.

### 8. Write the manager's update

Write five short findings, each supported by a number from your analysis, and two actions you recommend reviewing. Include one limitation of this synthetic dataset. Choose your three most useful graphs to support the update.

Start with assignment 1. You already know the core steps: create columns, sum, count, group, sort and filter. Ask for hints when needed; the calculations and conclusions are yours to work out.
