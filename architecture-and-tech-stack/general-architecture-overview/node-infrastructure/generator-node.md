# 🔍 Generator Node

The Generator Node is one of the first components in Ferrum Network's Node Infrastructure that looks for, validates and generates withdrawal request items on destination networks for depositted tokens on origin networks.

![Generator Node](<../../../.gitbook/assets/Generator Node.jpg>)

The deposits are monitored through on-chain activity by these Generator Nodes. Once the nodes identify new deposits on-chain they submit those requests to the DB. At this point, the validator nodes come into play.
