# E-commerce Sales & Profitability Analysis Using What-If Analysis in Excel

## 1. Project Overview

This project focuses on analysing the financial performance of an e-commerce business and understanding how different discount strategies could affect revenue and profitability.

The primary objective is to use **What-If Analysis in Microsoft Excel** to evaluate different business scenarios and help management make informed decisions before implementing a discount strategy.

An e-commerce company may increase discounts to attract more customers and generate additional orders. However, higher discounts do not necessarily translate into higher profits.

To investigate this, I developed a scenario-based financial model in Excel to compare different discount strategies and understand their potential impact on:

- Gross Sales
- Net Revenue
- Total Cost
- Total Profit
- Profit Margin

The analysis compares three discount scenarios: 5%, 10%, and 15%, against the company's existing financial performance.

---

## 2. Business Problem

The management of an e-commerce company wants to increase sales by introducing promotional discounts.

However, before implementing this strategy, management needs to understand:

- How would different discount percentages affect revenue?
- Would higher discounts generate enough additional orders to justify the reduction in selling prices?
- How would increasing order volumes affect operational costs?
- Which discount strategy would generate the highest estimated profit?
- Which scenario would provide the best profitability?

The challenge is to identify a discount strategy that supports business growth without unnecessarily reducing profitability.

---

## 3. Project Objective

The main objectives of this project are:

1. Analyse the existing financial performance of the e-commerce business.
2. Clean, validate, and prepare the dataset for analysis.
3. Calculate important financial metrics using Excel formulas.
4. Establish a baseline against which different scenarios can be compared.
5. Apply What-If Analysis to evaluate different discount strategies.
6. Compare the financial outcomes of different scenarios.
7. Identify the most financially attractive scenario under the defined assumptions.
8. Provide data-driven recommendations to management.

---

## 4. Dataset Description

The project uses a synthetic e-commerce dataset containing **500 order records**.

The dataset was created for analytical and educational purposes and represents a hypothetical e-commerce business.

### Dataset columns

| Column | Description |
|---|---|
| Order_ID | Unique identification number for each order |
| Order_Date | Date on which the order was placed |
| Region | Geographical region associated with the order |
| Category | Product category |
| Product | Name of the purchased product |
| Units | Number of units purchased |
| Unit_List_Price_INR | Selling price per unit before discount |
| Unit_Cost_INR | Cost incurred by the company per unit |
| Discount_Rate | Discount percentage applied to the order |
| Shipping_Cost_INR | Shipping and fulfilment cost |
| Marketing_Cost_INR | Marketing cost allocated to the order |

The dataset also includes calculated financial columns created during the analysis.

---

## 5. Tools and Technologies Used

- **Microsoft Excel:** Data cleaning, financial calculations, scenario modelling, and business analysis.
- **Excel Formulas:** SUM, COUNT, IFERROR, and arithmetic calculations.
- **What-If Analysis:** Evaluating the financial impact of different business assumptions.
- **Excel Formatting:** Organising financial information and presenting results.

---

## 6. Data Preparation and Financial Calculations

Before performing What-If Analysis, the dataset was inspected and validated.

The following checks were performed:

- Verified the total number of records.
- Checked for duplicate Order IDs.
- Checked for missing values.
- Reviewed data types and number formats.
- Verified numerical fields and calculated columns.

After data validation, the following calculated columns were created.

### A. Gross Sales

Gross Sales represents the total selling value before deducting discounts.

Formula:

```excel
=Units*Unit_List_Price
```

### B. Discount Amount

Calculates the total discount provided on an order.

Formula:

```excel
=Gross_Sales*Discount_Rate
```

### C. Net Revenue

Represents the revenue remaining after deducting discounts.

Formula:

```excel
=Gross_Sales-Discount_Amount
```

### D. Total Cost

Includes product costs, shipping costs, and marketing costs.

Formula:

```excel
=(Units*Unit_Cost)+Shipping_Cost+Marketing_Cost
```

### E. Profit

Calculates the profit generated from an order.

Formula:

```excel
=Net_Revenue-Total_Cost
```

### F. Profit Margin

Measures the percentage of net revenue retained as profit.

Formula:

```excel
=Profit/Net_Revenue
```

---

## 7. Baseline Financial Performance

After preparing the dataset, the overall financial performance of the business was calculated.

These figures represent the actual baseline performance within the synthetic dataset.

| KPI | Baseline Result |
|---|---:|
| Total Orders | 500 |
| Total Units Sold | 885 |
| Gross Sales | ₹17,73,515.00 |
| Total Discount | ₹1,24,093.45 |
| Net Revenue | ₹16,49,421.55 |
| Total Cost | ₹10,69,950.00 |
| Total Profit | ₹5,79,471.55 |
| Profit Margin | 35.13% |
| Average Order Value | ₹3,298.84 |

The baseline performance provides a reference point for evaluating the potential impact of different discount strategies.

---

## 8. What-If Analysis: Scenario Planning

### Business Question

What would happen to the company's revenue and profitability if management introduced different discount strategies?

To answer this question, three hypothetical scenarios were developed.

| Scenario | Discount Rate | Assumed Order Growth |
|---|---:|---:|
| Scenario A | 5% | 5% |
| Scenario B | 10% | 10% |
| Scenario C | 15% | 15% |

### Scenario assumptions

