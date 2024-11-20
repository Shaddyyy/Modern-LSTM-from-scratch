# Modern LSTM from scratch
Built using Pytorch, following the methodology of modular Programming

Written Tutorial on Original LSTM - https://arxiv.org/pdf/1909.09586

Stage 1 -> Single LSTM Cell 

NOTE:
1. cell state(aka CEC i.e. Constant Error Carousel) -> stores long-term memory
   
   -- it was there in Original LSTM
   
2. hidden state -> stores working memory

   -- not there in original LSTM (there in original RNN), but present in modern LSTM

3. In the Input Gate, the tanh NN is used to learn what to input and sigmoid NN is used to learn how much to consider out of it. (as the output of sigmoid is between 0 and 1)
   

Stage 2 -> Single LSTM Layer

NOTE:
1. Hidden states of each LSTM cell of the hidden layer are given to the cell one by one using for loop

Stage 3 -> Single LSTM Net

NOTE:
1. Initial hidden states and cell states are given to the Neural net and updated at every time step, to provide easily to the Net at the next time


IMPORTANT: Wondering aboout backward pass? Well the entire neural net is implemented in torch, with every single cell having nn.Parameters, so using autograd will easily work on it and will be much more efficient.

Also, will try to find time to implement state-of-the-art optimisers separately

THANKYOU!
