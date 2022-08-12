RNN (Recurrent Neural Networks) has short term memory- the neurons in RNN are connected to themselves over time., use for time series analysis

Three Types of RNNs:  

* one to many, e.g. input- image and output- the description of the image.
* many to one, e.g. input- a review and output- the sentiment of the review.
* many to many, translating sentences from one language to another.

![1_go8PHsPNbbV6qRiwpUQ5BQ](https://user-images.githubusercontent.com/85345738/138188641-fd0e6816-ef8e-46f1-986e-cca36b26755a.png)


**vanishing gradient problem**
------------------------------

*Recurring weight, w_rec-it is the weight that connects the same neuron over time which are randomly initialized at beggining. While back propagating after calculating the error to update weights the w_rec is multiplied again and again to the initial weights which was small.* 

*So continuous multiplication makes the gradient less in the initial time and the lower gradient make the network difficult to update the weight and longer to find final result so the initial layers of the network is not properly trained and those are used as input device for the layers.*

To sum up, if wrec is small, we will have vanishing gradient problem, and if wrec is large we will have exploding gradient problem.

> vanishing gradient problem solved by LTSM (Long Short-Term Memory) RNN model, which is used to predict the future stock price in this project.
