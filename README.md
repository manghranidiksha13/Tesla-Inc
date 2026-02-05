# Tesla Inc. Corporate Performance Dashboard (2026)



## **Project Overview**
This project analyzes Tesla's manufacturing efficiency, financial health, and market performance. Utilizing Power BI, it transforms raw global delivery and stock data into a 4-page interactive dashboard designed for executive-level decision-making.

## **Key Features & Insights**
* **Executive Summary:** Real-time tracking of Total Revenue ($120B target) and YoY Delivery Growth.
* **Production Analysis:** A regional deep-dive identifying gaps between production and actual deliveries.
* **Financial & Sustainability:** Visualization of profit margins alongside environmental impact metrics.

## **Technical Stack**
* **Tool:** Power BI Desktop.
* **Data Sources:** Kaggle and Tesla Investor Relations.
* **Advanced DAX:** Custom measures for time-intelligence.

## **DAX Measures Used**
### **Year-over-Year (YoY) Growth**
dax
YoY Growth % = 
VAR LY_Deliveries = CALCULATE([Total Deliveries], SAMEPERIODLASTYEAR('Dim_Calendar'[Date]))
RETURN DIVIDE([Total Deliveries] - LY_Deliveries, LY_Deliveries, 0)
