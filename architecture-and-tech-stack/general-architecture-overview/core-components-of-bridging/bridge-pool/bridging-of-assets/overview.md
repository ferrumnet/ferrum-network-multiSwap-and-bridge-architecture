# 📐 Overview

### Transparency, Security, and Speed

#### Transparency

The MultiChain Liquidity Pool Bridge approaches bridging through a swap and withdrawal flow. The intent-based approach enables the user to see the actual gas cost of the swap transaction on the source chain and the withdrawal transaction on the destination chain. Other bridges have to estimate the gas cost for the release of tokens and deposit into the destination wallet. In order to cover the gas cost, a buffer is added. The problem with this approach is the fact that the user doesn't know exactly how many tokens they will receive on the destination network. The intent-based approach utilized by the MultiChain Liquidity Pool Bridge solves this issue.

#### Security

Each swap transaction has the intent of the bridge transfer embedded in it. This means that an immutable record on the source chain is created the moment a swap is initialized. Instead of solely relying on validator or relay node infrastructure, the transaction authentication and verification process treats the on-chain data as the source of truth. The benefit of this approach is that even if the master node signature is compramised for withdrawal item creation, the withdrawal can only be sent to the address defined in the origination swap transaction of the transfer. Meaning the hacker will pay the gas to transfer tokens into the intended user's wallet doing the user a favor by paying gas fees for them.

#### Speed

With on-chain data serving as the source of truth, we can perform, validate and complete multichain bridge transfers at transaction speeds.&#x20;
