# Market data aggregator

A real time system that aggregates data from differents sources like Binance, kraken, alpha ventage, etc, and give real-time information ( normalise data) to the trader or another financial system like trading system, or alerte system.

## 1. Main goal

### Objectif

1. Collect of data in real time from different sources
2. Agregate data to get a unifie view. \
  
For example:
```json
{
  "symbols": [
    {
      "symbol": "AAPL",
      "type": "stock",
      "exchange": "NASDAQ",
      "last_price": 150.25,
      "volume": 1_200_000,
      "bid_price": 150.20,
      "ask_price": 150.30,
      "timestamp": "2024-09-12T12:34:56Z"
    },
    {
      "symbol": "BTCUSDT",
      "type": "crypto",
      "exchange": "Binance",
      "last_price": 27_500.10,
      "volume": 2_000_000,
      "bid_price": 27_490.00,
      "ask_price": 27_510.00,
      "timestamp": "2024-09-12T12:34:57Z"
    },
  ...
  ]
}
```
3. Serve data as a API for differents user or financial service 

### High view level of constrain

1. **High scalability**: The system should be able to extend to other data sources, and able to handle massive data sources.
2. **High availability**: the system should be robust to default
3. **Low latence**: The serve should traite and serve data as faster as possible, we serve each seconde ? minutes ? milliseconde ?

## 2. Technical tools and technologie
- Language and Framework: Python, FastAPI (or GraphQL?), ascycio, threading, aiohttp ou websockets
- Database: Redis, influxDB, TimeScaleDB
- Message system: kafka, RabbitMQ
- Scalability: Docker, Kubernetes
- API for data sources: [Binance](https://developers.binance.com/docs/binance-spot-api-docs/CHANGELOG), [Kraken](https://docs.kraken.com/api/), [Alpha vintage](https://www.alphavantage.co/), [coingecko](https://www.coingecko.com/fr/api), [alpaca](https://alpaca.markets/)
- Unit and integration test (pytest): Test each component to check everything work fine, and test if the system can handle huge data incoming
- Deploiement: aws

## 3. How to install ( or link )

## 4. How to use (run)

## 4. Improvement
1. fault managament for connexion, make a automatic system for reconnexion.
2. Uses timeouts to prevent the system from being blocked if an API becomes slow.
3. Load balancing
4. 
## 5. Fun a bug or contributed ?
If your found a issue or want to improve this project, feel free to submit a PR with the fix or the improvement 


## ressources

- [back testing with clairevoyant](https://github.com/anfederico/clairvoyant)
- [A lot example of projet for market data](https://github.com/anfederico?tab=repositories)
- [Banner marker ](https://banner.godori.dev/)
- [Shield io](https://shields.io/) 

