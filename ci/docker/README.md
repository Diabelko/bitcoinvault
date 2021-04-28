BitcoinVault
============================

### ENV's

| name | default value | notes |
|------|-------|-------|
| `BVAULTD_RPC_PASSWORD` | `xxxx` | RPC password for bvaultd 
| `BVAULTD_RPC_USER` | `root` | RPC username for bvaultd 
| `BVAULTD_RPC_ALLOW_IP_FIRST` | `127.0.0.0/24` | `rpcallowip` parameter first iteration 
| `BVAULTD_RPC_ALLOW_IP_SECOND` | `10.0.0.0/8` | `rpcallowip` parameter second iteration 
| `BVAULTD_NET_BAN_SCORE` | `100000` | `banscore` parameter, to disable, set to empty string 
| `BVAULTD_NET_BAN_TIME` | `60` | `bantime` parameter, to disable, set to empty string 
| `BVAULTD_TESTNET_ENABLED` | undefined | Allowed: `1`, so set if you want to run in testnet
| `BVAULTD_REGTEST_ENABLED` | undefined | Allowed: `1`, set if you want to run Regtest
| `BVAULTD_SERVER` | `1` | Allowed: `1` `server` parameter
| `BVAULTD_TXINDEX` | undefined | Allowed: `1` `txindex` parameter
| `BVAULTD_ZMQ_ENABLED` | `1` | Set other than `1` to disable ZMQ
| `BVAULTD_ZMQ_LISTEN_HOST` | `0.0.0.0` | Address to bind ZMQ
| `BVAULTD_ZMQ_LISTEN_PORT` | `8331` | ZMQ listen port


For more information how config is generated see template: `templates/bvaultd.conf.tmpl`


### Blockchain volume

> Important 

Blockchain data is stored in volume defined for path `/bitcoinvault/blockchain`. So when you run this image, make sur to bind proper volume 
Depending on `BVAULTD_NET` env
