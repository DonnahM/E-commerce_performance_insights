# Olist Customer Behavior & Value Analysis

## Project Overview
This project explores customer behavior, sales patterns, and product performance within the Olist eCommerce ecosystem. Using historical order, customer, payment, and product data, the analysis focuses on identifying where customer value is concentrated, how purchasing behavior differs across customers, and how these insights can inform marketing, retention, and strategic business decisions.

Rather than addressing a single predefined business problem, this project adopts an exploratory, analytics-driven approach to surface meaningful patterns and decision-relevant insights from the data.

**Dataset source:** Brazilian E-Commerce Public Dataset by Olist (Kaggle)  
[Brazilian E-Commerce Public Dataset by Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)


---

## Analytical Scope
The analysis emphasizes **descriptive and diagnostic analytics**, with a focus on:
- Customer purchasing behavior and order frequency patterns
- Customer value distribution and segmentation
- Revenue and profitability drivers across product categories
- Sales trends and order dynamics over time

While order fulfillment timestamps exist in the dataset, fulfillment performance analysis is intentionally limited. Several delivery-related timestamps contained missing values that required median imputation, reducing the reliability of downstream fulfillment insights. As a result, this project prioritizes **customer behavior and value analysis** over operational delivery performance.

This project does **not** include machine learning modeling. Given the dataset structure and the dominance of one-time buyers, the analytical objectives are better served through exploratory analysis and segmentation rather than predictive modeling.

---

## Objectives
The objectives of this analysis are to:
- Examine customer purchasing behavior, including order volume and spending patterns
- Assess customer value distribution and identify meaningful customer segments
- Identify revenue concentration across customers and product categories
- Derive actionable insights to support customer retention and strategic decision-making

---

## Data Overview
This analysis is based on the Olist eCommerce dataset, a relational dataset containing customer, order, payment, product, and logistics information. The dataset captures the lifecycle of an eCommerce transaction from purchase through post-purchase outcomes.

### Key Tables Used

- **Customers Table**  
  Contains unique customer identifiers and location information. Used for customer-level aggregation, behavioral analysis, and value segmentation.

- **Orders Table**  
  Contains order-level information and key lifecycle timestamps. Serves as the central table linking customers, payments, and order items.

- **Order Items Table**  
  Links orders to individual products and includes pricing and freight values. Used for revenue calculations and order value analysis.

- **Payments Table**  
  Contains payment method details, installment information, and payment values. Used to compute total spend per order and customer value metrics.

- **Products Table**  
  Provides product category information and metadata. Used for revenue and profitability analysis by category.

- **Sellers Table**  
  Includes seller location information and is referenced where relevant for contextual understanding.

---

## Methodology

This analysis followed a structured, analytics-first approach designed to extract interpretable insights from transactional eCommerce data. The focus was on behavioral patterns, revenue dynamics, and customer value rather than predictive modeling.

### Data Preparation & Integration
- Integrated relational tables (customers, orders, order items, payments, products, sellers) using consistent primary and foreign keys.
- Standardized data types, resolved duplicates, and validated joins.
- Handled missing timestamp values in the orders table using median imputation to preserve temporal continuity while minimizing bias.

### Behavioral Analysis
- Evaluated order volume and purchasing cadence to understand customer engagement patterns.
- Analyzed one-time versus repeat purchasing behavior to assess retention depth.
- Reviewed average order value (AOV) trends to distinguish revenue growth driven by order frequency versus basket size.

### Sales & Revenue Analysis
- Analyzed monthly order and revenue trends to identify seasonality and demand stability.
- Assessed revenue contribution by product category to identify concentration and diversification.
- Compared category-level performance to determine whether top categories meaningfully outperform peers or operate within tight competitive ranges.

### Customer Value & Segmentation
- Aggregated customer-level spend to evaluate value distribution.
- Assessed the practicality of frequency-based segmentation given the dominance of one-time buyers.
- Prioritized spend-based insights over forced segmentation where behavioral separation was weak.

This methodology ensures that insights are grounded in observable patterns and aligned with realistic business decision-making.


---

## Key Insights
- The customer base is heavily skewed toward one-time buyers, with repeat customers representing a small fraction of total users
- Revenue is concentrated among a minority of customers, indicating uneven customer value distribution
- Sales growth is primarily driven by order volume rather than increasing order frequency or average order value
- Product category analysis reveals clear revenue leaders, while profit margins remain tightly clustered across most categories

---

## Limitations
- Fulfillment and delivery performance insights are limited due to missing and imputed timestamp data
- The analysis is descriptive and diagnostic; no causal or predictive modeling is included
- External drivers such as marketing campaigns, promotions, or traffic sources are not incorporated

---

## Conclusions
This analysis provides a clear view of customer behavior and revenue structure within the Olist eCommerce ecosystem.

**Key conclusions include:**
- Customer behavior is overwhelmingly dominated by one-time purchases, indicating limited organic retention and a largely transactional customer base.
- Revenue growth is primarily volume-driven rather than frequency-driven, with average order values remaining relatively stable over time.
- Product category performance shows identifiable revenue leaders; however, profit margins across most categories are tightly clustered, suggesting competitive parity rather than outsized advantage.
- Customer value is broadly distributed, and order frequency alone provides limited segmentation power, reinforcing the need for retention- and lifecycle-focused strategies rather than optimization of repeat behavior that rarely occurs.

Overall, this project demonstrates that strong descriptive and diagnostic analytics can yield actionable insights without unnecessary model complexity. The findings support informed discussions around customer retention, category portfolio strategy, and realistic expectations for behavioral segmentation.

---

## Recommendations
- Prioritize retention strategies for high-value customer segments identified in the analysis
- Design targeted incentives to convert one-time buyers into repeat customers
- Use customer value insights to guide marketing spend allocation and segmentation strategies
- Align category strategy around both revenue contribution and margin sustainability


