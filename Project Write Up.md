# Traffic Sign Recognition

## Full Summary


### Build a Traffic Sign Recognition Project

The goals / steps of this project are the following:

Load the data set (see below for links to the project data set)
Explore, summarize and visualize the data set
Design, train and test a model architecture
Use the model to make predictions on new images
Analyze the softmax probabilities of the new images



### TLDR This started out as a very fun project then started to get frustrating because it was constantly tweaking out the data, which is normal except the waiting game. 

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
