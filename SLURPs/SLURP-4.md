| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| SLURP-4 | Nop Allocation stSDL Locking | Vote Pending | Eric Jaurena (@ericjaurena) | Implement Locking of Nops' stSDL and Require Council Vote to Unlock and Withdraw | [talk.stake.link](https://talk.stake.link/t/slurp-4-node-operator-staked-sdl-locking/65) | 2023-03-27 |

## Abstract

We propose instituting contract changes that will lock node operators' staked SDL (stSDL), and will require a governance proposal and Governing Council vote to unlock and withdraw any amount of SDL. 

## Rationale

Requiring a proposal and vote for the unlocking of node operators' stSDL will ensure several key benefits and alignments:

* Node operators will still have access to their SDL allocation for purposes of staff incentives, fundraising, liquidity provision, etc. but will be required to thoughtfully consider and delineate the intended use of tokens via a public proposal
* Community members will have visibility into and be able to offer their feedback on proposed use of SDL tokens by node operators
* The DAO will be able to burn stSDL from node operators in the event that they fail to fulfill their duties in serving the protocol
* Locking stSDL will enable directing rewards/fees from products like ixETH which node operators do not secure to only unlocked stSDL tokens, i.e. community stakers

## Specification 

Contract revisions to `DelegatorPool.sol`, the stSDL token contract, will remove the concept of a vesting schedule to node operator's stSDL allocations and allow the stake.link multi-sig to lock and unlock their stSDL allocations. All node operator stSDL allocations will be locked, and any unlocking, burning, etc. will only be performed after a publicly presented and reviewed proposal, and a succesful Governing Council vote.

### Token Distribution Proposal Framework

*At minimum, the proposal for unlocking and distribution of tokens must include:*

* Description of the purpose of the distribution of tokens
* The amount of tokens to distribute
* Timeframe over which tokens will be distributed
* The vesting schedule (if applicable) of the distribution of tokens to their final recipients

## Copyright
 
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
