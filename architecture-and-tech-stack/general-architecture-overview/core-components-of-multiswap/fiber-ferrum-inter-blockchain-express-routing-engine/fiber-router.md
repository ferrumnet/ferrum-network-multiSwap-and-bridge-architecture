# 🔄 FIBER Router

FIBER Router is the single point of contact with the MultiSwap [Fund Manager](fund-manager.md) and is responsible for the movement of assets from user wallets to Dex Routers and/or to the Fund Manager and vice versa.&#x20;

Thanks to the FIBER Router, no wallet or smart contract directly interacts with the [Fund Manager](fund-manager.md) providing additional layers of separation for any attack vectors targeting the liquidity stored in the [Fund Manager](fund-manager.md).

### Requests from FIBER Engine

The FIBER Router receives requests from the [FIBER Engine](fiber-engine.md) and processes them according to the requirements of each given request. These can include swaps for [Foundry Assets](../asset-types/foundry-assets.md), [Refinery](../asset-types/refinery-assets.md) or [Ionic Assets](../asset-types/ionic-assets.md), or even liquidity-related events.

### Foundry Asset swap requests for FIBER Router

When the FIBER Router receives a [Foundry Asset](../asset-types/foundry-assets.md) swap request from the [FIBER Engine](fiber-engine.md) on the source network, it takes the requested [Foundry Asset](../asset-types/foundry-assets.md) tokens out of the user's wallet and deposits them in the [Fund Manager](fund-manager.md) while sending the Fees to the [Fee Manager](fee-manager.md) if this is a fee-enabled transaction.

### Refinery Asset or Ionic Asset swap requests for FIBER Router

When the FIBER Router receives a [Refinery Asset](../asset-types/refinery-assets.md) or [Ionic Asset](../asset-types/ionic-assets.md) swap request from the [FIBER Engine](fiber-engine.md) on the source network, it takes the requested [Refinery Asset](../asset-types/refinery-assets.md) or [Ionic Asset](../asset-types/ionic-assets.md) tokens out of the user's wallet, moves them to the FIBER Router, then initiates the relevant DEX or Aggregator swap of this [Refinery Asset](../asset-types/refinery-assets.md) or [Ionic Asset](../asset-types/ionic-assets.md) to a [Foundry Asset](../asset-types/foundry-assets.md). Once the swap is completed, the DEX or Aggregator router deposits the [Foundry Asset](../asset-types/foundry-assets.md) into the FIBER Router. The router then deposits these tokens into the [Fund Manager](fund-manager.md) while sending the Fees to the [Fee Manager](fee-manager.md) if this is a fee-enabled transaction.
