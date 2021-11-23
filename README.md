# unit_14_homework

## Past prices or Fear and greed - which is a better indicator?

We constructed a neural network to predict a future price of bitcoin.
The particulars are:

Model: LSTM RNN <br />
Features to compare: Previous 10 day prices vs Previous 10 day Crypto Fear and Greed Index (FNG) <br />
Target: Close price of bitcoin <br />
Metrics: Mean squared error (MSE) <br />
Parameters|No 
---|:---:
No of layers|3
No of neurons|30
No of epochs|80
Batch size|8

## Previous prices

MSE for 10 days = 0.00473

MSE for other windows
Days|MSE
---|:---:
9 days|0.00444
8 days|0.00654
7 days|0.00516
6 days|0.00938
5 days|0.00926
4 days|0.00570
3 days|0.00574
2 days|0.00415
1 day|0.00214

## FNG

MSE for 10 days = 0.1179

MSE for other windows
Days|MSE
---|:---:
9 days|0.1225
8 days|0.1203
7 days|0.1198
6 days|0.1199
5 days|0.1250
4 days|0.1261
3 days|0.1330
2 days|0.1282
1 day|0.1227

## Conclusion
The model with previous prices as a feature performed far better than the one with FNG.  Since this is a regression model, it can be easily understood that
previous prices make a better model. But if we buid a binary calssification model (i.e. price will go up or down), a model with FNG may deliver better results.
In terms of experiment with different windows, for the previous price model, as you can imagine, a very short window such as two days and one day performed very well.
Other than that, the 10 day window perfomed the best in my model. For FNG the 10 day window model delivered the best result.



