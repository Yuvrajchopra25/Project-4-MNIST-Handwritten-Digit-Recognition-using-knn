# Project-4-MNIST-Handwritten-Digit-Recognition-using-knn
## Introduction:
This is the famous MNIST Machine Learning project in which we have to predict handwritten digits. The dataset used in this project is taken from kaggle.

## Digit Recognition System
Digit recognition system is the working of a machine to train itself or recognizing the digits from different sources like emails, bank cheque, papers, images, etc. and in different real-world scenarios for online handwriting recognition on computer tablets or system, recognize number plates of vehicles, processing bank cheque amounts, numeric entries in forms filled up by hand.

## Problem Statement:
This is the famous MNIST Machine Learning project in which we have to predict handwritten digits. The dataset used in this project is taken from kaggle.

## Requirements:
- Jupyter Notebook

## MNIST Dataset
Samples provided from MNIST (Modified National Institute of Standards and Technology) dataset includes handwritten digits total of 70,000 images consisting of 60,000 examples in training set and 10,000 examples in testing set, both with labeled images from 10 digits (0 to 9). This is a small segment form the wide set from NIST where size was normalized to fit a 2020 pixel box and not altering the aspect ratio. Handwritten digits are images in the form of 28 * 28 gray scale intensities of images representing an image along with the first column to be a label (0 to 9) for every image. The same has opted for the case of the testing set as 10,000 images with a label of 0 to 9.
![](https://corochann.com/wp-content/uploads/2017/02/mnist_plot-800x600.png)

## Importing the Modules:
- Pandas
- Numpy
- Matplotlib

### KNeighborsClassifier (KNN):
- Simplest Machine learning Algorithm you will find in Machine Learning
- Brute Force Approach is used in it. (Hence Act as a **Baseline** , if you use any other algo then that algo must have accuracy better than KNN)
- Complexity O( M*N + (M + klogM) + k ) per Query => if dataset is Large, this is gonna take much time to execute, where M is number of samples and N is number of features in each sample.


The k-nearest neighbors algorithm (k-NN) is a `non-parametric method` or `lazy learners` used for both `classification and regression.` In both cases, the input consists of the k closest training examples in the feature space.
The output depends on whether k-NN is used for classification or regression:

`In k-NN classification, the output is a class membership.`
An object is classified by a vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). 

If k = 1, then the object is simply assigned to the class of that single nearest neighbor.

`In k-NN regression, the output is the property value for the object.`
This value is the average of the values of its k nearest neighbors.

![](https://images.squarespace-cdn.com/content/v1/55ff6aece4b0ad2d251b3fee/1465017787823-KXFG6O0MU5NWYF8EI6UU/ke17ZwdGBToddI8pDm48kICIavOU0GBCWw19s1p5lSVZw-zPPgdn4jUwVcJE1ZvWULTKcsloFGhpbD8VGAmRSUJFbgE-7XRK3dMEBRBhUpycqPLetyMM_eWnzi1H9kYzvMtuY8jA9E1WuBOqLarM1WXLSloz6LILkqH1WHTAqb8/image-asset.png)

### ALGO
<ol>
    <li>Find distance of query point from all other point in dataset and store in as a list of tuple (distance,value OR label).</li>
    <li>Sort the list based on distance.</li>
    <li>Take first k-smallest or nearest elements from the sorted list.</li>
    <li>If problem is classification:-
        <ol>
            <li>Take the majority Vote Label and assigned to our Query Point.</li>
        </ol>
    </li>
    <li>If problem is Regression:-
        <ol>
            <li>Take the mean of values and assigned to our Query Point.</li>
        </ol>
    </li>
</ol>

## Score:
For this model, the accuracy on the test set is **0.98**, which means the model made the right prediction for **98%** of the handwritten digits in the given dataset. We can expect the model to be correct **98%** of the time for predicting the handwritten digits.

## Summary:
The MNIST handwritten digit recognition (and our implementation) is a perfect example to illustrate how a machine learning problem should be approached and how useful the outcome could be for computer vision.
