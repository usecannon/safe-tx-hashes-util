# Safe Transaction Hashes Calculator

## Overview

The _Safe Transaction Hashes Calculator_ is a Bash [script](./safe_tx_hashes_calculator.sh) designed to compute and display various hashes associated with Safe (formerly Gnosis Safe) multi-signature wallet transactions. This tool is particularly useful for developers and users working with Safe wallets who need to verify transaction hashes or understand the components that go into creating a Safe transaction.

## Features

- Supports multiple networks (Ethereum, Arbitrum, Polygon, etc.)
- Fetches transaction data from the Safe Transaction Service API
- Calculates and displays:
  - Domain Hash
  - Message Hash
  - Safe Transaction Hash

## Prerequisites

- Bash shell
- `curl` for making API requests
- `jq` for parsing JSON responses
- `chisel` and `cast` from the [Foundry](https://book.getfoundry.sh/) toolkit

## Installation

1. Clone this repository or download the `safe_tx_hashes_calculator.sh` script.
2. Make the script executable:
   ```console
   chmod +x safe_tx_hash_calculator.sh
   ```

## Usage

Run the script with the following command:

```console
./safe_tx_hashes_calculator.sh --network <network> --address <safe_address> --nonce <transaction_nonce>
```

### Parameters

- `--network`: The network where the Safe is deployed (e.g., ethereum, arbitrum, polygon)
- `--address`: The address of the Safe
- `--nonce`: The nonce of the transaction

### Example

```console
./safe_tx_hashes_calculator.sh --network arbitrum --address 0x111CEEee040739fD91D29C34C33E6B3E112F2177 --nonce 234
```

### Output

The script will output:

- Chain ID
- Domain Hash
- Message Hash
- Safe Transaction Hash

All hashes are displayed with the `0x` prefix in lowercase and the rest of the hash in uppercase.

## Supported Networks

- Arbitrum
- Aurora
- Avalanche
- Base
- Base Sepolia
- BSC (Binance Smart Chain)
- Celo
- Ethereum
- Gnosis Chain
- Linea
- Optimism
- Polygon
- Polygon zkEVM
- Scroll
- Sepolia
- xLayer
- zkSync

## Error Handling

The script includes error handling for:

- Missing or invalid parameters
- Network connection issues
- API response parsing errors

If you encounter any issues, make sure your input parameters are correct and you have an active internet connection.

## Security Considerations

TBD
