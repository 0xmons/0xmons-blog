title: 0xmons v1 Launch

The initial launch of the 0xmons platform is now live! Version 1 (Azathoth) is now released with two main components: Farming and Summoning. (Spawning is a planned feature coming later on.) In this post, I'll give an introduction to the platform, the three main components, the XMON token, and my thoughts on governance.

# Introduction

0xmons is an experimental NFT art project. It's 33% playing around with NFTs, 33% improving machine learning algorithms, and 33% developing a creative outlet for this glitchy, Cthulhu-esque aesthetic. <span class="hidden">It's also 1% an actual ritual to summon T H E D E E P, haha jk jk…unless???</span>.

In 0xmons, you play the role of an acolyte summoning monsters from the great beyond into tiny pixels on your screen.

The NFT part is obvious; the whole platform is built on Ethereum, and each monster is represented by [this ERC-721 contract](https://etherscan.io/address/0x0427743df720801825a5c82e0582b1e915e0f750). My work on this project has spawned some nice stuff that generalizes to being useful for other NFT projects, and I'll be open-sourcing as much as I can. 

The machine learning part is what drives the intrigue around the NFTs. Many projects have done algorithmically generated art. I am offering a different take, one that tries to be a bit more novel. I am using a Generative Adversarial Model trained on pixel art that spits out these monstrous blobs of pixels:

![monster 1](https://i.imgur.com/2AtVvfX.gif)
![monster 3](https://i.imgur.com/rtwcStw.gif)
![monster 4](https://i.imgur.com/iuPFsZ1.gif)
![monster 5](https://i.imgur.com/8Qn3f1d.gif)

Currently, the image generation is happening off-chain, but I have a few ideas I want to explore regarding on-chain registries and verification of each monster's image data. This will be next focus now that Azathoth is live.

As for the creative part, there's a whole mythos that's being developed along with these pixel monsters. You can look forward to a unique, interesting backstory for your 0xmon NFT. This backstory is also AI-generated, human-curated.

So, what makes 0xmons cool?

1. **Fully unique NFT:** Unlike other projects, every single 0xmon is 1 of 1. No one else will have the same 0xmon with your animation, name, epithet, or lore.
2. **Human-AI hybrid creativity:** Each 0xmon's animation, name, epithet, and lore was originally AI generated, and then hand-tweaked by a human (me!) This allows for a very interesting type of joint creative content that is currently rare in the NFT space.
3. **Onchain data:** (In Development) I'm currently working on a way for 0xmon users to encode their 0xmon's data directly on chain which solidifies their digital presence and allows for true art ownership, even if IPFS fails.

# Farming
You can currently stake XMON-ETH LP tokens to acquire more XMON tokens. This is the normal farming you're used to, no extra gimmicks. 

![farming pictures](https://i.imgur.com/9nyfoai.png)

~~The tentative plan is to distribute 800 tokens over 1 month for liquidity mining, and then extend that over additional months with more tokens.~~

See [this post](https://blog.0xmons.xyz/78686666310) for updated farming details.

# Summoning
Right now, you can stake your XMON tokens to acquire DOOM, and then redeem the DOOM for 0xmon NFTs. This is similar to how users redeem Pineapples for collectibles in MEME.

![summoning picture](https://i.imgur.com/AyenAiD.png)

The DOOM cost to summon a 0xmon goes up with subsequent summons. The summoner contract is deployed to mainnet [here](https://etherscan.io/address/0xd06337a401b468657de2f9d3e390ce5b21c3c1c0#code).

The initial parameters (subject to change) are:

* Max stake: 12 XMON
* Time to redeem first 0xmon: 1 week
* Time to redeem subsequent 0xmons: 1 additional week per summon

# Spawning (In Development)
The second method will be to acquire two 0xmons and then use them to spawn a third. Spawning takes an XMON fee. At launch, each pair of 0xmons can only be bred together once, e.g. monster A and monster B can only spawn 1 offspring. After spawning, there will be a delay before the monsters can spawn again.

![spawning screenshot](https://i.imgur.com/oxrkIaI.png)

Later generation 0xmons will require longer delays between spawns. The current spawning contract is deployed to mainnet [here](https://etherscan.io/address/0x4fad5ddc4e0186b932e27baa7d37d97457dfc868). Note that it is not live and future versions may be deployed.

# Security
Please note, **none of the 0xmons contracts have been audited**.

However, I take testing seriously. I've written a series of tests for all of the moving pieces which can be found [here](https://github.com/0xmons/0xmons-contracts-new/tree/main/test), and the test coverage is close to 100% for all components. I've also had the help of several alpha testers playing around with the Rinkeby testnet version, and nothing has broken.

That being said, this initial alpha launch still carries risk, so please keep that in mind.

# XMON 
[XMON](https://etherscan.io/address/0x3aaDA3e213aBf8529606924d8D1c55CbDc70Bf74) is the token used for this NFT ecosystem. It has a total supply of 10,000. Approximately 1,200 tokens were distributed in an airdrop to early participants from my previous experimental NFT projects. 

![xmon token logo](https://i.imgur.com/MUXU7Tj.png)

(Thanks to [@ecsypz](https://twitter.com/ecsypz) for the token design.)

~~XMON has an adjustable dev fee on transfer. It can be set from 0% to 10%, and it is currently set to 1%. Thus, when buying on Uniswap, you will need to set slippage above 1% to avoid errors.~~

The XMON fee is now set to 0%. It trades like any other ERC-20.

**Note that XMON is not a governance token. It is only used as a utility token for the 0xmons NFT platform.**

My current plan for token distribution is via LP farming and token bounties for projects that help grow the ecosystem.  I am very excited to sponsor art that fits the 0xmons c̸̙̹̥̲̬̮̟̯̓̾ụ̡̲͚̹̑̃͌ṙ̡͈̬̯̯̰̝̟̽s̟̞̝̪͇̹͙͕̉ͥ̒̑́e̳̟͋͟ͅḏ̻̎ͤ͋͗͢  aesthetic. Whether that's through writing, visuals, music, or otherwise, I welcome creative energy! Reach out to hello at 0xmons, and we can connect.

# Governance
It is common nowadays to have a platform's native token also double as the governance token. That is **not** happening here. Voting tokens in general have [several problems](https://www.zeframlou.com/2019/02/why-voting-tokens-are-fking-horrible.html), and I'm skeptical of community-based governance "just working" by default. Many projects are looking for good governors, but governance is a costly task, both in terms of time and effort. 

To that end, 0xmons is currently more like a personal art project of mine that I've opened up for participation from others, rather than a protocol governed by the crowd. While I don't have special minting privileges for the XMON token (there is no mint function), be aware that I can tweak *many* of the parameters related to the NFT minting process.

This includes:

* Minting new 0xmons without interacting with either the Summoner or the Spawner contracts.
* Changing anyone's DOOM balances.
* Changing any 0xmon's delay between spawns.

Additionally, the Azathoth summoning and spawning contracts are experimental. There may be future deployments of new ways to mint the 0xmon NFT.

Those tracking the XMON holders will know that the deployer address currently has the remaining 8,800 tokens. To reduce worries about rug-pulling, I'll be moving the funds to a multisig wallet. Because the community is still nascent, I've reached out to three public devs I know (and recommend!), and they've agreed to become signers for the remaining XMON tokens after initial bounties and farming pool are distributed.

They are:

1. [Zefram](https://twitter.com/boredGenius) from [88mph](www.88mph.app), a yield aggregator offering fixed-rate interest on multiple assets.
2. [Taylor](https://twitter.com/EclipseumToken) from [Eclipseum](https://eclipseum.org/), an asset designed to grow in value from Ethereum and maintain lower volatility.
3. [Alex](https://twitter.com/alexgausman) from [NFTX](https://nftx.org/#/), an index fund for different NFTs that allows anyone to create a new NFT fund.

As the project grows, and we see people take up bounties / contribute to the project, I hope to eventually add on more 0xmons community members to the multisig. For now, these three devs serve as a sanity check to make sure I don't do anything reckless like dump all the tokens on Uniswap.

**Note this has not happened yet, so please trade with caution. I will make another post once all the tokens have been distributed and accounted for.**

# Future
That's all for now! As I outlined in the Introduction, there is more that I want to develop after the initial launch, but the above outlines what is already live.

My next large-scale addition to the ecosystem will be creating a way for users to directly encode their 0xmon images on-chain. This will consist of an encoding library and a decoding library that other projects can also use. My first focus will be on static images, so the animations won't be on-chain, but future innovations could change this.

<span class="hidden">... thus the spirits beckon. No quarter shall be given to the lost lamb, but so in vain are their wanderings, that the paucity of relent shall scarcely go noticed. Dismiss the trepidation...</span>

> Owen