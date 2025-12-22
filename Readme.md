# Customer Segmentation - RFM Analysis

**Unlocking Customer Insights for Targeted Marketing & Revenue Growth**

Developed this project to solve a core business problem in e-commerce and retail: **How can we understand and group customers based on their actual purchasing behavior to deliver personalized marketing and improve customer retention?**

This repository contains a complete **RFM (Recency, Frequency, Monetary)** analysis + **K-Means clustering** pipeline on the **UCI Online Retail** dataset
### Business Problem
- Businesses often treat all customers the same, leading to wasted marketing spend and poor retention.
- Without segmentation, it's hard to identify:
  - High-value loyal customers (VIPs)
  - At-risk or dormant customers
  - New or low-engagement buyers

**Goal**: Segment customers into meaningful groups so the business can:
- Reward loyal customers with exclusive offers
- Re-engage at-risk customers with win-back campaigns
- Nurture new customers to increase lifetime value

### Solution Approach
1. **Data Collection & Cleaning**  
   - Fetched the UCI Online Retail dataset via `ucimlrepo`  
   - Removed cancelled orders and missing customer IDs  
   - Aggregated transactions by customer

2. **RFM Feature Engineering**  
   - **Recency** — Days since last purchase  
   - **Frequency** — Number of purchases  
   - **Monetary** — Total amount spent  
   - Created a clean RFM table for clustering

3. **Clustering with K-Means**  
   - Scaled features using StandardScaler  
   - Determined optimal number of clusters using Elbow Method and Silhouette Score  
   - Applied K-Means to segment customers into 4 meaningful groups

4. **Segmentation & Interpretation**  
   - Assigned interpretable labels to clusters  
   - Analyzed characteristics of each segment

### Customer Segments Identified
| Segment              | Description                              | Business Strategy                              |
|----------------------|------------------------------------------|------------------------------------------------|
| **VIP Customers**    | High spend, frequent, recent purchases   | Loyalty rewards, exclusive offers, premium service |
| **Regular Buyers**   | Moderate spend and frequency             | Upsell/cross-sell, product recommendations     |
| **At-Risk / Dormant**| Recent purchases low or none             | Re-engagement campaigns, discounts, win-back emails |
| **New / Low-Value**  | Few purchases, low spend                 | Onboarding offers, educational content         |

### Key Insights & Business Recommendations
- VIPs (top ~10–15%) contribute ~60–70% of revenue (Pareto principle) → prioritize them
- At-risk customers show a sharp drop in recency → target them within 30–60 days
- New customers can be nurtured into Regular or VIP with early promotions
- High-frequency but low-monetary customers are great for upselling

### Business Impact

- Enables personalized marketing at scale
- Improves customer retention by 15–30% (industry benchmarks)
- Increases average order value through targeted upselling
- Reduces marketing waste by focusing on high-potential segments
