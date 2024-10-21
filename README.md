# Safe Multisig Transaction Hashes

This Bash [script](./safe_hashes.sh) calculates the Safe transaction hashes by retrieving transaction details from the [Safe transaction service API](https://docs.safe.global/core-api/transaction-service-overview) and computing both the domain and message hashes using the [EIP-712](https://eips.ethereum.org/EIPS/eip-712) standard.

## Supported Networks

- Arbitrum (identifier: `arbitrum`, chain ID: `42161`)
- Aurora (identifier: `aurora`, chain ID: `1313161554`)
- Avalanche (identifier: `avalanche`, chain ID: `43114`)
- Base (identifier: `base`, chain ID: `8453`)
- Base Sepolia (identifier: `base-sepolia`, chain ID: `84532`)
- BSC (Binance Smart Chain) (identifier: `bsc`, chain ID: `56`)
- Celo (identifier: `celo`, chain ID: `42220`)
- Ethereum (identifier: `ethereum`, chain ID: `1`)
- Gnosis Chain (identifier: `gnosis`, chain ID: `100`)
- Linea (identifier: `linea`, chain ID: `59144`)
- Optimism (identifier: `optimism`, chain ID: `10`)
- Polygon (identifier: `polygon`, chain ID: `137`)
- Polygon zkEVM (identifier: `polygon-zkevm`, chain ID: `1101`)
- Scroll (identifier: `scroll`, chain ID: `534352`)
- Sepolia (identifier: `sepolia`, chain ID: `11155111`)
- X Layer (identifier: `xlayer`, chain ID: `195`)
- ZKsync Era (identifier: `zksync`, chain ID: `324`)

## Usage

> [!NOTE]
> Ensure that [`cast`](https://github.com/foundry-rs/foundry/tree/master/crates/cast) and [`chisel`](https://github.com/foundry-rs/foundry/tree/master/crates/chisel) are installed locally. For installation instructions, refer to this [guide](https://book.getfoundry.sh/getting-started/installation).

```console
./safe_hashes.sh [--help] [--list-networks] --network <network> --address <address> --nonce <nonce>
```

**Options:**

- `--help`: Display this help message.
- `--list-networks`: List all supported networks and their chain IDs.
- `--network <network>`: Specify the network (e.g., `ethereum`, `polygon`).
- `--address <address>`: Specify the Safe multisig address.
- `--nonce <nonce>`: Specify the transaction nonce.

Before you invoke the script, make it executable:

```console
chmod +x safe_hashes.sh
```

## Example

```console
./safe_hashes.sh --network arbitrum --address 0x111CEEee040739fD91D29C34C33E6B3E112F2177 --nonce 234
```

To list all supported networks:

```console
./safe_hashes.sh --list-networks
```

## Trust Assumptions

1. You trust my script 😃.
2. You trust Linux.
3. You trust [Foundry](https://github.com/foundry-rs/foundry/tree/master/crates/cast).
4. You trust the [Safe transaction service API](https://docs.safe.global/core-api/transaction-service-overview).
5. You trust[Ledger's secure screen](https://www.ledger.com/academy/topics/ledgersolutions/ledger-wallets-secure-screen-security-model).
