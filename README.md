# sample-nft-storage


> First steps

Developing apps and experiences for NFTs requires a bit of background knowledge and experience with blockchain smart contracts. This guide will walk through interacting with a simple "hello world" smart contract from JavaScript, just to get acquainted with the tooling and libraries we'll use in later guides.

> Smart contracts

A smart contract is any program that runs on a blockchain and uses a blockchain's ability to track state, process transactions, and interact with addresses. In the case of Ethereum, smart contracts can be written in Solidity or Vyper. We'll cover smart contract development with Solidity in other topics on NFT School, but in this tutorial, we'll focus on interacting with smart contracts that already exist.


> Blockchain environments

* mainnet
The mainnet is the official production network. It is considered the source of truth, and its tokens can be exchanged for "real world" money in various ways. As you might imagine, using the mainnet for development and testing is an expensive proposition.

* devnet
To make smart contract development practical, you can run a local development network, or devnet. This is usually a kind of lightweight simulator that has the same API as the mainnet, but runs on your development machine for fast feedback and iteration. The most popular devnets are bundled into blockchain development frameworks and provide quality-of-life features such as console logs and stack traces. For Ethereum, the main devnets are Ganache (opens new window), which is part of the Truffle Suite (opens new window), and the Hardhat network (opens new window), which is integrated into the Hardhat framework (opens new window).

* testnet
Because devnets are a simplified simulation of the real network, they don't always behave in quite the same way. This is a good thing when you want fast development cycles, but not so great when you want to know how your contract will actually work on mainnet.

For that, you can deploy and run your contract on a test network, or testnet. These networks generally run the same code as the mainnet, but they have separate blockchain states and may be configured differently in various ways.


> Building our app

#Download the Ethers JavaScript library
Now that we've created a testnet wallet and filled it with test ETH ready to fuel transactions on the blockchain, we are ready to do some development.

First make an empty directory named hello-eth:
mkdir hello-eth
cd hello-eth


To interact with Ethereum, we need a JavaScript library that makes JSON-RPC API (opens new window)calls. For smart contract interactions, the two main contenders are web3.js (opens new window)and Ethers (opens new window). We're using Ethers for this guide, since it's a bit easier for getting started.

# Install and run http-server
Now you'll need to run a web server. If you haven't done so already, install Node.js (opens new window). Then you can install and run http-server (opens new window)to serve what we've created:

npm install --global http-server
http-server .

The web server should provide URLs for you to copy/paste into your browser:

Starting up http-server, serving .
Available on:
  http://127.0.0.1:8081
  http://192.168.2.10:8081
  http://192.168.86.24:8081
  
  
Visiting any of these URLs in your browser will produce the message Hello, Hardhat!, which means that Ethers has made a call to the Greeting smart contract that Hardhat deployed to the Ropsten testnet.


# Conclusion

Great work! Now you have an easy route to interacting with smart contracts with JavaScript right in your browser, a Ropsten Testnet account loaded with ETH for fuel, and a general outline for building apps on top of Ethereum

> Source

https://nftschool.dev/tutorial/




