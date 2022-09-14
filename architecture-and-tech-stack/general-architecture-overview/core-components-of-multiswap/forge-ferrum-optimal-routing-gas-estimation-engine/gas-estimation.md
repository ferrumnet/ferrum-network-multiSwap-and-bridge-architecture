# ⛽ Gas Estimation

FORGE calculates GAS cost for the swap and bridging transactions on the source chain, as well as any necessary [Refinery Asset](../asset-types/refinery-assets.md) or [Ionic Asset](../asset-types/ionic-assets.md) swaps and [RDR](../fiber-ferrum-inter-blockchain-express-routing-engine/bridging-and-settlement/multichain-settlement-flow-mcsf/bridging-of-assets.md) transactions on the destination chain.

The GAS estimation is transparently shown to the user in the MultiSwap interface. If the GAS gathered according to the forecasted estimation is greater than the actual GAS cost, FORGE stores the excess gas in reserve associated with the user's address that initiated the swap.
