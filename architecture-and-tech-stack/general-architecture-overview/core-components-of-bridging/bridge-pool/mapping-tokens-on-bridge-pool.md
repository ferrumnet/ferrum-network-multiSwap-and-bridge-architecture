---
description: Learn how tokens can be mapped for bridging across networks
---

# 🤝 Mapping Tokens on Bridge Pool

There are 2 things to setup in the `bridgePool` smart contract `allowtarget` and `setFee`. In this section we'll cover mapping of tokens through `allowTarget`. To learn more about Setting Fees on Withdrawal see:

{% content-ref url="setting-fees-on-withdrawal.md" %}
[setting-fees-on-withdrawal.md](setting-fees-on-withdrawal.md)
{% endcontent-ref %}

### How to Map Tokens on the `bridgePool` smart contract

In the `bridgePool` the mapping of tokens can be set up by utilizing the `allowTarget` function.&#x20;

Here are the instructions to do so:

1. Go to the `bridePool` smart contract on the relevant networks explorer. e.g _BSC Scan, Rinkeby Etherscan etc_.
2. Go to `Write Contract` and connect the admin wallet. _Make sure you are on the correct network otherwise the wallet will not connect_.
3. Setting `allowTarget`. _This needs to be set up for each pair that should be mapped to the token. For example, suppose you are setting the FRM token on BSC Testnet to be mapped to the FRM token on Rinkeby and Mumbai (Polygon) testnet. In that case, you will need to add the token contract information of the current network (BSC Testnet) FRM token and each destination token in two separate transactions._
   * Go to `allowTarget` and add the following details to add the token.
     * `token (address)`
       * This is the Token Contract Address for the token you are adding on the current network.
     * `chainId (uint256)`
       * This is the `chainId` for the destination network of the Token Contract Address you are adding the mapping for. For example, if you are setting up the FRM Token in the BridgePool SC on Rinkeby to the FRM token on BSC Testnet then you would add the BSC Testnet chainId 97 here. _**Make sure to enter the correct chain chainId for the corresponding destination Token Contract Address**_.
     * `targetToken (address)`
       * This is the Token Contract Address for the token on the destination network. For example, if you are setting up the FRM Token in the BridgePool SC on Rinkeby to the FRM token on BSC Testnet then you would add the FRM BEP20 (BSC Testnet) Token Contract Address here.
   * Write the transaction and proceed through the MetaMask Prompts. _You can check the transaction status by clicking the_ `View Transaction` button.
   * Repeat this process for each network you are mapping this token to.
4. Now go to the other networks and repeat this process to complete the mapping. For example, if you have just completed mapping in BSC Testnet and you are mapping this token on Rinkeby and Mumbai (Polygon) Testnet as well, then you will need to go and repeat this process on Rinkeby and Mumbai (Polygon) Testnet now.

In order to set withdrawal fees for the token on the current network, you need to utilize the `setFee` function described here:

{% content-ref url="setting-fees-on-withdrawal.md" %}
[setting-fees-on-withdrawal.md](setting-fees-on-withdrawal.md)
{% endcontent-ref %}



