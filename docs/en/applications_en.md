# Applications

*Next we start to build decentralized apps with these LOGOs on MathChain.*

## MathSmartChainWallet

**MathSmartChainWallet = SecretStore + Off-chain Worker + DID**

MathWallet has supported more than 60 public chains, with over a million users so far, however we have never stopped thinking about the future of the blockchain world, and the most important issue is how to serve the mainstream users.

Smart Wallet is an area that MATH has always been researching, and we saw the value of Smart Wallet in lowering the barriers for new users to participate, there are some products that have done great in smart wallet field, such as Argent, Dapper, and MYKEY.

But we also saw some of the limitations of Smart Wallet today:

1. Account creation costs are high, because it need to create the mainnet contract for each new user.
2. Smart contract transaction has limitation in some scenarios, such as the exchange blocks the smart contract deposit, etc.
3. Difficulty for upgrading smart contract.

Thus, we are introducing a new generation of ‘Smart Chain Wallet’ which will address those problems by moving the logic of smart contract into MathChain.

In the design, distributed key management is powered by SecretStore. Social account verification is handled by Off-chain Worker in a decentralized way. And combine with DID, smartwallet is able to support namespace, spending limitation, social account recovery and lock/unlock functions.

## PolkaVault

**PolkaVault = SecretStore + Filecoin**

PolkaVault is the personal data vault for all users.

SecretStore module on MathChain allows us save the encrypted data on Filecoin storage service without any worries about our privacy. It moves computation and data storage off-chain while keeping the data ownership and permission control on-chain.

We will also able to share data with others through MathChain ecosystem. Data that no one will be able to read it without your permission (even node owners which is pretty important and was the handicap we had on previous schemes).

This scheme is GDPR friendly in order that no personal data or sensitive data is never deployed/uploaded to the blockchain, the user who encrypted it is the only one ho has the rights to share the document and the key session with others. The permissions are controlled on MathChain.

Since MathWallet is also the first batch of Filecoin Notaries, we will partnership with the best Filecoin storage service provider and bring Polkadot and Filecoin connected together.

A MathHub bridge will be built between MathChain and Filecoin, users only need to pay MATH and they will get storage space in Filecoin for private data. MathHub will handle the cross-chain token swap, etc.

This will also make data exchange market possible on MathChain in future.

Eventually, PolkaVault will be the data bank for everyone, and take the control of personal data back to user's own hands.

## MathSecretStore

**MathSecretStore = SecretStore + MathDappStore**

MathDappStore is the place to satisfy all the decentralized app needs and the entry for all DApp users. It lists 3000+ open-source dApps for 65 bockchains in 20 categories.

Most of the DApps in MathDappStore are open-source, which brings trust, but it also cause the fork issue. And currently this issue cannot be solved based on the current dappstore model.

Encrypt SmartContracts and create MarketPlaces with dApps giving developers the assurance that nobody will be able to read or copy their code. Only the security auditing team will be grant the decode access and publish their auditing results.

MathSecretStore will also become the world's first fully decentralized appstore, which MATH token will be used as governance token for rating, listing, indexing etc.

This will make those with dApp-designed businesses much more viable than apps in the Google Play Store and Apple App Store.

## MathHub

**MathHub = EVM + Off-chain Worker**

Currently there are normally 2 methods: PoA bridge and HTLC.

They have some limits:

1. Rely on a set of authorities.
2. Need multiple pools for different bridges.
3. Must go throught layer-1 network

For MathHub:

1. Bridge token as an intermediary asset which leverage Off-chain Worker mechanism to quickly move between different chains.
2. Wrapped cross-chain token and bridge token is able to swap use AMM DEX on each chain.
3. Incentive market maker to rebalancing of liquidity across the network.

## MathHub Rollup to Rollup Bridge

**MathHub Rollup to Rollup Bridge = MathHub + Rollup**

A rollup is a type of layer-2 solution that has become one of the cornerstones of the layer-1 scaling roadmap like Ethereum. Each rollup provides an execution environment that can process transactions in a similar way to layer-1 itself but at a fraction of the cost.

There are 2 requests we found in cross-rollup situation:

1. The duration of exits from rollups is very long
2. There is no cross-rollup protocols

But leverage MathHub's cross-chain function, we can:

1. Allow tokens to be quickly and easily sent from one rollup to the next
2. Enable fast-exits from rollups
3. Support cross-rollup contract calls eventually

## MathVPoS v2

**MathVPoS v2 = MathHub + EVM + MathVPoS v1**

Virtual Proof of Stake (VPoS) is a new kind of mining pool that rewards you with both mining reward and MATH tokens which TVL has exceed $150M.

MathVPoS v2 will be a smart staking aggregator and yield engine, like Yearn, for cross-chain assets and DeFi protocols.

MathHub & XCMP provides the cross-chain capability. Based on EVM, MathVPoS v2 is able to support on-chain strategies based on smart contract and bring the highest APR for users.

## DeFi with Privacy

**MathHub + EVM + SecretStore = DeFi with Privacy**

Blockchain is a decentralized network of nodes with constant data exchange regarding the modifications in their state or mempool. As the transaction order is not assigned until the finalization state any decentralized exchange based on Blockchain will be prone to frontrunning.

Front-running happens because bots are able to bid a slightly higher gas price on a transaction, incentivizing miners to place earlier in the order when constructing the block. The higher-paying transactions are executed first. Thus, if two transactions making a profit from the same contract call are placed in the same block, only the first takes the profit.

Evolve the permissioning SmartContract in order to create a private-transactions ecosystem, which is something that most of the blockchains want to do and with EVM + SecretStore, MathChain will be able to do that. At the same time, MathHub will be able to finish the interoperaibility with contracts on the other chains.

## MathPay

**MathPay = MathSmartWallet + DID + EVM**

MathPay is the Blockchain Micro-payment system.

There are still a lot of people do not have bank account in this world. They can use social account to create the DID in MathSmartWallet. Then they can start to use ERC20 standard tokens for payment in real life.

Combine with DeFi applications, they can do lending and swap. They can join yield farming to increase they assets and buy blockchain based insurance program.

Micro-payment will also bring new business models in real life, for example content creator can get paid with very small amount of tokens when their content get viewed, which will replace their current advertise model. The small amount can have 18 decimals which is not possible to happen in current digital payment system.

## ？

**MathDappFactory + Your Idea = ?**

MathDappFactory provides developer with great tools that make developing exchanges, games, and other DApps a snap.

Developers can leverage MathDappFactory to build their own ideas without a long learning curve. They can also propose a MathChain treasury request to create public good on MathChain and will be rewarded with MATH token if it passes the governance.

We gladly invite the developer community to join us on this journey.