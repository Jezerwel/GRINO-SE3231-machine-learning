# Midterm Exam

### 1. Does preprocessing affect the result of the model? Why?

Yes, preprocessing significantly affects how well the model works. Here's a simpler explanation:

First, the model needs complete data to learn effectively. If important information is missing, the model might not work correctly or could produce misleading results. This project addresses missing data by either filling in the gaps (for example, by using an average value if a house's building area isn't listed) or by removing entries if they have too much critical information missing. These choices directly shape the data the model learns from.

Second, machine learning models generally work with numbers rather than text. Therefore, details like suburb names or property types are converted into numerical codes that the model can understand. Without this conversion, the model couldn't use this valuable information. The specific method used for this conversion can also influence the model's performance.

Third, it's important to ensure that all types of information (features) are on a relatively similar scale. For instance, house prices can be very large numbers, while the number of rooms is a small number. Feature scaling adjusts these features so they are in a comparable range. This prevents features with initially larger values from unfairly dominating the model's learning process. In the case of clustering houses, scaling helps ensure that groups are formed based on the overall similarity of properties, not just because one feature (like price) had much larger numbers than another (like distance to the city center).

Finally, preprocessing also helps in managing unusual or extreme data points, often called outliers (e.g., a house that is exceptionally expensive or inexpensive for its area compared to others). Techniques used for handling missing data and for scaling features can also help lessen the distorting impact of these outliers, leading to a more robust and reliable model.

In summary, preprocessing steps like cleaning data, transforming features, and scaling are essential for preparing the data into a suitable format for the model, improving its accuracy, and ensuring reliable results.

### 2. What is your conclusion based on the interpretation or result of your model?

- **Linear Regression Model (Visualized in "Actual vs. Predicted Housing Prices" image):**

  - The scatter plot shows a positive correlation between actual and predicted prices, indicating some predictive power. Many points cluster around the "Perfect Fit" line.
  - However, there's noticeable variance, especially for higher-priced houses. The model seems to under-predict some very high-priced properties, suggesting precision could be improved. (The specific MSE and R2 scores from the notebook would provide a more quantitative assessment).

- **KMeans Clustering Model (Visualized in "KMeans Clusters: Price vs. Distance (K = 3)" image):**
  - The model clusters the housing data into 3 distinct groups based on 'Price' and 'Distance':
    - **Cluster 0 (Purple on the graph):** Represents properties with **lower prices** (mostly below 2 million) and located at **shorter distances** (primarily under a distance of 15). This group shows a high density of properties.
    - **Cluster 1 (Teal/Dark Green on the graph):** This cluster is diverse, encompassing properties across a **wide range of prices**, from lower values up to the **overall highest-priced properties in the dataset** (reaching near 10 million). These properties mostly found within a distance of 0-20.
    - **Cluster 2 (Yellow on the graph):** This cluster primarily consists of properties with **lower prices** (many below 2 million). Its distinguishing feature is that these properties are generally located at **further distances** (mostly between distances of 10 and 45).
  - **Interpretation:** The KMeans clustering helps identify distinct market segments. For instance, Cluster 0 might represent more affordable, centrally-located properties. Cluster 2 could signify properties in more suburban or outlying areas that are generally more affordable but can reach mid-range prices. Cluster 1 captures a broad mix, including the most premium-priced properties irrespective of their exact distance. This segmentation can be valuable for understanding market structure, targeted real estate strategies, or identifying specific investment opportunities.
