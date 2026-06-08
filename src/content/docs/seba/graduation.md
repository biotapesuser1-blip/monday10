---
title: Graduation | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## Graduation

Graduation is the key milestone for a validator in the Seba protocol. It signifies the shift from active participation to continuous reward collection.

A validator graduates after meeting two key conditions:

1.  Completing the entire graduation period without violating fee address requirements and with strong attestation performance.
    
2.  Include the validator ID as a ticker in a valid Heroglyphs block graffiti (e.g., #seba12345) after the validator's graduation period has ended and make sure the **execution reward of the block** goes to the Seba pool.
    

Graduation rewards come in the form of shares in the pybSeba Vault:

-   The number of shares is determined by the validator’s total attestation rewards during the period, multiplied by any applicable boost factor (up to 3.0x).
    
-   The calculation accounts for effective balance, meaning validators with more staked ETH earn proportionally more shares. However, missed attestations reduce the total, promoting optimal performance.
    

### 

Can a Validator ID Graduate multiple times?

Graduation occurs only once per validator ID. After graduating, a validator cannot gain more shares for that ID, but they can start a new validator and join again.

Last updated 7 months ago
