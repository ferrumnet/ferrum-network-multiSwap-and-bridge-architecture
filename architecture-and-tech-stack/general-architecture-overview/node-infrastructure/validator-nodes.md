# 🕵 Validator Nodes

The validator node verifies the newly received requests from the Generator Node against on-chain data. Once the verification is complete that this is indeed an authenticated on-chain request and not a spoofed request, the Validator Node adds it's signature as a verifier of the request.&#x20;

NOTE: Only authenticated validator node signatures are honored. If a validator node is not authenticated the master node will ignore these signatures.

![Validator Node](<../../../.gitbook/assets/Validator Node.jpg>)

