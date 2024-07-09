# Supply-Chain-Analysis-Dashboard
Analyzing Supplier Performance at Flavours 'n' Forks Bistro
Supply Chain Analysis Dashboard: Analyzing Supplier Performance at Flavours 'n' Forks Bistro
About the company
Flavours 'n' Forks Bistro, also known as F‘n’F Bistro a renowned culinary establishment, has made its mark in the vibrant restaurant industry  in the heart of Lagos by offering an array of delectable local and intercontinental dishes that tantalize the taste buds.

Problem Statement
Flavours 'n' Forks Bistro wants to serve the freshest food possible, but some of their suppliers haven't been delivering ingredients on time. This makes it difficult for the kitchen to cook meals as planned.

Project Goal: Improve supplier performance to ensure fresh ingredients arrive exactly when the kitchen needs them. Why? Flavours 'n' Forks Bistro prides itself on amazing food and happy customers. Late deliveries throw off the kitchen schedule, making it hard to maintain that high standard.

Data Description
F ‘n’ F Bistro has information on 1500 orders from their 10 suppliers, which will be analyze for actionable insights and they include: 
Supplier Data
Supplier_ID: Unique identifier for each supplier.
Supplier_Name: Name of the supplier.
Supplier_Email: Email address of the supplier.
Supplier_Location: Location or city where the supplier is based.
Supplier_Phone: Phone number of the supplier.
Order Data:
Supplier_ID: Unique identifier for the supplier associated with the order.
Order_Date: Date when the order was placed.
Delivery_Date: Date when the order was delivered.
Lead_Time: Number of days it took from order placement to delivery.
Order_Quantity: The quantity of the ingredient ordered.
Received_Quantity: The quantity of the ingredient received. 
Order_Status: Status of the order (e.g., "Paid" or "Cancelled").
Payment_Status: Payment status for the order (e.g., "Paid" or "Cancelled)
Order_Completion_Date: Date when the order was marked as completed. 
Ingredient_Name: Name of the ingredient ordered.


Tools: Power Query, Microsoft PowerBI

Skills applied: Power BI skills, Data Importation and Modelling, Dashboard Creation and Reporting, Exploratory Data Analysis, Data Visualization, and Supply chain Analysis Analysis

DAX Functions
Total Quantity = SUM('order_data (2)'[Received_Quantity])
Total Lead Time = SUM('order_data (2)'[Lead_Time])
No of Rows = COUNTROWS('order_data (2)')
No of Suppliers = DISTINCTCOUNT('supplier_data (2)'[Supplier_Name])
Sum Order Quantity = SUM('order_data (2)'[Order_Quantity])
Avg Lead Time = AVERAGE('order_data (2)'[Lead_Time])
Total Paid Orders = CALCULATE(COUNTROWS('order_data'),'order_data'[Payment_Status] = "Paid")
Total Cancelled Orders = CALCULATE(COUNTROWS('order_data'),'order_data'[Payment_Status] = "Cancelled")
Payment Compliance Rate = DIVIDE([Total Paid Orders], [No of Rows], 0)
Order Fulfillment Rate = DIVIDE([Total Quantity], [Sum Order Quantity], 0) 
Order Cancellation Rate = DIVIDE([Total Cancelled Orders], [No of Rows], 0)


Insights from the data
The overall order fulfillment rate is high at 95.1%, while the order cancellation rate is 4.9%. Further investigation and newer data maybe required. Vegetables have the highest cancellation rate, indicating supply or quality issues. Supplier payment compliance varies, with Elizabeth Austin at 98.1% and Jessica Hodges at 92.1%, which could affect contract negotiations. The total lead time is 23K, averaging 15.6 days, with Whitney Burch having the highest lead time. Tomatoes show high lead times and low supply, suggesting a need for better forecasting. A 3K difference exists between ordered (76K) and received quantities (73K). The supplier base is limited to 10, posing a risk. Specific suppliers like Jessica Hodges and Frances Wilson need attention for lower fulfillment rates. There are dips in received quantities in April and September that should be investigated.

Recommendations
Order Fulfillment and Cancellations
1.	Investigate Vegetable Supply Issues: Since vegetables have the highest cancellation rate, conduct a thorough investigation into the supply chain and quality control processes for these products. This could involve assessing supplier reliability, transportation conditions, and storage practices.
2.	Improve Supplier Payment Compliance: Address the payment compliance issues with suppliers like Jessica Hodges (92.1%). Ensuring timely payments may strengthen relationships and improve their fulfillment rates.
Lead Time Management
3.	Optimize Lead Times: With the overall average lead time at 15.6 days and Whitney Burch having the highest lead time, consider reevaluating logistics and inventory management practices. Implement strategies like buffer stock, safety stock, or alternative suppliers to reduce lead times.
4.	Enhance Forecasting for Tomatoes: Given the high lead times and low supply for tomatoes, improve demand forecasting and planning. Collaborate closely with suppliers to ensure better alignment of supply with demand.
Quantity Discrepancies
5.	Investigate Quantity Discrepancies: Address the 3K difference between ordered (76K) and received (73K) quantities by auditing the supply chain processes. This includes verifying order accuracy, delivery documentation, and possible losses or damages during transit.
Supplier Management
6.	Expand Supplier Base: Mitigate risk by expanding the supplier base beyond the current 10 suppliers. Diversifying suppliers can provide more flexibility and reduce dependency on a limited number of sources.
7.	Focus on Underperforming Suppliers: Pay special attention to suppliers like Jessica Hodges and Frances Wilson, who have lower fulfillment rates. Engage with them to understand their challenges and provide support to improve their performance.
Seasonal Variations
8.	Investigate Seasonal Dips: Examine the reasons behind the dips in received quantities in April and September. This could involve analyzing seasonal demand variations, supplier capabilities during these months, and any external factors affecting supply.
Contract and Negotiation Strategies
9.	Reevaluate Supplier Contracts: Use supplier payment compliance data to inform contract negotiations. For instance, leverage the high compliance rate of Elizabeth Austin (98.1%) as a benchmark when renegotiating terms with other suppliers.
10.	Implement Performance Metrics: Establish clear performance metrics and regular review processes for suppliers to ensure ongoing compliance and high fulfillment rates. This could include lead time targets, fulfillment rates, and quality standards.
Continuous Monitoring and Data Analysis
11.	Regular Data Updates: Ensure continuous monitoring and updating of data to reflect current performance. This allows for timely adjustments and more accurate decision-making.
12.	Invest in Technology: Consider investing in supply chain management software and tools to better track orders, manage inventory, and predict demand. This can help in identifying potential issues early and optimizing overall operations.


Data Source: https://amdari.io
Data Analyst: Kamaldeen O Omosanya (https://github.com/Geodatadetectve?tab=repositories)

