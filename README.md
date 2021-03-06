# THORChain

[![CircleCI](https://circleci.com/gh/thorchain/THORChain.svg?style=shield&circle-token=7bb2510a13b7e60483d2d86e09326a88f6c6fd63)](https://circleci.com/gh/thorchain/THORChain)
[![Maintainability](https://api.codeclimate.com/v1/badges/d44fc3f4756ca05a312c/maintainability)](https://codeclimate.com/github/thorchain/THORChain/maintainability)

THORChain is a lightning fast decentralised exchange protocol with cross-chain bridges and support for a layer 2 payment network. Read the whitepaper here: [THORChain Whitepaper](https://github.com/thorchain/Resources/blob/master/Whitepapers/THORChain/whitepaper-en.md)

This project is based on work done for the [Cosmos Project](https://github.com/cosmos/cosmos-sdk) by the Cosmos/Tendermint team.

Codeclimate: https://codeclimate.com/github/thorchain/THORChain

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them:

* Install Go (Version 1.11) and set GOPATH: [https://golang.org/doc/install](https://golang.org/doc/install)

### Installing

A step by step series of examples that tell you how to get a development env running

Thorchain can be installed to `$GOPATH/src/github.com/thorchain/THORChain` like a normal Go program:

```sh
go get github.com/thorchain/THORChain
```

Then install dependencies:

```sh
cd $GOPATH/src/github.com/thorchain/THORChain
dep ensure -update github.com/brejski/hid
make get_tools
make get_vendor_deps
make install
```

(`dep ensure` above is a workaround until https://github.com/cosmos/cosmos-sdk/issues/2253 is fixed.)

Verify that everything worked by running:

```sh
thorchaind version
```

and:

```sh
thorchaincli version
```

## Running the tests

```sh
make test
```

### Break down into end to end tests

```sh
make test_cli
```

### And coding style tests

```sh
make test_lint
```

## Deployment

```sh
make build-linux
```

## Built With

## Contributing

Please read [CONTRIBUTING.md](https://github.com/thorchain/Resources/blob/master/contributing.md) for details on code standards and the process for submitting pull requests to the project.

## Versioning

Update `version/version.go` before building.

## Authors

**thorchaindevs** *Initial Commit* [thorchainadmin](https://github.com/thorchainadmin)

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/thorchain/THORChain/blob/master/LICENSE.md) file for details

## Acknowledgments

Thanks to the [Interchain Foundation (ICF)](https://cosmos.network/) for [Cosmos SDK](https://github.com/cosmos/cosmos-sdk) and [Tendermint, Inc](https://tendermint.com/) for [Tendermint](https://github.com/tendermint/tendermint).
