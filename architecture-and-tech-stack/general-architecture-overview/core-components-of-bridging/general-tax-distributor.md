# 📬 General Tax Distributor

There are 2 things to setup in the GeneralTaxDistributor SC `setTokenInfo` and `setTokenTargetInfos`.

1. Go to the GeneralTaxDistributor smart contract on the relevant networks explorer. e.g _Testnet BSC Scan, Rinkeby Etherscan etc_.
2. Go to `Write Contract` and connect the admin wallet. _Make sure you are on the correct network otherwise the wallet will not connect_.
3. Setting `setTokenInfo`. _This needs only needs to be set up for the token contract on the current network._
   * Go to `setTokenInfo` and add the following details to add the token to the GeneralTaxDistributor.
     * `token (address)`
       * This is the Token Contract Address for the token you are adding on the current network.
     * `bufferSize (uint256)`
       * Set this to `1`.
     * `tokenSpecificConfig (uint8)`
       * Set this to `0x1`.
   * Write the transaction and proceed through the MetaMask Prompts. _You can check the transaction status by clicking the_ `View Transaction` button.
4. Setting `setTokenTargetInfos`.
   * Go to `setTokenTargetInfos` and add the following details to configure the `feeDistributionSplit` for withdrawals of the token on the current network.
     * `token (address)`
       * This is the Token Contract Address for the token you are adding on the current network.
     * `infos (tuple[])`
       * This is a tuple is a list of addresses that will receive the fee distribtuion for this token. Use this format to add the list of addresses
         * `[["ferrumFeeShareDistributionAddress",2], ["clientFeeShareDistributionAddress",2]]`
     * `weights (uint216)`
       * This is the distribution split. i.e. 50/50, 60/40 etc. You need to enter a `uint216 hex` here. Use this value for 50/50 splits
         * `0x0808`
   * Write the transaction and proceed through the MetaMask Prompts. _You can check the transaction status by clicking the_ `View Transaction` button.
5. Now go to the other networks and repeat this process to complete the mapping. For example, if you have just completed mapping in BSC Testnet and you are mapping this token on Rinkeby and Mumbai (Polygon) Testnet as well then you will need to go and repeat this process on Rinkeby and Mumbai (Polygon) Testnet now.
