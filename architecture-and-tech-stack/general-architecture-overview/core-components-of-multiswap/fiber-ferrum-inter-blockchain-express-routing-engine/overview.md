# 📐 Overview

At a high level, FIBER is responsible for finding the optimal path to conduct swaps across chains, as well as bridging and settlement. Depending on the asset type. If the asset has liquidity in the `bridgePool` these assets are classified as Foundry Assets. All foundry assets benefit from reduced fees during a swap across chains as one less swap needs to be conducted on the source or destination chain.&#x20;

### Typical FIBER request

A typical FIBER call includes the following parameters:

1. `sourceCABN`
2. `sourceFerrumNetworkIdentifier`
3. `destinationCABN`
4. `destinationFerrumNetworkIdentifier`
5. `amountSourceCABN` or `amountDestinationCABN`
   1. One of these values must be provided

{% hint style="info" %}
See [Glossary & Acronyms](../../../../resources/glossary-and-acronyms/) for more detail on `CABN` and `ferrumNetworkIdentifier`
{% endhint %}
