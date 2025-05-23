# Table of Crypto Exchange Server Locations

| Exchange       | Primary Data Centers (HFT Regions)               | Colocation Available?     | Notes                              | API URL for Ping Test          |
|----------------|------------------------------------------------|--------------------------|------------------------------------|-------------------------------|
| **Binance**    | Singapore (AWS), Tokyo, Frankfurt (AWS), US (Virginia) | No (best ping in Singapore) | Binance US – AWS in US             | `api.binance.com`             |
| **Bybit**      | Singapore (AWS), Tokyo, London (Equinix LD4), New York (NY4) | **Yes (LD4, SG1)**       | Best colocation in LD4             | `api.bybit.com`               |
| **OKX**        | Hong Kong (AliCloud), Singapore (AWS), London (LD4), Chicago/NY4 | **Yes (LD4, Hong Kong)** | Primary hosting – Hong Kong        | `www.okx.com`                 |
| **KuCoin**     | Singapore (AliCloud), Hong Kong, London (AWS)   | No (best ping in Singapore) | Relies on Alibaba Cloud           | `api.kucoin.com`              |
| **Bitget**     | Singapore (AliCloud), Hong Kong, London (AWS)   | No (best ping in Singapore) | Primary hosting – Singapore       | `api.bitget.com`              |
| **HTX (Huobi)**| Singapore, US (AWS), Frankfurt (AWS)            | No                       | Previously used AWS in Singapore  | `api.huobi.pro`               |
| **BitMEX**     | London (Equinix LD4), Singapore, US (AWS)       | **Yes (LD4)**            | Historically strong in LD4        | `www.bitmex.com`              |
| **Deribit**    | Amsterdam (AMS-IX), Singapore (AWS)             | **Yes (AMS-IX)**         | Best for EU futures               | `www.deribit.com`             |
| **Kraken**     | London (LD4), US (Chicago, San Francisco)       | **Yes (LD4, CHI)**       | HFT support in LD4 and CHI        | `api.kraken.com`              |
| **Coinbase**   | US (AWS, NY4/NY5), Frankfurt (AWS)              | No (close to NY4)        | Primary hosting – US              | `api.coinbase.com`            |
| **Phemex**     | Singapore (AWS), London (LD4), US (AWS)         | **Yes (LD4)**            | Competes with Bybit in LD4        | `api.phemex.com`              |
| **Gate.io**    | Singapore (AliCloud), Hong Kong, London (AWS)   | No                       | Uses AliCloud in Asia             | `api.gate.io`                 |
| **MEXC**       | Singapore (AliCloud), Hong Kong, US (AWS)       | No                       | Primary hosting – Singapore       | `api.mexc.com`                |
| **LBank**      | Hong Kong (AliCloud), Singapore, US (AWS)       | No                       | Limited HFT data                  | `api.lbank.info`              |
| **WhiteBIT**   | Frankfurt (AWS), Lithuania (Equinix)            | No                       | Focus on EU                       | `api.whitebit.com`            |
| **BingX**      | Singapore (AWS), London (LD4)                   | No                       | Growing in HFT segment            | `api.bingx.com`               |
| **Bitfinex**   | London (LD4), US (NY4), Singapore (AWS)         | **Yes (LD4, NY4)**       | One of the first HFT exchanges    | `api.bitfinex.com`            |
| **Upbit**      | Seoul (AWS), Singapore                          | No                       | Strong Korean liquidity           | `api.upbit.com`               |
| **Bithumb**    | Seoul (local data centers)                      | No                       | Korea-only                        | `api.bithumb.com`             |
| **Crypto.com** | Singapore (AWS), US (AWS), Frankfurt (AWS)      | No                       | Uses AWS globally                 | `api.crypto.com`              |

## **Additional FIX API Connection Information**

The following exchanges provide FIX API for high-frequency trading with specified recommended data centers:

