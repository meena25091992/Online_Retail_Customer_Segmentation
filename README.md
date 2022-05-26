# online_retail_customer_segmentation
Many small online retailers and new entrants to the online retail sector are keen to practice consumer-centric marketing in their businesses yet technically lack the necessary knowledge and expertise to do so. In this project we are using unsupervised machine learning techniques to segment customers for an online retailer.

On the basis of the Recency, Frequency, and Monetary model, customers of the business have been segmented into various meaningful groups using the k-means clustering algorithm, Hierarchical clustering and the main characteristics of the consumers in each segment have been clearly identified.

# Problem Statement

The main purpose of this project is to help the business better understand its customers and therefore conduct customer-centric marketing more effectively. In this project, our task is to identify major customer segments on a transactional data set which contains all the transactions for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

# Why Segment Customers?

Customer Segmentation is the process of dividing customers into homogeneous and distinct groups. It helps a company to develop an effective strategy for targeting its customers. This has a direct impact on the entire product development cycle, the budget management practices, and the plan for delivering targeted promotional content to customers.

Customer segmentation can also help a company to understand how its customers are alike, what is important to them, and what is not.

# Data Exploration and Preprocessing

At the very first I explored the dataset by looking at the top and bottom rows, checking its shape, columns and basic info, checked for duplicate and missing values. Dropped 5225 duplicate entries present in the dataset. The Description and CustomerID column has missing values which were 25% of total data and dropped missing values without losing much data.

Next, performed exploratory data analysis. Saw the minimum value for quantity is negative and after checking got to know about canceled orders. There were 8872 canceled orders in the dataset. Looked at the total number of products, transactions, and customers in the dataset. Some of the products had more than one description as the number of Stock codes and Description did not match. Then checked the number of transactions from each country and observed around 88% of transactions were from the UK. Next, I tried to get some insights from the data by plotting graphs and charts. I observed top 5 selling product and aslo observed which country maximum transactions and found that most customers were from the UK.

For the next step of RFM analysis, filtered the dataset by removing canceled orders and taking a subset of only UK based customers.

# RFM Analysis

RFM stands for Recency, Frequency, and Monetary. RFM analysis is a marketing technique in analyzing customer behavior such as how recently a customer has purchased, how often the customer purchases, and how much the customer spends. The advantage is that the customers’ behavior can be captured by using a relatively small number of features. The RFM variables are appropriate for capturing the specifics of the customer's purchase behavior.

After getting the RFM values, created quartiles on each of the metrics and assigned the required order. Divided each metric into 4 cuts. For example, the recency metric, the highest value, 4, is assigned to the customers with the least recency value (since they are the most recent customers). For the frequency and monetary metric, the highest value, 4, is assigned to the customers with the top 25% frequency and monetary values, respectively.

# RFM based Clustering models

First, used K-means clustering and built multiple clusters to find the optimal number of clusters using elbow method and silhouette method. From both methods I got k=2 as the optimal number of clusters.

Next, I used an Agglomerative Hierarchical Clustering algorithm but before that drew the dendrogram to evaluate the number of clusters. From dendrogram got two optimal clusters and then applied hierarchical clustering on RFM data using clusters k=2.

# Conclusion

We have performed RFM analysis on the online retail dataset and then used Recency, Frequency and Monetary values to form clusters using K-means clustering, Hierarchical clustering algorithms. K-means clustering and Hierarchical clustering segmented the customers very well using 2 clusters. We got two customer segments that were to be formed on this online retail dataset as a wholesale customer segment and average customer segment.
