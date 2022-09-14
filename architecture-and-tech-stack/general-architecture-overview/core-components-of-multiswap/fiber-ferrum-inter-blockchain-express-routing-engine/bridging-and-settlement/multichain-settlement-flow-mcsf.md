# ⚖ MultiChain Settlement Flow (MCSF)

MultiSwap enables any asset $$x$$ on network 1 to be swapped for any asset $$y$$ on network 2. To facilitate these multi-chain swaps, FIBER uses [MCSF](../../../../../resources/glossary-and-acronyms/acronyms.md#mcsf).&#x20;

The flow of swap and bridging of assets across chains follows four steps known as MultiChain Settlement Flow (MCSF)

<figure><img src="../../../../../.gitbook/assets/FIBER - Routing.gif" alt=""><figcaption><p>FIBER - MultiSwap - <a href="https://isoflow.io/app/project/cl7teuo4030zs0838hgqsnugh">See Full Flow</a></p></figcaption></figure>

1. Swap from User Asset to Bridgeable/Settlement Asset
2. Bridging of Asset
3. Swap from Bridgeable/Settlement Asset to User Desired Asset
4. Deposit of Desired Asset Into User's Wallet

### Swap from User Asset to Bridgeable/Settlement Asset

[Foundry Assets](../../asset-types/foundry-assets.md) are considered bridgeable assets. This means there is sufficient liquidity available for this asset on the destination network to facilitate bridging for the amount requested by the users.&#x20;

All other asset types must be converted to a Foundry Assets in order to facilitate bridging of these assets across chains.

<img src="../../../../../.gitbook/assets/file.drawing.svg" alt="" class="gitbook-drawing">

