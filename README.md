## Description

This project contains sample web applications using the [monero-ts](https://github.com/woodser/monero-ts) library.

## How to Run in a Browser
1. Download and install [Monero CLI](https://getmonero.org/downloads/)
2. Start monero-daemon-rpc with authentication and CORS access.  For example: `./monerod --stagenet --rpc-login superuser:abctesting123 --rpc-access-control-origins http://localhost:9100`
3. Start monero-wallet-rpc with authentication and CORS access.  For example: `./monero-wallet-rpc --daemon-address http://localhost:38081 --daemon-login superuser:abctesting123 --stagenet --rpc-bind-port 38083 --rpc-login rpc_user:abc123 --rpc-access-control-origins http://localhost:9100 --wallet-dir ./`
4. `git clone https://github.com/woodser/xmr-sample-app`
5. `cd xmr-sample-app`
6. `npm install`
7. If using Node.js >16, set OpenSSL legacy provider:
    - Unix: `export NODE_OPTIONS=--openssl-legacy-provider`
    - Windows: `set NODE_OPTIONS=--openssl-legacy-provider`
8. `./bin/build_browser_app.sh`
9. Access web app at http://localhost:9100