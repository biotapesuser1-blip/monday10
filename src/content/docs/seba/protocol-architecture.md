---
title: Protocol Architecture | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## Protocol Architecture

Seba integrates smart contracts and backend services to manage validator participation, monitor performance, and allocate perpetual yields.

The SebaPool contract serves as the entry point, managing validator registration, tracking graduation, and collecting rewards. Validators join by setting their fee address to the SebaPool contract, directing their execution and MEV rewards into the system.

Collected rewards are split:

-   Half are locked in the Yield Vault as principal to generate perpetual yield
    
-   The rest are converted into sBOLD and sent to the pybSeba Vault for distribution
    

> BOLD is the decentralized, over-collateralized stablecoin issued through the immutable smart contracts of the **Liquity v2** protocol. **sBOLD** is a staked, yield-bearing token, representing deposits that continuously accrue yield from underlying collateral. It allows users to keep their capital productive while maintaining full onchain liquidity, composability, and trustless access across DeFi. **sBOLD:** [0x50Bd66D59911F5e086Ec87aE43C811e0D059DD11](https://etherscan.io/token/0x50Bd66D59911F5e086Ec87aE43C811e0D059DD11)

The current SebaPool contract is: [0xe3B17b4533b339d3CBC26F57199d3fb937129894](https://etherscan.io/address/0xe3b17b4533b339d3cbc26f57199d3fb937129894)

### 

How Is Everything Tracked?

A backend service executes every five epochs to update validator statistics, save them to AWS S3, and retrieve data from Alchemy, Beaconchain, and Seba’s Subgraph. Blockchain transactions are secured through wallets managed in AWS Secrets Manager.

### 

How do you check for Stakers Union validators?

We verify Stakers Union NFT ownership on both Ethereum and Gnosis chains.

Yield strategy decisions start under multisig control and will move to DAO governance, with a target of 10% APY on locked principal.

Last updated 7 months ago
