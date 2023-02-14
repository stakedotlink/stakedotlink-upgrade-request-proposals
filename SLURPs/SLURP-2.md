| id | Title | Status | Author | Description | Discussions to | Created |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| SLURP-2 | Community council elections for Epoch 1 | Draft | Mashed Mole (@mashedmole) | Submit the two community council seats to a vote for Epoch 1 | [talk.stake.link](https://talk.stake.link/t/slurp-2-draft-community-council-elections-for-epoch-1/35) | 2023-02-14

## Abstract

SLURP #1 establishes the process to formally propose and ratify changes to the protocol. It establishes a council, which role will be to vote on SLURPS. Amongst this council are two  “community seats”. SLURP #1 specifies who these two community council members will be for the first Epoch.

This SLURP #2 proposes to submit these two community council seats to a community vote.

## Rationale
 
As describes in SLURP #1 itself, “The community proposes SLURPs and votes for community Council seats”. Submitting the first Epoch to this rule would bring consistency to the protocol.

Having the community seats picked by the core contributors could be seen as a conflict of interests as the incentives of both parties are not always necessarily aligned. Having the first Epoch set up this way could weaken the protocol's reputation and integrity.

Allowing the representatives for the community to be elected by the community itself would give more legitimacy to the protocol, and since the proposals are to be proposed by the community, having someone they elected as a council member will make the ideations and discussions more fluid and constructive.


## Specification 

### Vote (for the SLURP)

* Quorum: >= 50%
* Pass: > 50%

Should the vote pass and be considered `Approved`, it will modify SLURP-1 and nullify the pre-selected Community Council seats, but will not impact Node Operator Council seats. Should the vote fail this SLURP will be considered `Rejected`, and SLURP-1 in its entirety as written will be considered `Approved`. Should the vote fail to meet quorum, it will be considered as `Rejected`. 

### Excluded Addresses

#### Chainlink Labs
* `0xdedA4c43136D4f40F75073B0d815c648330fD072`

#### Node Operators
* `0x6879826450e576B401c4dDeff2B7755B1e85d97c`
* `0x20C0B7b370c97ed139aeA464205c05fCeAF4ac68`
* `0x26119F458dD1E8780554e3e517557b9d290Fb4dD`
* `0x479F6833BC5456b00276473DB1bD3Ee93ff8E3e2`
* `0xF2aD781cFf42E1f506b78553DA89090C65b1A847`
* `0xc316276f87019e5adbc3185A03e23ABF948A732D`
* `0xfAE26207ab74ee528214ee92f94427f8Cdbb6A32`
* `0x4dc81f63CB356c1420D4620414f366794072A3a8`
* `0xa0181758B14EfB2DAdfec66d58251Ae631e2B942`
* `0xcef3Da64348483c65dEC9CB1f59DdF46B0149755`
* `0xE2b7cBA5E48445f9bD17193A29D7fDEb4Effb078`
* `0x06c28eEd84E9114502d545fC5316F24DAa385c75`
* `0x6eF38c3d1D85B710A9e160aD41B912Cb8CAc2589`
* `0x3F44C324BD76E031171d6f2B87c4FeF00D4294C2`
* `0xd79576F14B711406a4D4489584121629329dFa2C`

### Candidate Eligibility

Following conclusion of voting on this SLURP, there will be a period of one week during which candidates will be able to put their name up for election. Node operators and Chainlink Labs employees are not allowed to run. You cannot put someone else’s name up to run for the election, only yours. Nominate yourself by posting a brief bio to be considered by voters in the `Elections` category of talk.stake.link.

### Voters (for the Community Seats Election)

Only SDL/stSDL/SDL in LP position not belonging to a node wallet or Chainlink Labs are allowed to vote 

### Election

After a one week nomination and discussion period on talk.stake.link, the candidates will be put up for a vote using [weighted voting](https://docs.snapshot.org/proposals/voting-types#what-is-a-voting-system) based on simple SDL/stSDL/SDL in LP position holdings for the voters designated above via Snapshot. The two candidates with the most votes will be elected for the first Epoch.




## Copyright
 
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
