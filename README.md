🛒 Online Retail Customer Segmentation

Unsupervised Learning using RFM Analysis

📌 Project Overview

This project focuses on segmenting customers of an online retail store based on their transaction history. 
By categorizing customers, businesses can create targeted marketing campaigns, improve retention, 
and identify high-value "VIP" shoppers.

🛠️ The RFM Framework

We used the RFM model to quantify customer behavior:
Recency ($R$): Days since the last purchase (lower is better).
Frequency ($F$): Number of unique transactions (higher is better).
Monetary ($M$): Total revenue generated (higher is better).

Data Pipeline

Data Cleaning: Removed rows with missing Customer ID and handled cancelled orders (Invoices starting with 'C').

Feature Engineering: Calculated the Total_Price and aggregated data to the customer level.

Outlier Management: Used clip(lower, upper) to cap extreme values that would distort clusters.

Preprocessing: Applied np.log1p to fix skewness and RobustScaler to normalize the data.

Clustering: Used the K-Means algorithm and the Elbow Method to determine the optimal number of customer groups.

📊 Key Results

The model successfully identified distinct segments, such as:

Champions: Recent, frequent, and high-spending customers.

At Risk: Customers who haven't shopped in a long time (e.g., 400+ days).

Loyalists: Consistent shoppers with moderate spending.

💻 Tech Stack

Language: Python

Libraries: Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib

Environment: Jupyter Notebook (Ubuntu/Linux)
