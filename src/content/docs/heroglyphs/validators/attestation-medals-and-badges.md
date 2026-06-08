---
title: Attestation (Medals & Badges) | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)
2.  [Validators](https://docs.heroglyphs.com/heroglyphs/validators)

## Attestation (Medals & Badges)

Being a valid hieroglyphs validator has its advantages, such as being rewarded for validating a block. Since producing a block is challenging for most people, we reward you for fulfilling your duty as a validator.

## 

Supported Third Party Liquid Staking

Here is the supported list of Third-Party Validator Services. They have a different medal rate compared to solo stakers, with a Medal Rate of 100%.

-   **Rocket Pool**
    
    -   Medal Rate: Minipool Size / 32
        
    

Although all validators are counted, you'll need an Identity to claim (see [Identity](https://docs.heroglyphs.com/heroglyphs/validators/identity) for more).

Claiming does not use your identity's receiver wallet, by default, badges will be sent to the validator's withdrawal credential for security reasons. However, if you prefer to receive badges in another wallet, you can [Redirect Badges](https://docs.heroglyphs.com/heroglyphs/validators/attestation-medals-and-badges#redirect-badges) (Before Claiming)

There are two important points to remember about our snapshot epoch:

1.  It advances in increments of 100. For example, if the current epoch is 12501, the next snapshot will be at 12600.
    
2.  Your attesting epoch expires after 30 days if not claimed
    

**Blocks** don't need to be specific to hieroglyphs. All blocks are counted.

Medals serve as our point system for evaluating your validator:

-   Attesting a block: +1 point
    
-   Failing to attest a block: -1 point
    
-   Producing a block: 0 points
    

In the end, you can claim your Medals to automatically convert them into $Badges

Badges are SBT (Soul Bounded Token), you cannot transfer them once you received them

1 Medals is worth **0.000297 Badges**. At **1 Badges** you can redeem it for a Genesis Token, as long you have the Genesis Key.

Already claimed badges cannot be redirected

To redirect your badges to another wallet:

2.  `<g> Claim` -> `<w> Redirect $BADGES rewards`
    

You will see this panel

![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252F9DYJDXcCVUHN5whUuOiG%252Fimage.png%3Falt%3Dmedia%26token%3D09ee9d86-54e7-4702-bae0-768b64b32017&width=768&dpr=3&quality=100&sign=fd0dedf&sv=2)

-   **Redirect as Withdrawal Credentials**: You want to **execute** the transaction with your WC wallet
    
-   **Generate Permit Signature**: You don't want to execute with your WC, you can **sign** a transaction with your WC and **execute** on another wallet
    
-   **Redirect with Permit**: This option is to execute the "**Generate Permit Signature**". Any wallet can execute the permit.
    

Do not sign any message that you do not understand or that does not align with the following:

Before signing, verify the domain of the signature. If you cannot find it or if it does not match, decline it and contact Heroglyphs.

```
0xe1439f74cd5286bf28b08978703bed2068de4260
```

Raw Data[](#raw-data)

```
{
    "types": {
        "EIP712Domain": [
            {
                "name": "name",
                "type": "string"
            },
            {
                "name": "version",
                "type": "string"
            },
            {
                "name": "chainId",
                "type": "uint256"
            },
            {
                "name": "verifyingContract",
                "type": "address"
            }
        ],
        "Redirect": [
            {
                "name": "to",
                "type": "address"
            },
            {
                "name": "nonce",
                "type": "uint32"
            },
            {
                "name": "deadline",
                "type": "uint32"
            }
        ]
    },
    "primaryType": "Redirect",
    "domain": {
        "name": "HeroglyphAttestation",
        "version": "v1",
        "chainId": 42161,
        "verifyingContract": "0xe1439f74cd5286bf28b08978703bed2068de4260"
    },
    "message": {
        "to":,
        "nonce":,
        "deadline":
    }
}
```

1.  Click on "Verify Third-Party details"
    
2.  Be sure the address is the **Contract Requester**
    

![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252FOBPmrQiFkGgcNbSJ6zen%252Fimage.png%3Falt%3Dmedia%26token%3D42fc8df0-dbea-482b-b584-7d48fda725ef&width=768&dpr=3&quality=100&sign=fe5acb46&sv=2)

-   You can view the **View Raw >** and verify against the Raw Data above.
    
-   Otherwise, make sure the **Interact Contract** is the **Contract Requester**.
    

![](https://docs.heroglyphs.com/~gitbook/image?url=https%3A%2F%2F722457140-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLxn2xdkLrgALvYnuDTh7%252Fuploads%252FfEmj3JZTMFfpwqCP7AU1%252Fimage.png%3Falt%3Dmedia%26token%3D0bbea6a0-53f8-440d-8b74-c51425efd88e&width=768&dpr=3&quality=100&sign=6eec0fe4&sv=2)

the general idea is the same, try to find for a "raw data" or "Interact Contract". Then validate the information
