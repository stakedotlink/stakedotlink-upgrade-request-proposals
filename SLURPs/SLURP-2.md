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

### Candidate Eligibility

Following conclusion of voting on this SLURP, there will be a period of one week during which candidates will be able to put their name up for election. Node operators and Chainlink Labs employees are not allowed to run. You cannot put someone else’s name up to run for the election, only yours. Nominate yourself by posting a brief bio to be considered by voters in the `Elections` category of talk.stake.link.

### Voters (for the Community Seats Election)

Only SDL/stSDL/SDL in LP position not belonging to a node wallet or Chainlink Labs are allowed to vote 

### Election

After a one week nomination and discussion period on talk.stake.link, the candidates will be put up for a vote using [weighted voting](https://docs.snapshot.org/proposals/voting-types#what-is-a-voting-system) based on simple SDL/stSDL/SDL in LP position holdings for the voters designated above via Snapshot. The two candidates with the most votes will be elected for the first Epoch.




## Copyright
 
Copyright and related rights waived via CC0.
