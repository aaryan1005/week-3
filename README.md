Project 3: Unsupervised Learning - Customer Segmentation
Goal: Use distance-based machine learning algorithms to discover hidden mathematical groupings in unlabeled retail data and translate them into actionable business personas.

📖 Project Overview
Retail datasets are often highly dimensional and difficult to analyze manually. This project leverages unsupervised machine learning to group customers based on purchasing behavior, demographics, and platform engagement. By reducing the noise in the data and applying clustering algorithms, we transform raw transaction logs into clear, targetable customer profiles.

Key Objectives:

Generate a realistic 22-feature retail dataset containing transactional and behavioral metrics.

Mitigate the "curse of dimensionality" using Principal Component Analysis (PCA).

Mathematically determine the optimal number of customer segments using the Elbow Method and Silhouette Score.

Translate the resulting mathematical clusters into actionable business strategies.

🧠 Methodology
1. Data Preprocessing & Standardization
Distance-based algorithms are highly sensitive to the scale of the data. All numeric features were scaled so that metrics like "Annual Income" do not overpower smaller-scale metrics like "Web Visits."

2. Dimensionality Reduction (PCA)
To ensure K-Means calculates distance effectively, the 22 original features were compressed down to 3 Principal Components. This captures the maximum variance in the data while stripping away underlying noise, allowing for clear 2D and 3D visualization.

3. Mathematical Cluster Optimization
The optimal number of clusters (K) was not guessed. It was proven using two rigorous evaluation metrics:

The Elbow Method: Plotted the Within-Cluster Sum of Squares (WCSS) to identify the point of diminishing returns.

The Silhouette Score: Validated the distinctness and separation of the clusters.

4. K-Means Clustering
Applied the K-Means algorithm using the mathematically proven optimal K to assign every customer to a distinct, non-overlapping segment.

📊 Business Personas Identified
The algorithm successfully identified 4 distinct customer segments. By mapping the clusters back to the original un-reduced data, we derived the following actionable business personas:

Segment Name	Identifying Behaviors	Recommended Business Action
Loyal Bulk-Buyers	High frequency, high basics spend, low discount usage.	Implement subscription models and volume-based incentives.
Premium Splurgers	Low frequency, massive average order value, buys electronics/premium items.	Offer VIP early access to new seasonal product drops.
Budget Deal-Seekers	High discount usage, high web visits, average spend.	Target with time-sensitive promotional codes and flash sales.
Churn Risk / Inactive	High recency days, high cart abandonment, low engagement.	Deploy aggressive win-back email campaigns and retargeting ads.
💻 Technical Stack
Language: Python

Data Manipulation: pandas, numpy

Machine Learning: scikit-learn (PCA, K-Means, StandardScaler)

Data Visualization: matplotlib, seaborn

🚀 How to Run the Project
1. Clone the repository:

Bash
git clone https://github.com/yourusername/customer-segmentation.git
cd customer-segmentation
2. Install dependencies:

Bash
pip install -r requirements.txt
3. Execute the pipeline:

Bash
python customer_segmentation.py
Note: Running this script will automatically generate the synthetic dataset, print the optimal variance metrics, output the business matrix to the console, and save the evaluation and clustering visualizations as PNG files in your directory.
