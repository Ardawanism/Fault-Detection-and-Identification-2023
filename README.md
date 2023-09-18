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
Two experiments are carried out in this section. For the 1st experiment, a simple data set with gaussian distrbution is generated. Then the principal directions for transforming the data are obtained and depicted on the generated distribution. The generated distribution and corresponding principal directions are depicted in the below figure.

<p align="center">
<a href="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/1.png"><img src="https://github.com/Ardawanism/Fault-Detection-and-Identification-2023/blob/master/Asset/Pix/1.png" align="center"></a>
</p>

