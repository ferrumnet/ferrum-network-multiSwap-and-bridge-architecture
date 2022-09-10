# 💰 Withdrawals

As described in the [Transparency, Security, and Speed](https://docs.ferrumnetwork.io/ferrum-ecosystem/v/infinityswap-and-bridge-architecture-overview/architecture-and-tech-stack/general-architecture-overview/core-components-of-bridging/bridge-pool/bridging-of-assets/overview#transparency-security-and-speed) section of the overview for this topic, the MultiChain Liquidity Pool Bridge follows a swap and withdraw intent-based approach to bridging of assets across chains.

### Pre-Requisite

You must complete a swap before attempting a withdrawal.

{% content-ref url="swap-initiation.md" %}
[swap-initiation.md](swap-initiation.md)
{% endcontent-ref %}

### How To Withdraw Tokens On The Destination Network

1. After completing the swap, the bridge UI will guide you to switch to the desired destination network
2. Once you switch your network, you will either see your withdrawal item waiting for verification or ready to withdraw
3. At this point you can follow the prompts on screen to complete the withdrawal
4. The UI will provide an option to add the token to your wallet, make sure to do that if this is your first time bridging this token to the specified chain