The scenario model uses the following assumptions:

1. A higher discount is assumed to generate an increase in order volume.
2. The assumed order growth is equal to the proposed discount percentage.
3. Average selling prices before discounts remain unchanged.
4. Total costs increase proportionally with the assumed order growth.
5. The proposed scenario discount is applied to scenario gross sales.
6. Other business factors are held constant for comparison.

**Important:** These assumptions are illustrative and are not proven demand relationships. Actual order growth would need to be estimated using historical data, market research, or controlled experiments.

### Scenario calculation methodology

**1. Scenario Gross Sales**

```excel
=Baseline_Gross_Sales*(1+Expected_Order_Growth)
```

**2. Scenario Net Revenue**

```excel
=Scenario_Gross_Sales*(1-Discount_Rate)
```

**3. Scenario Total Cost**

```excel
=Baseline_Total_Cost*(1+Expected_Order_Growth)
```

**4. Scenario Total Profit**

```excel
=Scenario_Net_Revenue-Scenario_Total_Cost
```

**5. Scenario Profit Margin**

```excel
=Scenario_Total_Profit/Scenario_Net_Revenue
```

These calculations were used to estimate the financial impact of each proposed discount strategy.

---

## 9. Scenario Analysis Results

The following table presents the estimated financial outcomes.

| Financial Metric | Scenario A (5%) | Scenario B (10%) | Scenario C (15%) |
|---|---:|---:|---:|
| Gross Sales | ₹18,62,190.75 | ₹19,50,866.50 | ₹20,39,542.25 |
| Net Revenue | ₹17,69,081.21 | ₹17,55,779.85 | ₹17,33,610.91 |
| Total Cost | ₹11,23,447.50 | ₹11,76,945.00 | ₹12,30,442.50 |
| Total Profit | ₹6,45,633.71 | ₹5,78,834.85 | ₹5,03,168.41 |
| Profit Margin | 36.50% | 32.97% | 29.02% |

### Key observations

**Scenario A – 5% Discount**

- Generates the highest estimated profit of ₹6,45,633.71.
- Provides the highest profit margin of 36.50%.
- Performs better than the other two scenarios under the defined assumptions.

**Scenario B – 10% Discount**

- Generates higher gross sales than Scenario A.
- However, estimated profit decreases to ₹5,78,834.85.
- Profit margin decreases to 32.97%.

**Scenario C – 15% Discount**

- Generates the highest gross sales.
- However, estimated profit decreases to ₹5,03,168.41.
- Profit margin falls to 29.02%.

---

## 10. Key Business Insights

The scenario analysis highlights several important findings.

1. Increasing discounts does not necessarily increase profitability.
2. Higher discounts can increase gross sales while reducing net revenue and profit.
3. Additional orders may increase operational costs.
4. Revenue growth should not be considered the only measure of business performance.
5. Profit and profit margin are important indicators when evaluating pricing and promotional strategies.

An important observation is that Scenario C generates the highest gross sales but the lowest estimated profit among the three scenarios.

This demonstrates why businesses should evaluate profitability rather than focusing only on sales growth.

---

## 11. Business Recommendation

Based on the scenario analysis, **Scenario A (5% discount) is the most financially attractive option** among the three alternatives.

It generates the highest estimated profit and profit margin under the assumptions used in this model.

I would recommend that management consider testing the 5% discount strategy on selected products or customer segments before implementing it across the business.

The company should then monitor actual order volume, revenue, discount costs, and profitability to determine whether the expected results are achieved.

The recommendation should be reviewed if actual customer demand responds differently from the assumptions used in the scenario model.

---

## 12. Limitations and Assumptions

This project uses a simplified financial model to demonstrate the application of What-If Analysis.

The following limitations should be considered:

- The dataset is synthetic and does not represent actual company transactions.
- Order growth percentages are hypothetical assumptions.
- The model assumes that costs increase proportionally with order growth.
- The model does not account for changes in customer behaviour, competitor pricing, or seasonal demand.
- Fixed operating expenses and other possible business costs are not separately modelled.
- The analysis estimates possible outcomes rather than predicting guaranteed future performance.

These limitations are important when interpreting the results and making business recommendations.

---

## 13. Skills Demonstrated

Through this project, I demonstrated the following skills:

- Data cleaning and validation in Excel.
- Financial data analysis.
- Excel formulas and calculated columns.
- Revenue, cost, and profitability calculations.
- What-If Analysis and scenario-based modelling.
- Business problem-solving.
- Comparative financial analysis.
- Business interpretation and recommendation.

---

## 14. Project Outcome

This project demonstrates how Microsoft Excel can be used beyond basic calculations to support business decision-making.

By developing a scenario-based financial model, I evaluated how different discount strategies could influence revenue, costs, and profitability.

The analysis showed that the highest discount does not necessarily produce the highest profit. Under the assumptions used, a 5% discount provided the most financially attractive outcome.

The project helped demonstrate the practical application of What-If Analysis in evaluating business decisions and communicating financial insights to management.

---

## 15. Conclusion

What-If Analysis is a valuable technique for businesses that need to evaluate different possibilities before implementing a decision.

Through this project, I applied scenario-based modelling to understand the relationship between discounts, order growth, revenue, and profitability.

The main takeaway is that **business decisions should be evaluated based on their overall financial impact, not just their potential to increase sales.

