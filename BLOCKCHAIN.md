# BLOCKCHAIN Q&A

## TABLE OF CONTENTS

- [BASICS](#basics)
  - What is a blockchain?
  - What are the characteristics of a blockchain?
  - What are the characteristics of the Bitcoin blockchain?
  - What is Bitcoin?
- [STRUCTURE](#structure)
  - What is a node in a blockchain?
  - How do the nodes interact in a decentralized blockchain?
  - What happens to the blockchain if a node goes down?
  - What happens if a node acts maliciously when processing the transactions?
  - Why should nodes act benevolent?
  - What is a block in a blockchain?
  - What information does a block contain?
  - What is the Genesis block?
  - How a block is created?
  - Why the nodes (miners) process the transactions in open blockchains?
- [KEYS](#keys)
  - What is the Private key?
  - What is the Public key?
  - What is a transaction signature?
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
  - Examples of Oracles
- [DAO](#dao)
  - What is a DAO?
  - Examples of DAOs
- [GAS](#gas)
  - What is Gas a blockchain like Ethereum?
  - Concepts related to Gas

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

<a name="structure"/>

## STRUCTURE

### What is a node in a blockchain?

It is a single instance in a decentralized system. It is one of the servers that runs the blockchain software.

### How do the nodes interact in a decentralized blockchain?

In a decentralized blockchain, the nodes participate generating the blocks that contain the transactions. They also validate the blocks that other nodes generate. In order to add a block to the blockchain, more than the half of the nodes must agree that the block information is valid.

### What happens to the blockchain if a node goes down?

If the blockchain contains several nodes and one of them goes down, it does not affect the blockchain. The blockchain will persist so long as there is at least one node always running.

On the contrary, if there is only one node in a blockchain and it goes down, in consequence the blockchain wont persist.

### What happens if a node acts maliciously when processing the transactions?

It depends on the blockchain. In general, the other nodes will ignore it, kick it out or maybe punish it.

### Why should nodes act benevolent?

In Bitcoin and other blockchains there are economic incentives for the nodes to act benevolent instead of maliciously.

### What is a block in a blockchain?

In a blockchain, each block is the unit where the information is stored.

### What information does a block contain?

It contains list of records (called transaction data), and metadata: a timestamp (UNIX time), a cryptographic hash of previous block (hash converts the previous block data into a fixed length of random data) and its current hash. It can contain more information, such as metadata.

- **Transaction data (or block body)**: it is basically a list of recordsor transactions. Toward efficiency, data inside a block is stored in the form of a Merkle tree.
- **Block header**: it contains metadata: data that describes other data, serving as an informative label. The header contains the following information.
  - Timestamp (UNIX time): it is a date and time value that tells at which time the block was created.
  - Nonce: it is an arbitrary number used only once in a cryptographic communication.
  - Previous hash (or Hash to the previous block). A hash is a unique fixed length string meant to identify a piece of data. They are created by placing said data into a hash function. Bitcoin uses SHA 256 while Ethereum uses Keccak-256 algorithms respectively.
  - Merkle Root (it will be the hash that the next block will set as "Previous hash").
  - Version: describes the structure of the data inside the block. This is used so that computers can read the contents of each block correctly.

### What is the Genesis block?

It is the first block in a blockchain. Its value is always hard coded. Since no previous block existed before it, hence the previous hash remains ‘0’ in this case.

### How a block is created?

The "miners" (nodes in the network) create the blocks. In each block, they include the transactions they want plus one coinbase (generation) transaction to their address. It is to note that for a block to be accepted by the network it needs to contain only valid transactions: inputs that are not yet spent, inputs that have the valid ammount, signature that verifies ok, etc..

### Why the nodes (miners) process the transactions in open blockchains?

They get paid for mining blocks in the blockchain native token.

<a name="keys"/>

## KEYS

### What is the Private key?

- The Private key, also known as "secret key" is like a password —a string of letters and numbers— that allows you to access and manage your crypto funds.
- The Private key is needed to make the transactions. Whoever has the Private key of a wallet, has access to its funds. That is why it is so important that the Private key is secure.
- **Not you keys, not your coins**: is a famous expression in the crypto ecosystem. It means that only if you have the Private key, then you really own the coins. On the other hand, if you have coins in a custodial service that does not give you the Private key, then you don't really own those coins because you could be censored by that custodial third party.

### What is the Public key?

- It is derived from your Private key, which makes them a matched pair.
- It is also a string of letters and numbers. This string is the direction where you receive the transactions.
- The Public key is also used to verify that a transaction came from you.

### What is a transaction signature?

The user that makes a transaction signs that transaction by their private key being hashed with their transaction data. With that signature, anyone can then verify this transaction hash with the user's public key.

In some blockchains like Bitcoin and Ethereum, that information is open: all public key and transaction information is available for anyone to see.

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

### What is a Hybrid Smart Contract?

It is a Smart Contract that includes offchain elements. The Oracles, of course, use Hybrid SC among other programs.

### Examples of Oracles

- **Chainlink (LINK)**: Chainlink allows blockchains to securely interact with external data feeds, events and payment methods, providing the critical off-chain information such as financial markets, cryptocurrenciy prices, weather, sport results, IoT sensor readers.
- **UMA (UMA)**: Universal Market Access, is a protocol for the creation of synthetic assets based on the Ethereum (ETH) blockchain.
- **Augur (REP)**: Augur (REP) is meant to harness the wisdom of the crowd through prediction markets on a protocol owned and operated by holders of the Ethereum-based Reputation token. In these markets users are said to be able to bet on the outcomes of events such as company performance, election results or even natural phenomena by purchasing shares that would either support or refute the proposed outcomes of such specified events.

<a name="dao"/>

## DAO

### What is a DAO?

A Decentralized Autonomous Organization (DAO) is an organization whose governance system is built on a decentralized blockchain. That means, the governance rules (token generation, token distribution, voting, decision making in general) are encoded in a Smart Contract.

### Examples of DAOs

- **Dash** is a blockchain, a cryptocurrency and a DAO because of its Governance and fund allocation system. It was created on May 2015 and it is still operational.
- **The DAO (organization)** was a Venture capital organization built in Ethereum in April 2016. It defunct in late 2016 due to hack.
- **Augur** is Prediction market dApp (Sports betting, finance, Insurance) built in Ethereum in July 2018 and still operational.
- **Steem** Data distribution, Social media, Name services, Industrial Steem March 2016 and still operational.

<a name="gas"/>

## GAS

### What is Gas a blockchain like Ethereum?

In Ethereum and other blockchains, in order to avoid spam and some hack attacks, every transaction pays a "gas fee" to node operators. Gas is a unit of computational measure. The more computation a transaction uses the more gas you have to pay for. The Gas could be payed in ether or other native token.

### Concepts related to Gas

- Gas: measure of computation use.
- Gas price: how much it costs per unit of gas. It changes all the time depending on the traffic: the higher the traffic, the higher the gas price. This is because users compete with each other with the fees they pay to miners.
- Gas limit: max amount of gas in a transaction.
- Transaction fee: Gas Used x Gas Price. For example: `21,000 gas x 1 GWEI (per gas) = 21,000 GWEI`
- GWEI: is the most commonly used unit of ether because "gas" prices are easily specified in it. For example, instead of saying that your gas costs 0.000000001 ETH, you can say your gas costs 1 GWEI.
