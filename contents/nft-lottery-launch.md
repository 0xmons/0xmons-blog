title: NFT-LOTTERY Launch

![nft lottery home](https://i.imgur.com/0cK61gt.png)

[NFT-LOTTERY](https://nft-lottery.xyz/#/) is now live on mainnet! Powered by ChainLink's VRF for randomness, now anyone can create a fair, on-chain RNG drop for any NFT of their choice.

# How to use it?

Pick an NFT, get 2 LINK tokens, and head over to [the create page](https://nft-lottery.xyz/#/create).

![create page](https://i.imgur.com/Zd7ZEng.png)

From there, you can set the following parameters:

* Start date
* End date
* Minimum number of tickets to sell
  * If you don't sell at least this many, ticket buyers can burn their ticket for a refund.
* Maximum number of tickets to sell
* Ticket price

There is a flat creation fee (currently 0.1 ETH), but NFT-LOTTERY takes none of the ETH you earn from ticket sales. Half of the fee is used to buy back XMON for XXMON stakers.

After approving the NFT, LINK, and creating the lottery, you'll get a new link for your lottery. That's where people can purchase tickets, and where you (as the lottery creator) will manage the lottery.

![lottery management screen](https://i.imgur.com/EMOtgPW.png)

After a lottery is over,  if it was successful,**you will need to make 2 more transactions**. The first is to distribute the lottery prize. This function calls the ChainLink VRF system to randomly select an NFT winner. It will take a few minutes after your transaction goes through to be picked up by the ChainLink network; after that, the NFT will go to a random ticket holder.

Only after the NFT has been distributed can you claim your ETH, which is also on the same page.

If a lottery was not successful, ticket holders will see a button to burn their tickets for a refund. You (as the lottery creator), will see a button to reclaim your locked up NFT and LINK.

# How does it work?

Behind the scenes, the NFT-LOTTERY contracts provide a scaffolding around ChainLink's VRF services and utilize a minimal proxy to reduce deployment costs. Each lottery costs around 500,000 gas to create, including the costs to lock in the NFT and LINK.

The actual lottery sale contract basically just escrows the assets as well as the ETH received until the Chainlink VRF call is made.

As an alpha release, NFT-LOTTERY does come with a few caveats. The biggest is that, due to an early design decision that favored simplicity, each lottery ticket is itself an NFT. This has pros and cons.

The biggest con is that it increases the gas to buy a ticket. Each ticket costs around 200,000 gas. However, it greatly simplifies the ChainLink VRF call.

**Because of this, NFT-LOTTERY is currently best suited for ticket sales of a few hundred at most**.

A v2 of NFT-LOTTERY would aim to have a constant gas fee for any number of tickets bought, and this is in the works. But it's not ready yet.

The biggest upside is that because each ticket is an NFT, we can get fancy with the on-chain rendering. [Here's](https://opensea.io/assets/0x1d2abd03eaeb28188ba7e3fae4ecd127db531b7a/1) what an NFT-LOTTERY ticket looks like:

![ticket image](https://i.imgur.com/nfgq8Jr.png)

As you can see, each ticket will show lots of relevant information about the actual lottery. You can track what item the ticket is for, the number of tickets sold, and the time left! And it's animated! Best of all, it's all on-chain, and there's some cool stuff going on to ensure that no two lottery tickets have the same colors for their progress bars.