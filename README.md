# Credit_Card_Financial_Analysis_using_SQL_and_PowerBI

## Project Overview
This dashboard provides comprehensive insights into credit card performance metrics using transaction and customer data. Built with Power BI and SQL, it delivers actionable intelligence to support strategic decision-making.

## Data Foundation
The project utilizes transaction and customer datasets from a credit card portfolio, processed through SQL before visualization. The data preparation workflow included:
- Creating normalized SQL tables for customer profiles and transaction history.
- Implementing table relationships to enable cross-analysis.
- Validating data integrity before visualization.

## Technical Implementation
### DAX Formulas
Several custom calculations were developed to derive meaningful insights:

```dax
AgeGroup = SWITCH(
    TRUE(),
    'public cust_detail'[customer_age] < 30, "20-30",
    'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40, "30-40",
    'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50, "40-50",
    'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60, "50-60",
    'public cust_detail'[customer_age] >= 60, "60+",
    "unknown"
)

The revenue tracking formulas enabled week-over-week performance monitoring that proved particularly valuable for identifying growth trends.

**Key Findings**

Analysis revealed several noteworthy patterns:

Revenue Growth: 28.8% week-over-week increase in the most recent period.
Product Performance: Blue and Silver cards account for 93% of total transactions.
Geographic Concentration: Three states (TX, NY, CA) represent 68% of portfolio activity.
Customer Engagement: Overall card activation rate stands at 57.5%.
Risk Metrics: The portfolio maintains a 6.06% delinquency rate.

**Business Applications**

These insights can inform several strategic initiatives:

Targeted marketing campaigns for high-performing card types.
Regional expansion opportunities beyond the three dominant states.
Customer activation programs to improve the current 57.5% rate.
Revenue optimization strategies leveraging the demographic segmentation.

**Future Development**
Potential enhancements include:

- Integrating predictive analytics for customer lifetime value.
- Creating executive-level summary dashboards.
- Implementing automated refresh schedules for real-time monitoring.


