
# Finance Analytics software

## Framework and Setup

### IDE and Software Setup

* JetBrains Pycharm project
* Bitbucket (Project exists there, we make a clone on GitLab)

### Core Library Usage

* Binance (Fetching data on Cryptocurrencies)
* Thalib (For computing the average parameters and other indicators)


## Deliverables

* Alerts Chatbot on Telegram whenever market is predicted to fluctuate
* Excel (CSV) store log of all these changes for future analysis
* Algorithm (as Python Script) that can predict market fluctuations 
  
No addition User Interface (UI) has been demanded, the analysis script will serve directly to the Telegram chatbot.

## Algortihmic Ideas

### Basic Analysis Functions

* SMA: Simple Moving Averages
* EMA: Exponentially Moving Averages
* WMA: Weighted Moving Averages
* RSI: Relative Strength Index
* HMA: Hull Moving Averages

### Modes of Analysis

We shall analyze the crossover in results of the above indicators with different parameters.
    eg. EMA-8 calculates exponentially moving averages for the past 8 records, EMA-20 over past 20 records.
We can use this to improve on the rules. The primary bulk of our work shall go into the **analysis of combinations of these parameters**.

<!-- Moving Average Convergence Divergence (MACD) is an example of a combination parameter (EMA-26 - EMA-12), which we can use as a starting point. (Note the key takeaways in the article here: https://www.investopedia.com/terms/m/macd.asp) -->

### Long Term Targets

Using Artificial Intelligence to enhance our predictions of market fluctuations from market indicators shall be done once the rule based phase is complete. (This will require us to grab more data from the past status of the market, therefore some modifications to the scraper.)
