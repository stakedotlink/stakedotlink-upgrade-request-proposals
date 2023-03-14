| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| SLURP-3 | SDL Community Airdrop | Vote Pending | Eric Jaurena (@ericjaurena) | Airdrop to SDL Community & LPL Community | [talk.stake.link](https://talk.stake.link/t/slurp-3-sdl-community-airdrop/40) | 2023-03-14 |

## Abstract

As described in the 2022-12-16 [LPL Migration Update](https://medium.com/linkpool/lpl-migration-update-c3708dec38e4) article, we propose an additional SDL airdrop to specific subsets of the SDL community.

## Rationale

This proposal was drafted after substantial feedback from the community, and is intended to enhance parity between the community's voting power when compared to the rest of voting actors within the protocol.

## Specification 

### Distribution

**Note:** all described tranches below would exclude node operators and Chainlink Labs. 

#### LPL Community

**Who:**

Previous LPL Holders based on the 2022-11-25 snapshot.

**How much:**
4,779,332 SDL tokens distributed pro-rata, based on the amount of the wallet's held LPL and staked LPL at the time of the November 25th snapshot.

#### LPL + SDL Community

**Who:**

Previous LPL Holders (excluding LinkPool) based on the 2022-11-25 snapshot who also retained greater than 50% of their original SDL allocation as of 2022-12-16, the time of the publishing of our [LPL Migration Update article](https://medium.com/linkpool/lpl-migration-update-c3708dec38e4). The SDL allocation is defined as SDL held, staked, and provided as liquidity to the SushiSwap SDL/LINK Liquidity Pool.

**How much:**

4,779,332 SDL tokens distributed pro-rata based on the amount of a wallet's SDL held, staked, and provided as liquidity to the SushiSwap SDL/LINK Liquidity Pool at the time of the December 16th snapshot.

#### SDL Community

**Who:**

SDL holders, stakers, and individuals who provided SDL as liquidity to the SushiSwap SDL/LINK liquidity pool as of the December 16th snapshot.

**How Much:**

4,779,332 SDL tokens distributed pro-rata based on the amount of a wallet's SDL held, staked, and provided as liquidity to the SushiSwap SDL/LINK Liquidity Pool at the time of the December 16th snapshot.

#### Unmigrated LPL Holders

**Who:**

LPL holders and stakers as of the November 25th snapshot who retained 100% of this amount of LPL through the December 16th snapshot but had not yet migrated their LPL tokens to SDL, and have migrated their LPL to SDL by 2023/04/03 (April 3rd, 2023) by 12:00 PM ET and retained at least 50% of that SDL amount as of the April 3rd snapshot. 

**How Much:**

These individuals would be considered as eligible for each tranche on a pro-rata basis, based on the amount of LPL staked and held as of the December 16th snapshot.

### Minting Mechanics

* Perform an SDL, stSDL, and SDL/LINK snapshot using the datetime stamp of the publication of [this article](https://medium.com/linkpool/lpl-migration-update-c3708dec38e4), for the purpose of identifying eligible wallets per the foregoing eligibility criteria

* Perform an SDL, stSDL, and SDL/LINK snapshot using the datetime of 2023/04/03 (April 3rd, 2023) 12:00 PM ET, for the purpose of identifying eligible wallets for the Unmigrated LPL Holders portion of the airdrop

* LinkPool to burn 9,339,796 SDL tokens, reducing allocation from 34,339,796 to 25,000,000

* DAO Multisig to mint 14,339,796 SDL tokens with a 180 day claim period

* Eligible wallets can claim corresponding SDL airdrop

* After the claim period, the DAO Multi-sig withdraws and burns unclaimed tokens

### Voting

After discussion on talk.stake.link, this SLURP will be formally proposed to the governing Council for voting.

## Copyright
 
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
