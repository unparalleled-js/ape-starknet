# Ape StarkNet

Plugins for the [StarkNet Ethereum L2 networks](https://starkware.co/starknet/).

## Dependencies

* [python3](https://www.python.org/downloads) version 3.7 or greater, python3-dev

## Installation

### via `pip`

You can install the latest release via [`pip`](https://pypi.org/project/pip/):

```bash
pip install ape-starknet
```

### via `setuptools`

You can clone the repository and use [`setuptools`](https://github.com/pypa/setuptools) for the most up-to-date version:

```bash
git clone https://github.com/ApeWorX/ape-starknet.git
cd ape-starknet
python3 setup.py install
```

## Quick Usage

Deploy a new account:

```bash
ape starknet accounts create <ALIAS> --network starknet:testnet
```

You can deploy the same account to multiple networks.

```bash
ape starknet accounts create <ALIAS> --network starknet:mainnet
```

Now, when you look at this account, you will see it has multiple contract addresses:

```bash
ape starknet accounts list
```

shows:

```bash
Alias                      - <ALIAS>
Public key                 - 0x123444444d716666dd88882bE2e99991555DE1c7
Contract address (testnet) - 0x6b7111AA4111e5B2229c3332B66696888164440A773333143333B383333a183
Contract address (mainnet) - 0x7873113A4111e5B2229c3332B66696388163440A373333143333B3833332122
```

Import an existing account:

```bash
ape starknet accounts import <ALIAS> --address 0x6b7111AA4111e5B2229c3332B66696888164440A773333143333B383333a183 --network testnet
```

## Development

This project is in development and should be considered a beta.
Things might not be in their final state and breaking changes may occur.
Comments, questions, criticisms and pull requests are welcomed.

## License

This project is licensed under the [Apache 2.0](LICENSE).
