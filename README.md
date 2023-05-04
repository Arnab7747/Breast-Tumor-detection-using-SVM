# Brest-Tumor-detection-using-SVM
A Summary of the Data Preprocing Approach used here:
assign features to a NumPy array X, and transform the class labels from their original string representation (M and B) into integers
Split data into training and test sets
Standardize the data.
Obtain the Eigenvectors and Eigenvalues from the covariance matrix or correlation matrix
Sort eigenvalues in descending order and choose the kk eigenvectors that correspond to the kk largest eigenvalues where k is the number of dimensions of the new feature subspace (k≤dk≤d).
Construct the projection matrix W from the selected k eigenvectors.
Transform the original dataset X via W to obtain a k-dimensional feature subspace Y.
Predictive model using Support Vector Machine (SVM)
Important Parameters
The important parameters in kernel SVMs are the

Regularization parameter C,
The choice of the kernel,(linear, radial basis function(RBF) or polynomial)
Kernel-specific parameters.
gamma and C both control the complexity of the model, with large values in either resulting in a more complex model. Therefore, good settings for the two parameters are usually strongly correlated, and C and gamma should be adjusted together.
