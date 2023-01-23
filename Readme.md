# HYDRA - Orderbook for NFTs on Solana

Decentralised order-books are a fundamental financial primitive, essential for large-scale adoption of blockchain based finance.
Unlike AMMs, Orderbooks offer more efficient pricing of assets, and []
Thus, they are the preferred method of exchange in Traditional Finance, by a massive margin

Solana, with its efficient parallel execution (Sealevel) runtime, enables cost effective order books to be developed, updated, and executed on-chain - Something that has so far not been practicable on EVM based chains with limited scalability and flexibility.
So far, Orderbooks on solana have focused on Trading of fungible tokens only. Liquid and efficient trading markets built on Orderbooks for NFTs are thus absent.

Hence, we propose Hydra, a decentralised orderbook for NFT trading. Building on an early prototype developed by SolWorks called Col8 (as suggested), we integrate that with Helius NFT APIs as a real-time data feed for bid and ask data. Incredibly, Helius indexes virtually *all* on chain NFT transactions on solana, so gathering bid/ask data from across the chain is possible using just a single API.

We demonstrate how the Hydra NFT orderbook can be updated with values provided by the Helius API through a series of tests. In this version, we utilise DeGods NFTs to demonstrate our concept. In the future, this PoC can easily be expanded to permissionlessly include any NFTs with previous on-chain transactions. Moreover, we could integrate the Helius API with on-chain oracles, to make the bid/ask update process fully autonomous. As next steps, we plan to release an SDK for users to query information about their preferred NFT in the future.

** Local Testing **

Clone this repo, and make sure you have the latest version of solana-sdk and anchor installed.

You can build & deploy the Rust Orderbook program by entering:

`anchor deploy`

And then you can test updating the Bid/Ask values by calling our updated tests folder:

`anchor test`


** Devnet Testing **




More information - We will be providing more detailed documentation, information on our roadmap and upcoming features, in our Wiki - Stay tuned!
