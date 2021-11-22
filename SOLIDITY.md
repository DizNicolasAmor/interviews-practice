# SOLIDITY Q&A

## TABLE OF CONTENTS

- [BASICS](#basics)
  - What is a Solidity?

<a name="basics"/>

## BASICS

### What is Solidity?

Solidity is high-level programming language used to create Smart Contracts that automate transactions on the blockchain. After being proposed in 2014, the language was developed by contributors to the Ethereum project. The language is primarily used to create smart contracts on the Ethereum blockchain and create smart contracts on other blockchains.

Solidity is similar to JavaScript. It also shares similar characteristics to the programming languages C++ and Python.

Solidity is statically typed, with support for inheritance, libraries, and complex user-defined types.

Solidity is the First Contract-Oriented Language.

### What is the EVM?

The Ethereum Virtual Machine (EVM) is a powerful, sandboxed virtual stack embedded within each full Ethereum node, responsible for executing contract bytecode. Contracts are typically written in higher level languages, like Solidity, then compiled to EVM bytecode.

This means that the machine code is completely isolated from the network, filesystem or any processes of the host computer. Every node in the Ethereum network runs an EVM instance which allows them to agree on executing the same instructions.

In other words, it's the environment in which all Ethereum accounts and smart contracts live. At any given block in the chain, Ethereum has one and only one 'canonical' state, and the EVM is what defines the rules for computing a new valid state from block to block

### What is an ABI?

ABI (Application Binary Interface) is an interface between two program modules, often between operating systems and user programs. In the ethereum blockchain, the ABI is an interface that allows humans to interact with the bytecode of deployed smar contracts.

Smart contracts written in high-level languages like Solidity or Vyper need to be compiled in EVM executable bytecode; when a smart contract is deployed, this bytecode is stored on the blockchain and is associated with an address. For Ethereum and EVM, a smart contract is just this sequence of bytecode. To access functions defined in high-level languages, users need to translate names and arguments.

ABI defines the methods and structures used to interact with the binary contract, just like API does but on a lower-level.

### What is web3?

Complete

### What is brownie?

Complete

### What is an truffle?

Complete

### What is SafeMaths and why to use it?

Complete

TODO

- global variables
- modifiers
- testnet
- faucets
- keeccack 256
- ERC20
- infura
- moralis
- truffle
- hardhat
- truffle vs hardhat
