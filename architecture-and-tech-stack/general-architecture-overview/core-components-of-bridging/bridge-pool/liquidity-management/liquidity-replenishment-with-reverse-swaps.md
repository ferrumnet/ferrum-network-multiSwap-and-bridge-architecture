# 🪙 Liquidity Replenishment With Reverse Swaps

### Decentralized Liquidity Storage and Replenishment

The [Liquidity Balancing Across Bridge Pool Smart Contract](https://docs.ferrumnetwork.io/ferrum-ecosystem/v/infinityswap-and-bridge-architecture-overview/architecture-and-tech-stack/general-architecture-overview/core-components-of-bridging/bridge-pool/liquidity-management/overview#liquidity-balancing-across-bridge-pool-smart-contract) process described in the overview page of this section explains how tokens are deposited by users into the `bridgePool` on the source chain and withdrawn from the `bridgePool` by users on the destination network. This process creates an imbalance of liquidity adding a surplus on the network where tokens are being transferred from and a deficit on the network where tokens are being withdrawn. We advise projects to regularly remove excess liquidity from the surplus and store it in a decentralized multisig safe. This can be done through a process known as Reverse Swap.&#x20;

### Reverse Swaps To Remove Excess Liquidity and Replenish Deficits

A reverse swap accomplishes the following:

1. Removes excess liquidity from the surplus on the source network
2. Replenish sufficient liquidity to support withdrawals on the destination network
3. Balances circulating supply across networks

To conduct a reverse swap, the token administrator simply goes to the bridge and conducts a simple swap from the deficit network to the surplus network. The swap amount can be as large as the total available liquidity on the surplus network.

<figure><img src="../../../../../.gitbook/assets/MultiChain Bridge - Bridge Pool - Liquidity Balancing.gif" alt=""><figcaption><p><a href="https://isoflow.io/app/project/cl7v5uo3w33o50838t5j92gcb">MultiChain Liquidity Pool Bridge - bridgePool Liquidity Balancing</a></p></figcaption></figure>

For example, let's assume that the liquidity on the surplus network has reached 1MM tokens, while the liquidity on the deficit network has fallen to 10K as a result of significant transfers from the surplus network to the deficit network. If a reverse swap in the amount of 900K tokens is initiated from the deficit network to the surplus network, this will update the liquidity on the deficit network from 10K to 910K. The liquidity on the surplus network will be reduced from 1MM to 100K. The token administrator will be able to extract 900K in liquidity and move it into a multisig safe, removing the "[Honey Pots for Hackers](https://docs.ferrumnetwork.io/ferrum-ecosystem/v/infinityswap-and-bridge-architecture-overview/architecture-and-tech-stack/general-architecture-overview/core-components-of-bridging/bridge-pool/liquidity-management/overview#liquidity-balancing-across-bridge-pool-smart-contract)" effect described in the [Liquidity Management Overview](https://docs.ferrumnetwork.io/ferrum-ecosystem/v/infinityswap-and-bridge-architecture-overview/architecture-and-tech-stack/general-architecture-overview/core-components-of-bridging/bridge-pool/liquidity-management/overview).

