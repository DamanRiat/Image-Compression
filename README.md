# Image Compression using K-Means Clustering

## Project Overview

This project demonstrates an image compression technique using the K-Means clustering algorithm. The primary goal is to reduce the number of unique colors in an image while retaining its visual quality. This is achieved by clustering the pixel colors into a smaller number of clusters and then replacing each pixel's color with the nearest cluster centroid.

## Methodology

### Initialization

- **Random Initialization**: The initial centroids for the K-means algorithm are selected randomly from the set of unique colors in the image.

### K-Means Clustering

1. **Calculate Clusters**: Each pixel in the image is assigned to the nearest centroid based on Euclidean distance.
2. **Move Centroids**: The centroids are updated to the mean of all pixels assigned to each centroid.
3. **Convergence Check**: The algorithm checks for convergence by comparing the change in centroids and the change in pixel assignments between iterations.

### Compression Process

- The K-Means algorithm iterates to refine the centroids, minimizing the loss, defined as the sum of squared distances between each pixel and its assigned centroid.
- The number of iterations and the convergence criteria are used to ensure the algorithm stops when the centroids stabilize.

### Image Reconstruction

- The compressed image is reconstructed by replacing each pixel's color with the nearest centroid.

## Results

The compressed image retains the visual appearance of the original image but with a reduced color palette, thus achieving compression. The final compressed image quality and the number of colors depend on the number of clusters (K) chosen.

## Implementation

The implementation uses the following steps:

1. **Load and Normalize Image**: The image is loaded and normalized to ensure the pixel values are suitable for clustering.
2. **K-Means Training**:
    - Initialize centroids.
    - Iteratively calculate clusters, move centroids, and check for convergence.
3. **Image Reconstruction**: Replace each pixel's color with the nearest centroid.
4. **Evaluation**: Compare the original and compressed images.

## Usage

### Prerequisites

- Python 3
- NumPy
- Matplotlib
- Jupyter Notebook

