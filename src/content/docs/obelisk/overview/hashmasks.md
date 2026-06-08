---
title: Hashmasks | Heroglyphs Protocol
---

1.  [Obelisk](https://docs.heroglyphs.com/obelisk)
2.  [Overview](https://docs.heroglyphs.com/obelisk/overview)

## Hashmasks

Please, read the [Overview](https://docs.heroglyphs.com/obelisk/overview) before proceeding.

**Important:** Once your Hashmask is linked, do not change its name or transfer it **BEFORE** claiming your rewards. Failing to do so might result in the loss of your rewards.

-   If you have already transferred your Hashmask, you may transfer it back **only** if no new linking has occurred.
    
-   If you have changed the name, change it back to what it was before **only** if the `updateName`function hasn't been called.
    

**Hashmasks** is the only collection directly integrated with Obelisk.

As a Hashmask user, you do not need to:

Your experience as a Hashmask user will differ slightly. Instead of renaming an Obelisk NFT, you’ll **link***(0.1 ETH)* your Hashmask to Obelisk as **Proof of Ownership**. After linking, you will rename your Hashmask directly using a different syntax.

To optimize the number of transactions, it is recommended to rename your Hashmask **before** linking. This will allow you to skip the "UpdateName" step.

You do not need an NFT Pass, so there is no `(@<NFT_PASS_NAME>)`. For tickers, instead of using `#`, use a capital "O", and separate them with spaces instead of commas. For example, based on the [Obelisk NFT](https://docs.heroglyphs.com/obelisk/overview#obelisk-nft), your Hashmask would look like this: `<UNIQUE_TEXT> OSenusret OSANC OKBSU`

The name of your Hashmask **MUST BE UNIQUE**, no two Hashmasks can have the same name. By using the **prefix** field, you can add your ID or an extra character to make it different than any other Hashmask.

Once your name has been changed, make sure to update it on the Obelisk side through our website.

If you transfer your Hashmask, a new Proof of Ownership must be established. Instead of paying 0.1 ETH again, you can transfer your link to the new holder. However, the new holder must have the Hashmask NFT in their wallet before calling this function; otherwise, the transaction will revert.
