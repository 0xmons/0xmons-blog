title: 0xmons Series 2 Plans

I'm excited to announce that the second series of 0xmons have finally been completed. This post will outline the details for how migrating your DOOM and summoning for series 2 will work.

Note: this post has been edited from the previous version to account for new details and updates.

# Series 2: 128 -> 192

Series 2 has 192 new 0xmons waiting for eager acolytes to summon. 

This is 64 more than the originally decided supply of 128. 

Reasoning: My goal with the series 2 distribution is to have a broader distribution of the 0xmons NFT. After investigating, I found that the current number of people with over 666 DOOM is actually  around 130. This is much more than  I expected. If we kept supply at 128 and did the migration, there would likely very few, if any left for stakers  to earn after the initial batch is summoned.

Many new people have joined since series 1, and I feel there's been an  implicit promise that those who had close to redemption rates in series 1 would be able to roll-over to redeem for series 2. Because of this, I'd prefer adding more 0xmons to the series 2 supply, rather than some  other method like reducing the amount of DOOM people can migrate over. 

Thus, here is what's happening:

1. First, I'm affirming my commitment to a total hard cap of less than 1000 0xmons  NFTs total, likely at 666 overall. Increasing the supply here just means there will be less supply to distribute in future series. 
2. Create 64 new 0xmons and add them to series 2, so that the new series 2 supply is 192 (excluding the early editions).
3. Create a generative NFT that is representative in some way of a  person's series 1 DOOM amount, as an additional bonus to large DOOM  stakers. (This will be likely done via snapshot to prevent people trying to game the system now.)

Overall, there are around 260 people staking, and I believe that around  150 people or so will hit 666 DOOM before the migration is fully  complete. 

My goal with this update is to ensure that: 
1. As many people who have been staking in earnest to get a 0xmon can  receive one.
2. There is additional excess supply (~40 0xmons) that will go to reward large stakers. 
3. Everyone is aware of what the currrent DOOM distribution looks like.
4. Ideally, the increased supply further reduces the tension to have a  gas war for redemption. 
5. Change as little as possible from the stated migration plan. This  requires no new smart contract or front-end updates, past what was  already written.

# Series 2 Preview

Once again, each 0xmon comes with a unique animation, epithet, and lore. The lore in particular has been improved with additional editing, small callbacks, and a stronger language model. I hope people can enjoy diving into the exciting backstory for each 0xmon.

