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
