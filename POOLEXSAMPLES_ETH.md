# Pool Exsamples for ETH
This is a collection of exsamples how to connect ethminer to your favorite ETH pool (alphabetic order).

* Stratum connection is preferred than getwork connection due its better network latency.
* If possible the samples use a protocol which supports reporting of hashrate (`--report-hashrate`) if pool supports this.

**Check for updates in the pool connection settings visiting the pools homepage.**

## Variables

We tried to merge the requirements of the variables so they match all pools.

| Variables  | Description                                                                                                                                               | Sample |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| ETH_WALLET | Replace `ETH_WALLET` with your Ethereum walletnumber including leading 0x.                                                                                | 0x1234567890ABCDEF1234567890abcdef12345678 |
| WORKERNAME | `WORKERNAME` may only contain letters and numbers. Some pools also only allow up to max 8 characters!                                                     | pl1rig01|
| EMAIL      | `EMAIL` may contain letters, numbers, underscores, dashes, dots and the @-sign. It **must** contain a @-sign and a dot!                                   | joe1.doe_jr-ny@acme.com |
| USERNAME   | `USERNAME` got from the pool (like [miningpoolhub.com](#miningpoolhubcom))                                                                                | my_username |
| WORKERPWD  | `WORKERPWD` is the password got from the pool for the worker (like [miningpoolhub.com](#miningpoolhubcom)) - if you have no password set try using 'x'    | my_workerpwd |
| BTC_WALLET | As some pools honor your work in BTC (eg [nicehash.com](#nicehashcom)) `BTC_WALLET` is your Bitcoin wallet address                                        | 1A2b3C4d5e5F6g7H8I9j0kLmNoPqRstUvW |

## Servers
The servers are listed in alphabetical order. To get best results reorder them from nearest to farest distance depending on your geographic location.

## Pools (alphabetic order)
| Pool Name | Pool Mainpage | Details about connection |
| -------- | ---------------------------- | - |
| [2miners.com](#2minerscom) | https://2miners.com/ | https://eth.2miners.com/en/help |
| [dwarfpool.org](#dwarfpoolorg) | https://dwarfpool.com/ | https://dwarfpool.com/eth |
| [ethermine.org](#ethermineorg) | https://ethermine.org/ | https://ethermine.org/|
| [ethpool.org](#ethpoolorg) | https://www.ethpool.org/ | https://www.ethpool.org/ |
| [f2pool.com](#f2poolcom) | https://www.f2pool.com/ | https://www.f2pool.com/help/?#tab-content-eth |
| [miningpoolhub.com](#miningpoolhubcom) | https://miningpoolhub.com/ | https://ethereum.miningpoolhub.com/ |
| [nanopool.org](#nanopoolorg) | https://nanopool.org/ | https://eth.nanopool.org/help |
| [nicehash.com](#nicehashcom) | https://www.nicehash.com/ | https://www.nicehash.com/help/which-stratum-servers-are-available |
| [sparkpool.com](#sparkpoolcom) | https://sparkpool.com/ | https://eth.sparkpool.com/ |



### 2miners.com

  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth.2miners.com:2020
  ```

### dwarfpool.org

  With email
  ```
  -P stratum1+tcp://ETH_WALLET@eth-ar.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-asia.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-au.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-br.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-cn.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-cn2.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-eu.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-hk.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-sg.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-ru.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-ru2.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-us.dwarfpool.com:8008/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-us2.dwarfpool.com:8008/WORKERNAME/EMAIL
  ```

  Without email
  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-ar.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-asia.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-au.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-br.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-cn.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-cn2.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-eu.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-hk.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-sg.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-ru.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-ru2.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-us.dwarfpool.com:8008
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-us2.dwarfpool.com:8008
  ```


### ethermine.org

  Non-SSL connection:
  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@asia1.ethermine.org:4444
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eu1.ethermine.org:4444
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@us1.ethermine.org:4444
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@us2.ethermine.org:4444
  ```

  SSL connection:
  ```
  -P stratum1+ssl://ETH_WALLET.WORKERNAME@asia1.ethermine.org:5555
  -P stratum1+ssl://ETH_WALLET.WORKERNAME@eu1.ethermine.org:5555
  -P stratum1+ssl://ETH_WALLET.WORKERNAME@us1.ethermine.org:5555
  -P stratum1+ssl://ETH_WALLET.WORKERNAME@us2.ethermine.org:5555
  ```


### ethpool.org

  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@asia1.ethpool.org:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eu1.ethpool.org:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@us1.ethpool.org:3333
  ```


### f2pool.com

  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth.f2pool.com:8008
  ```


### miningpoolhub.com

  ```
  -P stratum2+tcp://USERNAME.WORKERNAME:WORKERPWD@asia.ethash-hub.miningpoolhub.com:20535
  -P stratum2+tcp://USERNAME.WORKERNAME:WORKERPWD@europe.ethash-hub.miningpoolhub.com:20535
  -P stratum2+tcp://USERNAME.WORKERNAME:WORKERPWD@us-east.ethash-hub.miningpoolhub.com:20535
  ```

  HINT: It seems the password is not being verified by the pool so you can use simple 'x' as WORKERPWD.


### nanopool.org

  With email:
  ```
  -P stratum1+tcp://ETH_WALLET@eth-asia1.nanopool.org:9999/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-eu1.nanopool.org:9999/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-eu2.nanopool.org:9999/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-us-east1.nanopool.org:9999/WORKERNAME/EMAIL
  -P stratum1+tcp://ETH_WALLET@eth-us-west1.nanopool.org:9999/WORKERNAME/EMAIL
  ```

  Without email:
  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-asia1.nanopool.org:9999
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-eu1.nanopool.org:9999
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-eu2.nanopool.org:9999
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-us-east1.nanopool.org:9999
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eth-us-west1.nanopool.org:9999
  ```


### nicehash.com

  ```
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.br.nicehash.com:3353
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.eu.nicehash.com:3353
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.hk.nicehash.com:3353
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.in.nicehash.com:3353
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.jp.nicehash.com:3353
  -P stratum2+tcp://BTC_WALLET.WORKERNAME@daggerhashimoto.usa.nicehash.com:3353
  ```


### sparkpool.com

  ```
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@cn.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@eu.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@jp.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@kr.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@na-west.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@na-east.sparkpool.com:3333
  -P stratum1+tcp://ETH_WALLET.WORKERNAME@tw.sparkpool.com:3333
  ```
