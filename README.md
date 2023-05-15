# Alpha Vantage Plugin for OpenAI ChatGPT

This repository contains the OpenAPI specification and the plugin manifest for the Alpha Vantage Plugin for OpenAI's ChatGPT. This plugin allows ChatGPT users to fetch financial data from Alpha Vantage directly through the chat interface. 

## Disclaimer
Please note that this is an unofficial open-source project and is neither endorsed nor owned by Alpha Vantage Inc. This plugin is developed independently and Alpha Vantage Inc. bears no responsibility for it.

## Files

- `openapi_specification.json`: This file contains the OpenAPI specification that describes the Alpha Vantage API's endpoints and responses. 

- `plugin_manifest.json`: This file is the plugin manifest that describes how OpenAI's ChatGPT should interact with the Alpha Vantage Plugin.

## Getting Started

To use this plugin, you'll need to update the following placeholders in the `plugin_manifest.json` file:

- `https://your_domain/openapi.json`: Replace this with the URL where you host the `openapi_specification.json` file.

- `https://your_domain/logo.png`: Replace this with the URL of the logo you want to use for this plugin.

- `support@your_domain.com`: Replace this with the contact email for support related to this plugin.

- `https://your_domain/legal`: Replace this with the URL where you host the legal information related to this plugin.

## Features

The Alpha Vantage Plugin supports the following features:

- Fetching company overviews
- Fetching income statements
- Fetching balance sheets
- Fetching cash flow data
- Fetching earnings data
- Fetching earnings calendar

## Usage

The plugin is invoked with the phrase 'use alpha_vantage to...'. For example, 'use alpha_vantage to fetch the income statement for IBM'.

## Contribution

Contributions are welcome! If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are always welcome.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
