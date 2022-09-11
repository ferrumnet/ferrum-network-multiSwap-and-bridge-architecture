# ⚡ FIBER - Ferrum Inter Blockchain Express Routing Engine

At a high level, FIBER is responsible for finding the optimal path to conduct swaps across chains. Depending on the asset type. If the asset has liquidity in the `bridgePool` these assets are classified as Foundry Assets. All foundry assets benefit from reduced fees during a swap across chains as one less swap needs to be conducted on the source or destination chain.&#x20;

FIBER looks at the request from the user and assess the following criteria:

1. Source Chain
2. Source Asset
3. Destination Chain
4. Destination Asset

After reviewing these parameters, FIBER determines the categorization of the assets involved.&#x20;

1. [Foundry Assets](asset-types/foundry-assets.md)
2. [Refinery Assets](asset-types/refinery-assets.md)
3. [Ionic Assets](asset-types/ionic-assets.md)

The categorization of assets defines the available paths to swap and bridge assets across chains. Foundry Assets will typically skip interaction with an aggregator (1inch) or DEX (UniSwap). Instead, FIBER will prepare a path for Foundry assets to interact directly with the `bridgePool`. Saving liquidity provider fees for the part of the cross-chain swap that involves the Foundry asset.

In each case, FIBER not only determines the optimal path between `bridgePool` vs DEX swaps, but also queries multiple ecosystem aggregators, and DEXs to determine the best possible rate for the swap and bridging of assets across chains.
