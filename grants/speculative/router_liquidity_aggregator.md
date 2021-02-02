# Crosschain Order Routing

## Project Description
Router Protocol is building Cross-chain infrastructure that will seamlessly allow for liquidity to flow across chains, and also enable cross-chain price discovery. As the number of blockchains is increasing rapidly the liquidity across these chains is getting fragmented. Router aims to bridge this fragmented liquidity and enable cross-chain interaction between dapps and blockchains. Our first implementation is focused on smart order routing across various EVM supported chains. As more and more exchange venues develop across chains there are significant price differences due to constricted liquidity flows. Router infrastructure will enable natural arbitrage to play out and smooth out price imbalances across a vast pool of liquidity spanning multiple blockchains.


Our team is mainly based out of Singapore and Bengaluru. We are also developing an EVM supported substrate chain and intend to integrate our cross-chain bridging infrastructure with this chain. This infra can be plugged in between any two EVM supported chains. The reason we are developing this on Polka is because of its highly scalable infrastructure and the ability to allow cross-chain interactions by default.

## Team Members
* Ramani Ramachandran
* Shubham Singh
* Mounica Durga
* Chandan Choudhury
* Priyeshu Garg
* Mayank Rawat

## Team Website	
https://routerprotocol.com/

## Legal Structure 
Kailaasa Infotech PTE LTD (Singapore Entity)

## Team's Experience
The team behind Router Protocol has been working on blockchain, decentralized systems, and blockchain protocols for the past 6 years. Some of the projects built out by the team are as follows
- Fordex, the world’s first stable coin DEX, with a grant from the 0x foundation
- 108token, Asia’s first on-chain index token, an on-chain self re-balancing index built in collaboration with a leading national stock exchange
- The matching engine and the tech stack for a cryptocurrency derivatives platform
- Algorithmic trading bots for a futures arbitrage fund

In response to the increasing level of congestion in the Ethereum blockchain, we have recently launched an L2 AMM that supports Meta Transactions to allow gasless transactions [Gasless AMM](https://exchange.dfyn.network). We have also created an infra similar to `The Graph` for L2 chains like Matic to index L2 chain data and allow GQL based access. We are also working on a caching layer on top of this GQL layer to reduce the calls to the indexing node to optimize the overall turn-around time. Finally, we have also started working on cross-chain order routing infra and this will be the main focus of Router Protocol going forward. In addition to software development, the team also has significant experience working in financial services and product management.


### Go-to members for this project

Ramani Ramachandran (Ram), the lead product manager for this project, is an engineer with an MBA from MIT Sloan. Ram has experience in financial services and technology and has been in the cryptocurrency space since 2015. A frequent contributor to various media publications, Ram also blogs periodically at [Satoshi&Co](satoshiandco.substack.com). Ram has also designed and launched the above-mentioned products such as Fordex, 108token, and DFYN, as well as running one of Asia’s earliest crypto investment vehicles.

The team behind this project has significant experience in building financial systems and highly scaled applications. They have delivered various projects such as 108Token ( on-chain index ), Fordex (Stable Coin DEX), and the technology stack for Qume (Crypto Derivative Exchange).

Mounica Durga, a senior full-stack engineer in the team, has been working with blockchain technologies and protocols for the better part of her career. In the past, she had designed and developed the underlying architecture for Fordex ( built on 0x protocol for DEX). As part of her recent work, she has built ethereum and bitcoin wallets and microservices for Qume (CEX). She also has significant experience in developing with Rust and GQL. A lot of her work is not in public repositories but can be made available upon request.

Shubham Singh, a senior full-stack engineer in the team, has in-depth experience with Order matching engines as well as solidity. He worked as a lead dev building and optimizing matching engines for Fordex (DEX), Qume (CEX), and for a fund deploying futures arbitrage trading strategies. He has sound knowledge of both centralized and decentralized financial systems and most of his work has been in this space. His recent work involved AMM optimization to support gasless transactions for [DFYN](https://github.com/dfyn/dfyn-exchange/tree/meta-transaction-support) and indexing of blockchain data for L2 chains to allow for graph queries.



## Team Code Repos
`Most of the repositories are private but we are willing to share access if need be.`
* https://github.com/router-protocol
* https://github.com/dfyn
* https://github.com/Zenprivex

## Team LinkedIn Profiles
* Ramani Ramachandran: https://www.linkedin.com/in/ramaniram/
* Shubham Singh: https://www.linkedin.com/in/dev-shubham/ 
* Mounica Durga: https://www.linkedin.com/in/mounica-durga/
* Chandan Choudhury: https://www.linkedin.com/in/chandan-choudhury-3b748a23/

## Intended Language of Development
Solidity, Rust and Javascript

## Development Roadmap

Deliverables marked with * have been further broken down in the section “Detailed Description”

### Timeline and Milestones
#### Milestone 1
Duration: 6 weeks
Deliverables:
* D1: Repository including a README that describes the project and explains how to run, test, and contribute
* D2: Dockerization of the repository to run in CI pipeline and local development
* D3: Basic structure of solidity contracts*
* D4: Implementation of Root and Child chain contracts*
* D5: Unit test cases for core functionalities
 

#### Milestone 2
Duration: 6 weeks
Deliverables: 
* D6: Automation scripts for deployment and development on target chains
* D7: Implementation of contracts for cross-chain price path discovery*
* D8: Integration of chainlink to price discovery contracts
* D9: Basic structure of the validator node to verify cross-chain transactions*
* D10: Integration of contracts with validator nodes for event synchronization*
* D11: Integration of D7 with Root and child chain contracts
* D12: Manual Integration testing for cross-chain communication between contracts

#### Milestone 3
Duration: 6 weeks
Deliverables
* D13: Automated integration test cases*
* D14: Deployment on one of the parachains on **Rococo** testnet
* D15: Contract mapping dashboard for testnet*
* D16: Documentation and guidelines for integration: a) Submit Mapping, b) Integrate with Root and Child chain contracts, c) Local deployment

### Detailed Description
#### D4: Implementation of Root and Child chain contracts
Build the root chain and child chain contracts to store source and target contract maps for cross-chain interaction. This will allow users to map any contract on one chain to any contract on another chain. Build out a template to enable any contract to communicate across chains.


#### D7: Implementation of contracts for cross-chain price path discovery.
It is a mix of centralized and decentralized setup to find the optimal path for order execution. For identifying orders we will have a centralized setup for price discovery across various AMM's on different chains and for executing trades we trigger a contract call that will propagate from the bridge to the target chain and then target AMM. We are also exploring a potential integration with chainlink for the price discovery process.

#### D9: Basic structure of the validator node to verify cross-chain transactions.
The bridging infra will rely on proof-of-stake validators and these validators will be analyzing the blocks for changes originated from the source chain. Once these events are identified the changes will be propagated across the target chains. Validators will also enable the propagation of data bytes to allow cross-chain contract data transfer.

#### D10: Integration of contracts with validator nodes for event synchronization.
Prepare simulation of multiple validator nodes to validate transactions in a decentralized manner. A subset of active validators from the pool will be selected to act as block verifiers.

#### D13: Automated integration test cases.
Implement integration test cases on the `jest` framework and perform end-to-end testing for the overall infrastructure.

#### D15: Contract mapping dashboard for testnet.
Develop utilities to allow other developers to map their contracts to enable cross-chain data flow using router protocol.

## Funds Required Overall
100,000 USD

## Additional Information
* The team is currently implementing an EVM supported Substrate-based chain.
* The team has extensive experience in centralized and decentralized financial systems.
* The team is also looking into the state channels approach for cross-chain communication.
