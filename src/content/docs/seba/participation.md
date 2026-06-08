---
title: Participation | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## Participation

### 

How does the Participation Workflow?

The process starts when a solo validator registers their validator ID in the SebaPool contract and updates the validator’s fee address to point to this contract. This action immediately begins the graduation period, which is currently set to six months (measured in epochs).

-   During this period, the validator must correctly set the fee address and uphold strong attestation performance.
    

Participating in Seba is designed to be straightforward but relies on consistent validator performance and adherence to protocol rules. Failing to link the fee address to the Seba pool will reset the graduation period and attestation score to zero, requiring the validator to restart the entire process. The protocol enforces these rules strictly because they help maintain fairness among all participants and ensure yield sustainability.

The validator’s withdrawal address - or a registered reward address - receives pybSeba shares representing their perpetual yield entitlement.

### 

What Happens Once the Graduation Period ends?

After successfully completing the graduation period, the validator does not automatically receive their shares. Instead, they must be included in a valid Heroglyphs block proposal as a ticker associated with their validator ID, starting with the prefix 'seba'. Additionally, the **block reward of this block** should go to the Seba pool.

For example, if your validator ID is 888888 then the correct ticker to be used as part of the proposed block should be 'seba888888'

If you are the validator proposing the Heroglyphs block, use the following format in your validator's configuration to add one or multiple tickers to the proposed block graffiti field:

-   #YourValidatorID +,+ ticker1 +,+ ticker2 ...
    

Graffiti Example: #seba123456,seba999999,seba888888 (notice there are no spaces)

> **NOTE**: The graffiti in a valid Heroglyphs blocks must start with #, as shown in the example above.

On the client side of your validator, you should configure the fee address to the SebaPool contract: [0xe3...9894](https://etherscan.io/address/0xe3B17b4533b339d3CBC26F57199d3fb937129894)

Last updated 7 months ago
