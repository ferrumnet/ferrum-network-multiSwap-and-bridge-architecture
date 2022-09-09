---
description: Learn how liquidity is managed in the MultiChain Liquidity Pool Bridge
---

# ⚖ Liquidity Management

### Risk Mitigation through Decentralization

Unlike _**lock & mint**_ or _**burn & mint**_ bridges (**LMBM**) in the market today, the MultiChain Liquidity Pool Bridge does not have any operative or interactive control over the administration of any token contract.&#x20;

#### Single Point of Failure and Centralized Administration Problem

When a token utilizes LMBM bridges to launch on a new chain, the new token on the destination chain is typically minted as a mirror or wrapped asset. In almost every case, these destination chain tokens are minted by the LMBM bridging platform.&#x20;

This means the bridging platform has operative and interactive control over the administration of the token on the destination network. Furthermore, the bridging platform becomes the centralized source of exploit vectors for hundreds if not thousands of listed tokens and billions in asset value.&#x20;

#### Honey Pots for Hackers

For LMBM bridges, the minted-wrapped tokens need to be backed by the native tokens on the origin chain. This means that for every wrappedX token minted, an X token on the origin chain must be locked in a bridge pool. These tokens typically cannot be moved out of the bridge pools since they serve as the backing or peg for the minted-wrapped tokens on the destination chain.&#x20;

Over time these bridge liquidity pools can grow in size to billions in assets locked up. The enormous value of assets locked in these bridge liquidity pools creates a lucrative honeypot for hackers and bad actors to dedicate significant time and resources toward an exploit. Even if a hacker spends two years finding an exploit, the reward of hundreds of millions to billions in assets is worth the effort.&#x20;

#### Scale with Limited Exposure

The MutliChain Liquidity Pool Bridge maps native assets across networks to enable bridging. This means the bridge itself doesn't mint any tokens. Instead, the supply of the tokens across networks is managed by the administrators of the token contract. Typically these administrators are either the DAO or the management team of that specific organization.

A significant benefit of this approach is the ability to conduct hundreds of millions to billions in transacted volume with minuscule liquidity lockups. For example, the Ferrum MultiChain bridge has already done over a quarter billion dollars in transacted volume across Ethereum, Polygon, and BSC, with the average locked liquidity of under 5 million in the bridge pool across networks. All excess liquidity is constantly moved into decentralized multisig safes.

### Pre-Requisite

Before adding liquidity, you will need to complete Mapping Tokens on Bridge Pool.&#x20;

{% content-ref url="mapping-tokens-on-bridge-pool.md" %}
[mapping-tokens-on-bridge-pool.md](mapping-tokens-on-bridge-pool.md)
{% endcontent-ref %}

### Setting up Liquidity on the Bridge Pool Smart Contract

The MultiChain Liquidity Pool Bridge uses a balancing mechanism. This mechanism requires the user to deposit tokens into the `bridgePool` on the source chain. This deposit triggers a process for validating the swap and authorizing the withdrawal of tokens in the intended destination chain. Once the validation is completed, an authorized withdrawal item is generated, which enables the user to withdraw the tokens from the desired destination chain.&#x20;

In order to facilitate the transfer of assets across chains in the manner described above, sufficient liquidity must be present in the `bridgePool` of the destination chain. Lack of sufficient liquidity will still generate a valid withdrawal item, but the user will not be able to extract the tokens from the destination chain's `bridgePool` until sufficient liquidity is replenished.

#### Swap Initialization on Source Chain - Increases Liquidity Balance in BridgePool on Source Chain

<figure><img src="../../../../.gitbook/assets/MultiChain Bridge Swap - Token Deposit - BridgePool.gif" alt=""><figcaption><p>Swap Initialization on Source Chain Deposits Tokens From User's Wallet Into The Bridge Pool - <a href="https://isoflow.io/app/project/ckzr24q3hm0ch0838p1gpdz0k">See Full Flow</a></p></figcaption></figure>

#### Withdrawal Initialization on Destination Chain - Decreases Liquidity Balance in BridgePool on Destination Chain

<figure><img src="../../../../.gitbook/assets/MultiChain Bridge Withdrawal - Token Withdrawal - BridgePool.gif" alt=""><figcaption><p>Withdrawal Initialization on Destination Chain Withdraws Tokens From The Bridge Pool Into The User's Wallet Into - <a href="https://isoflow.io/app/project/ckzr24q3hm0ch0838p1gpdz0k">See Full Flow</a></p></figcaption></figure>
