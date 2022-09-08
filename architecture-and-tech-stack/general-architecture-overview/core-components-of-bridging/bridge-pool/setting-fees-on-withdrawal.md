# 🪙 Setting Fees on Withdrawal

The `bridgePool` does&#x20;

Setting `setFee`. This one is a lot simpler 😀

* Go to `setFee` and add the following details to set the `withdrawalFee` for the token on the current network.
  * `token (address)`
    * This is the Token Contract Address for the token you are adding on the current network.
  * `fee10000 (uint256)`
    * This will be the percentage integer followed by two zeros. For example, if the fee is 1% then enter 100, if it's 2% then enter 200.
* Write the transaction and proceed through the MetaMask Prompts. _You can check the transaction status by clicking the_ `View Transaction` button.
