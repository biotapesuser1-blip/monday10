---
title: Rocket Pool | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## Rocket Pool

Seba now supports Rocket Pool (RP) validators, allowing RP node operators to register their **Minipools** directly in Seba!

Minipools are Rocket Pool's version of a validator where the node operator does ***not*** need to contribute the full 32 ETH stake normally required to have a validator. Instead, users are able to stake a partial amount (either 8 ETH or 16 ETH), and the remaining ETH is provided by Rocket Pool users through the purchase of their **rETH** liquid staking token.

Rocket Pool supports two types of Minipools:

### 

How Minipools Work in Seba

RP validators registered in Seba earn attestation points **proportional** **to their personal stake**:

-   8 ETH Minipool: earns 25% of a normal validator’s attestation points
    
    *(32 /* *8 = ¼ = 25%)*
    
-   16 ETH Minipool: earns 50% of normal attestation points (*32 / 16 = ½ = 50%)*
    

Thinking about how Rocket Pool works, even though the Node Operator only Stakes 8 or 16 ETH within Rocket Pool, **the full 32 ETH validator weight still counts towards Seba's TVL.**

Normal validator within the Seba app must points their fee recipient to the Seba contract address. Rocket Pool validators cannot do this unless they opt into specific RP punishment modes which of course is not optimal. This led to the creation of a dedicated '**Back-Paying**' contract to handle this situation ([0xDF...E9E5](https://etherscan.io/address/0xDF5fff71608095e6eD34e582C1B7eBD0c5A9E9E5)).

Last updated 5 months ago
