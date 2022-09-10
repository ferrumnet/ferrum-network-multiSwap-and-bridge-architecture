# 🪙 Setting Fees on Withdrawal

The `bridgePool` does distribute fees. It follows [SRP](https://en.wikipedia.org/wiki/Single-responsibility\_principle) and is restricted to functionality strictly related to the bridging of assets. Through the nature of bridging, there is a `bridgeFee` that need to be collected and distributed for each transaction. In the case of the MultiChain Liquidity Pool Bridge, these fees are charged at the time of withdrawal. Since withdrawals are handled by the `bridgePool` smart contract, we need to configure the amount of fee the bridge pool must collect at the time of withdrawal. See "Bridging of Assets" for more detail on swap and withdrawal process.

{% content-ref url="bridging-of-assets/" %}
[bridging-of-assets](bridging-of-assets/)
{% endcontent-ref %}

### Pre-Requisite

You cannot configure a fee through the `setFee` function until you have configured the mapping of a token through `allowTarget`. See "Mapping of Tokens on Bridge Pool" for more details.

{% content-ref url="mapping-tokens-on-bridge-pool.md" %}
[mapping-tokens-on-bridge-pool.md](mapping-tokens-on-bridge-pool.md)
{% endcontent-ref %}

### How to Configure Set Fees For Token Withdrawals on The Bridge Pool

1. Go to `setFee` and add the following details to set the `withdrawalFee` for the token on the current network.
   1. `token (address)`
      1. This is the Token Contract Address for the token you are adding on the current network.
   2. `fee10000 (uint256)`
      1. This will be the percentage integer followed by two zeros. For example, if the fee is 1% then enter 100, if it's 2% then enter 200.
   3. Write the transaction and proceed through the MetaMask Prompts. _You can check the transaction status by clicking the_ `View Transaction` button.
2. Now go to the other networks and repeat this process to complete the fee configuration. For example, if you have just completed configuring fees in BSC Testnet and you are mapping this token on Rinkeby and Mumbai (Polygon) Testnet as well, then you will need to go and repeat this process on Rinkeby and Mumbai (Polygon) Testnet now to ensure `bridgeFees` are configured correctly.
