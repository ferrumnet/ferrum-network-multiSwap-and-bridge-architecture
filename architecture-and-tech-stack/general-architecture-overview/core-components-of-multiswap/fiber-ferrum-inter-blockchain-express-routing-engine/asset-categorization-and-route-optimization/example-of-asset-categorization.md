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

1. `bridgePool` liquidity check AKA Foundry Asset Check
2. `singleHop` swap check AKA Refinery or Ionic Asset Check
3. `aggregatedBestQuoteCheck` a check for the best price on source and destination networks
