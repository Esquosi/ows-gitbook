---
description: OWS Education / Blockchain Basics / Blockchain Consensus Protocols
cover: ../../../.gitbook/assets/Announcement Banner (Twitter) (2).png
coverY: 0
---

# What are Consensus Protocols?

Welcome to the third article of the ‘Blockchain Basics’ batch which is a part of OWS Education created by OWS team.&#x20;

In this article we will look into the three most common consensus protocols and how they all succeed at validating the truth of transactions.

{% embed url="https://youtu.be/TaVzJ_BcqZw" %}

Because blockchains are decentralised and autonomous, they must have a reliable decentralised method to ensure that all transactions on the network are orderly and truthful transactions. A consensus protocol is the agreed algorithm used by a blockchain network to validate the transactions as truthful.

The consensus protocols aim to solve two issues:

1. Keep transactions in order to avoid the double spending problem.
2. Prove prove that the content of transactions has not been tampered with.

In this video we will outline the most commonly used and developed consensus protocols, and their positives and negatives for their application.

### PoW (Bitcoin)

Proof-of-work was the first consensus protocol to be used on a blockchain network, Bitcoin. PoW aims to solve the consensus problem by making miners use time and energy to validate transactions. Let’s follow the transaction process for a PoW blockchain to see how it works.\
Once a transaction is made by a user, it is signed using their private key. &#x20;

Instead of having some centralised authority approve the transaction, miner nodes on the network race each other to prove to the rest of the network that the transaction is valid. They prove this by trying to be the first miner node to solve a time and energy consuming cryptographic problem. To solve the problem they must find the input to some one-way function that gives a correct output.

Once a miner node claims they have found the solution, the other nodes part of the network can check that the solution is correct by feeding it into the same function to check for the correct output. If it is, it validates the transaction received.

#### Positive

* When there are a lot of nodes, it is very secure.

#### Negative

* Slow transaction speeds and low scalability.

### PoS (NEAR, Ethereum)

Proof-of-Stake is a consensus protocol which aims to increase the scalability of a blockchain network. PoS offers a method to validate transactions that uses far less time and energy compared to PoW. PoS does this by giving any node which stakes a certain amount of cryptocurrency the power to validate transactions.

Let’s again follow the transaction process for a PoW blockchain to see how it works.\
Once a transaction is made by a user, it is signed using their private key. &#x20;

Instead of having miner nodes, a PoS blockchain network has validator nodes. Validator nodes stake a portion of their cryptocurrency so that the PoS algorithm can chose them at random to validate a transaction. For some PoS networks, the higher the stake means the higher the chance that you will be randomly picked to validate the transaction. Once a validator node is chosen, they validate the transaction and store it in a block. If a transaction that has been tampered with is validated, and the network realises, then the validator node loses their stake automatically.

#### Positive

* Scalable and low on hardware and energy usage. &#x20;

#### Negative

* Benefits those with more stake.

### PoH (Solana)

Proof-of-history is a consensus protocol that aims to increase speed and scalability by creating a verifiable list of transactions through time. Let’s go through the transaction validation process.

The PoH algorithm gives validator nodes turns to be transaction validators, where validator nodes are selected similarly to PoS.

Once a node is selected for the role, the PoH algorithm makes the validator node use a cryptographically secure one-way function that takes as input the transaction and outputs a hash. Then, that hash and the next transaction is inputted into the same function, to output another hash. Because each time the function is run, the hash of the previous one is required, it can be said that real time has passed between the two transactions. As a result, each hash tells us what transaction had to come before it. This results in a verifiable order of transactions as a function of time.

Once this sequence has been outputted, all other validator nodes can verify the sequence of the transactions by inputting their corresponding hashes.

#### Positive

* High throughput without compromising network security.

#### Negative

* Low decentralisation, due to specific hardware requirements.

In this video we outlined the three most common blockchain consensus protocols: PoW, PoS, and PoH. In the next videos part of this batch, we will discuss what use blockchains have for users, and what can be achieved on them.In this article we outlined the three most common blockchain consensus protocols: PoW, PoS, and PoH. In the next parts of this batch, we will discuss what use blockchains have for users, and what can be achieved on them.
