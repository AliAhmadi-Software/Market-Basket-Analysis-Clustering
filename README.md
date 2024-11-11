# Market Basket Analysis - Clustering

This project performs clustering analysis on customer data to understand spending behaviors and identify customer segments. The analysis compares the performance of **K-Means** and **DBSCAN** clustering algorithms on a customer dataset.

## Dataset Description

The dataset contains the following columns:

- **CustomerID**: Unique identifier for each customer.
- **Gender**: Gender of the customer (Male/Female).
- **Age**: Age of the customer in years.
- **Annual Income (k$)**: Annual income of the customer in thousand dollars.
- **Spending Score (1-100)**: A score assigned to the customer based on their spending behavior and purchasing patterns.

## Exploratory Data Analysis (EDA)

The dataset was examined to understand basic distributions and relationships among the variables:

- **Gender Distribution**: Insights into the number of male and female customers.
- **Age Distribution**: Histogram and boxplot visualizations for age.
- **Annual Income Distribution**: Distribution analysis and boxplots for income data.
- **Spending Score Analysis**: Spending behavior examined by gender, income, and age groups.

## Clustering Analysis

### 1. K-Means Clustering

K-Means clustering was applied to group customers into distinct clusters based on **Age**, **Annual Income**, and **Spending Score**:

- **Elbow Method**: The optimal number of clusters was determined using the Elbow method, with 4 clusters chosen as optimal.
- **Visualization**: Clustering results were visualized using scatter plots for clear representation of the formed clusters.
- **Further Experimentation**: Additional clustering was performed with 5 clusters for comparative purposes.

### 2. DBSCAN Clustering

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) was also applied to the same data:

- **Initial Parameters**: Using initial values of `eps=0.5` and `min_samples=5`, 7 clusters were identified, including a noise cluster (-1) with 60 samples.
- **Parameter Tuning**: By increasing `eps` to 0.6 and `min_samples` to 8, noise was reduced to 52 samples, resulting in 4 main clusters.
- **Visualization**: The tuned clustering results were visualized, showing improved separation of clusters.

## Comparative Analysis

- **K-Means**: This algorithm provided well-defined clusters based on spending patterns and income. It performed consistently, forming distinct groups but was limited in handling outliers or noise.
- **DBSCAN**: Better suited for complex, varied-density data, DBSCAN identified more natural clusters and handled outliers effectively. Adjusting parameters improved clustering quality, making it useful for this dataset.

## Conclusion

Both K-Means and DBSCAN have strengths in clustering customer data. **K-Means** is effective for general clustering, while **DBSCAN** is advantageous for handling outliers and discovering clusters of varying densities. Based on the dataset’s characteristics, DBSCAN with tuned parameters provided a slightly more robust clustering solution.

