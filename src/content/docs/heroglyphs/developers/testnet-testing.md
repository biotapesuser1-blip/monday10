---
title: Testnet Testing | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)
2.  [Developers](https://docs.heroglyphs.com/heroglyphs/developers)

## Testnet Testing

Call `HeroglyphRelay.executeRelay`. We removed the security on the testnet

```
function executeRelay(GraffitiData[] calldata _graffities) external 
    returns (uint256 totalOfExecutions_);
```

Where GraffitiData is

```
    struct GraffitiData {
        string validatorName; // validator identity name
        string[] tickers; // tickers in the graffiti, can be empty
        uint32[] lzEndpointTargets; //lzEndpointTargets for each tickers
        uint32 mintedBlock; // block minted
        uint32 slotNumber; // Slot of the block
        string graffitiText; // Graffiti Text -- Only for F-E
        uint32 validatorId; // Validator Id -- Much match the Graffiti ID's validator
    }
```

If for some reason you want to use badges, you can mint them with

> HeroglyphAttestation.faucet(address \_to)

## 

Deployed Contracts - Sepolia

```
0xaC5907c4B4B8d34523a02e6421bB84992C058400
```

```
0x48bCDb36e473a901527E21eC56bAe930d28C2D4d
```

```
0xdD1c1afA241663C6c3Bdb54C5112F0900eFFd52e
```

```
0x1bAE16B284df79e8562d1bdD9538B2e93a6c40Fc
```

```
0xd837D9810a1dC2C45107B3F5C04261C974D2C001
```
