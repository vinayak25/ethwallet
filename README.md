# Ethereum Exchange Wallet

A Decentralized Ethereum Exchange application built on Solidity programming language and Ethereum Block chain.

## Features

1. Able to buy or sell tokens.
2. Deposit and Withdraw Ether.
3. Events Logging/Tracking.
4. Book maintained for buy or sell tokens.
5. Uses Linked List.

## Introduction

### What is Ethereum?

Ethereum is a **decentralized platform that runs smart contracts**: applications that run exactly as programmed without any possibility of downtime, censorship, fraud or third party interference.

These apps run on a custom built **blockchain, an enormously powerful shared global infrastructure that can move value around and represent the ownership of property.**

This enables developers to create markets, store registries of debts or promises, move funds in accordance with instructions given long in the past (like a will or a futures contract) and many other things that have not been invented yet, all without a middle man or counterparty risk.




### What are dApp(s)?

Decentralized applications (dApps) are applications that run on a P2P network of computers rather than a single computer. dApps, have existed since the advent of P2P networks. They are a type of software program designed to exist on the Internet in a way that is not controlled by any single entity.

- Decentralized applications don’t necessarily need to run on top of a blockchain network. BitTorrent, Popcorn Time, BitMessage, Tor, are all traditional dApps that run on a P2P network, but not on a Blockchain (which is a specific kind of P2P network).
- As opposed to simple smart contracts, in the classic sense of Bitcoin, that sends money from A to B, dApps have an unlimited number of participants on all sides of the market.



### Why dApp(s)?

On traditional server architectures, every application has to set up its own servers that run their own code in isolated silos, making sharing of data hard. If a single app is compromised or goes offline, many users and other apps are affected.

On a blockchain, anyone can set up a node that replicates the necessary data for all nodes to reach an agreement and be compensated by users and app developers. This allows user data to remain private and apps to be decentralized like the Internet was supposed to work.

![infographics2-02](C:\Users\vinayak sarawagi\Desktop\Extra\6th Sem\XML\infographics2-02.png)

### What is Solidity?

Solidity is a contract-oriented, high-level language for implementing smart contracts. It was influenced by C++, Python and JavaScript and is designed to target the Ethereum Virtual Machine (EVM).

Solidity is statically typed, supports inheritance, libraries and complex user-defined types among other features.

### What is Remix?

Browser-based IDE with integrated compiler and Solidity runtime environment without server-side components.

### What is Truffle?

Truffle is a development environment, testing framework and asset pipeline for Ethereum.



## How we did this?

Solidity being the official language of Ethereum is used to create Smart Contracts. Smart Contracts are just like any other program written to run on networks, difference is that they run on Ethereum Block Chain.

We created 3 Smart Contracts using Solidity given below:

1. ##### Exchange.sol

2. ##### FixedSupplyToken.sol

3. ##### Owned.sol

Using Truffle, we created Test Cases that were used to test our Smart Contracts. The name of 3 test cases files are given below:

1. ##### 01_fixed_supply_token.js

2. ##### 02_exchange_test.js

3. ##### 03_trading_simple.js

The Smart Contracts were developed on Web-based IDE, Remix offered by Ethereum.

All Smart Contracts were tested using test cases created in Truffle on Ethereum TestRPC Private Network.



## How this works?

### The Ethereum Blockchain

The structure of the ethereum blockchain is very similar to bitcoin's, in that it is a shared record of the entire transaction history. Every node on the network stores a copy of this history.

The big difference with ethereum is that its nodes store the most recent state of each smart contract, in addition to all of the ether transactions. (This is much more complicated than described, but the text below should help you get your feet wet.)

For each ethereum application, the network needs to keep track of the 'state', or the current information of all of these applications, including each user's balance, all the smart contract code and where it's all stored.

Bitcoin uses unspent transaction outputs to track who has how much bitcoin.

While it sounds more complex, the idea is fairly simple. Every time a bitcoin transaction is made, the network 'breaks' the total amount as if it was paper money, issuing back bitcoins in a way that makes the data behave similarly to physical coins or change.

To make future transactions, the bitcoin network must add up all your pieces of change, which are classed as either 'spent' or 'unspent'.

Ethereum, on the other hand, uses accounts.

Like bank account funds, ether tokens appear in a wallet, and can be ported (so to speak) to another account. Funds are always somewhere, yet don’t have what you might call a continued relationship.


