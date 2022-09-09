# 📐 Overview

Our previous bridge node architecture and related infrastructure were in their infancy stage. For example, the signing of withdrawals was centralized to favor speed and security. In general, a simplified architecture was favored for v1.0.0. With the support of major backers such as Algorand, Casper and others, Ferrum Network started updating the Node Signing Architecture and related Infrastructure (v2.0.0) to enable decentralized Node signing. This major update was geared to provide additional security and reliability layers while allowing stakeholders like Algorand, Casper, and other networks in the ecosystem to run Generator and Validator nodes for withdrawals. The ability for more stakeholders to run Generator and Validator nodes brings state-of-the-art decentralization to the multi-chain protocol. This major upgrade will be pivotal in improving MultiSwap's architectural security without compromising speed and maintaining reliability.

#### Node Signing Architecture and Infrastructure v1.0.0

![Node Signing Infrastructure v1.0.0](<../../../.gitbook/assets/Node Signing Infrastructure v1.0.0.png>)

### New Node Infrastructure

The new node infrastructure is a culmination of three distinct node roles working together. Each adds an additional layer of security and authentication in order to reduce and discourage attack vectors on the system. The following nodes make up the bridging node infrastructure:

1. Generator Nodes
2. Validator Nodes
3. Master Node

Let's go over the roles of each node next.

View the full diagram by clicking the link below:

{% embed url="https://app.cloudcraft.co/view/840421d3-165a-4e5a-827a-60fcd2815529?embed=true&interactive=true&key=ba3db521-b5fc-440f-b3d5-377616ce714c" %}

#### Node Signing Architecture and Infrastructure v2.0.0

![Node Signing Infrastructure v2.0.0](<../../../.gitbook/assets/Node Signing Infrastructure v2.0.0.png>)
