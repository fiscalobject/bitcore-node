UFOcore Node
============

A UFO full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to [UFO Core with additional indexing](https://github.com/fiscalobject/ufo/tree/ufocore-0.13) for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Install

```bash
git clone https://github.com/fiscalobject/ufocore-node.git
cd ufocore-node
npm install
./bin/ufocore-node start
```

Note: For your convenience, we distribute ufod binaries for x86_64 Linux. Upon npm install, the binaries for your platform will be downloaded into the bin directory. For more detailed installation instructions, or if you want to compile the project yourself, then please see the Bitcore branch of [UFO Core with additional indexing](https://github.com/fiscalobject/ufo/tree/ufocore-0.13).

## Prerequisites

- GNU/Linux x86_32/x86_64, or OSX 64bit *(for bitcoind distributed binaries)*
- Node.js v0.10, v0.12 or v4
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~200GB of disk storage
- ~8GB of RAM

## Configuration

UFOcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your UFOcore Node.

```bash
./bin/ufocore-node create mynode
cd mynode
../bin/ufocore-node install <service>
../bin/ufocore-node install https://github.com/yourname/helloworld
```

This will create a directory with configuration files for your node and install the necessary dependencies. For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/bitpay/insight-api)
- [Insight UI](https://github.com/bitpay/insight-ui)
- [Bitcore Wallet Service](https://github.com/bitpay/bitcore-wallet-service)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node/blob/master/LICENSE).

Copyright 2018 UFO Core Developers

- bitcore: Copyright (c) 2013-2015 BitPay, Inc. (MIT License)
- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
