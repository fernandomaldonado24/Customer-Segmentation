# Customer-Segmentation
## The goal of this project is to segment customers of a retail business based on their purchasing behavior in order to surface actionable insights for marketing, product offerings, and customer retention strategies.

The dataset contains historical sales transactions, including product details, quantities, prices, invoice dates, and customer identifiers. These transactions span a diverse product catalog and a broad customer base, ranging from occasional buyers to frequent, high-value clients.
Over time, the company has observed that different customer groups exhibit unique purchasing patterns — some shop seasonally, others regularly; some focus on high-value items, others on bulk purchases. However, marketing campaigns have so far been executed without clear customer segmentation, which limits personalization and the efficient allocation of resources.
Now that the company is investing in data-driven decision-making, the objective is to identify distinct customer segments through clustering techniques. These insights will help:

- Tailor marketing strategies to each segment.
- Optimize promotions and product recommendations.
- Improve customer retention through targeted engagement.

## Dataset Structure
The dataset consists of a primary transactional table containing the following key features: CustomerID, UnitPrice, Quantity, InvoiceNo, InvoiceDate, StockCode, Description, and Country. Each row represents a single product line within an invoice, making it possible to capture detailed information about customer purchases, timing, location, and product attributes.

From this base table, several dimension tables were created to organize and filter data more effectively:

- Clusters – descriptive metadata for each customer segment identified.
- Country – reference data for the geographic location of the purchase.
- Date – calendar details such as month, month–year, and year for time-based analysis.

Two fact tables hold the main analytical content:

- Sales – the original transactional dataset, linked to the dimensions for filtering by product, time, or geography.
- Fact_Clustering – created after applying Machine Learning clustering algorithms to segment customers based on their purchasing behavior. This table stores aggregated behavioral metrics for each segment, enabling further analysis and reporting of customer profiles.

<img width="525" height="325" alt="ERD Ecomerce" src="https://github.com/user-attachments/assets/f86617b1-6b9d-42be-be9f-586231ec4155" />

## Insights Summary
To assess customer behavior and segment performance, we focused on the following key metrics:

- Total Sales – Total revenue generated over the analysis period.
- Average Basket Size – Average number of items purchased per transaction.
- Average Basket Spend – Average monetary value of each transaction.
- Customer Distribution by Cluster – Share of customers in each identified segment.

Overall Performance
Across all markets, total sales reached £1,122,596. The average basket size was 279.3 items, and the average basket spend was £61.0. Customer distribution by segment showed:

- Steady Essentials – 41% (1,778 customers)
- Power Loyalists – 39% (1,660 customers)
- Ghost Shoppers – 11% (471 customers)
- Fickle Returners – 9% (381 customers)

Segment Insights
Steady Essentials
- Total Spend: £2,116,615
- Average Spend: £26.9
- Product Diversity: 61

Profile: Customers with moderate recency and visit frequency, making steady purchases over time. Mid-range basket size and spend, low cancellation rates, and a preference for essential products. Reliable but not highly engaged buyers.

Fickle Returners
- Total Spend: £531,582
- Average Spend: £23.5
- Product Diversity: 59

Profile: Moderately active customers with average purchase frequency and spend, but the highest cancellation rate and number of returns. Behavior is inconsistent, indicating possible dissatisfaction or indecision. Represents a retention risk group.

Ghost Shoppers
- Total Spend: £604,203
- Average Spend: £38.2
- Product Diversity: 22

Profile: One-time or short-term buyers with purchases clustered in a brief period. Lowest total spend, product diversity, and visit frequency. Despite high average spend per visit, they show minimal long-term engagement and low overall business value.

Power Loyalists
- Total Spend: £2,867,842
- Average Spend: £32.4
- Product Diversity: 177

Profile: The most engaged and valuable customers. High purchase frequency, strong total and average spend, and broad product interest. Their recent activity and long purchase span reflect strong loyalty, making them high-priority for retention and long-term value generation.

## Recommendations
Power Loyalists:
- Increase retention programs for this segment — while already high-value, their broad product diversity suggests potential for upselling in underrepresented categories.
- Focus loyalty rewards on cross-selling rather than discounts, to avoid eroding margin.

Steady Essentials:
- Implement gradual engagement tactics (e.g., seasonal product bundles) to move them toward Power Loyalist behavior. Their low average spend per basket and stable habits suggest they respond better to curated offers than aggressive promotions.
- 
Fickle Returners:
- Address high cancellation rates with a targeted win-back program. Analyze cancellation reasons to determine if they stem from product quality, fulfillment delays, or mismatched expectations. Test smaller “trial” offers to reduce buyer hesitation.

Ghost Shoppers:
- Treat this segment primarily as a prospecting audience rather than retention targets — consider shifting investment from post-purchase engagement to pre-purchase targeting in other channels. Test welcome offers that incentivize a second purchase within 30 days.

Overall Portfolio:
- Shift retention and upselling resources from Ghost Shoppers to Power Loyalists and Steady Essentials, where lifetime value and engagement potential are higher.
Create tailored onboarding flows for Fickle Returners that address likely pain points before the second purchase.

## Dashboard
The interactive dashboard can be accessed in Power BI [link here](https://app.powerbi.com/view?r=eyJrIjoiYzcxZjk0YzktNzA4MS00ZGEwLWFhZTUtN2VlN2MwNzE3NWQ0IiwidCI6ImY2OTI5MWY5LTNkYTctNDJiMy05ZjEwLWYyZWFlMjU3ZDVhYiIsImMiOjR9).
This dashboard allows users to filter by country and customer segment, and focuses on trends and values across key sales and behavioral metrics. Users can explore total sales over time, average basket size, average basket spend, and the distribution of customers across segments. Additionally, it provides detailed profiles for each segment, including total spend, average spend, product diversity, and descriptive behavioral insights.
<p align="center">
<img width="638" height="351" alt="Ecommerce dashboard page 1" src="https://github.com/user-attachments/assets/f00f571b-a512-4f2f-8318-e5b42ebc316d" />
</p>
<p align="center">
<img width="638" height="350" alt="Ecommerce dashboard page 2" src="https://github.com/user-attachments/assets/7b43121a-a041-48df-84d2-1ea26fec07db" />
</p>
