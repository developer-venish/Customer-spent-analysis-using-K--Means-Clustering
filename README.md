# Customer-spent-analysis-using-K--Means-Clustering
ML Python Project

![](https://github.com/developer-venish/Customer-spent-analysis-using-K--Means-Clustering/blob/main/GRAPH.png)

![](https://github.com/developer-venish/Customer-spent-analysis-using-K--Means-Clustering/blob/main/graph1.png)

---------------------------------------------------------------------------------------

Note :- All the code in this project has been tested and run successfully in Google Colab. I encourage you to try running it in Colab for the best experience and to ensure smooth execution. Happy coding!

---------------------------------------------------------------------------------------

This code performs K-means clustering on a dataset containing two variables: 'INCOME' and 'SPEND'. It aims to find natural groupings (clusters) of data points based on these two features.

Let's go through the code step-by-step:

1. Importing Libraries:
   - The code imports the required libraries: pandas, numpy, matplotlib.pyplot, and files from the google.colab module.

2. Data Loading:
   - The code uses the 'files.upload()' function to upload a CSV file named 'dataset.csv'.
   - The uploaded file is read into a pandas DataFrame called 'dataset'.

3. Exploratory Data Analysis:
   - The code prints the shape of the dataset using `dataset.shape`, providing the number of rows and columns in the DataFrame.
   - It uses `dataset.describe()` to display statistical summary (mean, min, max, quartiles) of the data.
   - The first five rows of the dataset are displayed using `dataset.head(5)`.

4. Data Preparation:
   - The 'INCOME' and 'SPEND' columns are extracted from the DataFrame and stored in separate arrays, `Income` and `Spend`.
   - The 'Income' and 'Spend' arrays are combined into a 2D array 'X' using `np.array(list(zip(Income, Spend)))`.

5. Finding the Optimal K Value (Number of Clusters):
   - The code performs K-means clustering for different values of K (number of clusters) from 1 to 10.
   - It calculates the within-cluster sum of squares (WCSS) for each value of K and stores it in the list 'wcss'.
   - The WCSS measures the variance within each cluster and is used to find the optimal K value.
   - A plot of K values against their corresponding WCSS is generated to identify the 'elbow point' that represents the optimal K value. This point is where the rate of decrease in WCSS starts to slow down.

6. K-means Clustering:
   - The code performs K-means clustering with K=4 (as it is identified as the optimal value) using `KMeans(n_clusters=4, random_state=0)`.
   - The `fit_predict(X)` method is used to predict the cluster labels for each data point.

7. Visualization:
   - The data points are plotted based on their cluster labels using different colors.
   - The cluster centers (centroids) are also plotted in red squares.
   - The plot shows the 'Income' on the x-axis and 'Spent' on the y-axis, with data points divided into four clusters based on their similarity.

Overall, this code performs K-means clustering on a 2D dataset, identifies the optimal number of clusters, and visualizes the data points and cluster centers in a 2D plot. It provides insights into how customers' income and spending habits are grouped into distinct clusters.

---------------------------------------------------------------------------------------