Here are three such monsters you might summon (but you'll have to wait to see the animations!):



-



**Name**: Hull'sen

**Epithets**: Shield of the Abyss

**Lore**: A monstrous, blind, ancient creature with long, spindly limbs and a massive, faceless head. It is said to be the last in a line of guardians that defends the Abyss of Woe.



-



**Name**: Chaofraz

**Epithets**: Master of Hunger and Despair

**Lore**: A colossal entity said to have the power to bring famine to the earth. It is said to be visible from the Core World, and usually takes the form of a vast, black serpentine creature with three heads.



-



**Name**: Champitha

**Epithets**: The Keeper of Dreams

**Lore**: A benevolent and capricious entity, Champitha cares little for the happenings of the world. Her realm of dreams, however, has always been a place of serenity and balance. Now she is being forced to contend with the avarice of the Night Gods that reside in her realm.



-



Soon after series 2 is fully summoned, I'll also set up a provenance to provide a central point of reference for those who want to analyze the monster data. This also helps provide another layer of redundancy so people can make off-chain back-ups of the 0xmons data, if they so wish.

# Migration Details

As mentioned previously, DOOM that you have earned for series 1 will help give you a boost as we start series 2. If you have earned 666 DOOM or more, you will be able to migrate to series 2 with enough DOOM to summon one 0xmon. If you have less than 666 DOOM, you will be able to migrate to series 2 with a pro-rata amount of DOOM to summon one 0xmon. For example, if you have 333 DOOM in series 1, you will be able to migrate to series 2 with half of the amount of DOOM needed to summon one 0xmon.

Early next week, I'll push the new staking contract to mainnet and make sure that everyone can stake and migrate their DOOM with no issues. If that all goes well, I'll set the summoning time to be 48 hours afterwards so everyone can make accommodations for summoning. The fact that each 0xmon is unique, I hope, makes it less important to get a lower series number, but I suspect there may still be a bit of a gas war. So please keep that in mind.

The actual steps for migration will be:

1. Unstake from the existing staking contract. (1 transaction)
2. Stake into the new staking contract. (2 transactions, 1 to approve, 1 to stake)
3. Migrate your DOOM from the old contract to the new contract. (1 transaction)

Note that DOOM is migrated to the same address that accumulated it.

Once staking officially starts, the amount of DOOM needed to summon a series 2 0xmon will be approximately the amount generated by staking 12 XMON for 10 days. Staking in the v2 contract has no max XMON cap, but it scales by the square root of your stake. This means that if you stake:

* 1 XMON, it will take around 36 days.
* 2 XMON, it will take around 25 days.
* 5 XMON, it will take around 15 days.
* 10 XMON, it will take around 12 days.
* 20 XMON, it will take around 8 days.
* 100 XMON, it will take around 3.6 days.
* 1300 XMON, it will take them around 1 day.

#Why Sqrt Staking

Many staking contracts set some sort of max staking amount. This is usually designed to reduce the dominance of whales in accumulating rewards. However, a simple max stake limit is trivial to Sybil attack. Indeed, we see this happen where one person can set a max stake across several accounts which defeats the purpose of a max stake.

For the second version of the 0xmons staker, I've removed the max staking amount. Instead, the staker now applies a square root function to your staked amount when calculating points. I think this is a better way to address whale dominance. 

Importantly, the dominant strategy for someone with many tokens is no longer to just split across several accounts with max stake because max stake does not exist. A large holder can still split their tokens across several wallets, but the question of how much to allocate is now a more complex question. For a smaller holder, they need only to have more tokens than any one of the individual wallets to get rewards faster than the person who has split their holdings. 

Furthermore, even if someone has more tokens staked, a square root scaling means that someone staking twice as many tokens than you will not "lap" you. For example, if I am staking 5 XMON, and someone else is staking 10 XMON, they will get to summon in 12 days, and I will get to summon in 15 days. So I will still get a chance to summon once before they get their second summon. Under a normal scaling model, they would get to summon their second time when I summon my first time.

Ideally, this encourages whales to accumulate tokens and stake across a smaller set of addresses to increase their earning rate. But it hopefully also doesn't dishearten smaller holders because the larger stakers won't take all the rewards.

Of course, this doesn't mitigate the problem entirely. For example, under the new model, if someone had 100 XMON, they would still be able to summon one 0xmon relatively quickly. But I do not think there are ways to fully solve this, especially when token amounts are not equally distributed. I hope this is at least an improvement in the right direction.

# Next Steps

My immediate steps are to do some final tests on the staking contract, and then push it to mainnet. After that, I'll hook up the front-end and ensure that everyone can migrate and stake without issues. Once people are migrated over, I'll turn on the minting privileges and the summoning process can begin.

I'm aiming to push the updated staker to mainnet by Monday, and the upgraded front-end will go live by then. After that, I'll monitor things for the next two days, and make sure that people can migrate and stake. If that all goes well, I'll announce the exact time for summoning on Wednesday, and we can start summoning next Friday (April 2).

Once that is live, I'll work on the logistics for the Community 0xmon Contest (where we all collaborate on a 0xmon Community NFT) as well as a short story contest.

In addition, I've been working with 0xcoffee on a very cool artefact NFT drop for all of the existing 0xmons series 1 holders. So be on the lookout for that after series 2 drops!

Past that, I'll be working on a Lottery NFT primitive which I hope can provide more utility to the XMON token.

After that, it's the rest of the things on the [Roadmap](https://github.com/0xmons/ROADMAP/blob/main/ROADMAP.md).

<div class="hidden">also, Final DOOM is coming soon.</div>