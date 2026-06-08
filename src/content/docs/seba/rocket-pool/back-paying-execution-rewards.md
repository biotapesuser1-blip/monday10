---
title: Back-Paying Execution Rewards | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)
2.  [Rocket Pool](https://docs.heroglyphs.com/seba/rocket-pool)

## Back-Paying Execution Rewards

### 

Back-Paying Execution Rewards

RP validators must back-pay part of their execution rewards to Seba (doable within the Seba app). We created a dedicated contract to allow RP validators to do so:

**Contract:** ([0xDF...E9E5](https://etherscan.io/address/0xDF5fff71608095e6eD34e582C1B7eBD0c5A9E9E5))

Any RP validator registered on Seba which receives execution rewards must back-pay the appropriate share within 3375 epochs (~15 days).

**Required payment amounts:**

-   **8 ETH minipool:** pays 25% of received execution rewards
    
-   **16 ETH minipool:** pays 50%
    

Whenever a user has already signed up any Rocket Pool validators, these would appear together with a RP Tooltip under their personal validator stats when the related wallet is connected. Upon hovering on this tooltip, the user is able to see different types of information such as:

-   The RP Minipool worth (8 or 16 ETH)
    
-   How much have they paid in total Back-Pay towards that validator
    

If the validator requires a payment:

-   The amount to be paid and the exact amount of time available to back-pay before there is a penalty are available as well.
    
-   A button saying 'Edit Payback' will show up within the tooltip which, when clicked, copies that pay back amount and validator ID into the input fields located under this section.
    

Wether the values are entered manually or added into the 'Edit Payback' section via the use of the button mentioned above, in this section the user can write down exactly how much they would like to pay towards a certain validator ID and add it to their cart.

Once it has been added to the cart which will show up below, the user can choose to add more validators, edit the pay back amount of a certain ID or remove it from the cart entirely. Take a look at the total and proceed to do the transaction.

![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252FMXcrXjsfxBjZhyxESGnn%252Fimage.png%3Falt%3Dmedia%26token%3D03488a06-f2c8-4fe3-9733-eca36d8234ee&width=768&dpr=3&quality=100&sign=585a7e42&sv=2)

This is the whole Payback section within the Seba app

If the required back-pay is not completed within 3375 epochs (~15 days):

-   The validator’s attestation points are reset to zero
    
-   Their graduation period resets to zero
    

-   Validators *may* back-pay Seba early to avoid timing issues.
    
-   Payments do not need to come from the RP node address—any wallet may pay on their behalf.
    

Last updated 5 months ago
