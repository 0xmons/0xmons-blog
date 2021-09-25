title: Trustless NFT Lotteries with ChainLink

Soon you'll be able to run your own NFT lotteries, powered by ChainLink. I'm really excited for this because it leverages blockchain in all the relevant ways: it's the distribution of a digital asset in a trustless manner, with all conditions clear for everyone to see.

NFT-Lottery is launching soon on testnet, and then mainnet soon after. Thus, I thought I'd write a little bit about how v0 will work, and what will be live at launch.

To start, NFT-Lottery is completely permission-less. Anyone will be able to create a lottery for any ERC721 that they own for any price. An NFT lottery is basically a ticket sale (in v0, tickets are sold in ETH) where a random ticket holder then gets a specified NFT at the end of the duration. NFT-Lottery uses ChainLink's VRF to select a random ticket holder.

To improve the experience for both buyers and lottery creators, NFT-Lottery has several cool features:

First, the NFT is escrowed into the lottery contract during creation, so buyers know the NFT will be guaranteed there to be distributed at the end of the lottery.

Secondly, lottery creators have to specify a minimum number and maximum number of tickets to sell. If the minimum number isn't reached by the end of the lottery, buyers can burn their tickets to get their ETH back. As a corollary, the lottery creator can't claim their ETH until the NFT has been distributed.

Thirdly, the tickets themselves are NFTs with on-chain metadata/image that track the progress of the lottery. Users can get a rough idea of how the lottery is progressing, even from platforms like OpenSea.

Fourthly, *lottery creators keep all ETH from their ticket sales*. The NFT-Lottery platform only takes a flat fee during lottery creation.

The code is up on GitHub, has been robustly unit-tested, and peer reviewed. The next steps are building out a UI for testnet, and then an alpha mainnet launch afterwards. If you'd like to create a lottery for your own ERC721s, let me know on Twitter!