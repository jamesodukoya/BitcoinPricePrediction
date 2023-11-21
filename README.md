# BitcoinPricePrediction
The aim of this project is to predict the price of the Bitcoin cryptocurrency (BTC). The prediction model relies on data from the daily edits of the English Bitcoin Wikipedia page and up-to-date opening and closing dates of the currency from Yahoo Finance.

## Steps Involved
1. I aggregated comments from the Wikipedia page edits using the mwclient package
2. I then conducted a sentiment analysis of all comments for each day using the Transformers package and computed the average score for each day (assigning 0 to a negative score(negative comment) and 1 to a positive score)
   - Code for sentiment analysis: [Bitcoin_Sentiment_Analysis.ipynb](https://github.com/jamesodukoya/BitcoinPricePrediction/blob/main/Bitcoin_Sentiment_Analysis.ipynb)
3. I imported "BTC-USD" opening and closing rates per day using the YFinance package.
4. After cleaning up the data, I merged the data from both the YFinance and Wikipedia page edits.
5. I then trained a baseline model using a Scikit learn Random Forest classifier and used a backtesting function to evaluate the prediction accuracy.
   - Code for prediction model: [Bitcoin_Price_Prediction.ipynb](https://github.com/jamesodukoya/BitcoinPricePrediction/blob/main/Bitcoin_Price_Prediction.ipynb)
7. Then I used the XGBoost classifier and additional predictors to further improve the accuracy of the model.
