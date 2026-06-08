---
title: SebaPool | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## SebaPool

The Seba Pool functions as the coordination center for solo validators in the protocol. By pooling execution rewards, Seba can lock part as principal while distributing the rest as ongoing yield to graduates.

### 

Requirements to Participate

Once a validator chooses to join the pool, they are required to keep their fee address linked to the SebaPool contract throughout the entire graduation period. Any violation of this rule results in a reset of both the graduation timer and attestation points, ensuring that only validators who remain consistently aligned receive rewards.

Validators have the option to update their reward recipient address by registering it via the SebaPool contract using their withdrawal address. This offers operators greater flexibility in choosing how and where they receive their rewards. This can be done directly from the Seba front end.

The Seba Pool also offers reward boosts for validators who are part of aligned communities to receive a 2.5x reward boost:

-   Stakers Union members with the POAP in their reward address wallet (checked on Ethereum and Gnosis). Should owners chose to, they can bridge POAP's to Ethereum with the following [guide](https://poap.zendesk.com/hc/en-us/articles/9673605937549-How-Do-I-Migrate-My-POAP-To-Mainnet).
    
-   Kamisama NFT holders, provided the NFT remains in the reward address throughout participation.
    
-   100 Heroes NFT holders also qualify, but ownership must also be continuous (checked every epoch).
    
-   HeroSocks POAP holders also qualify for an extra 0.5x cumulative boost, making the total possible boost for a user 3.0x (2.5 + 0.5). Ownership must also be continuous (checked every epoch on Ethereum and Gnosis).
    

The system checks for continued ownership every epoch.

Seba provides an API for transparency, enabling users to access validator stats and block data. The validator stats endpoint allows querying multiple IDs at once, while the block endpoint offers pagination for efficient retrieval of historical data.

### 

Can you change the reward address?

Yes, you can set your reward address by connecting it with your withdrawal address and signing a transaction to update it.

Last updated 7 months ago
