# Alpha Vantage Plugin for OpenAI ChatGPT

This repository contains the OpenAPI specification and the plugin manifest for the Alpha Vantage Plugin for OpenAI's ChatGPT. This plugin allows ChatGPT users to fetch financial data from Alpha Vantage directly through the chat interface. 

## Disclaimer
Please note that this is an unofficial open-source project and is neither endorsed nor owned by Alpha Vantage Inc. This plugin is developed independently and Alpha Vantage Inc. bears no responsibility for it.

## Files

- `OpenAPI_Plugin_Specification.json`: This file contains the OpenAPI specification that describes the Alpha Vantage API's endpoints and responses.
  
- `ai-plugin.json`: This file is the plugin manifest that describes how OpenAI's ChatGPT should interact with the Alpha Vantage Plugin.

- `ai-plugin.json`: This is the main manifest file that includes the HTTP service authentication necessary for the plugin to interact with the Alpha Vantage API.
  
- `Unused_Manifest_Files/Plugin_Manifest_NoAuth.json`: This is an alternative version of the manifest file, which does not include authentication. It is not currently in use for this project, but has been preserved for potential use in other projects where authentication may not be required. It is stored in the `Unused_Manifest_Files` directory to avoid confusion.


## Getting Started

To use this plugin, you'll need to update the following placeholders in the `ai-plugin.json` file:

- `https://your_domain/openapi.json`: Replace this with the URL where you host the `OpenAPI_Plugin_Specification.json` file.

- `https://your_domain/logo.png`: Replace this with the URL of the logo you want to use for this plugin.

- `support@your_domain.com`: Replace this with the contact email for support related to this plugin.

- `https://your_domain/legal`: Replace this with the URL where you host the legal information related to this plugin.

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

This project is licensed under the MIT License - see the [[LICENSE]](https://github.com/Slyx737/Alpha-Vantage-ChatGPT-Plugin/blob/main/LICENSE.md) file for details.
