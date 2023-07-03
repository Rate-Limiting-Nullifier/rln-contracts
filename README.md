<h1 align=center>Foundry project for Rate-Limit Nullifier contract</h1>

<p align="center">
    <img src="https://github.com/Rate-Limiting-Nullifier/rln-contracts/workflows/Tests/badge.svg" width="140">
</p>

## How to use

### Install Foundry framework:
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### Build:
```bash
forge build
```

### Test:
```bash
forge test
```

### Deploy:

You can change values (env variables) used for 
the contract initialization in `.env` file.

To deploy to Goerli:
```bash
source .env
forge script script/RLN.s.sol:RLNScript --rpc-url $GOERLI_RPC_URL --broadcast --etherscan-api-key <YOUR-API-KEY> --verifier-url https://api-goerli.etherscan.io//api --verify -vvvv --private-key <YOUR-PRIVATE-KEY>
```

This will also verify contracts on Etherscan.

---

## What's RLN?

RLN is a zero-knowledge gadget that enables spam 
prevention in anonymous environments.

The core parts of RLN are:
* [zk-circuits in Circom](https://github.com/Rate-Limiting-Nullifier/circom-rln);
* registry smart-contract (this repo);
* set of libraries to build app with RLN ([rlnjs](https://github.com/Rate-Limiting-Nullifier/rlnjs), [zerokit](https://github.com/vacp2p/zerokit)).

---

To learn more on RLN and how it works - check out [documentation](https://rate-limiting-nullifier.github.io/rln-docs/).
