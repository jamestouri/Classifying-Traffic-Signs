## Project: Build a Traffic Sign Recognition Program (Write Up Below)
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---
In this project, you will use what you've learned about deep neural networks and convolutional neural networks to classify traffic signs. You will train and validate a model so it can classify traffic sign images using the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset). After the model is trained, you will then try out your model on images of German traffic signs that you find on the web.

We have included an Ipython notebook that contains further instructions 
and starter code. Be sure to download the [Ipython notebook](https://github.com/udacity/CarND-Traffic-Sign-Classifier-Project/blob/master/Traffic_Sign_Classifier.ipynb). 

We also want you to create a detailed writeup of the project. Check out the [writeup template](https://github.com/udacity/CarND-Traffic-Sign-Classifier-Project/blob/master/writeup_template.md) for this project and use it as a starting point for creating your own writeup. The writeup can be either a markdown file or a pdf document.

To meet specifications, the project will require submitting three files: 
* the Ipython notebook with the code
* the code exported as an html file
* a writeup report either as a markdown or pdf file 

# Summary of Project

#### 1. The first thing to do was preprocess the images.  Other than the suggestion of normalizing it with formula (X_train - 128) / 128, I grayscaled it into 1 layer

#### 2. From there I built out my LaNet Architecture to see how it works.  Training scores and Validation scores were just all right. I didn't change any of the Training Data, Validation Data, or Test Data sizes

#### 3. I wasn't really going anywhere with just the preprocessing and the CNN, so I did research and came across a bunch of tensorflow methods to help with augmenting the data. From there as you can see I randomized the data according to the number given while training the data set. 
#### After setting the EPOCHS to 40 and Batch Size a little down to 120, I started seeing better results.  I also changed the learning rate from .00001 to .0001.


#### 4. After the longest time of getting the validation accuracy to a solid score, I tested the data and got a 93.5% 

#### Final scores: Training Accuracy (N/A) Validation Accuracy (93.2%) Testing Accuracy (93.5%)

### Layer Architecture:

Layer | Description
| ------------- |:-------------:|
|Input | 32 32 1|
|Convolutional 3x3 | Output 30x30x10|
|Relu |         |
|Convolutional 3x3 | Output 28x28x100|
|Relu |           |
|Max Pool | Output 14x14x100|
|Convolutional 5x5 | Output 10x10x150|
|Relu |         |
|Max Pool | Output 5x5x150|
|Convolutional 2x2 | Output 4x4x250|
|Relu |         |
|Max Pool | Output 2x2x250|
|Relu |         |
|Convolutional 2x2 | Output 1x1x1000|
|Relu|        |
|Fully Connected | Output 500|
|Relu |       |
|Fully Connected | Output 300|
|Relu|      |
|Fully Connected | Output 120|
|Relu |       |
|Fully Connected | Output 84|
|Relu |     |
|Full Connected | Output 43|
|Softmax_Cross_Entropy |    |


#### 5. I got a 100% confidence in each of the choices for the photos.  This is something I realized I needed to work on:  Data visualizing, took a lot of blog posts and stack overflow to help me even on the most blantaly obvious answers.

### Overall, great experience 
