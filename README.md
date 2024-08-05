Abstract
Title: Anomaly Detection in Network Traffic Using Isolation Forest and Dimensionality Reduction Techniques

Abstract:

This study presents an approach for detecting anomalies in network traffic data using machine learning techniques, specifically the Isolation Forest algorithm combined with dimensionality reduction methods. The dataset utilized in this analysis includes temporal and numerical features of network traffic, including a date column and various numerical attributes.

Data Preprocessing:
The dataset, cs448b_ipasn.csv, includes a date column which is converted to a datetime format. From this date, the 'day of the year' is extracted and used as a numerical feature. Along with 'day_of_year', other relevant numerical features include 'l_ipn', 'r_asn', and 'f'. These features are selected for analysis after conversion and extraction.

Feature Scaling:
The numerical features are standardized using StandardScaler to ensure that all features contribute equally to the anomaly detection process.

Anomaly Detection:
The Isolation Forest algorithm, an unsupervised learning method designed to identify anomalies, is applied to the scaled features. The model is configured with a contamination rate of 1%, indicating the expected proportion of outliers. Anomalies are flagged as -1 and normal data as 1.

Dimensionality Reduction:
To facilitate visualization, the data is first reduced to two dimensions using Principal Component Analysis (PCA). Subsequently, t-Distributed Stochastic Neighbor Embedding (t-SNE) is employed to further reduce the dimensionality and enhance the separation between anomalies and normal data.

Visualization:
The results are visualized using a scatter plot where t-SNE components are plotted, and anomalies are highlighted in red while normal data points are in blue. This visualization aids in understanding the distribution and separation of anomalies within the network traffic data.

Conclusion:
The combination of Isolation Forest for anomaly detection and t-SNE for visualization provides a comprehensive view of anomalous patterns in network traffic. This approach can be instrumental for network security and monitoring applications by effectively identifying and visualizing unusual behavior.

