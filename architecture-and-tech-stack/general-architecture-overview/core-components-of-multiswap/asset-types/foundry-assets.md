# ⚒ Foundry Assets

Assets that have [single pair liquidity](../../core-components-of-bridging/bridge-pool/liquidity-management/liquidity-setup.md) added to the `bridgePool` are categorized as Foundry Assets. This liquidity can be added by Ferrum or the Token Administrators of listed tokens.&#x20;

A major benefit of Foundry Assets is that swaps involving Foundry Assets typically skip interaction with an aggregator (1inch) or DEX (UniSwap). Instead, [FIBER](../fiber-ferrum-inter-blockchain-express-routing-engine.md) will prepare a path for Foundry assets to interact directly with the `bridgePool`. Saving liquidity provider fees for the part of the cross-chain swap that involves the Foundry Asset.
