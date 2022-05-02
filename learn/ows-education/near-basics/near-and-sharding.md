---
description: OWS Education / NEAR Basics
cover: ../../../.gitbook/assets/Announcement Banner (Twitter) (1).png
coverY: 0
---

# NEAR and Sharding

Welcome to the fourth video of the ‘NEAR Basics’ batch, part of OWS Education, created by the OWS team. In this video we will look into how NEAR’s Sharding mechanism, Nightshade, works and how it allows the NEAR network to be scalable and secure.

Let’s begin!

{% embed url="https://youtu.be/udPKjirDgl0" %}

### PoS with and without Sharding

Now that we know how NEAR uses TPoS to select a set of nodes to validate transactions, let’s look into how the validator nodes actually compute transactions and how they come to an agreement for the global state of the NEAR blockchain.

* In PoS without Sharding, all validators must process every single transaction sequentially to agree on the state of the blockchain, what we call its ‘global state’. This limits the throughput of how many transactions can be processed per second, the TPS of a blockchain.
* On the other hand, in PoS with Sharding, validators only need to process a subset of transactions to agree on the global state. This allows the throughput of transactions to be increased considerably, up to 100,000 TPS for NEAR.

But how can validators of the NEAR network only process a subset of transactions and still come to a consensus about the global state of the NEAR blockchain?\


### NEAR’s chain of blocks

Let’s begin with two basic points:

* The NEAR blockchain can be thought of as a line of horizontal blocks, sequentially tied by their headers, like any typical blockchain, where its global state is the state of the most recent block.

![blockchain.png](https://codahosted.io/docs/hfGgtxGDfQ/blobs/bl-JjN8bMNfJF/b70d36b06304afe54e3ca1467b0761d1111611367ddd84be2bc02b511bead92f1f08923192502c1a556a5c241a436a3767590b5f0ffe55046718dd1f20db61218bd12ba4468d9773c0093f0d43349042e8632448e9300e5ed0832570996492bd35f48089)\


* For NEAR, each block is composed of chunks, which are just different bundles of transactions found in each block.

![NEAR block.png](https://codahosted.io/docs/hfGgtxGDfQ/blobs/bl-S7NGulDAu4/613be02e1f9f15547e7b2d27de206fad04d183a6adb8be0448fb681e2f610aa80bc620e1347c0a9f6549e62e68af0ea6c4aab88a3da3f9dd177cc22e1f0326d94a0f41cf87a77bd904f8e157f7c6863a3e42b57c187e70e9134dc6694ed780d3f9590020)

### Shards and Nightshade

So, what processes the transactions in each chunk?

Shards! NEAR uses a mechanism called Nightshade to organise how shards process transactions found in chunks and how shards handle cross-shard communication.

If we imagine blocks running horizontally and tied sequentially to their previous block, then shards also run horizontally and are tied sequentially to their corresponding shard from the previous block. This makes them like little chains within the main chain: each shard only processes its line of chunks for every block, communicating to other shards only if cross-shard transactions arise.

\
![Sharding.png](https://codahosted.io/docs/hfGgtxGDfQ/blobs/bl-1tGXH9wwe3/55daf6b8e55ee1f53d9eba1e949c4d5ef4f51d9f9b383e4a2811a42ed6daa0f9885b3ff8a0b6748bb8abc2322d72d49a198109b9a472cb95ed60238e5d287c5d0460c3e447fd552b506967a31654d2a1296053730ec6a8f816737f8e99445c2d279748f5)

\
The NEAR blockchain is capable of being split into 1000 shards, but uses dynamic re-sharding to use only what is needed according to demand. Because every shard only processes the transactions found in its chunk, chunks from different shards are processed in parallel to each other, increasing throughput, or TPS. This also means that each shard has its own local state.

### Validators and Doomslug

So, if each shard has its own local state, what does the processing in each shard and how can the local states of shards unify into a global state for the NEAR blockchain?\
Well, validator nodes selected by the TPoS algorithm are responsible for processing shards!\
The TPoS algorithm assigns validators at least one shard. Validators then process their chunks into local shard states. The TPoS algorithm then assigns block validators the responsibility of computing the global state of the NEAR blockchain, based on the local state of each shard part of the network, and creating a block from the computation.\
NEAR uses a mechanism called Doomslug to allow block validators to (i) gather shard states, (ii) compute, (iii) produce, and (iv) broadcast a block in under two seconds (the process commonly referred to as ‘finality’).

### Sharding on NEAR

So, we have now built up a description of NEAR’s Sharding: validator nodes are assigned shards. Each validator then processes all of the transactions found in the chunk of their shard, resulting in a local shard state. The network then takes all of the shard states and computes a global state.

### Sharding and the Blockchain Trilemma

Finally, what does this mean for the blockchain trilemma?\
ScalabilityAbout scalability, the combination of a potential TPS of 100,000 and a finality of under 2 seconds, renders the NEAR network highly scalable.\
SecurityAbout security, the probability that a single shard takes over decreases exponentially to the number of validators in a single shard. Additionally, Nightshade solves two known issues with Sharded blockchains: secure state validity and data availability.

* State validity ensures that shard states are valid even when the history of the shard is unknown.
* While Data availability ensures that data communicated across shards is valid and available.

How Nightshade solves these two issues will not be explained due to its complexity, but feel free to check out NEAR’s official document [here](https://near.org/papers/nightshade/#nightshade) for a description of it.\
In this document we explained how NEAR’s Nightshade allows validator nodes selected by the TPoS algorithm to process and validate transactions securely at scale. This also gave an answer to how NEAR has handled the Blockchain Trilemma.\
In the next doc we will explain how you can interact with the NEAR blockchain, using the easy-to-use NEAR Wallet.

### Sources

[Nightshade](https://near.org/papers/nightshade/#nightshade)

[Nightshade Whitepaper](https://near.org/downloads/Nightshade.pdf)

[Sharding](https://www.computerworld.com/article/3336187/sharding-what-it-is-and-why-so-many-blockchain-protocols-rely-on-it.html)

[Doomslug - 1 second Finality](https://near.org/blog/doomslug-comparison/)

### About Open Web Sandbox

A human-centric digital hub for everyone wishing to engage with projects building on top of the NEAR Protocol.

[Twitter](https://near.org/sandbox/) | [Website](https://twitter.com/OpenWebSandbox)

Written by [Jacopo Nuti](https://medium.com/@jacopo\_nuti).
