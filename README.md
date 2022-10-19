# "Insider Training": An Exploration of Insider Trades
In this repository, we try to see if we can mine insider data and use machine learning to generate investment insights, in lieu of having technical knowledge of investment strategies, the Greeks, etc.

This project is neither an investment pitch, nor does it constitute financial advice. It simply represents my curious, exploratory approach to data-driven knowledge generation!

### Where can the data be found?
Insider trade filings are published online by the SEC, and they can be found using the EDGAR API. However, it is much easier to pull data from sites that gather the filing data into tabular form such as https://www.benzinga.com/ .

Historic ticker data (e.g. daily opening, low, high, close, volume) was obtained with the Yahoo Finance API via the "yfinance" Python package.

### What machine learning model is used?
So far, I have explored using two model types. One is XGBoost, which is a gradient-boosting decision tree model, and the other is a neural network with one dense hidden layer and a dropout layer, implemented with the Keras Sequential API.

### What evaluation metrics are used?
You can see my commentary on model performance in the Jupyter notebook files "decision_tree" and "neural_net". Also, in order to evaluate the models in a way that is more demonstrative, I develop a simple trading strategy in "strateg_simulation" and benchmark it against the performance of the S&P500 ETF fund ("SPY") across the given time period.