| Exchange       | Instrument Types                    | Order Types              | Recommended Data Center |
|----------------|-------------------------------------|--------------------------|-------------------------|
| **Binance**    | Spot, Futures, Perpetuals          | Limit, Market           | Tokyo                   |
| **Coinbase**   | Spot                               | Limit, Market, Stop     | New York                |
| **HTX**        | Spot, Futures, Perpetuals          | Limit                   | Tokyo                   |
| **Kraken**     | Spot                               | Limit, Market, Stop     | London                  |
| **Bitstamp**   | Spot                               | Limit                   | London                  |
| **Gemini**     | Spot                               | Limit                   | New York                |
| **OKX**        | Spot, Futures, Perpetuals          | Limit, Market           | Hong Kong               |
| **KuCoin**     | Spot, Futures, Perpetuals          | Limit                   | Tokyo                   |
| **HitBTC**     | Spot, Futures, Perpetuals          | Limit, Market           | London                  |
| **CEX.io**     | Spot                               | Limit, Market           | London                  |
| **BitMEX**     | Futures, Perpetuals                | Limit, Market           | London                  |
| **Bybit**      | Spot, Futures, Perpetuals          | Limit, Market           | Tokyo                   |
| **Bitfinex**   | Spot, Futures, Perpetuals          | Limit, Market           | London                  |
| **Bithumb**    | Spot                               | Limit                   | Hong Kong               |
| **Gate.io**    | Spot, Futures, Perpetuals          | Limit                   | Tokyo                   |
| **ProBit**     | Spot                               | Limit                   | Tokyo                   |
| **Deribit**    | Futures, Perpetuals                | Limit, Market           | London                  |
| **Binance US** | Spot                               | Limit, Market           | Tokyo                   |
| **YoBit**      | Spot                               | Limit                   | London                  |
| **EXMO**       | Spot                               | Limit                   | London                  |
| **bitFlyer**   | Spot                               | Limit                   | Tokyo                   |
| **BitMart**    | Spot                               | Limit                   | Hong Kong               |
| **Amber**      | Spot                               | Limit, Market           | Tokyo                   |
| **WhiteBIT**   | Spot                               | Limit, Market           | London                  |
| **Bitget**     | Spot, Futures, Perpetuals          | Limit                   | Tokyo                   |
| **RuleMatch**  | Spot                               | Limit, Market           | London                  |

## **Confirmed Specific Data Center Information**

**Gemini**: Primary trading platform and network Point of Presence (PoP) are located in **Equinix NY5** data center in Secaucus, New Jersey.

**Coinbase Derivatives**: Trading platform operates from two locations:
- **Production**: Cyrus One Data Center in Aurora, Illinois (2905 Diehl Road, Aurora, Illinois, 60502)
- **Disaster Recovery/Integration/Staging**: Equinix NY5 Data Center in Secaucus, New Jersey (800 Secaucus Road, Secaucus, New Jersey, 07094)

**Kraken**: Plans to launch ultra-low latency colocation service through European data center in partnership with Beeks Group.

## **Curl Commands for Exchange Latency Testing**

| Exchange       | Curl Command for Time Endpoint Testing                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **Binance**    | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.binance.com/api/v3/time"`                        |
| **Bybit**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.bybit.com/v5/market/time"`                       |
| **OKX**        | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://www.okx.com/api/v5/public/time"`                     |
| **KuCoin**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.kucoin.com/api/v1/timestamp"`                    |
| **Bitget**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.bitget.com/api/v2/public/time"`                  |
| **HTX (Huobi)**| `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.huobi.pro/v1/common/timestamp"`                  |
| **BitMEX**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://www.bitmex.com/api/v1/stats"`                        |
| **Deribit**    | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://www.deribit.com/api/v2/public/get_time"`             |
| **Kraken**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.kraken.com/0/public/Time"`                       |
| **Coinbase**   | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.coinbase.com/v2/time"`                           |
| **Phemex**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.phemex.com/v1/md/time"`                          |
| **Gate.io**    | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.gateio.ws/api/v4/spot/time"`                     |
| **MEXC**       | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.mexc.com/api/v3/time"`                           |
| **LBank**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.lbank.info/v2/timestamp.do"`                     |
| **WhiteBIT**   | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://whitebit.com/api/v4/public/time"`                    |
| **BingX**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://open-api.bingx.com/openApi/spot/v1/common/time"`     |
| **Bitfinex**   | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api-pub.bitfinex.com/v2/platform/status"`            |
| **Upbit**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.upbit.com/v1/market/all"`                        |
| **Bithumb**    | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.bithumb.com/public/ticker/ALL_KRW"`              |
| **Crypto.com** | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.crypto.com/v2/public/get-book"`                  |
| **Gemini**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.gemini.com/v1/pubticker/btcusd"`                 |
| **Bitstamp**   | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://www.bitstamp.net/api/v2/ticker/btcusd/"`             |
| **HitBTC**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.hitbtc.com/api/3/public/time"`                   |
| **CEX.io**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://cex.io/api/ticker/BTC/USD"`                          |
| **ProBit**     | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.probit.com/api/exchange/v1/time"`                |
| **YoBit**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://yobit.net/api/3/info"`                               |
| **EXMO**       | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.exmo.com/v1.1/ticker"`                           |
| **bitFlyer**   | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.bitflyer.com/v1/getmarkets"`                     |
| **BitMart**    | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api-cloud.bitmart.com/system/time"`                  |
| **Amber**      | `curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.amber.com/v1/time"`                              |

