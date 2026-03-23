## Overview

This repository contains the solution for Task 8 of the AI & ML Internship, focusing on unsupervised learning using K-Means clustering. The objective was to apply K-Means to a dataset, determine the optimal number of clusters, visualize the results, and evaluate the clustering performance.

## Objective

The primary objective of this task was to perform unsupervised learning using K-Means clustering on a given dataset.

## Tools Used

* **Scikit-learn:** For implementing the K-Means algorithm, data scaling, and performance evaluation.
* **Pandas:** For data loading, manipulation, and analysis.
* **Matplotlib:** For visualizing the clusters and the Elbow Method.

## Dataset

The dataset used for this task is the **Mall Customer Segmentation Dataset**.
[cite_start]You can download the dataset from [click here to download dataset](https://www.kaggle.com/datasets/vjchauhan/mall-customers) (or the specific link provided in the task document ).
For this project, the dataset file `Mall_Customers.csv` is expected to be in the same directory as the Jupyter Notebook or Python script.

## Solution Steps

The following steps were performed to complete the task:

1.  **Load and Visualize Dataset:**
    * The `Mall_Customers.csv` dataset was loaded using Pandas.
    * Initial visualization of the `Annual Income (k$)` and `Spending Score (1-100)` features was performed to understand the data distribution.
    * Data was scaled using `StandardScaler` from Scikit-learn, which is crucial for distance-based algorithms like K-Means.

2.  **Fit K-Means and Assign Cluster Labels:**
    * K-Means clustering was applied to the scaled dataset.
    * Cluster labels were assigned to each data point based on the clustering result.

3.  **Use the Elbow Method to Find Optimal K:**
    * The Elbow Method was used to determine the optimal number of clusters (K). This involved calculating the Sum of Squared Errors (SSE) for a range of K values and plotting them. The "elbow" point in the plot indicates a suitable K.

4.  **Visualize Clusters with Color-Coding:**
    * The clusters were visualized using Matplotlib, with different colors representing different clusters.
    * Cluster centroids were also plotted to show the center of each cluster.

5.  **Evaluate Clustering Using Silhouette Score:**
    * The Silhouette Score was calculated to evaluate the quality of the clustering. A higher Silhouette Score indicates better-defined clusters.

## Code Structure

The core logic is implemented in a Jupyter Notebook (or Python script) which includes:

* Importing necessary libraries (`pandas`, `matplotlib.pyplot`, `sklearn.cluster.KMeans`, `sklearn.preprocessing.StandardScaler`, `sklearn.metrics.silhouette_score`).
* Code to load and preprocess the data.
* Implementation of the Elbow Method.
* K-Means model training and prediction.
* Visualization of results.
* Calculation of the Silhouette Score.
