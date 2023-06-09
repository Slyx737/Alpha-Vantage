# Alpha Vantage Financial Data Interface

This repository contains the OpenAPI specification and the manifest for the Alpha Vantage Financial Data Interface. This interface allows users to fetch financial data from Alpha Vantage directly through a conversational interface.

## Disclaimer
This is an unofficial open-source project and is neither endorsed nor owned by Alpha Vantage Inc. This interface is developed independently and Alpha Vantage Inc. bears no responsibility for it.

## Files

- `OpenAPI_Plugin_Specification.json`: Contains the OpenAPI specification that describes the Alpha Vantage API's endpoints and responses.
  
- `ai-interface.json`: Describes how the AI should interact with the Alpha Vantage Interface.

- `ai-interface.json`: This is the main manifest file that includes the HTTP service authentication necessary for the interface to interact with the Alpha Vantage API.
  
- `Unused_Manifest_Files/Interface_Manifest_NoAuth.json`: An alternative version of the manifest file, which does not include authentication. It is not currently in use for this project, but has been preserved for potential use in other projects where authentication may not be required.

## Setting Up API Key
Before you can use the Alpha Vantage Plugin, you will need to obtain an API key from Alpha Vantage.

### Step 1: Get Your API Key

1. Visit the [Alpha Vantage website](https://www.alphavantage.co).
   
2. Follow the instructions on the website to sign up for a [free API key](https://www.alphavantage.co/support/#api-key).

### Step 2: Configure the Plugin
After you've installed the plugin and start to use it for the first time, you will be prompted to enter your Alpha Vantage API key. For example, you might start by saying `use alpha_vantage to fetch the income statement for IBM.`

You will be prompted by ChatGPT to enter your Alpha Vantage API key. Provide the key at this prompt.

Note: This key is stored securely and is used to make requests to the Alpha Vantage API on your behalf.

## Security Best Practices
It's important to keep your API key secure as it links your plugin to your Alpha Vantage account. Do not share your API key in public spaces like public GitHub repositories or public forum posts. If you suspect that your API key might have been compromised, you can always generate a new one from the Alpha Vantage website

## Getting Started

To use this interface, you'll need to update the placeholders in the `ai-interface.json` file:

- `https://your_domain/openapi.json`: Replace this with the URL where you host the `OpenAPI_Plugin_Specification.json` file.

- `https://your_domain/logo.png`: Replace this with the URL of the logo you want to use for this interface.

- `support@your_domain.com`: Replace this with the contact email for support related to this interface.

- `https://your_domain/legal`: Replace this with the URL where you host the legal information related to this interface.

## Features

### Equities
- Get an overview, income statement, balance sheet, cash flow, earnings, and earnings calendar for a specific equity symbol.

### Cryptocurrencies
- Retrieve the daily, weekly, or monthly historical time series for a digital currency traded on a specific market.

### Currency Exchange
- Obtain currency exchange rates. You can ask for the currency you would like to get the exchange rate for, and the destination currency for the exchange rate.

### News Analysis Sentiment
- Fetch news articles based on certain topics, tickers, or timeframes, and analyze the sentiment of the articles.

### The Alpha Vantage Plugin supports the following features:

- Fetching company overviews
  
- Fetching income statements
  
- Fetching balance sheets
  
- Fetching cash flow data
  
- Fetching earnings data
  
- Fetching earnings calendar
  
- Fetching currency exchange rates
  
- Fetching daily, weekly, or monthly historical time series for a digital currency traded on a specific market
  
- Fetching economic indicators such as Consumer Price Index (CPI), Inflation, and Treasury Yields

## Usage

The plugin is invoked with the phrase `use alpha_vantage to...`

For example, `use alpha_vantage to fetch the income statement for IBM`. 

Or, to retrieve daily historical data for a digital currency, you might say `use alpha_vantage to fetch the daily historical data for BTC traded in USD`.

For economic indicators, you can use `use alpha_vantage to fetch CPI data.`

## News Sentiment (v1.01)
You can now fetch market news and sentiment data related to specific topics or sectors. This feature uses the newsSentiment function of the Alpha Vantage API.

To specify a topic, use the topics parameter followed by the topic of your choice. For instance, to fetch news related to the technology sector, you could use:

`use alpha_vantage to get news sentiment for tickers=AAPL with topics=technology`

Remember, you can specify multiple topics by separating them with a comma:

`use alpha_vantage to get news sentiment for tickers=AAPL with topics=technology,ipo`

This will fetch news articles that simultaneously cover technology and IPOs.

Below is the full list of supported topics:

- Blockchain: `blockchain`
- Earnings: `earnings`
- IPO: `ipo`
- Mergers & Acquisitions: `mergers_and_acquisitions`
- Financial Markets: `financial_markets`
- Economy - Fiscal Policy (e.g., tax reform, government spending): `economy_fiscal`
- Economy - Monetary Policy (e.g., interest rates, inflation): `economy_monetary`
- Economy - Macro/Overall: `economy_macro`
- Energy & Transportation: `energy_transportation`
- Finance: `finance`
- Life Sciences: `life_sciences`
- Manufacturing: `manufacturing`
- Real Estate & Construction: `real_estate`
- Retail & Wholesale: `retail_wholesale`
- Technology:`technology`

## Contribution

Contributions are welcome! If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are always welcome.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

