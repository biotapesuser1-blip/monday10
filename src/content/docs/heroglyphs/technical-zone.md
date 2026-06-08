---
title: Technical Zone | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)

## Technical Zone

Ethereum 2.0 consists of EPOCHs, SLOTs, and BLOCKs. An epoch contains 32 slots, and each slot contains 1 block.

It is important to note that not every slot is proposed, so the ratio between blocks and epoch-slots is not consistent. Once a slot has been proposed, it contains multiple pieces of data.

See an example from the Beacon chain below. The Heroglyph protocol utilizes the block graffiti\_text to verify whether the text is a Heroglyph recognized Graffiti.

```
"data": {
    "attestationscount": 128,
    "attesterslashingscount": 0,
    "blockroot": "...",
    "depositscount": 0,
    "epoch": 280373,
    "eth1data_blockhash": "...",
    "eth1data_depositcount": 1460883,
    "eth1data_depositroot": "...",
    "exec_base_fee_per_gas": 20662807983,
    "exec_block_hash": "...",
    "exec_block_number": 19768739,
    "exec_extra_data": "...",
    "exec_fee_recipient": "...",
    "exec_gas_limit": 30000000,
    "exec_gas_used": 11704811,
    "exec_logs_bloom": "...",
    "exec_parent_hash": "...",
    "exec_random": "...",
    "exec_receipts_root": "...",
    "exec_state_root": "...",
    "exec_timestamp": 1714487519,
    "exec_transactions_count": 145,
    "graffiti": "...",
    "graffiti_text": "Lighthouse/v5.1.3-3058b96",
    "parentroot": "...",
    "proposer": 965785,
    "proposerslashingscount": 0,
    "randaoreveal": "...",
    "signature": "...",
    "slot": 8971958,
    "stateroot": "...",
    "status": "1",
    "syncaggregate_bits": "...",
    "syncaggregate_participation": 0.9921875,
    "syncaggregate_signature": "...",
    "voluntaryexitscount": 0,
    "votes": 31448,
    "withdrawalcount": 16
  }
```

* * *

Heroglyph Protocol is offering the power to utilize the graffiti feature of a validator. It contains four modules:

A graffiti needs an identity (`@<IdentityName>`) so the block producer can be rewarded. Heroglyph doesn't use the `Fee Recipient` of the produced block.

Tickers allow developers to build on top of Heroglyph. All your contract needs is to inherit the function `ITickerOperation::onValidatorTriggered`. Then, you connect your contract to your ticker and voila, you are hooked into the Heroglyph Protocol. The only thing missing is a validator using your ticker in their graffiti `#<TICKER_NAME>`.

Heroglyph Relay is the one receiving the graffiti metadata and executes its logic. It will receive an array of

```
struct GraffitiData {
	string validatorName;
	string[] tickers;
	uint32[] lzEndpointTargets;
	uint32 mintedBlock;
	uint32 slotNumber; 
	string graffitiText;
	uint32 validatorUUID
}
```

then:

-   via Validator Identity, it fetches the address of the validator,
    
-   via Tickers, it fetches the contract to call `onValidatorTriggered` on.
    

Heroglyph Node is a decentralized Web3 function running a task every 2 minutes. It fetches every block in an epoch, filters out the blocks with invalid graffiti, and then computes the graffiti into the `GraffitiData struct` to finally call the Heroglyph Relay.
