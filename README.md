# Motivation

It is increasingly common for open source projects to accept donations via a variety of mechanisms, such as PayPal, Open Collective, Patreon, or cryptocurrencies.

However, there is currently no easy way to discover which of the projects you rely on accepts donations. And there is no way to automate distributing donations among many projects.

This project specifies a simple file format that allows an open source project to specify how to send it money, so that the discovery and distribution can be automated.

# Example

```
{
  "PayPal": "project@paypal.com",
  "BTC": "1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2",
  "USDC": "0x0000000000000000000000000000000000000000"  
}
```

# Location

A `.donate` file MUST be located in the root of the repository and all-lowercased.

# Format

The `.donate` file MUST be formatted as [JSON](https://www.json.org/).

# Currently Supported Payment Types

| Type | Description |
|-|-|
| PayPal | A [PayPal](http://paypal.com) address |
| BTC | A [bitcoin address](https://en.bitcoin.it/wiki/Address) |
| USDC | A [USDC](https://www.coinbase.com/usdc) address |
