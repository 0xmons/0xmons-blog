title: ZKNFT alpha release

I'm excited to announce that [ZKNFT](https://zknft.xyz/#/) is now released for the public! Be warned, this is an **alpha release**, so there will be some bugs! 

First, for those who don't know, ZKNFT is a proof-of-concept NFT marketplace showcasing the zkSync NFT API. 

![home page](https://i.imgur.com/f7RV1jl.png)

[zkSync](https://zksync.io/) is a zk-rollup that supports ERC20 tokens, NFTs, and asset swaps. They're adding full programmability later this year, including Solidity support.

**Full Disclosure: I was given a grant to work on ZKNFT, so it's a community release and not an "official" zkSync product. **

For those who are curious how NFTs work technically on zkSync, the [dev docs](https://zksync.io/dev/nfts/#what-s-live) are a good place to dive in. Briefly, though, there are a few changes compared to what you might be used to on other EVM chains:

1.  Rather than deploying your own NFT contract, all NFTs on zkSync are issued from the "same" contract. They all have sequential IDs.
2. Related to 1, you are restricted to a 32 byte content hash for each NFT that you mint. For ZKNFT, we interpret this as the IPFS hash for a metadata JSON object that conforms to the [OpenSea metadata standard](https://docs.opensea.io/docs/metadata-standards.)
3. There is a delay of a few hours between minting and full "finality" on L1 because of the zero-knowledge proof generation. Thus,NFT  transfers on zkSync can only happen a few hours after mint.

In exchange for this, however, there are several great benefits:

1. You can migrate your NFTs from zkSync back to Ethereum mainnet. If you choose to migrate your NFT back to L1, you can choose a minting contract of your choice, which adds some more optionality.
2. As a zk-rollup, zkSync allows for more throughput meaning computation costs are much lower. Mints/transfers/swaps all cost somewhere in the range of 0.00006 ETH!
3. You can exit the rollup within hours, rather than days (compared to an optimistic rollup), for much more convenience.

So, what's live on ZKNFT today?

First of all, **minting**.

![minting page](https://i.imgur.com/FqhPMPh.png)

Just like on other minting platforms, you have a familiar form to input all of your NFTs metadata, and then mint the NFT. Behind the scenes, the images are pinned to IPFS using [nft.storage](https://nft.storage/) which is powered by Protocol Labs. 

Secondly, **managing**.

![nft view page](https://i.imgur.com/51I18yC.png)

You can view your zkSync NFT collection and send your NFTs to other addresses. You can also view the collections of others, individual NFTs, etc.

Thirdly, **swaps**.

![offer page](https://i.imgur.com/hmstCw4.png)

The zkSync API technically allows for arbitrary bundle swaps of assets. Currently, you can NFT to NFT or NFT for ETH swaps on ZKNFT. You can make offers in either NFT or ETH, and the owner can accept them.

(In fact, you can pay for *all* transactions on zkSync using one of many different supported tokens (e.g. DAI or ZRX), but, again, for simplicity, all fees on ZKNFT are taken in ETH.)

Those are the three features at launch, and I encourage you to play around and see what it's like to mess with NFTs on a zk-rollup.

All mints/transfers/swaps on ZKNFT have *no additional fees*. Partially this is because the ZKNFT API makes it annoying to bundle additional fees into operations. But the other reason, of course, is that I think it's useful to have at least one open marketplace that the community can play with. Due to Alex Gluchowski's insistence, the [ZKNFT code](https://github.com/0xmons/zknft) is licensed under the permissive MIT license. Feel free to remix and use for any personal *or* commercial use, and PRs are always open!

