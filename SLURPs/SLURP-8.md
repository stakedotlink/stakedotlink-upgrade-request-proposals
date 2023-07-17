| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| SLURP-8 | SDL Tokenomics v2.0 | Vote Pending | Jonny Huxtable | Introduce reSDL | [talk.stake.link](https://talk.stake.link/t/slurp-8-sdl-tokenomics-v2-0/74) | 2023-07-17 |


## Abstract

We propose a major update in the SDL tokenomics for the stake.link platform. Ushering in a new era of liquid staking tokenomics by implementing a reward escrow model that boosts rewards and staking allocations and keeps skin-in-the-game for the participating node operators & ecosystem partners.

## Rationale

With stake.link being live and having solidified its position as the first of its kind liquid staking offering for the Chainlink Network, now is the perfect opportunity to reflect on how the protocol was originally designed. By redesigning native tokenomics with the focus on simplicity, clarity and scalability it will lay the foundation for future iterations of not just Chainlink Staking but for the platform's long-term success.

With this proposal, we believe it will solidify how the native token provides security and value to the platform. By keeping the proposition simple, rewarding its participants with boosted rewards and allocations from their long-term participation, it creates positive feedback loops that benefit all.

## Motivation

After various discussions, especially [SLURP-5](https://talk.stake.link/t/slurp-5-solidify-sdl-supply-economics/69/4), it’s become abundantly clear that for the platform to secure its success and growth the tokenomics need to be changed to promote value accrual and simplicity. If there’s active community members that still have questions on design decisions, ambitions and reasons then the marketable case for the existence of the native token is not sound. For a platform to see critical success, the establishment of the core community and their understanding of the core value proposition needs to be well understood.

We truly believe that stake.link not only is an incredibly beneficial platform to anyone that looks for staking options on the Chainlink Network, but serves as an extremely important pillar in the growth of Chainlink Economics 2.0 by increasing security, promoting capital efficiency, and directly enabling collaboration between node operators and token holders. The implementation of the native token needs to promote that goal by design.


### Timing

With the launch of the LINK staking pool and it consistently being full, outside of any future initiatives, it provides an opportunity to revisit and rethink tokenomics with minimal impact on the existing functionality. In addition, with the expectation of further Chainlink Staking iterations to be released at the [end of the year](https://blog.chain.link/chainlink-staking-launch-details/), it’s a perfect time to rework tokenomics that ensure the launch of the next iteration of stake.link is optimised to benefit token holders.


### Goals

The main three goals for the revisit of tokenomics were:

* Increase the reward rate for long-term participants
* Increase staking allocations for long-term participants
* Promote an increase in long-term participation
 
### Design Decisions

In the current token model, if someone uses the platform and wants to provide value with long-term commitment, there’s no benefit in doing so versus a participant who wants to hold the native token for shorter term gains. For example, staking SDL prior to a LINK pool increase without the incentives to keep and stake the token once the allocation has been secured.

By implementing a reward escrow tokenomics model, similar to the vote escrow tokenomics first designed by Curve, it benefits committed participants in three major areas: reward rate, staking allocation and governance votes.

Upon the inception of the new reward escrow model for SDL, it gave the opportunity to revisit the original token allocations and incentives as the new design doesn’t blend with the initial idea of Node Operator allocations. The reward escrow model, especially when taking into account some technical design issues, would be an anti-pattern to how SDL was created on launch.

In order to implement the new rewards escrow tokenomics, we needed to change the original design where the amount of staked SDL tokens directly determines the share of fees. This new system considers not just the number of staked SDL tokens, but also how long they are locked in for. This means that the amount of SDL tokens used to calculate your rewards can change, depending on your chosen lock-in period. In practical terms, this would affect the distribution of rewards from the staking pools. Specifically, it would have changed how rewards were divided between node operators and community stakers.

Based on that reason, it encouraged an entire rethink of the token distribution and how the platform rewards long-standing node operators and community members alike.


### Token Distribution

The idea to revisit the token distribution is to secure the third goal of promoting long-term participation. 

With the original design of locked SDL allocations to participating node operators, it resulted in equal weighting between key value providers with token usage governed by the DAO. Although, it has the trade-off of an inflated total supply with significant amounts of locked tokens that in practice will never become unlocked.

That’s why in this SLURP, as well as the implementation of a reward escrow token implementation, we propose to simplify the token allocation to provide five clear token tranches: 

* community
* node operators
* treasury
* core contributors
* ecosystem partners


### Reward Escrow

Vote escrow is a widely adopted style of native tokenomics design that was originally created by Curve Finance. The aim is to promote long term participation in the platform by increasing boosts and governance votes while giving holders the opportunity to vote on gauges that direct where rewards are distributed.

By implementing a similar model for liquid-staking, it allows the platform to achieve the goals of increasing the reward rate and staking allocations for long term participants, solving the issue that was mentioned earlier in regards to short-term gains by holding the native token for benefitting from pool increases.

Importantly, reward escrow scales more as the platform grows. The larger the total stake and rewards flowing through the platform for work performed, the larger the rewards directed to the participants who lock for longer periods of time. From a user perspective the rewards from staked tokens such as LINK don’t increase when the size of the pool scales. Although with reward escrow within SDL, it does. Having this positive loop is critical for encouraging extended participation, giving the design decision for implementing reward escrow.

When designing and implementing our reward escrow model, it was important to take into consideration the advancements that have been made in this area. With that, we felt it was important for the locked SDL positions to be represented as a transferable NFT similar to what is seen in [Velodrome](https://docs.velodrome.finance/tokenomics).


### Node Operator Incentives

With the removal of the locked SDL tokens for Node Operators, the platform still needs to incentivise node operators to have skin in the game and participate for the immediate and long-term future. The incentivisation of Node Operators to participate and join is critical to the platform's growth and success.  

With the proposed major iteration of tokenomics, the design rationale is to keep this process clear and simple, by allocating an amount of SDL from the treasury to each node operator that currently participates in the platform and for any new node operators that join.

To keep node operators incentivised, the allocations for any existing and new node operators will be linearly vested over a 4 year period. By doing this, it gives node operators the freedom to decide how they use their own SDL. Whether that’s for further initiatives that benefit the platform or staking it and locking it to earn more rewards. If a node operator chooses to exit the platform, the currently locked and vesting tokens can be claimed and sent back to the treasury.

### SDL Mint Function

As part of the clarification and simplification of the tokenomics, the SDL mint function should no longer be required as tokens will no longer be minted as part of Node Operators joining the platform. The removal of the mint function is not in-scope of this proposal, but if this proposal is ratified then we seek to remove the mint function before the end of 2023. The time delay is to avoid any unforeseen circumstances that could negatively impact the platform.

### Staking Allocations

As outlined in this proposal, the locking of SDL will boost staking allocations in-line with the multipliers detailed in the specification. The details of the new staking queue system will be outlined in a separate SLURP.

## Specification

### Token Distribution

* **Community**: 30,000,000 SDL (30%) (Unchanged)
* **Core Contributors**: 20,000,000 SDL (20%)
* **Treasury**: 40,910,000 SDL (40.91%)
* **Ecosystem Partners**: 7,690,000 SDL (7.69%)
* **Current Node Operators**: 1,400,000 SDL (1.4%)

**Total Supply**: 100,000,000 SDL

#### Community

The community bucket of SDL remains unchanged, the airdrop will continue as ratified in [SLURP-3](https://talk.stake.link/t/slurp-3-sdl-community-airdrop/40). The only change this proposal makes is that once the airdrop ends, rather than the DAO multi-sig withdrawing and burning unclaimed tokens, the multi-sig would withdraw and add to the Treasury bucket to retain the total supply amount.

#### Core Contributors

The core contributor concept is fundamental to the success of any project, stake.link included. Core contributors are those entities or individuals who lay the groundwork, dedicating substantial time, skill, and, often, significant financial resources to bring a project to life. For instance, from May 2022 to June 2023, stake.link was bootstrapped with a USD 1,911,014.00 investment from its core contributor, LinkPool.

The allocation of tokens to core contributors is a strategic move, designed to further align the interests of these contributors with the project's long-term success. It represents an appreciation of their initial investments and a reinvestment into the project, securing an influential stake for those who have contributed the most. With this perspective, we hope our community gains a better understanding of the core contributor token allocation, recognizing it as a necessary step for sustainable growth and innovation.

Core Contributor allocation as follows:

- 10M Founders Allocation, vested over 48 months
- Budget beyond Founders Allocation set at 1M annually
- Usage beyond this budget requires Governance Council approval 

#### Treasury

The treasury amount will be increasing by just over 10M SDL as part of this proposal. Reason being is that the treasury will be now used for Node Operator incentives as well as the existing proposals for items such as liquidity incentives. The treasury bucket having a long runway is critical to the platform's success due to needing to incentivise, giving the cadence for the increase. The specifics on the proposed models for Treasury usage are detailed below.

#### Ecosystem Partners

Ecosystem Partners are reserved to teams and individuals within the Web3 space who are interested in actively participating in the advancement of the protocol. In the current situation, the 7.69M SDL amount for ecosystem partners is allocated to Chainlink. This preserves the original percentage allocation that was made during the launch of SDL. To facilitate this change, Chainlink will burn 12,310,000 SDL around the time of proposal ratification.

Any new ecosystem partners that join the stake.link platform will receive their SDL amount as ratified by the DAO from the SDL amount in Treasury.

#### Current Node Operators

The 1.4M SDL bucket represents the current amount of SDL that is unlocked and awarded to Node Operators upon joining the platform. This amount will increase gradually over time the more Node Operators that join and the more incentives are distributed. The exact proposal for incentive distributions is detailed below.

### Fee Changes

With this proposal, node operators will receive a percentage fee (initially set at 5%) assessed against their own rewards, as defined by the rewards that flow through the Chainlink Staking delegator pool assigned to their representative staking allocation. This solves the problem of representative fees at scale, since node operators will earn a fee from only their own rewards rather than a percentage of the pool.

In addition, the community fee will increase to 15%. The fee is taken from the overall pool rewards and sent to the new SDL pool. The increase in fees to the SDL pool for the community stakers represents an 8.48x increase from the current fee model.

The core contributor fee will remain at 3%. Currently this fee is spent on the Chainlink Automation jobs that trigger the token rebases.

Overall, this keeps the sum of fees at 23%.

### Reward Escrow

As outlined, the reward escrow will mark a large change in how the SDL platform works for native token participants. The details are as follows:

* **No Lock**: 1x SDL Multiplier
* **Minimum 12 Month Lock**: 2x SDL Multiplier
* **Minimum 24 Month Lock**: 4x SDL Multiplier
* **Minimum 36 Month Lock**: 6x SDL Multiplier
* **Minimum 48 Month Lock**: 8x SDL Multiplier

As detailed in Motivations, when SDL is staked & locked, users will receive a transferable NFT that wraps the underlying SDL. Once the lock period is over, the NFT can be redeemed for the underlying SDL.

#### Locking Mechanism

Once SDL is staked and locked, users will receive full reward boosting as per their initial multiplier until the NFT holder initiates a withdrawal request. Withdrawal requests can be initiated after the NFT has exceeded past 50% of its lock-in duration and will last for 50% of its locked duration.

**Example A**:
* User locks SDL for 48 months, receiving 8x multiplier
* After 24 months, the user initiates a withdrawal request
* For 24 months, the user receives no multiplier for the remaining duration
* After 24 months, the NFT is burned and SDL is unlocked

**Example B**:
* User locks SDL for 12 months, receiving 2x multiplier
* After 48 months, the user initiates a withdrawal request
* User receives no multiplier for 6 months, reflecting 50% of their total lock-in period

To further clarify, when SDL is locked, the period is a minimum lock-in. The locked SDL will receive its full multiplier for infinite time until a withdrawal request is initiated. Withdrawal requests can be initiated after 50% of the minimum lock period, and last for 50% of the minimum lock period. If a withdrawal request is not initiated, then the full multiplier is retained.

The technical reasoning for implementing lock-in and withdrawal with no linear decay is due to decay not applying until an action is performed on-chain. In the projects that implement vote escrow the decay is only applied once a transaction is sent to the platform that interacts with the contracts, if the user performs no action then the boost they receive does not decrease.

Keeping that in mind, if someone locked SDL for 48 months receiving an 8x multiplier while they left it untouched for the duration of the lock-in, they would receive the full 8x multiplier for the full duration without any decay.

In this model, a user will receive their full multiplier up until the point of a withdrawal request. When modelled, if a user withdraws 50% of the way through their lock-in period, then the amount of boost they receive on average is the exact same as a linear decay. This implementation further incentivises users to keep long positions as they receive full multipliers up until they decide to withdraw. Since the locked position is represented by a transferable NFT, it also provides the user with the ability to exit without needing to wait the full period.

### Reward Escrow Modeling

To understand the value added by including reward escrow into the native token, it’s important to model the outcomes based on the current scenario and in a scenario of pool growth to prove the model.

#### Current Scenario

It’s important to note that within the current scenario, the concentration between lock-in periods is unknown due to no knowledge of how much SDL will be locked for how long.

Parameters:
* **SDL Staked**: 15,000,000
* **SDL Price**: $0.125
* **LINK Staked**: 750,000
* **LINK Price**: $6
* **Overall LINK Reward Rate**: 7%
* **0,1,2,3,4 Year Lock Concentration**: 5%, 10%, 60%, 15%, 10%

Exact rates being 0.58%, 1.16%, 2.32%, 3.48% and 4.63% respectively.

#### Growth Scenario

Within the growth scenario, the parameters provided are not an expectation of future growth. It is simply a model to prove how the model performs.

Parameters:
* **SDL Staked**: 20,000,000
* **SDL Price**: $0.125
* **LINK Staked**: 7,500,000
* **LINK Price**: $6
* **Overall LINK Reward Rate**: 7%
* **0,1,2,3,4 Year Lock Concentration**: 5%, 10%, 60%, 15%, 10%

Exact rates being 4.34%, 8.69%, 17.38%, 26.07% and 34.76% respectively.

As demonstrated with the above, even with the increase in total amount of SDL staked and locked within the SDL pool, under the exact same conditions the model performs exceptionally well at scale, encouraging long-term participation.

### Node Operator Incentives

#### Incentivization Model for Node Operators

This proposal seeks to restructure the allocation of SDL tokens for Node Operators, aligning with the new token distribution structure and the 100M SDL maximum supply. The goal is to ensure Node Operators maintain active engagement and continue to contribute to the platform by holding significant stakes.

Under this revised model, existing Node Operators' current SDL holdings will be burned. In replacement, they will be awarded a vesting schedule of 1,000,000 SDL over a four-year (48-month) tenure. This mechanism enables Node Operators to progressively unlock their vested SDL, which can then be staked in the SDL pool. Additionally, functionality will exist to claw back unvested SDL to treasury in the case of Node Operator exit or performance degradation.


#### Onboarding New Node Operators

As new Node Operators join the platform, they will be granted SDL tokens from the treasury, subject to a 48-month vesting schedule. The recruitment of Node Operators is anticipated to occur in batches, which may influence the specific SDL allocation for each operator. This allocation will be subject to governance decisions and is expected to reduce incrementally with each successive batch. This approach rewards early adopters while sustaining direct incentives for new participants.

As part of this revision, it is proposed that each Node Operator in the forthcoming batch will receive an allocation of 500,000 SDL.


#### Incentives Model Governance

The Node Operator incentivization model will be subject to an annual review by the Council, with potential amendments proposed through a SLURP. Under certain circumstances, driven by market conditions, proposals may be initiated outside the regular annual review cycle. 

### Deployment

#### SDL Pool

If ratified, then the deployment for SLURP-8 would require a new SDL pool to be deployed and current stakers will need to mint one or more reSDL NFTs with or without lock-in periods, determining the boost to their rewards and staking allocations.

In addition to the new SDL pool being deployed, the current SDL pool will be upgraded by the protocol multi-sig, triggering the current amounts of locked stSDL allocations to Node Operators to be burnt.

Unfortunately, it is not possible to upgrade the current SDL pool to support the new rewards escrow model as the change to represent locked positions within NFTs makes it incompatible with the current design.

#### Core Contributor & Treasury Amounts

Upon ratification, the protocol multi-sig will mint the required remaining Treasury amount to the existing wallet. 

The Core Contributor amount will be freshly minted and sent to the existing LinkPool multi-sig wallet: [`0x6879826450e576b401c4ddeff2b7755b1e85d97c`](https://etherscan.io/address/0x6879826450e576b401c4ddeff2b7755b1e85d97c).

#### Treasury

The treasury amount will be increasing by just over 10M SDL as part of this proposal. Reason being is that the treasury will be now used for Node Operator incentives as well as the existing proposals for items such as liquidity incentives. The treasury bucket having a long runway is critical to the platform's success due to needing to incentivise, giving the cadence for the increase. The specifics on the proposed models for Treasury usage are detailed below.

#### Ecosystem Partners

Ecosystem Partners are reserved to teams and individuals within the Web3 space who are interested in actively participating in the advancement of the protocol. In the current situation, the 7.69M SDL amount for ecosystem partners is allocated to Chainlink. This preserves the original percentage allocation that was made during the launch of SDL. To facilitate this change, Chainlink will burn 12,310,000 SDL around the time of proposal ratification.

Any new ecosystem partners that join the stake.link platform will receive their SDL amount as ratified by the DAO from the SDL amount in Treasury.

#### Current Node Operators

The 1.4M SDL bucket represents the current amount of SDL that is unlocked and awarded to Node Operators upon joining the platform. This amount will increase gradually over time the more Node Operators that join and the more incentives are distributed. The exact proposal for incentive distributions is detailed below.

### Fee Changes

With this proposal, node operators will receive a percentage fee (initially set at 5%) assessed against their own rewards, as defined by the rewards that flow through the Chainlink Staking delegator pool assigned to their representative staking allocation. This solves the problem of representative fees at scale, since node operators will earn a fee from only their own rewards rather than a percentage of the pool.

In addition, the community fee will increase to 15%. The fee is taken from the overall pool rewards and sent to the new SDL pool. The increase in fees to the SDL pool for the community stakers represents an 8.48x increase from the current fee model.

The core contributor fee will remain at 3%. Currently this fee is spent on the Chainlink Automation jobs that trigger the token rebases.

Overall, this keeps the sum of fees at 23%.

### Reward Escrow

As outlined, the reward escrow will mark a large change in how the SDL platform works for native token participants. The details are as follows:

* **No Lock**: 1x SDL Multiplier
* **Minimum 12 Month Lock**: 2x SDL Multiplier
* **Minimum 24 Month Lock**: 4x SDL Multiplier
* **Minimum 36 Month Lock**: 6x SDL Multiplier
* **Minimum 48 Month Lock**: 8x SDL Multiplier

As detailed in Motivations, when SDL is staked & locked, users will receive a transferable NFT that wraps the underlying SDL. Once the lock period is over, the NFT can be redeemed for the underlying SDL.

#### Locking Mechanism

Once SDL is staked and locked, users will receive full reward boosting as per their initial multiplier until the NFT holder initiates a withdrawal request. Withdrawal requests can be initiated after the NFT has exceeded past 50% of its lock-in duration and will last for 50% of its locked duration.

**Example A**:
* User locks SDL for 48 months, receiving 8x multiplier
* After 24 months, the user initiates a withdrawal request
* For 24 months, the user receives no multiplier for the remaining duration
* After 24 months, the NFT is burned and SDL is unlocked

**Example B**:
* User locks SDL for 12 months, receiving 2x multiplier
* After 48 months, the user initiates a withdrawal request
* User receives no multiplier for 6 months, reflecting 50% of their total lock-in period

To further clarify, when SDL is locked, the period is a minimum lock-in. The locked SDL will receive its full multiplier for infinite time until a withdrawal request is initiated. Withdrawal requests can be initiated after 50% of the minimum lock period, and last for 50% of the minimum lock period. If a withdrawal request is not initiated, then the full multiplier is retained.

The technical reasoning for implementing lock-in and withdrawal with no linear decay is due to decay not applying until an action is performed on-chain. In the projects that implement vote escrow the decay is only applied once a transaction is sent to the platform that interacts with the contracts, if the user performs no action then the boost they receive does not decrease.

Keeping that in mind, if someone locked SDL for 48 months receiving an 8x multiplier while they left it untouched for the duration of the lock-in, they would receive the full 8x multiplier for the full duration without any decay.

In this model, a user will receive their full multiplier up until the point of a withdrawal request. When modelled, if a user withdraws 50% of the way through their lock-in period, then the amount of boost they receive on average is the exact same as a linear decay. This implementation further incentivises users to keep long positions as they receive full multipliers up until they decide to withdraw. Since the locked position is represented by a transferable NFT, it also provides the user with the ability to exit without needing to wait the full period.

### Reward Escrow Modeling

To understand the value added by including reward escrow into the native token, it’s important to model the outcomes based on the current scenario and in a scenario of pool growth to prove the model.

#### Current Scenario

It’s important to note that within the current scenario, the concentration between lock-in periods is unknown due to no knowledge of how much SDL will be locked for how long.

Parameters:
* **SDL Staked**: 15,000,000
* **SDL Price**: $0.125
* **LINK Staked**: 750,000
* **LINK Price**: $6
* **Overall LINK Reward Rate**: 7%
* **0,1,2,3,4 Year Lock Concentration**: 5%, 10%, 60%, 15%, 10%

Exact rates being 0.58%, 1.16%, 2.32%, 3.48% and 4.63% respectively.

#### Growth Scenario

Within the growth scenario, the parameters provided are not an expectation of future growth. It is simply a model to prove how the model performs.

Parameters:
* **SDL Staked**: 20,000,000
* **SDL Price**: $0.125
* **LINK Staked**: 7,500,000
* **LINK Price**: $6
* **Overall LINK Reward Rate**: 7%
* **0,1,2,3,4 Year Lock Concentration**: 5%, 10%, 60%, 15%, 10%

Exact rates being 4.34%, 8.69%, 17.38%, 26.07% and 34.76% respectively.

As demonstrated with the above, even with the increase in total amount of SDL staked and locked within the SDL pool, under the exact same conditions the model performs exceptionally well at scale, encouraging long-term participation.

### Node Operator Incentives

#### Incentivization Model for Node Operators

This proposal seeks to restructure the allocation of SDL tokens for Node Operators, aligning with the new token distribution structure and the 100M SDL maximum supply. The goal is to ensure Node Operators maintain active engagement and continue to contribute to the platform by holding significant stakes.

Under this revised model, existing Node Operators' current SDL holdings will be burned. In replacement, they will be awarded a vesting schedule of 1,000,000 SDL over a four-year (48-month) tenure. This mechanism enables Node Operators to progressively unlock their vested SDL, which can then be staked in the SDL pool. Additionally, functionality will exist to claw back unvested SDL to treasury in the case of Node Operator exit or performance degradation.


#### Onboarding New Node Operators

As new Node Operators join the platform, they will be granted SDL tokens from the treasury, subject to a 48-month vesting schedule. The recruitment of Node Operators is anticipated to occur in batches, which may influence the specific SDL allocation for each operator. This allocation will be subject to governance decisions and is expected to reduce incrementally with each successive batch. This approach rewards early adopters while sustaining direct incentives for new participants.

As part of this revision, it is proposed that each Node Operator in the forthcoming batch will receive an allocation of 500,000 SDL.


#### Incentives Model Governance

The Node Operator incentivization model will be subject to an annual review by the Council, with potential amendments proposed through a SLURP. Under certain circumstances, driven by market conditions, proposals may be initiated outside the regular annual review cycle. 

### Deployment

#### SDL Pool

If ratified, then the deployment for SLURP-8 would require a new SDL pool to be deployed and current stakers will need to mint one or more reSDL NFTs with or without lock-in periods, determining the boost to their rewards and staking allocations.

In addition to the new SDL pool being deployed, the current SDL pool will be upgraded by the protocol multi-sig, triggering the current amounts of locked stSDL allocations to Node Operators to be burnt.

Unfortunately, it is not possible to upgrade the current SDL pool to support the new rewards escrow model as the change to represent locked positions within NFTs makes it incompatible with the current design.

#### Core Contributor & Treasury Amounts

Upon ratification, the protocol multi-sig will mint the required remaining Treasury amount to the existing wallet. 

The Core Contributor amount will be freshly minted and sent to the existing LinkPool multi-sig wallet: [`0x6879826450e576b401c4ddeff2b7755b1e85d97c`](https://etherscan.io/address/0x6879826450e576b401c4ddeff2b7755b1e85d97c).
