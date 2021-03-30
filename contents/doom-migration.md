title: Series 2 Migration Guide

I'm excited to announce that the new staking contract for series 2 is now live on mainnet [here](https://etherscan.io/address/0xA3300bfc13556Fa5146fFdE34e92a0230A1C3197). 

The UI can be found [here](https://0xmons.xyz/#/summon2)

There is 1 main change to the previous series 2 plan, which is the introduction of a larger supply, from 128 to 192 (excluding the early editions from February). The rationale and discussion can be found on Discord, Telegram, as well as the updated post on migration plans found [here](https://blog.0xmons.xyz/81127166310). 

Below are the steps for how you can migrate your DOOM, stake into the new staking contract, and summon a 0xmon.

# Migrating DOOM

As previously mentioned, those with 666 DOOM or above in the previous staking contract will be able to start series 2 with enough DOOM for a full summon. In series 2, you need around 238 DOOM to summon a 0xmon. Because of the square root scaling, 1 DOOM in series 1 is not the same as 1 DOOM in series 2. **Note that even if you have less than 666 DOOM, you can still migrate your DOOM.** You'll just get a lower amount than 238, scaled pro-rata. For example, if you had 333 DOOM (50% of 666) in series 1, you'd be able to migrate over with around 119 DOOM (50% of 238) in the series 2 staker.

To migrate, all you have to do is click the Migrate Doom button on the UI and approve the transaction that pops up:

![migrate doom](https://i.imgur.com/QECCDoE.png)

That's all you need to do.

However, there are two caveats to this process:

First, each account can only migrate their DOOM once, so it's recommended to start staking in the new contract (details below) after you migrate.

Secondly, you **must** migrate your DOOM by Friday, April 02, at 10 am Pacific Time, otherwise you lose the opportunity to migrate. This is also communicated on the UI.

# Staking 

To stake into the new contract, you'll first need to unstake from the old contract which is still found at the same link [here](https://0xmons.xyz/#/summon).

After that, head to the Staking XMON form on the new page. You can click your balance, and the form will autopopulate. It's the same approve and stake flow you're used to. Two transactions, one to approve spending your XMON, and one to actually do the deposit.

As mentioned before, this new staker has no max staking limit. You can stake as much as you want, and the DOOM you earn will scale with the square root of your staked amount. Also, the UI now shows an estimated amount of DOOM per day instead of hour.

# Summoning

As you will see on the UI, the new staking contract already has the 192 0xmons preloaded in. Starting on Friday, April 02, at 10 am Pacific Time, you will be able to spend your DOOM and start summoning 0xmons.

While I don't anticipate any issues with the 0xmons metadata, I will be releasing an IPFS hash of the provenance ahead of time, to act as the source of truth, in case any issues arise.

With the date being now set in advance, I hope people can make their arrangements to be available to summon. Even if you are a few hours late, the increased supply should be enough of a buffer so if you don't care about series ordering, there should not be too much of a need for a gas war.

# Next Steps

For the next few days, I'll be finishing up the series 2 generation of the new 0xmons. I will also be monitoring the staking contract and UI in case any issues arise. If there are no other complications, I will be excited for everyone to unveil the new series of 0xmons this Friday.

