# BLOCKCHAIN Q & A

## TABLE OF CONTENTS

- [BASICS](#basics)
  - What is a blockchain?
  - What are the characteristics of a blockchain?
  - What are the characteristics of the Bitcoin blockchain?
  - What is Bitcoin?
- [SMART CONTRACTS](#smart-contracts)
  - What is a Smart Contract?
  - What does turing completeness mean?
  - Is Bitcoin turing complete?
  - What about Ethereum and other blockchains, are they turing complete?
  - Blockchains with or without Smart Contracts
- [ORACLES](#oracles)
  - What is the Oracle problem?
  - What is an Oracle?
  - What is a Hybrid Smart Contract?

<a name="basics"/>

## BASICS

### What is a blockchain?

A blockchain is a specific type of database: it stores data in blocks that are chained togehter.

### What are the characteristics of a blockchain?

It depends on the implementation. A blockchain could be:

- **Centralized or decentralized.** If there is only one node in the network (the entity that validates the transactions and writes the data to storage), it is centralized. The more number of nodes, the more decentralized the blockchain is.
- **Open or closed.** If the blockchain allows anyone to connect and run a node, then it is open. The more regulations and bans there are for running a node, the more closed the blockchain is.
- **Public or private.** Some information on the blockchain may be public, while some may be private. For example, on the Bitcoin blockchain, the balance of each wallet and its transaction history are public. In contrast, on the Monero blockchain, they are private.
- **Mutable or immutable.** Immutability means that the data entered is irreversible. While it can be argued that there is no absolute immutability, each blockchain uses different mechanisms to make mutability as difficult as possible. For example, bitcoin uses cryptography and the Proof of Work consensus method to make it very very difficult to mutate its blockchain data.

### What are the characteristics of the Bitcoin blockchain?

The goal of the Bitcoin blockchain is to be an open and censorship-resistant protocol (communication system). Therefore, it has the following characteristics: it is a decentralized open and public blockchain that uses cryptography and PoW consensus method to aim immutability.

### What is Bitcoin?

- It is a protocol (see previous answer), a communication system that aims to be decentralized and allow p2p transactions.
- It is an application. It is the first app buildt with this protocol.
- It is also the monetary unity that is used in the app.

<a name="smart-contracts"/>

## SMART CONTRACTS

### What is a Smart Contract?

- It is a contract in the sense that it is an agreement between the parties that interact with it.
- It is "smart" in the sense that it is a program stored in a blockchain. The transactions that happen in it are processed by the blockchain, which means that, in a decentralized and open blockchain, they can be executed automattically without a centralized authority.

### What does turing completeness mean?

Turing completeness refers to any device, system or program (such as a Smart Contract) which in theory can (for the most part) solve any reasonable computational problem, given enoght physical resources.

### Is Bitcoin turing complete?

- It is said that the Bitcoin scripting language is not turing complete because it does not have loops, branching and stuff. But there is a debate among this concept.

### What about Ethereum and other blockchains, are they turing complete?

- Some people say for example, that Ethereum is turing complete or, in other words, that the Ethereum blockchain is a distributed turing machine. It is because Solidity language can perform **looping** and **branching** statements as well as **local state** storage. This functionality is important to have in order to implement most non-trivial computer programs.
- However, some people say Ethereum is not turing complete, because a programm cannot run forever, due to gas limits.

### Blockchains with or without Smart Contracts

From the above considerations, blockchains could be classified according to whether they are "turing complete" or not, or in other words, whether they have SC or not. This feature is important since SCs are programs that have many implementations. For example, generating another type of cryptocurrency called Tokens.

- Without SC: the network processes and stores transaction data in its native currency.
  - Examples:BTC, BCH, LTC, XRP.
- With SC: the network, besides that, also stores and execute programs called Smart Contracts. With SC, a different type of cryptocurrencies could be created: the tokens.
  - SC blockchain examples: ethereum, bsc, polkadot, kusama, polygon, avalanche, cosmos, terra, cardano.
  - Token examples: DAI, USDC, USDT, UNI, CAKE, AAVE, MANA, COMP, WBTC.

<a name="oracles"/>

## ORACLES

### What is the Oracle problem?

Some SC applications need real world data (for example, the price of an asset, the identity of a person or an educational certificate). In order to fulfill that requirement, they use Oracles. The Oracle problem consist on how to achieve descentralization in an oracle.

### What is an Oracle?

An Oracle is a device that bring world data into a blockchain or execute some computation process outside the blockchain.
