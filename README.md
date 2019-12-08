Recurrent Neural Networks(RNN) are the state of the art algorithm for sequential data. This is because they can remember their previous inputs, through an internal memory.

In this project I have developed a simple LSTM network to learn sequences of characters from Alice in Wonderland storybook. 
Then using this model I can generate new sequences of characters given input a random sentence from the textbook.

I have build 2 different techniques to build the LSTM model for text generation.
We know that a unique property of LSTM is that the training data contains 3 parameters or we can say that training data should be a 3 dimension vector i.e batch-size,timesteps and features

In the 1st method I will be initializing a 3 dimensional vector (basically a zero matrix of 3 dimension) as our training vector . Let the sequence length be 20(means training on 20 characters and predicting the 21st character) , so the batch size is (total characters/20), timesteps is 20 and features is (unique elements set after hot encoding them)

In the 2nd method initially the training data will be a 1d array(comparitively easy) and after the storing the required data into it, using the reshape function I will be converting it into a 3 dimensional vector. Let the sequence length be 20(means training on 20 characters and predicting the 21st character) , so the batch size is (total characters/20), timesteps is 20 and feature is 1

I have only made a simple text generator, so I just need to set the target by shifting the corresponding input sequence by one character. Obviously my target sequence will have the same length with the input sequence.
