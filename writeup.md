# **Traffic Sign Recognition** 

### **Build a Traffic Sign Recognition Project**

Here is process for the traffic sign recognition:
* Load the data set (see below for links to the project data set)
* Explore, summarize and visualize the data set
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report

---
### Data Set Summary & Exploration

I used the pandas library to calculate summary statistics of the traffic
signs data set:

* The size of training set is ?

* The size of the validation set is ?

* The size of test set is ?

* The shape of a traffic sign image is ?

* The number of unique classes/labels in the data set is ?

  ```n_train = y_train.size

  n_validation = y_valid.size
n_test = y_test.size
  image_shape = X_train[0].size
n_classes = np.unique(train['labels']).size
  
print("Number of training examples =", n_train)
  print("Number of testing examples =", n_test)
print("Image data shape =", image_shape)
  print("Number of classes =", n_classes)```
  ```




#### Include an exploratory visualization of the dataset.

This histogram shows the density of x_train. The histogram shows index = 2 has most probability density

![histogram](./images/hist.png)

```
max index:  [2]
max value:  0.0591355252408731
```

And the below image shows the example image of training set

![example](./images/example.png)



### Model Architecture

My final model consisted of the following layers:



![Lenet](./images/lenet.png)



#### Type of optimizer, the batch size, number of epochs and any hyperparameters such as learning rate.

Here are my hyperparameters

1. EPOCHS: 40
2. BATCHES: 128
3. Optimizer: AdamOptimizer
4. Rate: 0.001
5. Loss: cross entropy

#### Validation set accuracy

My final validation set accuracy: 0.955


#### Test a Model on New Images

Here are five German traffic signs that I found on the web:

![construction](./test data/construction.png)![merge](./test data/merge.png)
![rightturn](./test data/rightturn.png)![speed_limit_20](./test data/speed_limit_20.png)
![stopsign](./test data/stopsign.png)



#### Prediction result

Here are the results of the prediction:

| Image			        |     Prediction	        					|
|:---------------------:|:---------------------------------------------:|
| Construction | Construction |
| rightturn | rightturn 	|
| stopsign	| stopsign	|
| merge	   | merge					|
| speed_limit_20	| speed_limit_20 |




```
File: construction.png
Ground truth:25
Prediction:25
Top5 predicted labels:[25 20 12  3 13]
Top5 probabilities:[1.0000000e+00 2.8951269e-25 2.1459419e-26 1.6217206e-27 6.3754525e-30]


File: rightturn.png
Ground truth:33
Prediction:33
Top5 predicted labels:[33 11 13  3 39]
Top5 probabilities:[1.0000000e+00 9.1046104e-10 7.3238854e-10 2.7891700e-10 2.0124501e-10]


File: speed_limit_20.png
Ground truth:0
Prediction:0
Top5 predicted labels:[ 0  4  1  8 10]
Top5 probabilities:[1.0000000e+00 3.7319120e-16 3.2458792e-17 1.3770356e-26 1.6570948e-30]


File: stopsign.png
Ground truth:14
Prediction:14
Top5 predicted labels:[14 17  1 33 13]
Top5 probabilities:[1.0000000e+00 3.8114595e-16 6.5742879e-17 2.4698998e-17 1.5976099e-17]


File: merge.png
Ground truth:24
Prediction:24
Top5 predicted labels:[24 26 27 11 28]
Top5 probabilities:[9.9990296e-01 8.8019231e-05 5.2436194e-06 2.0037028e-06 1.3471815e-06]


Total accuracy: 1.0
```






#### 


