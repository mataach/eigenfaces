## Q1. Computationally Efficient Eigenfaces

Partition the provided face data into your training and testing data, e.g. 8 images and 2
other images of each face identity for training and testing respectively.
Apply PCA to your training data i.e. compute the eigenvectors and eigenvalues of the covariance matrix S=(1/N)AAT directly, and use the low-dimensional computation of eigenspace i.e. using (1/N)ATA of your training data.
Show and discuss, in comparison, including: the eigenvectors and eigenvalues, the mean image, how many eigenvectors are with non-zero eigenvalues, if the eigenvectors and eigenvalues obtained by the two methods are identical, what are the pros/cons of each method. Give physical meanings and show respective measurements for your answers.

Hereinafter, we use the low-dimensional PCA technique:
Do face image reconstruction while varying the number of PCA bases learnt. Show and discuss the results quantitatively and qualitatively for different face images.
Perform PCA-based face recognition by the NN classification. Report and discuss, including: recognition accuracies (success rates), example success and failure cases, the confusion matrices, time/memory, by varying the parameter values. Give insights and reasons behind your observations.


## Q2. Incremental PCA

Use the same data partition into training and testing as in Q1. Further divide the training data equally into four subsets, each with 104 images (i.e. two images per person). Starting with the first subset, keep adding a more subset into your training.
Perform Incremental PCA, and compare it with the counterpart i.e. batch PCA, and PCA trained only by the first subset, in terms of training time, reconstruction error, face recognition accuracy.
Show and discuss, including: how accurate your incremental method is, what important parameters in the method are (and how they are set). Provide your own discussions and measurements to support.


## Q3. PCA-LDA Ensemble for Face Recognition

Use the provided face data, and the same data partition into training and testing as in Q1.

### PCA-LDA
Perform the PCA-LDA based face recognition with the NN classifier. Report and discuss, in comparison to PCA method, including:
- recognition accuracies by varying the hyper-parameter values, e.g. M_pca and M_lda
- ranks of the scatter matrices,
- the confusion matrix, example success and failure cases


### PCA-LDA Ensemble
Show, measure and discuss the results, by varying its parameter values. Give insights and reasons behind your answers, including:
- randomisation in feature space
- the number of base models, the randomness parameter,
- the error of the committee machine vs the average error of the individual models
- fusion rules (majority voting and sum)
- recognition accuracy and confusion matrix
