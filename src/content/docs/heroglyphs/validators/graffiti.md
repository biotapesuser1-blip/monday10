---
title: Graffiti | Heroglyphs Protocol
---

1.  [Heroglyphs](https://docs.heroglyphs.com/)
2.  [Validators](https://docs.heroglyphs.com/heroglyphs/validators)

## Graffiti

Heroglyph Graffiti is constructed with the following format:

-   `#` precedes the tickers' names, separated by commas.
    
-   `@` precedes the Graffiti Id's name.
    
-   `-` precedes the global chain to execute all tickers on.
    

If `-` is missing, the default chain will automatically be used as global. If `#` or `@` are missing, the graffiti is invalid and won't be executed by Heroglyphs.

**Note:** You will have to pay the LayerZero fee on the target chain if you are not minting on Arbitrum.

Example of a valid graffiti: `#lueygi,69@atum-a` `#lueygi,69@atum` `#@atum`

Examples of invalid graffiti: `@atum-a` `#lueygi-a` `#lueygi@-a` `lueygi@atum`

You can override a specific ticker's execution chain by adding it after the ticker name: `#TickerNameA:OverriddenChain,TickerNameB@0xAtum`

For example: `#lueygi:h,69@atum` In this example, `lueygi` will be minted on **Base**, and `69` on **Arbitrum**.

### 

Cross-chain fee & claiming

When minting from another chain, you'll need to pay the layer-zero fee on the target chain, requiring extra steps.

For simplification, let's consider minting `lueygi` on `base`:

3.  Execute `lueygi.claimAction(srcChainLzEndpoint, [0])`.
    
    1.  `[0]` is the id of the minting, for simplification, we will say this is our first time doing so
        
    

You'll pay the layer-zero fee with WETH and receive your token on the base chain

## 

Cross-chain graffiti's code

```
enum EGraffitiChains {
  ARBITRUM = "a",
  ETHEREUM = "b",
  BNB_CHAIN = "c",
  AVALANCHE = "d",
  POLYGON = "e",
  OPTIMISM = "f",
  FANTOM = "g",
  DFK = "h",
  HARMONY = "i",
  DEXALOT_SUBNET = "j",
  CELO_MAINNET = "k",
  MOONBEAM = "l",
  FUSE_MAINNET = "m",
  GNOSIS = "n",
  DOS_CHAIN = "o",
  KLAYTN_MAINNET_CYPRESS = "p",
  METIS = "q",
  CORE_BLOCKCHAIN_MAINNET = "r",
  OKXCHAIN_MAINNET = "s",
  POLYGON_ZEVM = "t",
  CANTO = "u",
  ZKSYNC_ERA_MAINNET = "v",
  MOONRIVER = "w",
  TENET = "x",
  ARBITRUM_NOVA = "y",
  METER_MAINNET = "z",
  KAVA = "aa",
  MANTLE = "bb",
  HUBBLE = "cc",
  LINEA = "dd",
  BASE = "ee",
  ZORA = "ff",
  VICTION = "gg",
  LOOT = "hh",
  MERIT_CIRCLE = "ii",
  TELOS_EVM = "jj",
  OPBNB_MAINNET = "kk",
  ASTAR = "ll",
  AURORA_MAINNET = "mm",
  CONFLUX_ESPACE = "nn",
  ORDERLY_MAINNET = "oo",
  SCROLL = "pp",
  HORIZEN_EON_MAINNET = "qq",
  XPLA_MAINNET = "rr",
  MANTA = "ss",
  SHIMMER = "tt",
  INJECTIVE = "uu",
  RARIBLE = "vv",
  XAI = "ww",
  REAL = "xx",
  TILTYARD = "yy",
  BLAST = "zz",
  FRAXTAL = "aaa",
  ASTAR_ZEVM = "bbb",
  MODE = "ccc",
  MASA = "ddd",
  HOMEVERSE = "eee",
  MERLIN = "fff",
  DEGEN = "ggg",
  SKALE = "hhh",
  XLAYER = "iii",
  SANKO = "jjj",
  BOB = "kkk",
}
```
