# Stock Sentiment Analysis

This project performs sentiment analysis on news headlines related to publicly traded companies using the NewsAPI and TextBlob. It classifies news as Positive, Negative, or Neutral for each stock symbol and provides an option to upload the results to Azure Blob Storage.

## Features

- Fetches real-time news articles for a list of stock symbols  
- Analyzes sentiment using TextBlob  
- Provides sentiment summary per stock symbol  
- Exports results to CSV  
- Uploads the analysis file to Azure Blob Storage  

## Tech Stack

- Python  
- Pandas  
- TextBlob  
- NewsAPI  
- Azure Blob Storage SDK

## How It Works

1. Load API key from a local file  
2. Fetch latest news for selected stock symbols  
3. Perform sentiment analysis on each article’s title and description  
4. Export results to a CSV file  
5. Upload the file to an Azure Blob Storage container  

## Files

- `stock_sentiment_analysis.ipynb`: Main notebook containing all code  
- `apikey`: Plain text file containing your NewsAPI key (not tracked in GitHub for security)  
- `sentiment_analysis_results.csv`: Output file containing sentiment-labeled news data

## Example Stock Symbols

MSFT, AAPL, NVDA, AMZN, GOOG, GOOGL, META, BRK/A, BRK/B, LLY


## Azure Integration

Make sure to update the following values in the script for Azure Blob upload:
- `container_name`
- `blob_name`
- `connection_string` (do not expose your keys in public repositories)

## Note

Your NewsAPI key and Azure Blob Storage credentials should be stored securely. Avoid uploading `.apikey` or `.env` files to GitHub.

## To Do

- Improve sentiment accuracy using advanced NLP models  
- Add visualizations for sentiment distribution  
- Support historical sentiment tracking  
