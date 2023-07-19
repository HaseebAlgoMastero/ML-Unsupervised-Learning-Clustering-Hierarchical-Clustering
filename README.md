# ML-Unsupervised-Learning-Clustering-Hierarchical-Clustering
Hierarchical clustering is another unsupervised machine learning algorithm, which is used to group the unlabeled datasets into a cluster and also known as hierarchical cluster analysis or HCA.

In this algorithm, we develop the hierarchy of clusters in the form of a tree, and this tree-shaped structure is known as the dendrogram.

Sometimes the results of K-means clustering and hierarchical clustering may look similar, but they both differ depending on how they work. As there is no requirement to predetermine the number of clusters as we did in the K-Means algorithm.

<h2>The hierarchical clustering technique has two approaches:</h2>


<h2>Agglomerative:</h2> Agglomerative is a bottom-up approach, in which the algorithm starts with taking all data points as single clusters and merging them until one cluster is left.
<h2>Divisive:</h2> Divisive algorithm is the reverse of the agglomerative algorithm as it is a top-down approach.
<h2>Why hierarchical clustering?</h2>
As we already have other clustering algorithms such as K-Means Clustering, then why we need hierarchical clustering? So, as we have seen in the K-means clustering that there are some challenges with this algorithm, which are a predetermined number of clusters, and it always tries to create the clusters of the same size. To solve these two challenges, we can opt for the hierarchical clustering algorithm because, in this algorithm, we don't need to have knowledge about the predefined number of clusters.

In this topic, we will discuss the Agglomerative Hierarchical clustering algorithm.

<h2>Agglomerative Hierarchical clustering</h2>
The agglomerative hierarchical clustering algorithm is a popular example of HCA. To group the datasets into clusters, it follows the bottom-up approach. It means, this algorithm considers each dataset as a single cluster at the beginning, and then start combining the closest pair of clusters together. It does this until all the clusters are merged into a single cluster that contains all the datasets.

This hierarchy of clusters is represented in the form of the dendrogram.

<h2>How the Agglomerative Hierarchical clustering Work?</h2>
The working of the AHC algorithm can be explained using the below steps:

<h2>Step-1:</h2> Create each data point as a single cluster. Let's say there are N data points, so the number of clusters will also be N.
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning.png">
<h2>Step-2:</h2> Take two closest data points or clusters and merge them to form one cluster. So, there will now be N-1 clusters.
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning2.png">
<h2>Step-3:</h2> Again, take the two closest clusters and merge them together to form one cluster. There will be N-2 clusters.
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning3.png">
<h2>Step-4</h2>: Repeat Step 3 until only one cluster left. So, we will get the following clusters. Consider the below images:
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning4.png">
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning5.png">
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning6.png">
<h2>Step-5:</h2> Once all the clusters are combined into one big cluster, develop the dendrogram to divide the clusters as per the problem.
Note:</h2> To better understand hierarchical clustering, it is advised to have a look on k-means clustering
<h2>Measure for the distance between two clusters</h2>
As we have seen, the closest distance between the two clusters is crucial for the hierarchical clustering. There are various ways to calculate the distance between two clusters, and these ways decide the rule for clustering. These measures are called Linkage methods. Some of the popular linkage methods are given below:

<h2>Single Linkage:</h2> It is the Shortest Distance between the closest points of the clusters. Consider the below image:
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning7.png">
<h2>Complete Linkage:</h2> It is the farthest distance between the two points of two different clusters. It is one of the popular linkage methods as it forms tighter clusters than single-linkage.
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning8.png">

<h2>Average Linkage:</h2> It is the linkage method in which the distance between each pair of datasets is added up and then divided by the total number of datasets to calculate the average distance between two clusters. It is also one of the most popular linkage methods.
<h2>Centroid Linkage:</h2> It is the linkage method in which the distance between the centroid of the clusters is calculated. Consider the below image:
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning9.png">
From the above-given approaches, we can apply any of them according to the type of problem or business requirement.

The dendrogram is a tree-like structure that is mainly used to store each step as a memory that the HC algorithm performs. In the dendrogram plot, the Y-axis shows the Euclidean distances between the data points, and the x-axis shows all the data points of the given dataset.

<h2>The working of the dendrogram can be explained using the below diagram:</h2>
<img src = "https://static.javatpoint.com/tutorial/machine-learning/images/hierarchical-clustering-in-machine-learning10.png">
In the above diagram, the left part is showing how clusters are created in agglomerative clustering, and the right part is showing the corresponding dendrogram.
<ul>
<li>As we have discussed above, firstly, the datapoints P2 and P3 combine together and form a cluster, correspondingly a dendrogram is created, which connects P2 and P3 with a rectangular shape. The hight is decided according to the Euclidean distance between the data points.</li>
<li>In the next step, P5 and P6 form a cluster, and the corresponding dendrogram is created. It is higher than of previous, as the Euclidean distance between P5 and P6 is a little bit greater than the P2 and P3.</li>
<li>Again, two new dendrograms are created that combine P1, P2, and P3 in one dendrogram, and P4, P5, and P6, in another dendrogram.</li>
<li>At last, the final dendrogram is created that combines all the data points together.</li>
<li>We can cut the dendrogram tree structure at any level as per our requirement.</li>
</ul>
<h2>Note:</h2> For Python Implementation check the Repository
<h2>Enjoy Machine learning</h2>
