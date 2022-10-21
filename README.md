# Ledger Staderlabs BNBx Plugin

This is a plugin for the Ethereum application which helps parsing and displaying relevant information when signing a Staderlabs BNBx transaction.

## Prerequisite

Clone the plugin to a new folder.

```shell
git clone https://github.com/stader-labs/app-plugin-staderlabs-bnbx.git
```

Then in the same folder clone two more repositories, which is the plugin-tools and app-ethereum.

```shell
git clone https://github.com/LedgerHQ/plugin-tools.git                          #plugin-tools
git clone --recurse-submodules https://github.com/LedgerHQ/app-ethereum.git     #app-ethereum
```

## Documentation

Need more information about the interface, the architecture, or general stuff about ethereum plugins? You can find more about them in the [ethereum-app documentation](https://github.com/LedgerHQ/app-ethereum/blob/master/doc/ethapp_plugins.asc).

## Smart Contracts

Smart contracts covered by this plugin are:

| Network | Contract Name | Smart Contract                               |
| ------- | ------------- | -------------------------------------------- |
| BSC     | StakeManager  | `0x7276241a669489E4BBB76f63d2A43Bfe63080F2F` |

## Build

Go to the plugin-tools folder and run the "./start" script.

```shell
cd plugin-tools  # go to plugin folder
./start.sh       # run the script start.sh
```

The script will build a docker image and attach a console.
When the docker image is running go to the "app-plugin-bnbx" folder and build the ".elf" files.

```shell
cd app-plugin-bnbx/tests             # go to the tests folder in app-plugin-bnbx
./build_local_test_elfs.sh           # run the script build_local_test_elfs.sh
```

## Tests

To test the plugin go to the tests folder from the "app-plugin-bnbx" and run the script "test"

```shell
cd app-plugin-bnbx/tests             # go to the tests folder in app-plugin-bnbx
yarn test                            # run the script test
```
