# BLOCKCHAIN DEVELOPMENT Q&A

## TABLE OF CONTENTS

- [BASICS](#basics)
  - What is the EVM?
  - What is an ABI?
- [SOLIDITY](#solidity)
  - What is a Solidity?
  - What does Contract-Oriented mean?
  - ERC standards
- [FRAMEWORKS](#frameworks)
  - Brownie
  - Truffle
  - Hardhat
  - Truffle vs Hardhat
- [INFRASTRUCTURE](#infrastructures)
  - Infura
  - Moralis

<a name="basics"/>

## BASICS

### What is the EVM?

The Ethereum Virtual Machine (EVM) is a powerful, sandboxed virtual stack embedded within each full Ethereum node, responsible for executing contract bytecode. Contracts are typically written in higher level languages, like Solidity, then compiled to EVM bytecode.

This means that the machine code is completely isolated from the network, filesystem or any processes of the host computer. Every node in the Ethereum network runs an EVM instance which allows them to agree on executing the same instructions.

In other words, it's the environment in which all Ethereum accounts and smart contracts live. At any given block in the chain, Ethereum has one and only one 'canonical' state, and the EVM is what defines the rules for computing a new valid state from block to block

### What is an ABI?

ABI (Application Binary Interface) is an interface between two program modules, often between operating systems and user programs. In the ethereum blockchain, the ABI is an interface that allows humans to interact with the bytecode of deployed smar contracts.

Smart contracts written in high-level languages like Solidity or Vyper need to be compiled in EVM executable bytecode; when a smart contract is deployed, this bytecode is stored on the blockchain and is associated with an address. For Ethereum and EVM, a smart contract is just this sequence of bytecode. To access functions defined in high-level languages, users need to translate names and arguments.

ABI defines the methods and structures used to interact with the binary contract, just like API does but on a lower-level.
<a name="solidity"/>

## SOLIDITY

### What is Solidity?

Solidity is high-level programming language used to create Smart Contracts that automate transactions on the blockchain. After being proposed in 2014, the language was developed by contributors to the Ethereum project. The language is primarily used to create smart contracts on the Ethereum blockchain and create smart contracts on other blockchains.

Solidity is similar to JavaScript. It also shares similar characteristics to the programming languages C++ and Python.

Solidity is statically typed, with support for inheritance, libraries, and complex user-defined types.

Solidity is the First Contract-Oriented Language.

### What does Contract-Oriented mean?

As the native language of Ethereum, Solidity has built-in commands, to access a part of the blockchain. For example, a timestamp or address of a particular block.

A contract-oriented language differs from largely object-oriented languages like Java and C++ in that its emphasis is on contracts and functions. Solidity is typed statically. It also supports libraries, inheritance, and other user-defined features which tend to be more complex. The language compiles all the instructions into a sandbox of bytecode so that these instructions can be read and interpreted in the Ethereum network.

### ERC standards

ERC (Ethereum Request for Comments) means the protocol proposal submitted by Ethereum developers. The ERC contains technical and organizational precautions and standards. The number after ERC is the number of the proposal. The most common ERC standards are ERC-20 and ERC-721.

#### ERC-20 Ethereum fungible tokens

It is currently the most widely known standard. It was born in 2015 and was officially standardized in September 2017. The agreement specifies a set of basic interfaces for **fungible tokens**: it stipulates that an ERC-20 Token needs to have its name, symbol, total supply, and other functions including transfer and remittance.

This enables smart contracts (tokens) to share a common set of standards. For example, to enable a token to define its total supply of tokens, “totalSupply” is used, instead of “totalNumber” or “totalTokens”. Compliance to the standard avoids confusion and enables tokens to interact with wallets, exchanges and different smart contracts smoothly without running into issues due to individual token differences.

The set of functions defined by the ERC-20 standard are:

```
totalSupply - get the total token supply
balanceOf - get the account balance of account address
transfer - send amount of tokens
transferFrom - define where the tokens are transfering from
approve - allow tokens to be withdrawn from sending address
allowance - returns the remaining tokens of the address
```

- Source: https://info.etherscan.com/what-is-erc20-token/
- EIP: https://eips.ethereum.org/EIPS/eip-20

#### ERC-721 non-fungible tokens

It is also a well known standard since it is related to NFT. The ERC-721 standard stipulates that all tokens that meet the standard must have a unique Token ID. Based on that, each Token is unique.

Unlike ERC-20, ERC-721 tokens are non-fungible; each and every ERC-721 token has its own unique value and is to be treated individually.

Think of currency: for example, each ERC-20 token can be compared to a $5 bill where you can exchange one $5 bill with another $5 bill without any difference in value. In the case of ERC-721, think of the example of CryptoKitties. Each kitty is different in value, has individual traits, and is often treated as a collectible.

- Source: https://info.etherscan.com/what-is-erc721/
- EIP: https://eips.ethereum.org/EIPS/eip-721

#### ERC-1155 Multi Token Standard

While ERC-20 tokens are fungible and ERC-721 tokens non-fungible, ERC-1155 is a multi token standard - the same token contract may include any combination of fungible tokens, non-fungible tokens or semi-fungible tokens.

Fungible tokens work like currency. A $5 bill may be exchanged with another $5 bill without any difference in value. Non-fungible tokens such as CryptoKitties are unique. Each kitty is valued differently, has individual traits, and is often treated as a collectible.

A semi-fungible token works the same way as fungible tokens initially. It could be exchanged for another of the same token contract with no difference in value until a particular condition is met. From then on, it becomes non-fungible and cannot be simply exchanged with one another.

An example to think of is that of a ticket to watch Manchester United in a Premier League match. Before the match starts, the ticket could be exchanged for that of another Premier League match (with similar opponent quality) at the same value. After it ends, the same ticket could be of vastly different value depending on its owner. To some, it may represent a historic moment in their life and is extremely valuable as memorabilia. To others, it may be one of many or even represent an occasion to forget. In this way a ticket that was once fungible with others later becomes non-fungible.

- Source: https://info.etherscan.com/what-is-erc1155-token/
- EIP: https://eips.ethereum.org/EIPS/eip-1155

<a name="frameworks"/>

## FRAMEWORKS

### Brownie

complete

### Truffle

complete

### Hardhat

complete

### Truffle vs Hardhat

complete

<a name="infrastructures"/>

## INFRASTRUCTURES

### Infura

complete

### Moralis

complete