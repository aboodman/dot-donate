# Motivation

It is increasingly common for open source projects to accept donations via a variety of mechanisms, such as [PayPal](https://www.paypal.com/us/home), [Open Collective](https://opencollective.com/), [Patreon](https://www.patreon.com/), or cryptocurrencies.

However, there is currently no easy way to discover which of the projects you rely on accepts donations. And there is no way to automate distribution of donations among many projects.

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

# Semantics

All the fields are optional. If more than one payment type is specified, it means that users may pay the project via any of the listed payment types.

# Currently Supported Payment Types

| Type | Description |
|-|-|
| PayPal | A [PayPal address](http://paypal.com) |
| BTC | A [bitcoin address](https://en.bitcoin.it/wiki/Address) |
| USDC | A [USDC address](https://www.coinbase.com/usdc) |

# Thanks

* The [thanks](https://www.npmjs.com/package/thanks) package by Feross Aboukhadijeh is a centralized directory that first attempted to solve the discovery problem, but only for the NPM ecosystem.
* Solomon Hykes encouraged the separation of this idea from other projects, and was right.
* [BackYourStack](https://github.com/opencollective/backyourstack) attempts to solve the discovery problem by scanning a repository for dependencies that accept donations via OpenCollective.
