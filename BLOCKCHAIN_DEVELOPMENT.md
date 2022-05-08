# BLOCKCHAIN DEVELOPMENT Q&A

## TABLE OF CONTENTS

- [BASICS](#basics)
  - What is the EVM?
  - What is an ABI?
- [SOLIDITY](#solidity)
  - What is a Solidity?
  - What does Contract-Oriented mean?
  - ERC standards
    - ERC-20 Ethereum fungible tokens
    - ERC-721 non-fungible tokens
    - ERC-1155 Multi Token Standard
- [DESIGN PATTERNS](#design-patterns)
  - Access Restriction
  - Emergency Stop
  - State Machine
  - Withdrawal
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

<a name="design-patterns"/>

## DESIGN PATTERNS

### Access Restriction

**Motivation**

Restrict the access to certain contract functionalities.

**Use cases**

- your contract functions should only be callable under certain circumstances.
- you want to apply similar restrictions to several functions.
- you want to increase security of your smart contract against unauthorized access.

**Implementation**

1. Create a modifier with the condition to the access restriction. For example, `onlyOwner` or `onlyBy(address _account)` and use the **Guard Check pattern** (check for the required circumstances and throws an exception, in case they are not me).
2. Use that modifier in the target functions.

**Code example**

```
contract ExampleAccessRestriction {
    address public owner = msg.sender;
    uint public lastOwnerChange = now;

    modifier onlyBy(address _account) {
        require(msg.sender == _account, "Access denied");
        _;
    }

    modifier onlyAfter(uint _time) {
        require(now >= _time, "Access denied due to time condition");
        _;
    }

    modifier costs(uint _amount) {
        require(msg.value >= _amount, , "Incorrect amount parameter");
        _;
        if (msg.value > _amount) {
            msg.sender.transfer(msg.value - _amount);
        }
    }

    function changeOwner(address _newOwner) public onlyBy(owner) {
        owner = _newOwner;
    }

    function buyContract() public payable onlyAfter(lastOwnerChange + 4 weeks) costs(1 ether) {
        owner = msg.sender;
        lastOwnerChange = now;
    }
}
```

**Helpful links**

- `Ownable.sol` contract from OpenZeppelin: https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol
- https://fravoll.github.io/solidity-patterns/access_restriction.html

### Emergency Stop

**Motivation**

A specific user (owner) will have the option to disable critical contract functionality in case of an emergency.

**Use cases**

`Pausable contract` from the _OpenZeppelin_ library.

**Implementation**

1. An `isStopped` or `isPaused` boolean state variable represents if the contract is stopped or not.
2. With `stopContract` or `resumeContract` functions, authorized entities could change that boolean's value.
3. Modifiers such as `onlyWhenStopped` and `stoppedInEmergency` could be used in critical functions.

**Code example**

```
contract ExampleEmergencyStop {
  bool paused = false;

  constructor(){ }

  modifier onlyOwner {
    require(msg.sender == owner);
    _;
  }

  modifier isPaused {
   require(paused);
   _;
  }

  modifier notPaused {
   require(! paused);
   _;
  }

  function pauseContract() public onlyOwner notPaused {
     paused = true;
  }

  function unpauseContract() public onlyOwner isPaused {
     paused = false;
  }

  function depositEther() public notPaused { }

 function emergencyWithdrawal() public isPaused { }
}
```

**Helpful links**

- https://fravoll.github.io/solidity-patterns/emergency_stop.html
- https://dev.to/jamiescript/design-patterns-in-solidity-1i28#emergency

### State Machine

**Motivation**

A contract that has to transition several states during its life cycle. At each of the states the contract has to behave in a different way and provide different functionality to its users.

**Use cases**

Auctions, crowdfunding, loans, gambling, and many more. Even the Solidity documentation acknowledges its conventionality by listing it as one of the common patterns.

**Implementation**

There are different ways one state can transition into another. Sometimes a state ends with the end of a function, another time the state is supposed to transition after a specified amount of time.

1. Representation of the stages: an enum variable called Stages is used to model the different stages.
2. Interaction control for the functions: a function modifier is used to restrict functions in the contract (it checks if the contract stage is equal to the required stage before executing the called function).
3. Stage transitions. There are several ways to manage transitions: sometimes it is related to specific business logic, and sometimes it is related to automatic timed transitions. Generally a `transitionAfter()` modifier is used to trigger the transition after certain functions.

**Code example**

```
contract Pool {
  enum Stages {
        Initialize,
        Contribute,
        Collect,
  }

  constructor(){ }

  Stages public stage = Stages.Initialize;

  modifier atStage(Stages _stage) {
        require(
            stage == _stage,
            "Wrong pooling stage. Action not allowed."
        );
        _;
   }

  function init(...) external atStage(Stages.Initialize) {
        ...
        currentStage = Stages.Contribute;
  }

  function contribute(...) external atStage(Stages.Contribute) {
        ...
        if (hasContributionThresholdReached) {
            currentStage = Stages.Collect;
        }
  }

  function collect(...) external atStage(Stages.Collect) { }
}
```

**Helpful links**

- https://soliditydeveloper.com/design-pattern-solidity-stages
- https://fravoll.github.io/solidity-patterns/state_machine.html

### Withdrawal

**Motivation**

A safe way to withdraw funds.

**Use cases**

Any situation where funds need to be distributed to more than one account. It could be an air drop, a dividend, a crowdfunding that refunds some tokens or something else.

**Implementation**

The `withdrawFunds` function talks with one untrusted address at a time. That means each befeficiary claims their own reward. This is a good practice because:

- we avoid `for` loops. If there are many beneficiaries, the transaction could become very expensive and not be processed.
- we avoid `onlyOwner`. If something happens to that single point of failure, the withdrawal function wont be able to execute.
- the befeficiary pays the gas for their own transaction.

**Code example**

```
contract WithdrawalPattern {

  mapping(address => uint) public balances;

  constructor(){ }

  function sendFunds(){
    balances[msg.sender] += msg.value;
  }

  function withdrawFunds(uint amount) public returns(bool success) {
    require(balances[msg.sender] >= amount);// guards up front
    balances[msg.sender] -= amount;         // optimistic accounting
    msg.sender.transfer(amount);            // transfer
    return true;
  }
}
```

**Helpful links**

- https://blog.b9lab.com/the-solidity-withdrawal-pattern-1602cb32f1a5

<a name="frameworks"/>

## FRAMEWORKS

### Brownie

- Github: https://github.com/eth-brownie
- Docs: https://eth-brownie.readthedocs.io/en/stable/

**Brownie** is a Python-based development and testing framework for smart contracts targeting the Ethereum Virtual Machine.

Features

- Full support for Solidity and Vyper.
- Contract testing via pytest, including trace-based coverage evaluation.
- Property-based and stateful testing via hypothesis.
- Powerful debugging tools, including python-style tracebacks and custom error strings.
- Built-in console for quick project interaction.
- Support for ethPM packages.

### Truffle

- Web: https://trufflesuite.com/

**Truffle** is a development environment, testing framework and asset pipeline for blockchains using the Ethereum Virtual Machine (EVM). With Truffle, you get:

- Built-in smart contract compilation, linking, deployment and binary management.
- Automated contract testing for rapid development.
- Scriptable, extensible deployment & migrations framework.
- Network management for deploying to any number of public & private networks.
- Package management with EthPM & NPM, using the ERC190 standard.
- Interactive console for direct contract communication.
- Configurable build pipeline with support for tight integration.
- External script runner that executes scripts within a Truffle environment.

### Hardhat

- Web: https://hardhat.org/

**Hardhat** is a development environment to compile, deploy, test, and debug your Ethereum software.

Hardhat comes built-in with **Hardhat Network**, a local Ethereum network designed for development. Its functionality focuses around Solidity debugging, featuring stack traces, console.log() and explicit error messages when transactions fail.

**Hardhat Runner**, the CLI command to interact with Hardhat, is an extensible task runner. It's designed around the concepts of tasks and plugins. Every time you're running Hardhat from the CLI you're running a task. E.g. `npx hardhat compile` is running the built-in compile task.

A lot of Hardhat's functionality comes from plugins, and, as a developer, you're free to choose which ones you want to use.

### Truffle vs Hardhat

| TRUFFLE              | HARDHAT                                           |
| -------------------- | ------------------------------------------------- |
| more rigid structure | more flexible (run custom scripts, using plugins) |
| default web.js       | default ethers.js                                 |
| no console.log       | console.log inside solidity                       |
| no stack traces      | stack traces                                      |

<a name="infrastructures"/>

## INFRASTRUCTURES

### Infura

- Web: https://infura.io/

Infura is a Web3 Development Platform. It provides the tools and infrastructure that allow developers to easily take their blockchain application from testing to scaled deployment. Mainly, it offers an Ethereum API and IPFS API.

### Moralis

- Web: https://moralis.io/

Moralis is a Web3 Development Platform. It provides managed backend for blockchain projects. Automatically syncing the balances of your users into the database, allowing you to set up on-chain alerts, watch smart contract events, build indexes, and so much more.
