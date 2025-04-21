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

### **Key Data Centers for HFT**  
1. **London (Equinix LD4)** – Bybit, OKX, BitMEX, Kraken, Phemex, Bitfinex.  
2. **Singapore (AWS/AliCloud)** – Binance, Bybit, KuCoin, Bitget, Gate.io, MEXC.  
3. **New York (NY4/NY5)** – Bybit, OKX, Coinbase, Bitfinex.  
4. **Amsterdam (AMS-IX)** – Deribit (best for EU futures).  
5. **Chicago (CHI)** – Kraken, CME Group (if including Bitcoin futures).  

### **HFT Tips:**  
- **Colocation**: If the exchange supports it (Bybit, OKX, Kraken, BitMEX, Deribit), rent a server in **LD4 (London)** or **NY4 (New York)**.  
- **Asia**: For Binance, Bybit, OKX – **Singapore (AWS)**.  
- **Testing**: Use `ping` and `traceroute` (e.g., `ping api.binance.com`).  
