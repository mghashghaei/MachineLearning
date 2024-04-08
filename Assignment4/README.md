# MachineLearning
Machin Learning Course
In this project for my coursework, I studied how to use the K-means clustering algorithm. The goal was to learn how K-means works for grouping data points and then apply it to compressing images. Below, I’ll explain the steps I took, the challenges I faced, and what I found out.

Understanding K-means Clustering

K-means is a common algorithm used in unsupervised learning. It’s great for grouping data points together. The aim is to split n observations into k clusters, where each observation goes to the cluster with the closest average value. Here’s how it works:

Start by picking k random points called centroids. Each centroid represents the center of a cluster.
Keep doing these two steps:
Assign each data point to the nearest centroid.
Recalculate the centroids by finding the average of all points in each cluster.
Repeat until the assignments don’t change much, trying to make the clusters as tight as possible.
Setting Up the Environment

First, I set up my Python environment and imported some libraries I needed:

pythonCopy code
import numpy as np
import matplotlib.pyplot as plt
from utils import *
%matplotlib inline
Phase 1: Finding Closest Centroids

My first task was to write a function called find_closest_centroids. This function finds the closest centroid for each training example. Here's a basic outline of what I did:

pythonCopy code
centroids = kMeans_init_centroids(X, K)
for iter in range(iterations):
  idx = find_closest_centroids(X, centroids)
  centroids = compute_centroids(X, idx, K)
Phase 2: Computing New Centroids

After assigning points to the closest centroids, I needed to find new centroids. This involved averaging the data points in each cluster:

pythonCopy code
def compute_centroids(X, idx, K):
 # I implemented the details here
Application to Image Compression

Now, let’s talk about applying K-means to compressing images. The idea is to reduce the number of colors in an image by grouping similar colors together. Here’s what I did:

Dataset Preparation: I loaded the image and prepared the data.
Applying K-means: I used K-means to find the most representative colors.
Image Reconstruction: I mapped each pixel’s color to the closest centroid and rebuilt the image with fewer colors.
Results and Conclusion

Using K-means for image compression showed how it can reduce the image’s color space while keeping its essence. This project not only helped me understand K-means better but also showed its usefulness in saving and sharing digital images more efficiently. Overall, it was a great learning experience!

5





