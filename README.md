# market-data-aggregator

A real time system that aggregates data from differents sources (Binance, kraken, alpha ventage, etc) to give real-time information ( normalise data) to the trader or another financial system like trading system, or alerte system.

## 1. Main goal

### Objectif

1. Collect of data in real time from different sources
2. Agregate data to get a unifie view. For example:
```json
{
  "symbol": "AAPL",
  "name": "Apple Inc.",
  "exchange": "NASDAQ",
  "last_price": 150.25,
  "open_price": 148.50,
  "high_price": 151.00,
  "low_price": 147.75,
  "volume": 1_200_000,
  "bid_price": 150.20,
  "ask_price": 150.30,
  "timestamp": "2024-09-12T12:34:56Z"

}
```
3. Serve data as a API for differents user or financial service 

### High view level of constrain

1. **High scalability**: The system should be able to extend to other data sources, and able to handle massive data sources.
2. **High availability**: the system should be robust to default
3. **Low latence**: The serve should traite and serve data as faster as possible 

## 2. Technical constrain

## 3. Improvement
1. fault managament for connexion, make a automatic system for reconnexion.
2. Uses timeouts to prevent the system from being blocked if an API becomes slow.

## Exigence du projet
1. Plusieurs sources de donnees, afin d'avoir la possibilite de scaler sur plusieurs sources. Trois sources pour un premier temps: [Binance](https://developers.binance.com/docs/binance-spot-api-docs/CHANGELOG), [Kraken](https://docs.kraken.com/api/), [Alpha vintage](https://www.alphavantage.co/), [coingecko](https://www.coingecko.com/fr/api), [alpaca](https://alpaca.markets/)\. Il faudra definir une architecture pour la scalabilite a d'autres sources des donnees
2. Utiliser les api stream ou websocket pour une collecte en temps reel. ( Le traitement pourrait se faire aussi en temps reel en fonction de l'evolution du projet)
3. Definir un format unique pour les donnes, apres transformations: csv, json, etc
4. Frequence de mise a jour: chaque jour, heure, minutes, seconde, millisecondes, etc
5. Choisir une base de donnes permettant un stockage temporelle type redis,TimeScaleDB ou influxDB qui permet une lecture/ecriture rapide
6. Developper une Api rest ou GraphQL permettant ou utlisateur ou d'autre service de consommer ces donnees recupterees et agregees sous format normalise
7. 
