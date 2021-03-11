# Modules

*Basic modules are the LEGOs for MathChain applications.*

## SecretStore

Secret Store allows user to store on the blockchain a fragmented ECDSA key which retrievals are controlled by a SmartContract. All of this, running under a Threshold System that makes nodes unable to read the keys on it’s own and makes your documents or secrets totally safe.

It will bring privacy capability to MathChain.

## DID

A Decentralized Identifier (DID) is a new type of identifier that is globally unique, resolveable with high availability, and cryptographically verifiable.

MathChain DID is associated with account public keys, and can connect to service endpoints, for establishing secure communication channels.

## EVM

This is the Substrate's Ethereum compatibility module. It allows MathChain to run unmodified Ethereum dapps. Run a normal web3 application via the compatibility layer, using local nodes, where an extra bridge binary is acceptable. It is able to import state from Ethereum mainnet.

It also contains the basic tools to support EVM including block explorer, web3js support wallet etc.

It will power MathChain to be the EVM compatible layer 2 blockchain with high performance. And combine with small wallet, dappstore, datastore, it will bring more interesting applications to MathChain.

## Off-chain Worker

Off-chain Workers allows the processes that are too intensive or data that's too massive to be handled by specialized nodes on the network, all while storing the code for how to do the work on-chain to ensure participants are automatically kept up to date with the latest logic that their chain dictates.

## XCMP

XCMP (Cross-chain Message Passing) is the mechanism to route messages between parachains and parathreads. It supports a smart contract that exists on parachain A will route a message to parachain B in which another smart contract is called that makes a transfer of some assets within that chain.

It will make MathChain able to do cross-parachain message exchange.