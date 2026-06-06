#  Customer Segmentation Using K-Means Clustering

##  Business Problem

The business aims to better understand customer behavior in order to improve delivery operations and marketing strategies. Customers differ in order value, delivery distance, and frequency of delays, making it difficult to apply a one-size-fits-all strategy. The goal is to segment customers into meaningful groups to support data-driven decision-making.



##  Dataset

The dataset contains delivery and customer transaction information with the following key features:

- Order_Value_USD: Monetary value of each order
- Distance_Km: Delivery distance in kilometers
- Dispatch_Hour: Time of order dispatch
- Delivery_Window_Hours: Expected delivery time window
- Previous_Delays_For_Customer: Number of past delivery delays
- Driver_Experience_Years: Experience level of assigned drivers

These features were used to understand customer behavior and delivery patterns.



##  Clustering Method

The K-Means clustering algorithm was used to group customers into distinct segments based on similarity in behavior.

Steps followed:
1. Data preprocessing and feature selection
2. Standardization of numerical variables
3. Determining optimal number of clusters using the Elbow Method
4. Applying K-Means clustering
5. Assigning cluster labels to each customer
6. Visualizing clusters using scatter plots and summary statistics

K-Means was chosen due to its simplicity, efficiency, and effectiveness in identifying patterns in numerical data.



##  Main Results

The clustering model identified several distinct customer groups:

- Low-value, short-distance customers (most frequent segment)
- High-value customers with larger order amounts
- Long-distance delivery customers with moderate spending
- Mixed behavior clusters with inconsistent patterns

The scatter plot of Order Value vs Distance shows clear separation between these groups, confirming that the clustering model successfully captured meaningful patterns in the data.



## 💡 Business Recommendations

Based on the clustering results, the business can implement the following strategies:

### 1. High-Value Customers
- Offer loyalty rewards and premium delivery services
- Prioritize fast and reliable delivery for retention

### 2. Low-Value Customers
- Use discounts and promotions to increase spending
- Encourage repeat purchases through marketing campaigns

### 3. Long-Distance Customers
- Optimize delivery routes to reduce cost and delays
- Assign more experienced drivers to complex deliveries

### 4. Operational Improvements
- Use cluster insights to improve logistics planning
- Reduce delivery delays by analyzing problematic segments



## 📌 Conclusion

K-Means clustering provides a powerful way to segment customers based on behavioral and operational data. These insights enable the business to move from a generic strategy to a targeted, data-driven approach that improves efficiency, customer satisfaction, and profitability.
