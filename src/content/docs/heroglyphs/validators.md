---
title: Validators | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)

## Validators

-   Solo Validator | Full Validator: Have their own node, with 32 ETHs staked into it, and participate into Ethereum Network
    
-   Minipods: Uses third party services like Rocket Pool, to stake under 32 ETHs to participate into Ethereum Network
    

Any protocol that allows you to modify the node's graffiti are supported to execute produced block in Heroglyphs.

But not all of them are supported to receive attesting rewards (Medals). For more: [Attestation (Medals & Badges)](https://docs.heroglyphs.com/heroglyphs/validators/attestation-medals-and-badges)

This is "Getting Started" for Heroglyph Protocol, if you want to enter the Heroglyph Game, go to [How to play](https://docs.heroglyphs.com/heroglyphs/game/how-to-play)

3.  Save the graffiti into your node
    

Congratulations! You are now a valid hieroglyph validator!

[Attestation (Medals & Badges)](https://docs.heroglyphs.com/heroglyphs/validators/attestation-medals-and-badges)

Each validator needs an ID of its own.

If you do not want to do multi-graffiti, you can create a **Parent <> Child** relationship

![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252FkLHVO21EMLGm2cuLqPFZ%252Fimage.png%3Falt%3Dmedia%26token%3Dc3d0c9f1-a717-41f6-a481-9ef90634e362&width=768&dpr=3&quality=100&sign=e4b0b971&sv=2)

Parent <> Child Relationship

### 

Create the Parent <> Child Relation

1.  Find your id that you wish to be the "Parent". This is the one you will be using in the graffiti
    
2.  Link your other ids with (Add Child Identities) ![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252FITdQKlwApcawk8eMMyJ2%252Fimage.png%3Falt%3Dmedia%26token%3D3b07527b-f3d6-442d-9a69-2cc0a13579b2&width=300&dpr=3&quality=100&sign=41905232&sv=2)
    

## 

Why my block has been skipped

1.  **Bad** **Graffiti:** Graffiti needs to start with `#` and have an ID `@`
    
2.  **Identity Not found:** Your Identity is not attached to the validator index and / or the Child Identity is not linked to the parent.
    

## 

Why my Ticker has been ignored

1.  **Ticker Not Found:** Ticker doesn't exist
    
2.  **No Contract Found:** No contract attached to the ticker
    
3.  **Ticker Surrendered:** Ticker went underwater by the tax system and is now disabled
    
4.  **Ticker Reverted:** Ticker reverted during execution, the event `TickerReverted` is emitted when it does happen
    

You can test your graffiti via our website -> `<f> Graffiti Tool` -> `<w> Test Graffiti`

It will tell you if

-   Your Graffiti is well formated
    

-   If your Tickers are valid or Active.
