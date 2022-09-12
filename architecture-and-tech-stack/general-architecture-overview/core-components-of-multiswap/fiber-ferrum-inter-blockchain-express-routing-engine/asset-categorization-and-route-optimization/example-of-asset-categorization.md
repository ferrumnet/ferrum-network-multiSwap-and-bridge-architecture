# 📂 Example of Asset Categorization

Let's take [a typical FIBER call](../overview.md#typical-fiber-request) and add some example parameters to understand the flow of events.

{% hint style="info" %}
These are not actual FIBER call parameters. Some of these parameters will require querying the FIBER engine to get`CABN`, or `ferrumNetworkIdentifer` information.

The information below is just to demonstrate the logic used by FIBER to categorize and optimize swap paths across chains.
{% endhint %}

1. `sourceCABN`: BUSD
2. `sourceFerrumNetworkIdentifier`: BSC
3. `destinationCABN`: USDT
4. `destinationFerrumNetworkIdentifier`: Polygon
5. `amountSourceCABN`: 100000000000000000000 (wei value)
6. `slippage`: 2% per chain (4% total)

### **FIBER Asset Categorization**

When FIBER receives this call, it starts the process of categorizing the `sourceCABN` and `destinationCABN`. In order to categorize the FIBER engine conducts the following checks:

#### Foundry Asset Check (FAC)

Conducts a`bridgePool` liquidity check to determine if the asset has sufficient liquidity available in the `bridgePool` to be categorized as a [Foundry Asset](../../asset-types/foundry-assets.md) for this swap.

#### Refinery or Ionic Asset Check (RIAC)

Conducts if there is pair liquidity available with the bridgeable asset. i.e. Is it possible to convert user's asset to bridgeable asset in a single hop or swap. If the user's asset can be swapped for the bridgeable asset in a single hop then the asset will be categorized as a [Refinery Asset](../../asset-types/refinery-assets.md). Otherwise the asset will be categorized as an [Ionic Asset](../../asset-types/ionic-assets.md).

#### Aggregated Best Quote Check (ABQC)

`aggregatedBestQuoteCheck` a check for the best price on source and destination networks. Checks quotes from aggregators such as 1inch and compares those quotes against DEX quotes from DEX Router contracts. Suggest all options available rated from best to worst.
