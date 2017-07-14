# AriseCoin (ACO) ERC20-Explorer
### Lightweight explorer for the AriseCoin Ethereum (ERC20) Token

ACO explorer is an explorer based on the original ERC20-Explorer built with NodeJS, Express and Parity. It does not require an external database and retrieves all information on the fly from a backend Ethereum node. You must install either Geth or Parity of it to work.

A demo instance connected to the AriseCoin Token is available at [aco.arisebank.com](http://aco.arisebank.com).

## Current Features
* Browse AriseCoin transactions and accounts
* AriseCoin Named accounts
* AriseCoin event log browser
* Supports Transfer and Approval events
* Live Backend Geth/Parity Node status display
* Support for all [Bootswatch](https://bootswatch.com/) skins
* Accounts enumeration
* Supports IPC and HTTP backend connections
* Responsive layout

Missing a feature? Please request it by creating a new [Issue](https://github.com/arisebank/aco-erc20-explorer/issues).

## Getting started

Supported OS: Ubuntu 16.04 (Not recommended, but tested in production)

Supported Ethereum backend nodes: Parity, Geth (tested)

1. Setup a nodejs & npm environment
2. Install the latest version of the Parity Ethereum client
3. Start parity using the following options: `parity --warp`
4. Clone this repository to your local machine: `git clone https://github.com/gobitfly/erc20-exporter`
5. Install all dependencies: `npm install`
6. Rename `config.js.example` into `config.js` and adjust the file to your local environment & token
7. Start the explorer: `npm start`
8. Browse to `http://localhost:3000`

Please note that pre-ICO the initial data export will take seconds. After the ICO, it could take up to 10 hours. Once completed it is recommended to change the exportStartBlock parameter in the config file to a block number that is around 30.000 blocks behind the current tip of the chain and restart the exporter.
