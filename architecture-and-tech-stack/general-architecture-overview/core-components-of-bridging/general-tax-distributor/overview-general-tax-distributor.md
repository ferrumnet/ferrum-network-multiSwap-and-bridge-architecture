# 📐 Overview

The `GeneralTaxDistributor` is a general purpose smart contract responsible for distributing fees to specified destinations. In the MultiChain Liquidity Pool Bridge architecture, the `GeneralTaxDistributor` is configured to receive fees collected by the `bridgePool`.

### Pre-Requisite

You need to map the `setFee` function in the `bridgePool` before configuring the `GeneralTaxDistributor`.

{% content-ref url="../bridge-pool/setting-fees-on-withdrawal.md" %}
[setting-fees-on-withdrawal.md](../bridge-pool/setting-fees-on-withdrawal.md)
{% endcontent-ref %}

### Fee Configuration

Sending tokens directly to the `GeneralTaxDistributor` without specifying a distribution method and configuration will result in the `globalConfig` being initiated.

You can customize the distribution mechanism by defining the distribution addresses and the ratio of the split that should be received by each of them.
