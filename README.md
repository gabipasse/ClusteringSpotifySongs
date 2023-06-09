# ClusteringSpotifySongs

Initially, a smaller dataframe of SpotifySongs was clustered into 5 "supergenres" using kmeans_pca. Then, a bigger dataframe was clustered into 50 different clusters.

The earliest was done by pipelining said dataframe using StandardScaler to keep track of all values accordingly to their standard deviation and PCA to get the 2 principal bilinear components from said dataframe. Then, Kmenas PCA was used to agroup all songs into one of 5 different "supergenres" (clusters).

The latter was done accordingly to the same logic from the previous one, but one hot encoding was used to encode the "artists" column of said dataframe. As that encoding was used, it was combined with an argument of n_components = 0.7. It was done because the encoding generated 875 columns; meaning that going for an argument of explained variance. At the clustering stage, these 20000 songs were clustered into one of 50 different clusters. Then, the first two principal components generated by the first PCA were used to calculate the euclidean distances between the choosen song and each of the other songs that were grouped in the same cluster as said song; sorting these songs accordingly to this distance.