## **Batch Testing Script**

For testing all exchanges simultaneously, you can use the following bash script:

```bash
#!/bin/bash

echo "=== Crypto Exchange Latency Test ==="
echo "Testing from: $(curl -s ipinfo.io/city), $(curl -s ipinfo.io/country)"
echo "Date: $(date)"
echo "=================================="

declare -A exchanges=(
    ["Binance"]="https://api.binance.com/api/v3/time"
    ["Bybit"]="https://api.bybit.com/v5/market/time"
    ["OKX"]="https://www.okx.com/api/v5/public/time"
    ["KuCoin"]="https://api.kucoin.com/api/v1/timestamp"
    ["Bitget"]="https://api.bitget.com/api/v2/public/time"
    ["HTX"]="https://api.huobi.pro/v1/common/timestamp"
    ["BitMEX"]="https://www.bitmex.com/api/v1/stats"
    ["Deribit"]="https://www.deribit.com/api/v2/public/get_time"
    ["Kraken"]="https://api.kraken.com/0/public/Time"
    ["Coinbase"]="https://api.coinbase.com/v2/time"
    ["Gate.io"]="https://api.gateio.ws/api/v4/spot/time"
    ["MEXC"]="https://api.mexc.com/api/v3/time"
    ["WhiteBIT"]="https://whitebit.com/api/v4/public/time"
    ["Bitfinex"]="https://api-pub.bitfinex.com/v2/platform/status"
)

for exchange in "${!exchanges[@]}"; do
    url="${exchanges[$exchange]}"
    printf "%-12s: " "$exchange"
    time=$(curl -o /dev/null -s -w "%{time_total}" "$url" 2>/dev/null)
    if [ $? -eq 0 ]; then
        printf "%.3f seconds\n" "$time"
    else
        echo "FAILED"
    fi
done
```

## **Usage Instructions**

**Single Test:**
```bash
curl -o /dev/null -s -w "Time: %{time_total} seconds\n" "https://api.binance.com/api/v3/time"
```

**Multiple Tests (10 times):**
```bash
for i in {1..10}; do curl -o /dev/null -s -w "Test $i - Time: %{time_total} seconds\n" "https://api.binance.com/api/v3/time"; done
```

**Test with Additional Information:**
```bash
curl -o /dev/null -s -w "Total: %{time_total}s | DNS: %{time_namelookup}s | Connect: %{time_connect}s | Transfer: %{time_starttransfer}s\n" "https://api.binance.com/api/v3/time"
```

### **Key Data Centers for HFT**  
1. **London (Equinix LD4)** – Bybit, OKX, BitMEX, Kraken, Phemex, Bitfinex, HitBTC, CEX.io, Deribit, YoBit, EXMO, WhiteBIT, RuleMatch  
2. **Tokyo** – Binance, HTX, KuCoin, Bybit, Gate.io, ProBit, Binance US, bitFlyer, Amber, Bitget  
3. **New York (NY4/NY5)** – Coinbase, Gemini, Bybit, OKX, Bitfinex  
4. **Hong Kong** – OKX, Bithumb, BitMart  
5. **Amsterdam (AMS-IX)** – Deribit (best for EU futures)  

### **HFT Tips:**  
- **Colocation**: If the exchange supports it (Bybit, OKX, Kraken, BitMEX, Deribit), rent a server in **LD4 (London)** or **NY4/NY5 (New York)**
- **Asia**: For Binance, Bybit, OKX – **Tokyo** or **Singapore (AWS)**
- **Testing**: Use `ping` and `traceroute` (e.g., `ping api.binance.com`)
- **FIX API**: Many exchanges provide FIX API with recommended data centers for optimal performance
