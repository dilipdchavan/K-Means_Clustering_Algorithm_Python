# K-Means_Clustering_Algorithm_Python


## What is Clustering?
To assemble or group something with common purpose or common features.
Based on the analogy, in K-means clustering we will group similar data points from a set of observations together.

## K clustering is an
•	Unsupervised machine learning algorithm
•	An iterative algorithm
•	Finds groups in a given unlabeled data set
•	Helps categorize similar data points to a cluster.
•	No prior categorization is required except for the input features that will help with clustering the data points

K-means clustering algorithm is an iterative algorithm where K specifies the number of clusters in which we need to group the data points.

Step 1: Choose the number of clusters. we refer it by K
Step 2: Randomly select K centroids. These centroids can be from the dataset or could be any random point
Step 3: Assign each data point to the nearest centroid
Step 4: Recompute the new centroid and place the new centroid for each cluster
Step 5: Based on new centroid, check if any data points in the dataset can be reassigned to a different cluster, if the data points changed the cluster then go to step 3. If no reassignment happened then all the data points are grouped in K clusters.

## Random initialization trap
when the centroids are randomly initialized, each run of k means produce different WCSS. Incorrect choice of centroids lead to suboptimal clustering.
To solve the issue of incorrect centroids, we use K-means++, where we select the centroids as far as possible at initialization.
The idea is to have centroids to create distinct clusters centers to have optimal clustering to converge fast.




## We will now run these steps on the dataset plotted in Python. [Clustering_K_Means.ipynb]

We import KMeans from sklearn.cluster for K Means algorithm.
I have downloaded the dataset in my default Jupyter folder and names it as heart.csv.
Reading the data into heart_data dataset

We first try to use the elbow method to know the optimal number of clusters using WCSS- within cluster sum of squares.
We apply feature engineering and select relevant features from the dataset

Calculating WCSS
we first create an empty list wcss_heart to store the different values for wcss for different number of clusters.
we chose clusters from 1 to 10 and property inertia_ gives sum of squared distances of data points to their closest cluster center.

let’s plot the data between number of clusters and within cluster sum of squares.
By Elbow method, we see that sudden drop happens at 2 , so the optimal number of cluster for heart dataset is 2.
Now run KMeans using k-means++ random initialization
Now visualize the data along with centroids.

