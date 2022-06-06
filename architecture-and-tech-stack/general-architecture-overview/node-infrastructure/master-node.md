# ✒ Master Node

The Master Node looks for requests that have met the verification threshold. The verification threshold is the number of authenticated validator node signatures required before a request is considered verified and authenticated. These parameters are configured by master node administrators through a quorum.&#x20;

Once the Master Node has received the threshold signatures from authenticated validator nodes, it signs the withdrawal requests. The master node signature generates a valid one-time use withdrawal item.

![Master Node](<../../../.gitbook/assets/Master Node.jpg>)

![Multiple-Validator Signatures](<../../../.gitbook/assets/Multi Validator Node Verification.jpg>)
