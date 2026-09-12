# Currency Converter

A React-based currency converter that fetches live exchange-rate data from a public API.

## Features

- Convert between supported currencies
- Fetch live exchange rates
- Clear loading state while fetching data
- Clear error state when the request fails
- Empty state when the requested currency pair is not covered by the data source
- Reviewer controls to demonstrate required application states
- Responsive layout for desktop and mobile screens

## Application States

The application demonstrates four main states:

### 1. Loading State

Click `Convert` or `Test Live Data`.

The application displays a loading message while exchange-rate data is being fetched.

### 2. Success State

Enter an amount, select supported currencies, and click `Convert`.

For example:

`5 USD → CAD`

The application displays the converted amount and exchange rate using live data.

### 3. Error State

Click `Simulate Error` in the `Reviewer State Tests` section.

The application displays:

> Unable to load exchange rates. Please check your connection and try again.

This allows the reviewer to verify the error state without modifying the source code.

### 4. Empty State

Click `Test Unsupported Pair`.

The application successfully requests exchange-rate data and then checks for a currency code that is not present in the returned data.

The application displays a message explaining that the requested currency pair is not covered by the data source.

This is treated as a data gap rather than a request failure.

## Reviewer Testing

The required states can be demonstrated without changing the source code.

| State | How to test |
|---|---|
| Loading | Click `Convert` or `Test Live Data` |
| Success | Enter an amount and convert supported currencies |
| Error | Click `Simulate Error` |
| Empty | Click `Test Unsupported Pair` |

## API

Exchange rates are fetched from the ExchangeRate-API Open Access endpoint.

## Tech Stack

- React
- Vite
- JavaScript
- CSS
- ExchangeRate-API

## Running Locally

Clone the repository and install dependencies:

```bash
npm install