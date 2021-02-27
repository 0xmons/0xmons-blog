title: 0xmons v3 Dagon: Multisender, Composable NFTs

I'm excited to announce a new development milestone in the 0xmons project, so we're bumping it up to a new version again. This time, it's Dagon, one of the rulers of the Deep Ones. Those of you in the Discord and Telegram may have already seen that I've been working on a new Multisender/Locker, and it's now live on mainnet! In this post, I'll explain what the contract does, how it can be used, and two other updates (Encode Club Hackathon and the upcoming 0xmons auction).

The code and tests can be found on GitHub [here](https://github.com/0xmons/multisender).

The contract can be found on Etherscan [here](https://etherscan.io/address/0xc653e1b3a971078812a72d11c45ad71e00f3ad1f).

Front-end coming soon (TM).

# Multisender

The first thing this contract allows you to do is bulk-send tokens. You can send ERC20, ERC721, or ERC1155 tokens, but only one token contract at a time. You can send these assets to either a direct list of addresses, or you can send them to a list of ERC721 token holders. This can make it easy to, for example, airdrop tokens to holders of NFTs that you've created.

The cost is 0.025 ETH per multisend, and this fee can be adjusted lower (but never higher!) by the owner (me). The ETH fee goes to the multisig for the 0xmons project.

However, if you hold at least 1 XMON token or 1 0xmon NFT, it is free to use.

# Generalized Asset Bundle NFTs

The second feature is what I'm incredibly excited about. This contract allows anyone to permissionlessly lock *any* asset–ERC20/721/1155–inside of an ERC721 NFT. Then, only the holder of the NFT can retrieve the locked asset. This is a generalization of my previous sender/locker, which allowed users to lock ERC20 tokens insde of ERC721 NFTs. Now, users can even lock other ERC721s inside! 

![locker image](https://i.imgur.com/yHGbad6.png)

For example, in the above image, Alice owns a 0xmons NFT, and someone has used the contract to lock some ERC20 tokens, ERC1155 tokens, and an ERC721 token inside. As the 0xmons NFT owner, she can withdraw all of these assets from the contract at any time.

What are some possible use-cases?

1. Delayed token airdrops
2. Offering a token bonus to those who purchase an NFT
3. Offering an NFT bonus to those who purchase an NFT
4. Russian nesting dolls NFT

Now, any ERC721 can become a generalized asset bundle, holding whatever you want! This is a primitive that I hope can be useful for other projects looking to e.g. offer tokenized index funds, p2p trading, and more.

This protocol is entirely free to use.

# The Essentials 0xmons Auction

What better way to demo a new protocol than to show it off? Those following the blog will have seen that I created [four special 0xmons](https://blog.0xmons.xyz/81012566310) to celebrate the completion of series 1. I have used the Generalized Asset Bundle contract to "lock" the four artist edition NFTs into each one of the 0xmons NFTs!

Tomorrow, at 9:00 AM Pacific time, the four 0xmons will go on auction for 1 week. Each one of these 0xmons already has both their static *and* animated data encoded on-chain using calldata. (Although not contract storage–you may spend gas to do that at your peril.)

Like last time, half of the ETH raised will go towards providing additional XMON-ETH liquidity on  Uniswap, locked for 1 year.

And what to call this set of four 0xmons? The first was called the Founders Edition, as it helped kick off the project. Ryujin helped bring my attention to the name The Essentials Edition which I think is a great fit. (As for why, I'll leave that to you, dear reader.)

# Encode Club Results

As some of you may already know, I presented 0xmons at the Encode Club hackathon, and the project took first place! You can can watch the recording of my pitch [here](https://twitter.com/encodeclub/status/1364373949845557253). The other projects were also very cool, and I also highly recommend giving [Float](www.floatprotocol.eth.link) and [revert](www.revert.finance) a look as well.

# Roadmap

There is now a rough roadmap up on [GitHub](https://github.com/0xmons/ROADMAP) for those who want a bigger picture view of what's coming next for the project. Thank you to everyone for the support, and I can't wait to share more updates soon.