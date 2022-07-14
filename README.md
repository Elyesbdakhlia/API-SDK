# API-SDK
First test version which includes 6 endpoints:

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

response = sdk.historical.moves.total_oi(currency="btc", start="2022-06-07", end="2022-06-14", limit="10", page="2")
for i in response.items:
    print(i.v)
                                     


```

## Documentation for available API Endpoints

|Class | Sub-class | Method                                                             | Description                                    |
|------------ |----------|--------------------------------------------------------------------|------------------------------------------------|
|*realtime* | options  | get_atm(market, currency, period)      | At the money Implied Volatility Term Structure |
|*realtime* | options  | gex_date(market, currency, maturity)                               | Gamma Exposure by Expiration                   |
|*realtime* | options  | greeks(market, currency, maturity, optiontype)                     | Greeks                                         |
|*realtime* | derivs   | oi_gainers(market, oitype, period)                                 | oi gainers                                     |
|*historical* | options  | iv(market, instrument, start(opt), end(opt), limit(opt), page(opt) | Instrument Historical Implied Volatility       |
|*historical* | move     | total_oi(currency, start(opt), end(opt), limit(opt), page(opt)     | total oi                                       |








