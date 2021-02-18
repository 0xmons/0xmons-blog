title: Second Artist Drop and Updates

I'm excited to release the new artist feature for the second special edition 0xmons. I'll also give an update on the recent XMON grants, as well as some other news about myself.

<style>
img { 
  image-rendering: optimizeSpeed;             
  image-rendering: -moz-crisp-edges;          
  image-rendering: -o-crisp-edges;          
  image-rendering: -webkit-optimize-contrast;
  image-rendering: pixelated;               
  -ms-interpolation-mode: nearest-neighbor; 
  width: 12rem;
  height: auto;
}
</style>


# Coingecko

First, to get the obvious thing out of the way, we are now listed on [Coingecko](https://www.coingecko.com/en/coins/xmon). Now, on to more exciting matters.

# RHL Pixels Artist Drop

Last month, we had a fantastic [artist drop](https://blog.0xmons.xyz/78686666310) by [ReffSQ](https://twitter.com/Reff_SQ) to kick off the 0xmons project. Today, I'd like to introduce the next set of commissions by [RHLPixels](https://twitter.com/RhlPixels)! They do a lot of retro JRPG pixel art, and it was wonderful to get their rendition of 4 brand new 0xmons. Commissions appear to be closed at the moment, but they were also great to work with, and I highly recommend giving their Twitter a follow.

<div class="hidden">Though in plain site we hide, the messages must be seen. Divine the secret, and discover a trivial insight.</div>

Without further ado, here are the 4 new special editions:

## Özymiann

![](https://i.imgur.com/s9W5hsW.gif)

![](https://i.imgur.com/h9zhV9e.gif)

Epithets: Atlas of the Eighth Continent

Lore: The fabled Eighth Continent rests on their back. They are said to carry the soul of a nascent world on a perilous journey. Özymiann is one of the few Old Ones that can be sensed from the Material Plane due to its immense life energy. A passing notice can cure minor ailments, but a long meditation on its existence may induce terramorphesis.

## Westallmudoe

![](https://i.imgur.com/jOrTKaS.gif)

![](https://i.imgur.com/avnbYAg.gif)

Epithets: The Lone Observer Where Corners Meet

Lore: Shrouded in a cloak of stars, Westallmudoe watches the rest of the worlds in her own geometric space. Her manifold covers every living thing in a fine mesh, allowing her to sense the coming and goings of others. Twice in the past she has stepped in to avert catastrophe, but each time, the world loses an Integral Facet.

## El'mh

![](https://i.imgur.com/HAFpkBc.gif)

![](https://i.imgur.com/DoZTWVO.gif)

Epithets: Scion of the Shifting Sands

Lore: A gigantic monstrosity whose very tips are sensed as immense pyramids. The true body of El'mh is said to be locked deep under the ground. It appears to be a fan of constrictive order, and it prefers mortals to pay it respects through large monuments. A long standing tale tells of a deep grudge between El'mh and Wökr; Huacas describes it as 'essential'.

## Naaaaxs

![](https://i.imgur.com/8EOjJ3M.gif)

![](https://i.imgur.com/DHKQL6v.gif)

Epithets: It That Submerges

Lore: Dwelling in the depths of the unconscious mind, Naaaaxs is a primordial memetic predator. He spreads through the persistence of dualistic ontologies. The Absolving Church has made it their goal to eradicate this potent force, but their efforts to suppress knowledge on Naaaaxs only bolster his reach. Unsuspecting victims are pulled directly into their own id, which consumes them.

## Distribution Details
Similar to last time, I will put all 4 bundles up for bidding. However, I would like to try something a little different this time. Last time, OpenSea didn't have a way to automatically end the auction, and I had to accept offers manually. I am working on a contract to automatically "lock" ERC721 tokens into other ERC721 tokens. So the plan is that I would lock each artist edition into the normal 0xmon NFT, and the winner can either redeem it if they wish, or keep it locked inside.

I'm still working on testing this contract, so no concrete dates on when the auction will get set up, but I hope in around a week.

In addition, the four special edition 0xmons version will have their static image already encoded directly on-chain. You'll have to pay yourself for animated encoding, though.

Like last time half of the ETH raised goes to locked liq for the XMON-ETH pair for 1 year, and the other half goes to fund development, deployment, minting costs etc.

# Noa's New GAN
I've sent a 20 XMON grant to [Noa](https://twitter.com/NoaNabeshima) for their work with both using GPT-3 to generate the current 0xmons names/descriptions, as well as training an entirely new GAN for a later 0xmons series.

Below, you can see an animation of the interpolated outputs from the new GAN:

<p>
<video controls width="500" height="500">
  <source type="video/mp4" src="https://i.imgur.com/6nOvH7V.mp4"></source>
</video>
</p>

Some other choice monsters, as static images:

![](https://i.imgur.com/h5ZVAZP.png)

![](https://i.imgur.com/aZJeE5O.png)

![](https://i.imgur.com/PQTHJO7.png)

![](https://i.imgur.com/NwQorEX.png)

![](https://i.imgur.com/TSUm3km.png)

![](https://i.imgur.com/NyKe1Fm.png)

![](https://i.imgur.com/PruEQBG.png)

These likely won't show up until series 3, but I wanted to give everyone a sneak peek of what's been going on behind the scenes. I love the well-defined body parts, but I realize this new version may be polarizing. That's why I haven't made concrete plans to implement them yet. Nonetheless, Noa's work has been invaluable in fleshing out some of the machine learning particulars, and anyone hiring for ML engineering or R&D should definitely reach out to him via Twitter. 

# Dev Incentives
Now that the project has matured, I think it is a good time to talk about developer incentives. When the project initially launched, there was a 1% fee on transfer that went to pay for development. That was turned off to save gas and improve interoperability with other protocols.

Since then, I have not allocated a share of tokens for myself. Everything I've earned has come from the same LP farming initiative that has been accessible to everyone else. Commissions for the artwork and contract deployments have also all been out of pocket for me.

With the recent surge of interest on OpenSea, I think it's more than fair to say that this project brings value. To continue (and retroactively fund develoment) on this project, I'm proposing a linearly vested share of 185 XMON tokens from the multisignature wallet to the deployer address (xmon.eth).

While I've been staunch on XMON not being a governance token, I think it's fair to open this amount up for discussion in both Telegram and Discord, and I won't be setting up multisig txs to move funds until then.

There has also been talk about setting up voting for the 0xmons NFT holders which I think is an interesting idea. I've now configured the [snapshot](https://snapshot.page/#/xmon.eth) page to instead read your 0xmons NFT balance instead of XMON balance which basically implements this idea. 

# Personal Updates
As some people may know, I'm finishing up my final year of university right now. It has been incredibly tiring to juggle the various development activities with coursework, and my coursework is current very behind.

Because of this, I'll likely be doing dev updates slower than the sprint I did in January.

I'll commit to having weekly blog posts that detail how development is going, and, as always, you can track the TODO repo on [GitHub](https://github.com/0xmons/TODO/issues).

I want to resume my normal brisk pace of development, but in all honesty, that likely cannot resume until the end of March when classes end for me. 

Additionally, I will be presenting 0xmons at the [Encode Hack Club](https://medium.com/encode-club/encode-hack-club-announcing-the-finalists-61c5f0eed554) presentations on Tuesday, February 23rd. If any of you would like to watch my project (and others), it is free for everyone to register.

That's it for now, and I'll catch you all on awhoaq cpa9aqr icaodfaaoh.

Thank you!