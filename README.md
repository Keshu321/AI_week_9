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

https://github.com/Keshu321/AI_week_9-16/blob/main/Week12_lab%20_group%20F.ipynb

## content 

- Keeping Gradients Healthy

- Introduction to LSTM

LSTM is an example of a gated unit. It consists of logistic sigmoid
functions known as gates in addition to traditional activation functions.
 ![image](https://user-images.githubusercontent.com/92859942/205247773-bfbc0a5e-2aab-4e8d-9734-f16c5c2a55af.png)

- Creating a network of LSTM cells

![image](https://user-images.githubusercontent.com/92859942/205248182-4134e1b9-fc3e-42dc-8c5e-cc43a37f9bc2.png)


Figure above shows how multiple LSTM cells are connected into a
recurrent network layer. This is just like a regular RNN, but each neuron
has been replaced by the more complex LSTM cell. This results in a
network with two sets of state. We have the internal state (c) inside of each
LSTM cell, but we also have the state(h) in the global recurrent
connections just as in an RNN that is based on simple neurons.
The figure makes it obvious that an LSTM based RNN has four times as
many parameters (weights) to train as a regular RNN. In addition to the
input activation neurons, there are also three gate-neurons that each
receives the same number of inputs as the input neuron.

- Alternative view of LSTM
LSTM is often thought about in terms of entire layers rather than individual
units. In some texts, a cell refers to an entire layer of units rather than to a
single unit

![image](https://user-images.githubusercontent.com/92859942/205248431-bc4f4c69-2dff-424c-a4ab-6c66de850a3d.png)


Figure above shows an LSTM layer unrolled in time for three timesteps.
For each timestep, the layer receives c and h from the previous timestep
and x from the current timestep and outputs new values for c and h.
The middle part of the figure shows the internals of the LSTM layer.
Each rectangle represents multiple neurons (the same number as the
number of LSTM units in the layer), where each neuron receives a
vector of inputs and produces a single output. The ones marked with the
Greek letter sigma ( ) represent the gates, and the ones marked tanh
represent the input and output activation functions. The curved line from
x
(t)
represents a concatenation; that is, we form a wider vector, which
contains the elements of both h
(t−1) and x
(t)
. All other operations
(represented by circles/oval) represent multiple instances (the same
number as the number of LSTM units in the layer) of the operation,
where each of these instances receives a single input value (as opposed
to a vector for the rectangles) and produces a single output value.

# Week 13 

link : 


## content 

- Encoding text

We need to encode text properly to use text as input to our RNN.
We use one-hot encoding just as we did for categories in our image
classification problems.
 One-hot encoding works fine for characters, given that a typical
alphabet contains only tens of characters. as a side note, one-hot
encoding words is less efficient: It results in much wider vectors
because the width of the input vector is the same as the total number of
symbols to encode. A typical language contains tens or hundreds of
thousands of words
![image](https://user-images.githubusercontent.com/92859942/205249228-17a111ac-e61b-4034-bffe-f1950c9d50cf.png)

- Longer-term prediction and autoregressive models
- 
Long-term prediction can be done by repeatedly feeding the predicted
output back as inputs to the model. This works only if the network
predicts all the variables needed as input. It is known as an
autoregressive model.

When the output is a softmax function, we typically do not feed the exact
output back as input, but instead we identify the most probable element
and use the one-hot encoded version of that element as input to the
network.

- Beam Search
Beam search enables us to create multiple alternative predictions
when feeding back output as inputs to a network.

- Bidirectional RNNS

Bidirectional RNNs predict an element from both the past and the future.

- Different combinations of input and output sequences
Input/output combinations for RNN unrolled in time. gray
represents input, blue represents the network, and green represents outputs.

![image](https://user-images.githubusercontent.com/92859942/205249694-0eb2a6ce-6949-410f-9eeb-08d81c163948.png)


# Week 14 


