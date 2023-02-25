# :icon-rocket: Getting Started

Welcome to the Wraph.io developer documentation!

Wraph.io is a tool that allows you to create a GraphQL endpoint that aggregates multiple REST APIs that live behind it. With Wraph.io, you can easily create a single API that combines data from different sources, without having to worry about the details of each individual API.
Configuration

Wraph.io is configured using a JSON file that describes the various REST APIs that you want to combine. Here's an example configuration:

css

[    {        "name": "BitstampTicker",        "url": "https://www.bitstamp.net/api/v2/ticker/{pair}/",        "params": {            "pair": "BTCUSD"        }    }]

This configuration sets up a single API called "BitstampTicker" that retrieves the ticker for the BTC/USD trading pair from the Bitstamp API. The "{pair}" placeholder in the URL is replaced with the value of the "pair" parameter, which is set to "BTCUSD" in this case.
Usage

To use Wraph.io, you first need to start the server by running the following command:

php

wraph serve <config_file>

Where <config_file> is the path to your configuration file.

Once the server is running, you can access the GraphQL endpoint at http://localhost:8000/graphql. You can use any GraphQL client to send queries to the endpoint and retrieve data from the configured APIs.

For example, to retrieve the ticker for the BTC/USD trading pair from the Bitstamp API, you could send the following query:

graphql

query {
  BitstampTicker {
    last
  }
}

This would return the last traded price for the BTC/USD trading pair from the Bitstamp API.
Conclusion

Wraph.io makes it easy to combine data from multiple REST APIs into a single GraphQL endpoint. With its simple configuration and easy-to-use API, you can quickly create powerful applications that leverage data from different sources. If you have any questions or feedback, please feel free to reach out to us at support@wraph.io.
