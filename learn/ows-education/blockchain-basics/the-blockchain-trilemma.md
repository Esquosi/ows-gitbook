---
description: OWS Education / Blockchain Basics / The Blockchain Trilemma
cover: ../../../.gitbook/assets/Announcement Banner (Twitter) (2).png
coverY: 0
---

# The Blockchain Trilemma

Welcome to the second piece of the ‘Blockchain Basics’ batch which is a part of OWS Education created by OWS team.&#x20;

In this article we will look into the three facets of the Blockchain Trilemma: Decentralisation, Scalability and Security.

{% embed url="https://youtu.be/l0SGWEcnlWs" %}



The trilemma is concurrently achieving decentralisation, scalability, and security all at once. Some blockchain developers don’t believe that the trilemma is attainable, while more ambitious developers think all three properties can be achieved simultaneously.\
So, what do these terms mean specifically and why are they currently so hard to have together?

### Decentralisation

Decentralisation is a term that is often used but also often misunderstood or underrepresented. We will take the time here to give it the attention it requires. The term is used for a blockchain network that does not operate through a central entity to manage or censor its activity but is rather operated collectively by all nodes part of the network. Decentralisation can be split into two categories, political decentralisation and architectural decentralisation.\
Political decentralisationPolitical decentralisation is about who is part of the decision-making process for a blockchain system. The decentralisation of decision-making in blockchains happens in two main ways.

1. The first way is how its decentralised for the users, which can execute transactions on a blockchain network without the interference of a central entity to confirm, trust, or execute these transactions on their behalf.
2. While the second way blockchains are politically decentralised is in way the nodes of the system manage to reach a consensus about what transactions were made and by who, without a central point of verification.

Architectural decentralisationOn the other hand, architectural decentralisation is about how dispersed the information state of the blockchain is on its physical infrastructure. To be architecturally decentralised, blockchains must have a safe way for its nodes to store the information that they have reached a consensus about, so that they all hold the same single line of truth.

### Scalability

Scalability is the term used to describe the ability of a blockchain to support high transactional throughput and growth. A way to measure this is by the transactions per second a blockchain network can process. It is about how much a system can increase its output, proportional to its input. Scalability can be increased by improving the networks consensus protocol, as solana has done with PoH, or sharding the consensus process, as NEAR and Ethereum are doing.

### Security

Security is the term used to describe how hack-proof a blockchain network is against malicious attacks. The security of a blockchain should prohibit malicious attacks on three levels.

1. The first level is for the users. The security of users’ wallets must be guaranteed to avoid theft of assets or un-consensual transactions.
2. The second is for the consensus protocol. The security of the consensus protocol must be guaranteed so that the consensus reached by the nodes is reliable and consistent.
3. The third is for the blockchain data structure. The security of the data structure must be guaranteed so that the information stored on the chain of blocks by the nodes is reliable and consistent, avoiding what is called the 51% attack (or versions of it).

### Trade-offs of picking any two features.

Decentralisation and Security compromise Speed for two reasons.

1. The first is that if you need every node to reach a consensus about what transactions were made and by who, you will slow down the process.
2. While the second is that if you need every node to store the same single line of truth on a chain of blocks, it will take time for each chain of blocks to update.

Decentralisation and Scalability compromises Security for one reason.

1. The more decentralised a blockchain system, the less centralised security and encryption features it can have, which are the most effective security methods we have.
2. A scaled consensus protocol will lose security as branches disperse the security of it.

Scalability and Security compromise Decentralisation for one reason.

* A way to have a scalable and secure system is to reduce the amount of nodes and increase the barriers to entry to become one.

### Solutions.

On-chain solution

* Create more but less secure secondary blockchains for scalability. This is what sharding does, splitting the work up into on-chain shards. Zero-knowledge proofs are still in development.

Off-chain solution

* Creates a layer 2 where transactions and work is done off-chain, only computing the output on the blockchain. This allows the systems to speed up.

\
In this article we talked about the issues that the Blockchain Trilemma brings forth. In the next piece we will discuss how the industry is trying to overcome them.
