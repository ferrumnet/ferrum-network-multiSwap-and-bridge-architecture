# 📐 Overview - FIBER

### Introducing FIBER Engine

At a high level, FIBER is responsible for finding the optimal path to conduct swaps across chains, as well as bridging and settlement; depending on the asset type. If the asset has liquidity in the `bridgePool` these assets are classified as Foundry Assets. All foundry assets benefit from reduced fees during a swap across chains as one less swap needs to be conducted on the source or destination chain. FIBER conducts its work through FIBER Engine which interacts with the FIBER Router, Fund Manager, and external entities.&#x20;

### Typical `multiChainSwap` request sent to [FIBER Engine](fiber-engine.md)

A typical FIBER call includes the following parameters:

1. `sourceCABN`
2. `sourceFerrumNetworkIdentifier`
3. `destinationCABN`
4. `destinationFerrumNetworkIdentifier`
5. `amountSourceCABN` or `amountDestinationCABN`
   1. One of these values must be provided
6. `destinationAddress`
7. `slippage`: default max 2% per chain
8. `platformFeeCABN`
9. `isFeeEnabled`

{% hint style="info" %}
See [Glossary & Acronyms](../../../../resources/glossary-and-acronyms/) for more detail on `CABN` and `ferrumNetworkIdentifier`
{% endhint %}
