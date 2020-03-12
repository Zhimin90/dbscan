Modified by: Zhimin Zou
Modified original McCormick's code. Altered DBSCAN algorithm to have a maximum
density for each cluster. When growing each cluster, if max density has been reached,
the Breadth first search stops and returns search points for the next cluster to group.

This project contains a simple implementation of DBSCAN intended to illustrate how the algorithm works. It was written to go along with my blog post [here](http://mccormickml.com/2016/11/08/dbscan-clustering/).

My implementation can be found in `dbscan.py`.

In `scikit-dbscan-example.py`, I run both my implementation and the scikit-learn implementation on a dataset and confirm that the resulting labels match.

To improve the performance of my implementation, you would want to use matrix-vector operations to perform the distance calculations (instead of calculating each distance individually in a for-loop).
