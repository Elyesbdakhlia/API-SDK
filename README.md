# API-SDK
First version:
120 endpoints
## Requirements.

Python 3.7+

## Installation & Usage
### pip install



```sh
pip install SDK-Laevitas-test
```
Then import the package:
```python
from Laevitas import SDK 
```



## Getting Started

Please follow the procedure and then run the following:

```python
from Laevitas import SDK

# create an instance of the API class
sdk = SDK.api()

# Configure your api key
sdk.configure('your-api-key')

response = sdk.historical.move.total_oi(currency="btc", start="2022-06-07", end="2022-06-14", limit="10", page="2")
for i in response.items:
    print(i.v)
                                     


```

## Documentation for available API Endpoints

|Class | Sub-class | Method                                                                                           | Description                                        |
|------------ |-----------|--------------------------------------------------------------------------------------------------|----------------------------------------------------|
|*realtime* | options   | get_atm(market, currency)                                                                        | At the money Implied Volatility Term Structure     |
|*realtime* | options   | gex_date_all(market, currency)                                                                   | Gamma Exposure All Expirations                     |
|*realtime* | options   | maturities(market, currency)                                                                     | Active Expirations                                 |
|*realtime* | options   | oi_expiry(market, currency)                                                                      | Open Interest By Expiration                        |
|*realtime* | options   | oi_strike_all(market, currency)                                                                  | Open Interest By Strike All Expirations            |
|*realtime* | options   | oi_type(market, currency)                                                                        | Open Interest By Type                              |
|*realtime* | options   | top_traded_option(market, currency)                                                              | Top Traded Instrument                              |
|*realtime* | options   | v_expiry(market, currency,)                                                                      | Volume By Expiry                                   |
|*realtime* | options   | v_strike_all(market, currency,)                                                                  | Volume By Strike All Expirations                   |
|*realtime* | options   | volume_buy_sell_all(market, currency,)                                                           | Buy/Sell Volume Last 24h All Expirations           |
|*realtime* | options   | iv_strike(market, currency,strike)                                                               | IV Term Structure By Strike                        |
|*realtime* | options   | oi_strike(market, currency,maturity)                                                             | Open Interest By Strike                            |
|*realtime* | options   | oi_net_change_all(market, currency,hours)                                                        | Open Interest Change All Expirations               |
|*realtime* | options   | top_instrument_oi_change(market, currency,hours)                                                 | Top Instrument OI Change                           |
|*realtime* | options   | volume_buy_sell(market, currency,maturity)                                                       | Buy/Sell Volume Last 24h                           |
|*realtime* | options   | v_strike(market, currency,maturity)                                                              | Volume By Strike                                   |
|*realtime* | options   | summary_trades(market, currency,hours)                                                           | Summary trades                                     |
|*realtime* | options   | v_strike(market, currency,maturity)                                                              | Volume By Strike                                   |
|*realtime* | options   | oi_net_change_all(market, currency,hours)                                                        | Open Interest Change All Expirations               |
|*realtime* | options   | gex_date(market, currency, maturity)                                                             | Gamma Exposure by Expiration                       |
|*realtime* | options   | greeks(market, currency, maturity, optiontype)                                                   | Greeks                                             |
|*realtime* | options   | iv_all(market, currency, maturity, type)                                                         | Implied Volatility Skew                            |
|*realtime* | options   | iv_table(market, currency)                                                                       | Implied volatility table                           |
|*realtime* | options   | oi_net_change(market, currency, maturity, hour)                                                  | Open Interest Change By Expiration                 |
|*realtime* | options   | snapshot(market, currency)                                                                       | Snapshot                                           |
|*realtime* | futures   | instruments()                                                                                    | available futures instruments                      |
|*realtime* | futures   | alt_currency ()                                                                                  | available futures currency                         |
|*realtime* | futures   | perpetual_funding(currency)                                                                      | Perpetual Funding                                  |
|*realtime* | futures   | futures_yield(currency)                                                                          | Futures Yield                                      |
|*realtime* | futures   | futures_basis(currency)                                                                          | Futures Basis                                      |
|*realtime* | futures   | volume_breakdown(currency)                                                                       | Volume Breakdown                                   |
|*realtime* | futures   | oi_breakdown(currency)                                                                           | Open Interest Breakdown                            |
|*realtime* | futures   | futures_curve(currency, market(opt))                                                             | futures term structure                             |
|*realtime* | futures   | markets_oi_gainers_and_losers(currency, option, hour)                                            | Futures Open interest Change                       |
|*realtime* | futures   | snapshot(market)                                                                                 | snapshot                                           |
|*realtime* | move      | oi_group()                                                                                       | Open Interest group                                |
|*realtime* | move      | oi_expiry()                                                                                      | Open Interest expiry                               |
|*realtime* | move      | volume_expiry()                                                                                  | Volume expiry                                      |
|*realtime* | move      | volume_group()                                                                                   | Volume group                                       |
|*realtime* | move      | volume_expiry_buy_sell()                                                                         | Volume expiry buy sell                             |
|*realtime* | move      | volume_contract_buy_sell()                                                                       | Volume contract buy sell                           |
|*realtime* | move      | volume_top_contract()                                                                            | volume top contract                                |
|*realtime* | move      | volume_type_buy_sell ()                                                                          | volume type buy/sell                               |
|*realtime* | move      | oi_top_contract()                                                                                | Open Interest top contract                         |
|*realtime* | move      | big_trades()                                                                                     | Big trades                                         |
|*realtime* | move      | contract_name()                                                                                  | Contract names                                     |
|*realtime* | move      | expirations()                                                                                    | Expirations                                        |
|*realtime* | move      | ftx_vs_deribit()                                                                                 | Ftx vs deribit                                     |
|*realtime* | move      | live()                                                                                           | Live                                               |
|*realtime* | defi      | dovs()                                                                                           | dovs                                               |
|*realtime* | defi      | ribbon()                                                                                         | ribbon                                             |
|*realtime* | defi      | friktion()                                                                                       | friktion                                           |
|*realtime* | defi      | squeeth()                                                                                        | squeeth                                            |
|*realtime* | defi      | thetanuts()                                                                                      | thetanuts                                          |
|*realtime* | derivs    | futures(market, currency, maturity)                                                              | futures                                            |
|*realtime* | derivs    | perpetuals(market, currency)                                                                     | perpetuals                                         |
|*realtime* | derivs    | summary(currency)                                                                                | summary                                            |
|*realtime* | derivs    | oi_gainers(market, oitype, period)                                                               | oi gainers                                         |
|*realtime* | derivs    | price_gainers(market, oitype, period)                                                            | price gainers                                      |
|*realtime* | derivs    | top_funding(market )                                                                             | top_funding                                        |
|*realtime* | derivs    | top_gainers_losers(change, type)                                                                 | top gainers losers                                 |
|*historical* | options   | option(market, instrument, start(opt), end(opt), limit(opt), page(opt)                           | options                                            |
|*historical* | options   | iv(market, instrument, start(opt), end(opt), limit(opt), page(opt)                               | Instrument Historical Implied Volatility           |
|*historical* | options   | price(market, instrument, start(opt), end(opt), limit(opt), page(opt)                            | Instrument Historical Price                        |
|*historical* | options   | oi_volume(market, instrument, start(opt), end(opt), limit(opt), page(opt)                        | Instrument Historical Open Interest & Volume       |
|*historical* | options   | underlying_price(market, instrument, start(opt), end(opt), limit(opt), page(opt)                 | Instrument Historical Underlying Price             |
|*historical* | options   | oi_strike(market,currency, maturity ,date)                                                       | Historical Open Interest By Strike                 |
|*historical* | options   | volume_strike(market,currency, maturity ,date)                                                   | Historical Volume By Strike                        |
|*historical* | options   | volume_pc_ratio(market, currency, start(opt), end(opt), limit(opt), page(opt)                    | Volume Put/Call Ratio                              |
|*historical* | options   | gex_index(market, currency, start(opt), end(opt), limit(opt), page(opt)                          | Gamma Exposure Index                               |
|*historical* | options   | max_pain(market, currency, start(opt), end(opt), limit(opt), page(opt)                           | Max Pain Monthly Expiration                        |
|*historical* | options   | atm_iv(market, currency, start(opt), end(opt), limit(opt), page(opt)                             | At the money Implied Volatility (Rolling Maturity) |
|*historical* | options   | volume_total(market, currency, start(opt), end(opt), limit(opt), page(opt)                       | Volume total                                       |
|*historical* | options   | oi_pc_ratio(market, currency, start(opt), end(opt), limit(opt), page(opt)                        | Open Interest Put/Call Ratio                       |
|*historical* | options   | oi_total(market, currency, start(opt), end(opt), limit(opt), page(opt)                           | Instrument Historical Implied Volatility           |
|*historical* | options   | vix(market, currency, start(opt), end(opt), limit(opt), page(opt)                                | Vol Index                                          |
|*historical* | options   | dvol(market, currency, start(opt), end(opt), limit(opt), page(opt)                               | Deribit Volatility Index (DVOL)                    |
|*historical* | options   | atm_iv_model(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                 | At the money Implied Volatility model              |
|*historical* | options   | butterfly(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                    | Butterfly                                          |
|*historical* | options   | butterfly_model(market, currency, type, start(opt), end(opt), limit(opt), page(opt)              | Butterfly model                                    |
|*historical* | options   | realized_vol(market, currency, start(opt), end(opt), limit(opt), page(opt)                       | realized vol                                       |
|*historical* | options   | skew(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                         | Skew                                               |
|*historical* | options   | skew_model(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                   | Skew model                                         |
|*historical* | options   | risk_reversal(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                | Risk Reversal                                      |
|*historical* | options   | risk_reversal_model(market, currency, type, start(opt), end(opt), limit(opt), page(opt)          | Risk Reversal model                                |
|*historical* | options   | gamma_bands(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                  | Gamma Bands                                        |
|*historical* | options   | total_oi(market, currency, maturiy, start(opt), end(opt), limit(opt), page(opt)                  | Total open interest                                |
|*historical* | options   | iv_bid_ask(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                   | iv bid/ask                                         |
|*historical* | options   | total_volume(market, currency, maturity, start(opt), end(opt), limit(opt), page(opt)             | total volume                                       |
|*historical* | options   | volumeOiByExchange(currency, maturity, start(opt), end(opt), limit(opt), page(opt)               | Volume open interest exchange                      |
|*historical* | futures   | oi_weighted_funding(currency, start(opt), end(opt), limit(opt), page(opt)                        | Open interest weighted funding                     |
|*historical* | futures   | oi_weighted_volume_funding(currency, start(opt), end(opt), limit(opt), page(opt)                 | Open interest weighted volume                      |
|*historical* | futures   | oi_weighted_basis(currency, start(opt), end(opt), limit(opt), page(opt)                          | Open interest weighted basis                       |
|*historical* | futures   | total_oi(currency, start(opt), end(opt), limit(opt), page(opt)                                   | Total open interest                                |
|*historical* | futures   | total_oi_by_margin(currency, start(opt), end(opt), limit(opt), page(opt)                         | Total open interest by margin                      |
|*historical* | futures   | total_volume(currency, start(opt), end(opt), limit(opt), page(opt)                               | Total volume                                       |
|*historical* | futures   | total_volume_by_margin(currency, start(opt), end(opt), limit(opt), page(opt)                     | Total volume by margin                             |
|*historical* | futures   | realized_volatility(currency, start(opt), end(opt), limit(opt), page(opt)                        | Realized volatility                                |
|*historical* | futures   | alt_summary(currency, start(opt), end(opt), limit(opt), page(opt)                                | Alt summary                                        |
|*historical* | futures   | alt_markets(currency, start(opt), end(opt), limit(opt), page(opt)                                | Alt markets                                        |
|*historical* | futures   | market_index(currency, start(opt), end(opt), limit(opt), page(opt)                               | Market index                                       |
|*historical* | futures   | indices_price(currency, start(opt), end(opt), limit(opt), page(opt)                              | Indices price                                      |
|*historical* | futures   | futures_annualized_basis(currency, option, start(opt), end(opt), limit(opt), page(opt)           | Futures annualized basis                           |
|*historical* | futures   | perpetual_funding_exchange(currency,option, start(opt), end(opt), limit(opt), page(opt)          | Perpetual funding exchange                         |
|*historical* | futures   | total_oi_by_exchange(currency, option, start(opt), end(opt), limit(opt), page(opt)               | Total oi by exchange                               |
|*historical* | futures   | total_volume_by_exchange(currency, option, start(opt), end(opt), limit(opt), page(opt)           | Total volume by exchange                           |
|*historical* | futures   | perpetual_yield(market, currency, start(opt), end(opt), limit(opt), page(opt)                    | Perpetual yield                                    |
|*historical* | futures   | perpetual_funding(market, currency, start(opt), end(opt), limit(opt), page(opt)                  | Perpetual funding                                  |
|*historical* | move      | total_oi(market, currency, start(opt), end(opt), limit(opt), page(opt)                           | total open interests                               |
|*historical* | move      | volume_buy_sell(market, currency, start(opt), end(opt), limit(opt), page(opt)                    | volume buy sell                                    |
|*historical* | move      | iv_type(market, currency, type, start(opt), end(opt), limit(opt), page(opt)                      | iv type                                            |
|*historical* | move      | iv_historical_open_future(market, currency, is_open, start(opt), end(opt), limit(opt), page(opt) | iv historical open future                          |
|*historical* | move      | total_volume(market, currency, start(opt), end(opt), limit(opt), page(opt)                       | total volume                                       |
|*historical* | move      | historical_iv(contract_name, market, start(opt), end(opt), limit(opt), page(opt)                 | historical iv                                      |
|*historical* | move      | historical_oi(contract_name, market, start(opt), end(opt), limit(opt), page(opt)                 | historical oi                                      |
|*historical* | move      | historical_price(contract_name, market, start(opt), end(opt), limit(opt), page(opt)              | historical price                                   |
|*historical* | move      | historical_volume(contract_name, market, start(opt), end(opt), limit(opt), page(opt)             | historical volume                                  |
|*historical* | move      | open_future(contract_type)                                                                       | open future                                        |
|*historical* | defi      | dovs_auctions(protocol, start(opt), end(opt), currency(opt), limit(opt), page(opt))              | dov auctions                                       |
|*historical* | derivs    | perpetuals(market, symbol, start(opt), end(opt), limit(opt), page(opt) )                         | perpetuals                                         |
|*historical* | derivs    | futures(market, symbol, date)                                                                    | futures                                            |
|*historical* | derivs    | summary(currency, start(opt), end(opt), limit(opt), page(opt) )                                  | summary                                            |







 


