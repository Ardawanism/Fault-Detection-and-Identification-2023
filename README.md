# Fault-Detection-and-Identification-2023
In this repo, a few topics about useful Machine Learning and Deep Learning algorithms for Fault Detection and Identification are taught.
## Context
Machine Learning and Deep Learning algorithms play an important role in Intelligent Condition Monitoring and Data-Driven Fault Detection and Identification. Some of useful algorithms are implemented from scratch and investigated in depth in this repo. At first, PCA and LDA dimension reduction methods are implemented from scratch and investigated. Then, Multi-Layer Perceptron is utilized for solving Classification and Regression tasks. RBF Neural Network is also implemented from scratch and utilized for a classification task on a simple generated data set. Moreover, Dense, RBF, Convolutional and Convolutional-Recurrent Neural Networks are utilized for Fault Identification on Case Western Bearing Health data set.
## Dataset
For PCA and LDA investigation a custom synthetic data set is used. Also for taching MLP for Regression and Classification, and RBF for Classification a custom synthetic data set is used.
For Fully Connected Autoencoder for dimensionality reduction a custom bearing data set containing 12 statistical features is used. Moreover, The Case Western Reserve University bearing  data set which contains signals of various bearing health states is utilized for training MLP, RBF, Convolutional and ConvLSTM networks. The signals are segmented by sliding a window with size 420 in a non-overlapping manner. The window size ischoosen based on the sampling frequency and the motor rotational speed. The data set contains 4 classes, namely Healthy, Inner Race, Ball and Outer Race.

This dataset is taken from the website https://engineering.case.edu/bearingdatacenter/download-data-file
## Berief list of implemented algorithms and neural networks

1.   PCA and LDA
2.   MLP for Classification and Regression tasks
3.   RBF for Classification task
4.   Fully Connected Autoencoder for dimensionality reduction
5.   MLP for CWRU bearing Fault Classification
6.   RBF for CWRU bearing Fault Classification
7.   CNN for CWRU bearing Fault Classification
8.   ConvLSTM for CWRU bearing Fault Classification
### PCA and LDA
Two experiments are carried out in this section. For the 1st experiment, a simple data set with gaussian distrbution is generated. Then the principal directions for transforming the data are obtained from PCA and are depicted on the generated distribution. The generated distribution and corresponding principal directions are depicted in the below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/1.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/1.png" align="center"></a>
</p>

For the 2nd example, a simple data set with 3 classes is generated. The generated data set is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/2.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/2.png" align="center"></a>
</p>

Then the principal components are obtained from PCA and are depicted on the scatter plot of data in 2 dimensional space. The result is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/3.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/3.png" align="center"></a>
</p>

Then the principal components are obtained from PCA and the data is projected to each of obtained directions. The result is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/4.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/4.png" align="center"></a>
</p>

Furthermore, using the same data set and LDA, the principal components for transforming the data are acquired. The result of transforming data without dimensionality reduction as well as transforming the data along each of principal directions (reducing one dimension) are depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/5.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/5.png" align="center"></a>
</p>

### MLP for Regression
The target function for regression is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/6.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/6.png" align="center"></a>
</p>

The error during training procedure is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/7.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/7.png" align="center"></a>
</p>

The predicted values by the regression network for samples belonging to train data set and test data sets are depicted in figure below.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/8.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/8.png" align="center"></a>
</p>

Apparentely, for large values of independent variable the predicted values are not accurate enough, so we use powers of independent variable x (x^2, x^3, ...) in order to achieve a better regression model. The error during training procedure is depicted in below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/9.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/9.png" align="center"></a>
</p>

The achieved result is depicted in below figure. Obviously the results are more accurate for large values of independent variable x.
<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/10.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/10.png" align="center"></a>
</p>

