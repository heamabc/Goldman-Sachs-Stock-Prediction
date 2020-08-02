# Goldman-Sachs-Stock-Prediction

* [Data](#Data)
    * [Related Stocks Price](#Related-Stocks-Price)
    * [Fixed Income Security](#Fixed-Income-Security)
    * [Global and Local Economy](#Global-and-Local-Economy)
    * [Technical Indicator of GS](#Technical-Indicator-of-GS)
    * [ARIMA of GS](#ARIMA-of-GS)
    * [Fourier Transform of GS](#Fourier-Transform-of-GS)
    * [Twitter Sentiment of Financial Market](#Twitter-Sentiment-of-Financial-Market)

## Data
As our model need to train and predict daily, we will use prices of different financial securities as the features of our model. On the other hand, we generated some feature to capture the trends and behaviour of the stock price and performed some natural language processing to obtain investors' opnion towards the market.

### Related Stocks Price
We believe that stocks related to Goldman Sachs will affect the price movement of GS. Therefore, we include some of the stocks that is related to Goldman Sachs. We consider which stocks to be included based on 3 different criterion. 
- 1. Economical Analysis. We examined if the stock is related Goldman Sachs based on some economical reasoning, for example, are they belong to the same industry, do they have to same customer maket. 
- 2. Statistical Analysis. We calculated the correlation of the stock price and stock return of the related stocks.
- 3. Bloomberg Indicator. Bloomberg Intelligence can tell us some of the major competitors of Goldman Sachs. We included those competitors in this category.

### Fixed Income Security
We believe that the fixed income market affect the stock market in general significantly. Also, as an investment bank, the business will be greatly affected by any fluctuation in interest rate. Therefore, we include several fixed income securities such as LIBOR, Fed Funds, and some other fixed income ETF.

### Global and Local Economy
The overal performance of the economy is a great factor affecting the stock market. Therefore, we include some composite indeces and ETF to reflect the economy. Eg, S&P500, HSI, FTSE, etc.

### Technical Indicator of GS
Base on the theory of techinical analysis, the technical indicators can tell us some of the short term and long term trends of the stock price. We include technical indicator in order to capture those trends.

### ARIMA of GS
In statistics, ARIMA can predict the stock price reasonably accurately. After some validation of the model, ARIMA model of (2,1,1) is the best model.

### Fourier Transform of GS
Like technical indicator, fourier transform can help us capture some short term and long tern trends and behavriour. We include several fourier transforms of GS in our model as features.

### Twitter Sentiment of Financial Market
The stock market is also greatly affected by the investors' opinion towards the market. We captured all the tweets from the twitter account @market (https://twitter.com/markets) and used a pretrained natural language processing package BERT to analyse the sentiment of the tweets.

## Model
### LSTM
We used on layer of LSTM. Performed Xavier initialization and triangular learning rate.
https://colab.research.google.com/drive/1lZEOXqNrxw_Vj2eZSkbyRecn6pSA0Ilk?usp=sharing


## Results
![train_test](https://github.com/heamabc/Goldman-Sachs-Stock-Prediction/blob/master/Illustration1.png)
![test](https://github.com/heamabc/Goldman-Sachs-Stock-Prediction/blob/master/Illustration2.png)
