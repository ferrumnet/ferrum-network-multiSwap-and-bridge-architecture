# 🧠 FIBER Engine

FIBER Engine is the brains behind MultiSwap. It is the main source of contact for anyone looking to do a MultiChain swap utilizing MultiSwap.&#x20;

### :pencil: The Checks

FIBER Engine receives a request, then starts conducting a set of checks on the source and destination networks, including [FAC](asset-categorization-and-route-optimization/example-of-asset-categorization.md#foundry-asset-check-fac), [RIAC](asset-categorization-and-route-optimization/example-of-asset-categorization.md#refinery-or-ionic-asset-check-riac), and [ABQC](asset-categorization-and-route-optimization/example-of-asset-categorization.md#aggregated-best-quote-check-abqc) checks.&#x20;

### :arrows\_counterclockwise: The Requests

Once FIBER Engine has conducted the necessary checks and determined the most optimal route for the MultiChain Swap request, it sends the request to the [FIBER Router](fiber-router.md) to process the request.

### :busts\_in\_silhouette:The Nodes

FIBER also interacts with the nodes and waits for verification from the MultiSwap node infra before authorizing withdrawAndDeposit or withdrawSwapAndDeposit requests on the destination networks through the [FIBER Router](fiber-router.md).
