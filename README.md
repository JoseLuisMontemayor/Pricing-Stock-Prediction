# Pricing-Stock-Prediction

### Introduction

The stock pricing prediction aims to determine the future movement of an asset value on play on the financial market. It is extremely challenging since it depends on several micro and macro factors, such as politics, economic conditions, unexpected events and as well the financial performance of the company/asset. It is known that there are several types of analysis to evaluate the actual and future value of an asset, starting with the technical and fundamental. Alternatives are in place, it is important the exploration of options to rely on when making an analysis for an investment oportunity. In this project the Long Short Term Memory model takes place. 

The platform of Yahoo Finance was employed to take action. This site is one of the largest business and financial news site in the world, with access to databases, insights and content about corporations and financial assets. It was wanted to use a large database of the project, with the most accurate information of the asset analyzed and also which included fundamental information to take into account for the project. From this website containing infinite quantity of information, the database for the stock price of "Apple Inc." was retrieved. 

Link to PPT: https://docs.google.com/presentation/d/1ZuNw5GRWOOs0pZLTcXs5W2V-zNxsyXQ9cqAgHOuuDhM/edit?usp=sharing

### Purpose of the Project

The purpose of this project is to analyze if the Long Short Term Memory model can be applied and used effectively to predict the future price of the Apple stock. With this information we could also predict if an investment on Apple would be a good alternative for long term investors. For now the opportunity of investment will be based on numerical values and it´s trend. 

### Database

As mentioned, the platform of Yahoo Finance was used to retrieve the data for the stock of Apple Inc. The information was redeemed from the 1st of January 2012 to the 17th of December of 2019. The database was fulfilled by the daily price stocks of the company throughout almost 8 years. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/1.%20Dates_Stock.PNG)

On the next image, the behavoir of the stock throughout the last years it can be visualized:

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/2.%20Stock_History.PNG)

### Code

It is important to mention, is that it was established that the amount of the data to train the model is about 80%.

To create the data scaled training it was divided into the x_train and the y_train, which x_train is our independent training variable and y_train the dependent. On the x_train variable, the last 60 values were appended from position 0 to position 59, while the y_train contains the 61st value which is at position 60. On the code below it can be seen how it goes.

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/3.%20Split%20x-y-train.PNG)

As for the model choice, as mentioned before, the Long Short Term Memory model was applied. This is one type of time series analysis, which has a significance in financial analytic and forecasting any type of data in any field. It is a type of recurrent neural network capable of learning order dependence in sequence prediction problems, this means that the outputs are used along with the next elements as the inputs for the next step of information processing. The advantage of the LSTM model is that it adds long-term memory in an even more performant way, since it allows even more parameters to be taken into account it makes the most of the recurrent network, making it more powerful and accurate in a forecasts. The disadvantages are that the model may take longer to train and requiere more memory, as the same that LSTMs are sensitive to different random weight initializations.

As mentioned, the Long Short Term Memory model was in use, utilizing for the architecture 2 LSTM layers with 50 neurons and 2 Dense layers with 25 and 1 neurons. This with the purpose of the flow of the model. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/4.%20LSTM%20Model.PNG)

For the training of the model, the x and y train variables were taken into account, as well as a batch size of 1 (total number of training examples in a single batch) and 1 epoch (The number of iterations when an entire dataset passes through a neuro network). For the testing data, the last 60 values are appended to the x_test to train the model. The y_test are all of the values that are wanted the model to predict, the actual test values. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/5.%20Train_Test%20Model.PNG)

To evaluate the model, the measure of the Root Mean Squared Error (RMSE) was used to determine how accurate the model predicts the response. The RMSE model is the standard deviation of the residuals, it tells you how concentrated the data is around the line of best fit. The lower value of this number indicates a better fit. We can see below that the result for the model is 1.527, which can be interpreted as a good result for the established metrics. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/6.%20Root%20Mean%20Squared%20Error.PNG)

After all, now we can see the viualization of tha actual model. The blue line defines the data on which the information was trained on, the red line indicates the actual closing stock price for Apple for the rest of the days, and the yellow line represents the projections of the model. It can be seen that the validation and predicted data are actually similar, and have the same tendency regarding movements regarding the days viewed. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/7.%20Visualization%20Model.PNG)

As part of the activity, a test was ran to verify the predicted and actual data of the price stock of the 18th of December in 2019. On the image below we can see that the predicted price reaches $64.60, and the actual price of that day is $69.93, a difference of less than $5.50 or less than 8%. We can see that the model is close but still with an opportunity margin to take into account. 

![](https://github.com/JoseLuisMontemayor/Pricing-Stock-Prediction/blob/main/Resources/8.%20Run%20Test.PNG)

### Conclusion

It can be concluded based on the results of the model that it may be effective if utilized for a long term investment. We saw at the end that the results had a margin of opportunity, but it has to be taken into account that it ran over the same tendency that it showed in the image comparing through the actual and predicted months. Also, (not financial advice) Apple stock may be a good opportunity for a long term investment, since it can be seen that throughout the years it has been growing continuously. The model should also be applied to other stocks in the industry to analyze the reliance and the level of error that it may contain. Improvements based on trial and error can benefit significantly the predictions.  








