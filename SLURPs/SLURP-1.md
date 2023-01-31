| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| SLURP-1 | Establish Formal Governance | Draft | Eric Jaurena (@ericjaurena) | Establish formal governance structure and SLURP process for stake.link protocol | [talk.stake.link](https://talk.stake.link/t/slurp-1-and-slurp-0-formalize-stake-link-governance-structure-and-processes-and-slurp-purpose-and-guidelines/19) | 2023-01-30

## Abstract

This SLURP is intended to formalize the roles of the four entities that govern the stake.link protocol, as well as the process for formally proposing and ratifying changes to the protocol via stake.link Upgrade Request Proposals (SLURPs). These entities are the stake.link community (SDL holders, stakers, and liquidity providers), the Governing Council, the Core Contributors, and the stake.link Multi-sig Holders.

The community proposes SLURPs and votes for community Council seats, the Council votes on SLURPs, the Core Contributors implement SLURPs, and the Multi-sig issues contract changes.

## Rationale
 
Currently, the stake.link protocol has no formal governance structure, and no process for parties to formally propose changes and upgrades to the protocol. 

The adoption of Council style governance allows for both meaningful formal community input and rapid iteration of the protocol. 

## Specification 

### SLURP Process and Format

#### Format

Defined by [SLURP-0](https://github.com/stakedotlink/stakedotlink-upgrade-request-proposals/blob/main/SLURPs/SLURP-0.md)

#### Process

1. Informal ideation, vetting, discussion, and development in [Discord](https://discord.gg/QZ3KsuJtCx)
2. Formal discussion, development, and initial draft proposal of SLURP in [Discourse](https://talk.stake.link)
3. Formally propose SLURP in [Github](https://github.com/stakedotlink/stakedotlink-upgrade-request-proposals)
4. Council votes on SLURPs via [Snapshot](https://snapshot.org/#/stakedotlink.eth)

### Council Composition

#### Community Seats
* Seth Vanderlaan
* Jimmy Russles

#### Node Operator Seats
* Peter - Chainlayer
* Thorsten - Cryptomanufaktur
* Jonny - LinkPool
* Ryan - LinkPool
* Eric - LinkPool

### Council Terms

#### Community Seats

6 month Epochs (terms of service), future members determined by straight voting power determined by SDL, stSDL, and SDL in LP positions.

#### Node Operator Seats

12 month Epochs, members appointed by Multi-sig holders

#### Council Member Voting Power

Leveraging an implementation similar to the [Thales Council](https://etherscan.io/address/0xA71F5fACaF3e021897931BE44b10d68F89EC6a3B#code), NFTs will be assigned to Council members during their tenure and revoked at the end of the Epoch of their service.

### Voting

After discussion on talk.stake.link, this SLURP (SLURP-1), paired with the implementation specifications of SLURP-0, will be put up for a YES/NO vote based on simple SDL/stSDL/SDL in LP position holdings via Snapshot.

## Copyright
 
Copyright and related rights waived via CC0.
