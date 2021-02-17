# Oracle Based Bridge

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
Rust and Javascript

## Development Roadmap

Deliverables marked with * have been further broken down in the section “Detailed Description”

### Timeline and Milestones
#### Milestone 1
Duration: 6 weeks
Deliverables:
* D1: Repository including a README that describes the project and explains how to run, test, and contribute
* D2: Dockerization of the repository to run in CI pipeline and local development
* D3: Basic oracle adapter structure in `Rust`
* D4: Implemetation of withdrawal and deposit notification backend*
* D5: Unit test cases for core functionalities
 

#### Milestone 2
Duration: 6 weeks
Deliverables: 
* D6: Implementation of bridge dashboard UI in ReactJS 
* D7: Integration of bridge UI and notification backend
* D8: Add `plug-and-play` API layer of bridge in NodeJS*
* D9: Develop supporting contracts to allow asset transfer between **EVM** chains
* D10: Deploy bridge between **Rococo Testnet** and **Ethereum Testnet**
* D11: Integration testing for cross-chain communication using oracle based bridge

#### Milestone 3
Duration: 6 weeks
Deliverables
* D13: Publish bridge as oracle adapter on Chainlink Network
* D14: Integrate bridge UI with bridge oracle adapter
* D15: Documentation and guidelines for integration: a) Use Bridge, b) Integrate with other Chains, c) Local deployment and development
* D16: Deployment of bridge on Polkadot network

### Detailed Description
#### D4: Implemetation of withdrawal and deposit notification backend
Build Rust based event watcher backend that will listen to specific events from source chain and perform varoius actions on target chain.

Source Chain Events
- `Deposit`
- `Withdraw`
- `SyncState`

Target Chain Triggers
- `Mint`
- `Burn`
- `SyncState`


#### D7: Implementation of bridge dashboard UI in ReactJS
Public facing user interface to perform various actions.

Allowed actions
- `Cross-chain Transfer`
- `Cross-chain Swap`


#### D8: Add `plug-and-play` API layer of bridge in NodeJS
Allow users to interact with bridge using API calls. This will also help developers to integrate their dapps with the Router bridge.

Allowed Actions
1. Authentication Endpoints
    - `generateAPIKEY`
    - `deleteAPIKEY`
    - `getAPIKEY`
2. Public Endpoints
    - `transferStatus`
    - `swapStatus`
3. Private Endpoints
    - `deposit`
    - `withdraw`
    - `swap`
    - `transferData`

#### D13: Integration testing for cross-chain communication using oracle based bridge
Implement integration test cases on the `jest` framework and perform end-to-end testing for the overall infrastructure.

## Funds Required Overall
30,000 USD

## Additional Information
* The team is currently implementing an EVM supported Substrate-based chain.
* The team has extensive experience in centralized and decentralized financial systems.
* The team is also looking into the state channels approach for cross-chain communication.
