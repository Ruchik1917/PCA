# PCA and GMM Clustering on MNIST

In this project, we used Principal Component Analysis (PCA) to reduce the dimensionality of the MNIST dataset. After reducing the data, we applied Gaussian Mixture Model (GMM) clustering to group the digits. PCA was implemented from scratch, while standard libraries were used for SVD and GMM.

## Steps

1. Loaded the MNIST handwritten digit dataset.
2. Performed PCA from scratch with three different component sizes:
   - 32 components
   - 64 components
   - 128 components
3. Applied GMM clustering with three different cluster sizes:
   - 10 clusters
   - 7 clusters
   - 4 clusters
4. Visualized the sample images from each cluster to observe grouping behavior.
5. Compared the cluster characteristics with the previous K-Means clustering task.
6. Created a function to find the optimal number of PCA components that retain most of the information.
7. Analyzed where PCA might fail and what limitations it has.

## Files

- `pca_gmm_clustering.ipynb` – Main notebook with PCA implementation, clustering, and visualizations
- `pca_from_scratch.py` – PCA implemented from scratch using basic NumPy operations
- `optimal_components.py` – Function to find the best number of PCA components
- `README.md` – This explanation file

## Visualizations

We visualized the clusters by showing examples of digits grouped together after PCA and GMM. This helped us see how well the model was separating the digit classes.

## Comparison with Previous Task

Compared to K-Means clustering with cosine similarity:
- PCA helped reduce noise and improved clustering quality in lower dimensions.
- GMM was able to handle overlapping classes better than K-Means in some cases.
- Some digits still overlapped, showing PCA has limits when it comes to preserving fine details.

## Conclusion

PCA is a powerful tool for simplifying complex data while keeping essential patterns. When combined with GMM, it offers a more flexible clustering approach. However, PCA can miss subtle patterns, especially when reducing to too few components. Choosing the right number of components is crucial for keeping important information.