### What is Ethereum Virtual Machine?

With ethereum, every time a program is used, a network of thousands of computers processes it.

Contracts written in a smart contract-specific programming languages are compiled into 'bytecode', which a feature called the 'ethereum virtual machine' (EVM) can read and execute.

All the nodes execute this contract using their EVMs.

Remember that every node in the network holds a copy of the transaction and smart contract history of the network, in addition to keeping track of the current 'state'. Every time a user performs some action, all of the nodes on the network need to come to agreement that this change took place.

The goal here is for the network of miners and nodes to take responsibility for transferring the shift from state to state, rather than some authority such as PayPal or a bank. Bitcoin miners validate the shift of ownership of bitcoins from one person to another. The EVM executes a contract with whatever rules the developer initially programmed.

Actual computation on the EVM is achieved through a stack-based bytecode language (the ones and zeroes that a machine can read), but developers can write smart contracts in high-level languages such as Solidity and Serpent that are easier for humans to read and write.

## Functions Explained

1. ##### getBalance(string symbolName)

   ​	Used to get the Balance of the remaining Tokens.

2. ##### hasToken(string symbolName)

   ​	Used to check if a particular user "symbolName" has token or not.

3. ##### getBuyOrderBook(string symbolName)

   ​	Used to retrieve the ledger book of the "Buy" requests of a particular user "symbolName". 

4. ##### getSellOrderBook(string symbolName)

   ​	Used to retrieve the ledger book of the "Sell" commands of a particular user "symbolName".

5. ##### getEthBalanceInWei()

   ​	Used to get the balance of Ether in Wei.

6. ##### buyToken(string symbolName, uint priceInWei, uint amount)

   ​	Used to post a "Buy" request to a particular user "symbolName" for a "amount" of tokens 			for a price "priceInWei".

7. ##### withdrawToken(string symbolName, uint amount)

   ​	Used to withdraw certain number of "amount" token(s) from a particular user "symbolName" account.

8. ##### depositToken(string symbolName, uint amount)

   ​	Used to deposit "amount" Token(s) to a particular user "symbolName". 

9. ##### cancelOrder(string symbolName, bool isSellOrder, uint priceInWei, uint offerKey)

   ​	Used to cancel the order request received for user "symbolName".

10. ##### addToken(string symbolName, address erc20TokenAddress)

   ​	Used to add a new token user "symbolName" with a assigned address "erc20TokenAddress".		

11. ##### withdrawEther(uint256 amountInWei)

    ​	Used to withdraw Ether amounting to "amountInWei".

12. ##### depositEther()

    ​	Used to deposit Ether.

13. ##### sellToken(string symbolName, uint priceInWei, uint amount)

    ​	Used to sell "amount" number of token(s) to a user "symbolName" for a price of "priceInWei".


## Requirements

1. Remix IDE

2. Truffle Framework

3. Node.js

4. Ethereum TestRPC Network

5. Geth for Ethereum

6. Meta Mask or Mist

7. Private Network using following genesis.json

   ```json
   {
     "coinbase"   : "0x0000000000000000000000000000000000000001",
     "difficulty" : "0x00020",
     "extraData"  : "",
     "gasLimit"   : "0x8000000",
     "nonce"      : "0x0000000000000042",
     "mixhash"    : "0x0000000000000000000000000000000000000000000000000000000000000000",
     "parentHash" : "0x0000000000000000000000000000000000000000000000000000000000000000",
     "timestamp"  : "0x00",
     "alloc": {
           "7df9a875a174b3bc565e6424a0050ebc1b2d1d82": { "balance": "300000" },
           "0x563E223eFBE1811631e82fb1DAaD1070AeDFd315": { "balance": "4000000000000000000000000000000000000000000000" }
       },
     "config": {
           "chainId": 15,
           "homesteadBlock": 0,
           "eip155Block": 0,
           "eip158Block": 0
       }
   }
   ```



## Future Works

1. Creating a Graphical User Interface(GUI) for easy interaction with user/client.
2. Can be deployed on Rinkeby Test Network or Main Ethereum Network.
3. Can be used for Initial Coin Offerings(ICOs) - a Cyptocurrency crowd funding.



## Conclusion

We successfully compiled and ran the Solidity Programs which offer the main back-end of the application.
