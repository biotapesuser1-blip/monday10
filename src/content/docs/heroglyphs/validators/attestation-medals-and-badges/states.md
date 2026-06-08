---
title: States | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)
2.  [Validators](https://docs.heroglyphs.com/heroglyphs/validators)
3.  [Attestation (Medals & Badges)](https://docs.heroglyphs.com/heroglyphs/validators/attestation-medals-and-badges)

## States

A batch enters the "Queued" state under one of two conditions:

-   There are 100 validators in the batch.
    
-   The batch has been open for 2 hours.
    

In the "Queued" state, the batch is prepared for execution. It can be initiated manually or automatically when someone attempts to join the batch. Our system also checks for queued batches hourly to start them.

When a batch is "Executing," it typically indicates a failure. Execution speed is expected to be under then seconds. If a batch remains in this state for four hours, it expires.

Manual intervention is required to retry the batch.

* * *
