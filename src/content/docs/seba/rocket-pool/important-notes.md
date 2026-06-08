---
title: Important Notes | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)
2.  [Rocket Pool](https://docs.heroglyphs.com/seba/rocket-pool)

## Important Notes

### 

Strong Recommendation About Smoothing Pool

RP validators who opt into Seba are strongly advised NOT to opt into the Rocket Pool Smoothing Pool and should instead receive execution rewards via the RP distribution contract.

This is not enforced but highly recommended for two reasons:

If a validator proposes a block with a large execution reward:

-   The smoothing pool spreads the reward across many participants
    
-   The validator loses direct access to the reward
    
-   But Seba still expects their share of back-pay
    

This may result in the validator needing to pay more than they actually receive.

#### 

2\. Smoothing Pool Withdrawal Delay

-   Smoothing pool rewards unlock every 28 days
    
-   Seba requires back-pay within 15 days
    

This means validators using the smoothing pool may be forced to pay upfront out of pocket.

It is strongly advised to use the RP Distributor Contract instead of the RP Smoothing pool for these reasons. Please keep this in mind!

Last updated 5 months ago
