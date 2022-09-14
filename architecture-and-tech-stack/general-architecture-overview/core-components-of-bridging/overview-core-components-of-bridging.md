# 📐 Overview

From a smart contract, module, and blockchain interaction standpoint there are a few core components that enable multi-chain bridging and swapping of assets.

1. Bridge Pool
2. General Tax Distributor
3. Node Infrastructure

At a high level, the Bridge Pool is responsible for the mapping of tokens that can be transferred across networks and setting the withdrawal fee amount that is to be sent to the General Tax Distributor. The General Tax Distributor is responsible for setting the fee distribution and split of those fees per the config. i.e. How much fee should be sent to which wallet.

<figure><img src="../../../.gitbook/assets/Two Way Liquidity Pool Bridge Flow.gif" alt=""><figcaption><p><a href="https://isoflow.io/app/project/ckzr24q3hm0ch0838p1gpdz0k">MultiChain Bridge Flow</a></p></figcaption></figure>
