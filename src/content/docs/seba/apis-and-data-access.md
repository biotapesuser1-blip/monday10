---
title: APIs & Data Access | Heroglyphs Protocol
---

1.  [Seba](https://docs.heroglyphs.com/seba)

## APIs & Data Access

Seba offers robust API endpoints for developers and participants to query validator and protocol data.

Allows batch retrieval of performance data for multiple validator IDs via a comma-separated query parameter.

**Example:**

[https://dp32uxbkno310.cloudfront.net/validator-stats/?validators=1062282,1062287,1062281​](https://dp32uxbkno310.cloudfront.net/validator-stats/?validators=1062282,1062287,1062281%E2%80%8B)

The properties that can be retrieved are the following:

```

export interface TrackedValidator {
 id: number // Validator ID
 attestationPoints: bigint // Number of attestation points accrued
 rewardAddress: string // Validator withdrawal address
 startEpoch: number // Epoch on which the graduation period started
 lastProcessedEpoch: number, // Last processed epoch for this validator
 graduationEligibilityEpoch: number, // Epoch on which this validator will become eligible for graduation
 successfulProposals: number, // Total amount of succesful proposals since registration
 failedProposals: number, // Total amount of failed proposals since registration
 rewardsContributed: number, // Total amount of rewards contributed to Seba Pool
 graduated: boolean // Wether the validator has graduated
 effectiveBalance: number // Current effective balance
 lastProposedValidGraduationBlockEpoch: number
 /* Last epoch on which a graduation block was proposed for this validator (does not mean a graduation
 will happen automatically because validator needs to run trough complete graduation period as prerequisite) */
}
```

Returns blocks associated with SebaPool participation, with support for pagination. Example:

```
https://dp32uxbkno310.cloudfront.net/blocks/?p=0&size=10
```

The properties that can be retrieved are the following:

```
export interface BlockProposal {
    blockHash: string
    blockNumber: number
    timestamp: number
    blockReward: number
    blockMevReward: number
    producerReward: number
    feeRecipient: string
    gasLimit: number
    gasUsed: number
    baseFee: number
    txCount: number
    internalTxCount: number
    uncleCount: number
    parentHash: string
    uncleHash: string
    difficulty: number
    posConsensus: PosConsensus
    relay: Relay
    consensusAlgorithm: string
}
```

Last updated 8 months ago
