# 🚀 Liquidity Setup

### Liquidity Management by Token Administrator

The Token Administrator, typically the project, organization, or DAO who launched the original token is responsible for managing liquidity in the `bridgePool` smart contracts. This is similar to managing sufficient liquidity in a DEX liquidity pool to support trading. If liquidity is drained on the `bridgePool` then withdrawals will not be possible until sufficient liquidity is replenished through the liquidity management dashboard.

### Single Asset vs Pair Liquidity Pools

The liquidity pool set up in the `bridgePool` smart contract is a single asset pool. Unlike DEX liquidity pools, you don't need to pair your token with a fee or swappable token to add `bridgePool` liquidity.

### Pre-Requisite

Before adding liquidity, you will need to complete Mapping Tokens on Bridge Pool.&#x20;

{% content-ref url="../mapping-tokens-on-bridge-pool.md" %}
[mapping-tokens-on-bridge-pool.md](../mapping-tokens-on-bridge-pool.md)
{% endcontent-ref %}

### Adding Single Asset Liquidity to Bridge Pool

To add initial liquidity, we recommend using our liquidity management dashboard. You can use the Ferrum dashboard or your own white labeled link if you are utilizing our white label bridge implementation.

1. Go to the [Ferrum Liquidity Management Dashboard](https://bridge.ferrum.network/frm/liquidity/add)
2. Connect your wallet and select the desired network
3. Select your token from the drop-down list
4. Enter the desired amount of tokens in the input field
5. Click or touch the add liquidity button and go through the transactions flow in MetaMask

<figure><img src="../../../../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Ferrum Liquidity Management Dashboard</p></figcaption></figure>

The white labeled version can be accessed by going to your `bridgeUrl/liquidity/add`

### Removing Liquidity

It's unlikely that you need to remove liquidity from the bridge. This is similar to removing liquidity from a DEX. An event that only happens if you are decommissioning that DEX, network, or project. However, if you need to remove liquidity for any reason, you can do so by going to: `bridgeUrl/liquidity/remove`. Here you can follow the prompts to remove the available liquidity. The amount of liquidity you can remove is subject to the maximum liquidity added by the connected wallet and the amount of liquidity available in the `bridgePool` at the time.

For Liquidity balancing, and replenishment see our Reverse Swap process instead

{% content-ref url="liquidity-replenishment-with-reverse-swaps.md" %}
[liquidity-replenishment-with-reverse-swaps.md](liquidity-replenishment-with-reverse-swaps.md)
{% endcontent-ref %}
