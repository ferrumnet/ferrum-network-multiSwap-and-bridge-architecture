# 📐 Overview

From a smart contract, module, and blockchain interaction standpoint there are a few core components that enable multi-chain bridging and swapping of assets through the MultiSwap protocol.

1. Bridge Pool
2. General Tax Distributor
3. Node Infrastructure



Quantum Routing (IBC similarities)

1. Swap - Source
   1. Swap or bridge
   2. Optemized Swap
2. Bridging and Settlement
3. Swap - Destination

At a high level, the Bridge Pool is responsible for the mapping of tokens that can be transferred across networks and setting the withdrawal fee amount that is to be sent to the General Tax Distributor. The General Tax Distributor is responsible for setting the fee distribution and split of those fees per the config. i.e. How much fee should be sent to which wallet.
