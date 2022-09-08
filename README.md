# Pricing-Stock-Prediction

### Introduction

The stock pricing prediction aims to determine the future movement of an asset value on play on the financial market. It is extremely challenging since it depends on several micro and macro factors, such as politics, economic conditions, unexpected events and as well the financial performance of the company/asset. It is known that there are several types of analysis to evaluate the actual and future value of an asset, starting with the technical and fundamental. Alternatives are in place, it is important the exploration of options to rely on when making an analysis for an investment oportunity. In this project the Long Short Term Memory model takes place. 

The platform of Yahoo Finance was employed to take action. This site is one of the largest business and financial news site in the world, with access to databases, insights and content about corporations and financial assets. It was wanted to use a large database of the project, with the most accurate information of the asset analyzed and also which included fundamental information to take into account for the project. From this website containing infinite quantity of information, the database for the stock price of "Apple Inc." was retrieved. 

### Purpose of the Project

The purpose of this project is to analyze if the Long Short Term Memory model can be applied and used effectively to predict the future price of the Apple stock. With this information we could also predict if an investment on Apple would be a good alternative for long term investors. For now the opportunity of investment will be based on numerical values and it´s trend. 

### Database

As mentioned, the platform of Yahoo Finance was used to retrieve the data for the stock of Apple Inc. The information was redeemed from the 1st of January 2012 to the 17th of December of 2019. The database was fulfilled by the daily price stocks of the company throughout almost 8 years. 

* Insert Date_Stock*

On the next image, the behavoir of the stock throughout the last years it can be visualized:

* Insert Stock History*

### Code

It is important to mention, is that it was established that the amount of the data to train the model is about 80%.

To create the data scaled training it was divided into the x_train and the y_train, which x_train is our independent training variable and y_train the dependent. On the x_train variable, the last 60 values were appended from position 0 to position 59, while the y_train contains the 61st value which is at position 60. On the code below it can be seen how it goes.

* Insert the split x-y-train*

As for the model choice, as mentioned before, the Long Short Term Memory model was applied. This is one type of time series analysis, which has a significance in financial analytic and forecasting any type of data in any field. It is a type of recurrent neural network capable of learning order dependence in sequence prediction problems, this means that the outputs are used along with the next elements as the inputs for the next step of information processing. 

It was considered an adequate choice to predict the future price of Apple.  






