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
![Screenshot 2023-05-04 134808](https://user-images.githubusercontent.com/113490566/236148756-584abe14-2819-4519-91f2-bc6c27219266.png)
Observation
There are two possible predicted classes: "1" and "0". Malignant = 1 (indicates prescence of cancer cells) and Benign = 0 (indicates abscence).

The classifier made a total of 174 predictions (i.e 174 patients were being tested for the presence breast cancer).
Out of those 174 cases, the classifier predicted "yes" 58 times, and "no" 113 times.
In reality, 64 patients in the sample have the disease, and 107 patients do not.
Rates as computed from the confusion matrix
Accuracy: Overall, how often is the classifier correct?

(TP+TN)/total = (57+106)/171 = 0.95
Misclassification Rate: Overall, how often is it wrong?

(FP+FN)/total = (1+7)/171 = 0.05 equivalent to 1 minus Accuracy also known as *"Error Rate"*
True Positive Rate: When it's actually yes, how often does it predict 1?

TP/actual yes = 57/64 = 0.89 also known as "Sensitivity" or *"Recall"*
False Positive Rate: When it's actually 0, how often does it predict 1?

FP/actual no = 1/107 = 0.01
Specificity: When it's actually 0, how often does it predict 0? also know as true positive rate

TN/actual no = 106/107 = 0.99 equivalent to 1 minus False Positive Rate
Precision: When it predicts 1, how often is it correct?

TP/predicted yes = 57/58 = 0.98
Prevalence: How often does the yes condition actually occur in our sample?

actual yes/total = 64/171 = 0.34
