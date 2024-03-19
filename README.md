# Face-Recognition
**Objective**

The goal of this project was to apply the Eigenfaces method, combining Principal Component Analysis (PCA) for feature extraction and the nearest neighbor classifier for face recognition. The project utilized the Yale B face database, featuring 10 individuals photographed under 64 different lighting conditions.

The approach involved three key steps:

1. Data Preparation: Each 50x50 pixel image from the training set was transformed into a 2500-dimensional vector and stored in a matrix. PCA was then applied to extract the principal components, which, when visualized as images, are known as Eigenfaces.
2. Feature Extraction: Both training and test set images were projected into a lower-dimensional space (d dimensions) called eigenspace, from which low-dimensional features were extracted.
3. Classification: Faces were recognized in the eigenspace using a nearest neighbor classifier with Euclidean distance as the metric.
The datasets were divided into subsets (Set_1 to Set_5) based on the image numbers, with Set_1 used for training. The project evaluated the Eigenfaces algorithm's ability to handle different lighting conditions in the test images compared to the training images.

**Results**
* A function loadImages(path, set_number) was implemented to read images and return a data matrix along with labels.
* The Eigenfaces method was trained with d=9 and d=30 using images from Set_1 and tested across all sets to report classification accuracy. The findings showed expected 100% accuracy on Set_1 and varied accuracy on other sets, highlighting the method's generalization capabilities.
* The top 9 eigenvectors (Eigenfaces) were visualized and analyzed for their representation significance.
* Using d=9 and d=30 Eigenfaces from Set_1, a random image from each set was reconstructed to comment on the reconstruction quality.

# Image Classification Using SVMs
**Objective**

The second project aimed to explore the performance of Support Vector Machines (SVMs) in recognizing handwritten digits using the MNIST dataset.

**Methodology**

* Data Loading and Preprocessing: The MNIST dataset comprising 70,000 images was loaded, with each image vectorized into a 784-dimensional vector and normalized.
* SVM Training and Testing: SVMs were trained with linear and RBF kernels, experimenting with different parameter values to identify the combination that yields the highest classification accuracy on both the training and test sets.
* PCA and SVM Application: PCA was applied to the dataset with three different retained variance values. For each, SVMs were retrained using the best parameters identified earlier to report on the number of components, classification accuracy, and execution times.

**Results**
* The project detailed the SVM kernel types, parameter values (C and gamma), and their impact on classification performance.
* For each PCA-applied dataset, the number of components retained, classification accuracy, and execution times were documented, offering insights into the trade-off between classification accuracy, dimensionality reduction, and algorithm execution time.
