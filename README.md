Project Title: Data Redundancy Optimization in HDFS via Machine Learning Clustering Techniques

Overview:
This project focuses on optimizing data redundancy in the Hadoop Distributed File System (HDFS) using machine learning clustering techniques. HDFS typically uses replication to ensure fault tolerance and availability, but this can lead to excessive use of storage. The goal of this project is to intelligently analyze block-level metadata and identify opportunities to reduce unnecessary replication while maintaining system performance and reliability.

Problem Statement:
HDFS stores multiple replicas of each data block by default to ensure reliability. While this improves data availability, it also consumes significant storage resources. Many blocks may not require such high levels of replication, especially those that are rarely accessed. By analyzing the characteristics of each data block, it is possible to cluster them based on their usage patterns and suggest optimized replication strategies.

Approach and Methodology:
1. Data was collected to simulate HDFS block metadata, including features like block size, replication count, access frequency, and storage node information.
2. The data was preprocessed by performing normalization and feature engineering to prepare it for clustering.
Several clustering techniques were applied, including K-Means, DBSCAN, and Hierarchical Clustering, to group similar data blocks based on their behavior.
3. The clusters were analyzed to identify which types of blocks could safely have reduced replication without risking data loss or performance degradation.
4. A recommendation system was developed to suggest optimal replication factors for different categories of blocks.
5. The system was validated through simulations that monitored changes in storage utilization and data availability.

Tools and Technologies Used:
-Python for data processing and model development
-Libraries such as Pandas, NumPy, and Scikit-learn
-Visualization tools including Matplotlib and Seaborn
-Simulated or pseudo-distributed HDFS setup

Project Structure:
-A data folder containing example HDFS metadata
-Preprocessing scripts for data cleaning and feature preparation
-Clustering scripts implementing different algorithms
-Analysis scripts for evaluating and visualizing clustering results
-A results folder with output reports and visualizations

Key Results:

-The clustering models successfully identified patterns in block behavior
-K-Means performed effectively in separating low-access from high-access blocks
-The project showed potential for meaningful storage savings, particularly for cold data blocks
-Visualizations made it easier to interpret the clustering outcomes and explain recommendations
