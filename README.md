# Retail Sales Analytics: Transforming Transaction Data into Strategic Intelligence

## Executive Summary:
In today’s competitive retail environment, our organization needed to better understand how pricing, purchasing behavior, and temporal patterns impact revenue performance.  
Using **AWS Cloud Services** — including **S3, Lambda, Glue, Athena, and QuickSight** — I designed and deployed a **serverless data analytics pipeline** to extract, transform, and visualize retail transaction data at scale.

The analysis revealed that **revenue gains can be maximized through pricing optimization, smarter promotional timing, and enhanced cross-selling strategies**.  
Based on these insights, I recommend the following data-driven actions to increase overall profitability:

- Adjust pricing thresholds across high-volume categories to align with customer spending elasticity.  
- Schedule promotions during high-performing time windows identified through temporal trend analysis.  
- Implement targeted cross-sell campaigns based on correlated purchasing volumes.  

These strategies provide a scalable framework for driving **revenue growth**, **inventory efficiency**, and **customer engagement** using real-time analytics.

---

## Business Problem:
Despite collecting millions of retail transactions, the business lacked a **centralized analytics system** to translate this data into actionable intelligence.  
Executives needed clear answers to:
- Which products and price points generate the highest total spending?  
- When do customers spend the most, and how can we capitalize on these peaks?  
- How can we identify patterns in purchase quantities to enhance cross-selling and demand forecasting?  

The goal was to build an **automated AWS analytics pipeline** that continuously delivers insights into these questions — replacing manual Excel-based reporting with scalable, real-time intelligence.

![AWS Retail Data Flow](images/aws_data_pipeline.png)

---

## Methodology:
The end-to-end pipeline was built entirely within AWS, using the following architecture:

1. **Data Ingestion – Amazon S3**  
   - Transactional sales data (CSV format) was stored in an S3 data lake.  
   - Event triggers were configured for automatic downstream processing upon file upload.

2. **Data Transformation – AWS Glue**  
   - A Glue ETL job cleaned, joined, and normalized datasets (pricing, product, and transaction history).  
   - Partitioned the data by date and category to optimize Athena queries.

3. **Automation – AWS Lambda**  
   - Lambda functions automated job triggers and metadata updates whenever new files were added to S3.  
   - The pipeline achieved a fully serverless, event-driven design with no manual intervention.

4. **Data Query – Amazon Athena**  
   - SQL-based queries aggregated total revenue, spending averages, and price sensitivities.  
   - Created optimized Athena tables for use by QuickSight.

5. **Visualization – Amazon QuickSight**  
   - Developed an interactive retail analytics dashboard visualizing:  
     - *Average Total Spent vs. Average Price Per Unit*  
     - *Daily and Seasonal Spending Trends*  
     - *Quantity and Cross-Selling Indicators*

---

## Skills:
**AWS Services:** S3, Lambda, Glue, Athena, QuickSight  
**Data Engineering:** ETL pipelines, serverless automation, data partitioning  
**Analytics:** SQL, aggregation, correlation, pricing optimization, trend forecasting  
**Visualization:** Interactive dashboards, KPI tracking, time-series charts  
**Programming:** Python (for Glue and Lambda scripts), SQL (for Athena)  

---

## Results & Business Recommendations:
The cloud-based analytics platform uncovered key insights that drive measurable outcomes:

- **Pricing Optimization:**  
  Premium-priced product categories generated the highest total spending per customer, highlighting opportunities for margin improvement without volume loss.

- **Temporal Spending Patterns:**  
  Spending peaked on specific weekdays and seasonal periods, informing promotional timing and restocking decisions.

- **Volume & Cross-Selling Opportunities:**  
  Quantity-based correlations identified strong cross-selling relationships, especially between complementary product groups.

These findings directly inform the following recommendations:

- Implement **automated price adjustments** for high-impact SKUs.  
- Schedule **targeted promotions** during identified high-spend cycles.  
- Integrate **cross-sell prompts** in POS systems based on data-driven pairing patterns.

The AWS-powered pipeline reduced manual reporting time by over **80%**, and improved decision-making visibility for stakeholders across product, sales, and marketing teams.

![QuickSight Retail Dashboard](images/quicksight_dashboard.png)

---

## Business Impact:
- **Data Refresh Frequency:** Real-time via Lambda triggers on S3 uploads  
- **Operational Efficiency:** Reduced ad hoc data requests by 6–8 hours per week  
- **Revenue Lift Potential:** Estimated 12–15% through optimized pricing and promotions  
- **Scalability:** Fully serverless, maintenance-free architecture  

---

## Next Steps:
- Extend the ETL pipeline to incorporate **customer segmentation data** for deeper personalization.  
- Integrate **forecasting models in AWS SageMaker** to predict demand and optimize inventory.  
- Expand **QuickSight dashboards** to include profitability by region, store, and product line.  
- Deploy **automated alerts** for anomalies in revenue and transaction volume.

---

## Tools & Architecture:
**Cloud:** AWS (S3, Lambda, Glue, Athena, QuickSight)  
**Languages:** Python, SQL  
**Visualization:** Amazon QuickSight  
**Data Storage:** AWS S3 (Parquet + CSV partitions)  
**Orchestration:** Event-driven serverless triggers via Lambda  
**Security:** IAM roles and S3 bucket policies for data access control  

---

## Repository Structure:
retail-sales-analytics/
├── lambda/
│ └── trigger_glue_job.py
├── glue/
│ └── transform_sales_data.py
├── athena/
│ └── retail_analysis_queries.sql
├── images/
│ ├── aws_data_pipeline.png
│ ├── quicksight_dashboard.png
│ ├── pricing_strategy.png
│ ├── temporal_patterns.png
│ └── volume_behavior.png
├── reports/
│ └── Retail_Sales_Analytics_Report.pdf
├── requirements.txt
└── README.md


---

## Author:
**Aurel Sahiti**  
Data Science Graduate Student | Cloud Data Engineering & Retail Analytics  
📊 [LinkedIn](https://linkedin.com/in/aurelsahiti) | 🌐 [GitHub](https://github.com/aurelsahiti)

---
