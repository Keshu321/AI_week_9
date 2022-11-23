# week 9 content 

• Logistic unit for binary classification

• Softmax unit for multiclass classification

• Linear unit for regression

• The Boston Housing dataset

• Predicting house prices with a DNN

• Improving generalization with regularization

• Experiment: Deeper and regularized models for house
price prediction

• Concluding remarks on output units and regression
problems

https://github.com/Keshu321/AI_week_9/blob/main/74874_9.1_Untitled5.ipynb

https://github.com/Keshu321/AI_week_9/blob/main/94874_week_9.2_Untitled6.ipynb

## week 10 content 

• VGGNet

• GoogLeNet and ResNet

• Transfer Learning

• Data Augmentation as a Regularization Technique

• Mistakes made by CNNs

• Reducing parameters with Depthwise Separable Convolution

• Striking the right network design balance with EfficientNet

https://github.com/Keshu321/AI_week_9/blob/main/Week_10_lab_session_dog_image.ipynb

## week 11 content 

• ***Limitations of Feedforward Networks***

The first idea for solving the sales forecasting problem is to just use a fully
connected feedforward network1 with a linear output unit.We standardize this
month’s book sales and, optionally, sales of other goods, then provide these
numerical values to the network and hope that the network can use that data to
learn to output the book demand for next month

• ***Recurrent Neural Networks***

A simple form of RNN can be created by connecting the outputs from a fully
connected layer to the inputs of that same layer. The
figure shows a three-value input vector connected to a fully connected layer of
four neurons. The bias values are omitted from the figure.Along with the three
inputs (and bias input), each neuron has four additional inputs. These inputs
receive the output values from the four neurons but are delayed by one
timestep.


• Mathematical Representation of a Recurrent layer

With a tanh activation function this can be written as follows:
y = tanh(Wx)

• ***Combining layers into an RNN***

![image](https://user-images.githubusercontent.com/92859942/200756273-23a25f26-412d-46ca-862b-4344ff66cb97.png)


• ***Alternative veiw of RNN and Unrolling in Time***

![image](https://user-images.githubusercontent.com/92859942/200756389-cb0027a6-ea7f-446f-bb06-386166798eab.png)


• ***Backpropagation Through Time***

Once the network is unrolled, we can backpropagate the error in the
same way as we do for a feedforward network. However, it might be
somewhat computationally expensive in cases with long input sequences.

• Programming Example: Forecasting book sales

![image](https://user-images.githubusercontent.com/92859942/200756155-7e2dc181-e34a-4bce-bcd9-0cd9164a8aae.png)


https://github.com/Keshu321/AI_week_9/blob/main/week11_Lab(1-4).ipynb

# week 12 




