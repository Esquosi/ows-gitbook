---
description: OWS Education / NEAR Basics
cover: ../../../.gitbook/assets/Announcement Banner (Twitter) (1).png
coverY: 0
---

# NEAR and TPoS

Welcome to the third document of the ‘NEAR Basics’ batch, part of OWS Education, created by the OWS team. In this doc we will look into how NEAR’s Thresholded Proof of Stake algorithm works, and how it overcomes the decentralisation part of the Blockchain Trilemma.\


{% embed url="https://youtu.be/rgWX_5P6EsY" %}

### Consensus algorithms

Proof-of-Stake is the chosen consensus protocol on NEAR that enables validator nodes to reach consensus about transactions. Check out our video on PoS here if you want to know how this family of algorithms work. More specifically, NEAR uses a Thresholded PoS election mechanism to randomly select its validator nodes.\
Let’s run through how the TPoS selection process works.\


### Node selection process

The selection process for validator nodes on the NEAR network happens once every 12-hour epoch. For each epoch n of time, 1,474,560 seats must be allocated to a set of validator nodes - which on NEAR are called ‘witnesses’. Seats give witnesses various responsibilities, some of which are to process transactions, create, and sign blocks.\
![TPoS .png](https://codahosted.io/docs/hfGgtxGDfQ/blobs/bl-GYdA8KZozj/f2037e41f188dfdf5ba231a677ae0141ada87adc43ed0aa5fe4448a93b979bb24e46acfc36e29e9b9898e0859838825f2d08405df3963fb01993431d4b9c5320d9c4cb43e26d22f90ec78c749b5b50469304e6906d83407d4112f0d36d230919670a8b4a)\
\
The TPoS algorithm is responsible for pseudorandomly computing the selection of witnesses. Essentially, every 12 hours the protocol reshuffles the network’s witnesses, randomly selecting new ones.\
So, how are witnesses actually selected?\


### How are witnesses selected?

Nodes that want to be selected as witnesses for epoch n+1 will submit a special transaction (StakeAction) indicating an amount of tokens staked, locking that amount in the transaction for three days. Based on the set of all special transactions submitted during epoch n, the TPoS algorithm will determine the minimum threshold of staked tokens needed to become a witness for epoch n+1. All nodes that are above the threshold will be selected as a witness, and some number of seats (out of the possible 1,474,560) relative to their staked amount will be allocated to them. Check out the [NEAR Explorer](https://explorer.near.org/) to see how many witnesses (validator nodes) are currently validating the NEAR network.\


### What do witnesses do?

Once the witnesses are selected, they will be responsible for verifying transactions and signing blocks for the following epoch (n+1), receiving block rewards and transaction fees as compensation for their contribution to the network.\
Let’s now talk about decentralisation and security in TPoS!\


### TPoS and Decentralisation

About decentralisation, because the reward for validating blocks is proportional to the stake, meaning that two accounts with 10 tokens staked each, earn the same rewards as one account with 20 tokens staked, there is no incentive to pool computational resources or stake, so the decentralisation of validator nodes is maintained.The network also does not require nodes to have high performance hardware to run as validator nodes. Maintaining low barriers to entry.\


### TPoS and Security

About security, to rewrite a block or perform a long range attack, a malicious actor must know the private keys of the witnesses that hold 2/3 of the stake for the previous 2 epochs. The probability of this happening is negligible, rendering the TPoS algorithm highly secure.  \
In this document we discussed how TPoS is used by the NEAR network to select validator nodes. We also briefly explained how TPoS ensures the consensus process is decentralised and secure.\
In the next doc we will look at how the NEAR network uses Nightshade as a Sharding mechanism to process and store transactions at scale.

### Sources:

[Article](https://near.org/blog/thresholded-proof-of-stake/)

[NEAR Wiki](https://wiki.near.org/resources/faq/integrator-faq#validators)

### About Open Web Sandbox

A human-centric digital hub for everyone wishing to engage with projects building on top of the NEAR Protocol.

[Twitter](https://near.org/sandbox/) | [Website](https://twitter.com/OpenWebSandbox)

Written by [Jacopo Nuti](https://medium.com/@jacopo\_nuti).
