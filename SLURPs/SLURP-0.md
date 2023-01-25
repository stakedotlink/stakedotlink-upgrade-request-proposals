---
id: slurp-1
title: SLURP-1:SLURP Purpose and Guidelines
status: Draft
author: Eric Jaurena @ericjaurena
description: SLURP-1:SLURP Purpose and Guidelines
discussions-to: https://talk.stake.link 
hide_title: false
sidebar_label: SLURP-1
---

## What is a SLURP?

SLURP stands for stake.link Upgrade Request Proposal, it has been adapted from the EIP (Ethereum Improvement Proposal), SIP (Synthetix Improvement Proposal), and TIP (Thales Improvement Proposal) standards. The purpose of this process is to ensure changes to the stake.link protocol are transparent and well governed.

A SLURP is a design document providing information to the stake.link community about a proposed change to the protocol. The author is responsible for building consensus within the community and documenting dissenting opinions.

## SLURP Rationale

SLURPs are intended to be the primary mechanism for proposing new features, collecting community input on an issue, and for documenting the design decisions for changes to Thales. TIPs will describe standards, protocol specifications, and contract standards. 

It is recommended that a single SLURP contain only a single key proposal or idea. The more focused the SLURP, the more successful it is likely to be.

A SLURP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement.

## SLURP Work Flow

Parties involved in the process are the *author*, the *stake.link Governing Council* and a *specific Council member* assigned to this individual SLURP, the *stake.link Core Contributors*, and the *stake.link community*.

:warning: Before you begin, vet your idea with the community, this will save you time. Ask the stake.link community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will have broad support or the intended effect. The appropriate initial public forum to gauge interest around your proposal is [the stake.link Discord](https://discord.gg/QZ3KsuJtCx). After gauging interest and initially vetting your idea, the appropriate forum to further develop and formalize your idea is [the stake.link Discourse forum](https://talk.stake.link).

Your role as the author of a SLURP is to write the SLURP using the style and format described below, shepherd the discussions in the appropriate forums, build community consensus around the idea, and incorporate relevant feedback. Following is the process that a successful SLURP will move along:

Each status change is requested by the SLURP author and reviewed by the stake.link Core Contributors. Use a pull request to update the status. Please include a link to where people should continue discussing your SLURP. The stake.link Core Contributors will process these requests as per the conditions below.

* **Draft** -- This SLURP is work-in-progress and being reviewed by a stake.link Council member with the author.
* **Vote Pending** -- This SLURP is scheduled for vote on the stake.link Snapshot space.
* **Approved** -- This SLURP has passed community governance and is now being prioritised for development.
* **Implemented** -- This SLURP has been implemented and deployed to mainnet.
* **Rejected** -- This SLURP has failed to reach community consensus.

## What belongs in a successful SLURP?

Each SLURP should have the following components:

- **Preamble** - Headers containing metadata about the SLURP, including the SLURP number, a short descriptive title (limited to a maximum of 44 characters), and the author details.
- **Simple Summary** - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the SLURP.
- **Abstract** - a short (~200 word) description of the technical issue being addressed.
- **Motivation** - The motivation is critical for SLURPs that want to meaningfully change the stake.link protocol. It should clearly explain why the existing specification is inadequate to address the problem that the SLURP solves. SLURP submissions without sufficient motivation may be rejected outright.
- **Specification** - The technical specification should describe the syntax and semantics of any new feature.
- **Rationale** - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- **Test Cases** - Test cases may be added during the implementation phase but are required before implementation.
- **Copyright Waiver** - All TIPs must be in the public domain. See the bottom of this TIP for an example copyright waiver.

## SLURP Formats and Templates

SLURPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that SLURP as follows: `assets/SLURP-X` (for SLURP **X**). When linking to an image in the SLURP, use relative links such as `../assets/SLURP-X/image.png`.

## SLURP Header 

Each SLURP document must begin with the following markdown header fields completed, preceded and followed by three hyphens (`---`). 

`- id`: A unique document id. If this field is not present, the document's id will default to its file name (without the extension).

`- title`: The title of your document. If this field is not present, the document's title will default to its id.

`- status`: Draft | Vote Pending | Approved | Implemented | Rejected

`- author`: [a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s)]

`- description`: Short description of SLURP 

`- discussions-to`: [URL pointing to the official discussion thread]

`- created`: date created on

`- updated`: comma seperated list of dates

`- hide_title`: Whether to hide the title at the top of the doc. (True/False)

`- sidebar_label`: The text shown in the document sidebar and in the next/previous button for this document. If this field is not present, the document's `sidebar_label` will default to its title.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses, or usernames of the authors/owners of the TIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> `[Random J. User](address@dom.ain)`

or

> `[Random J. User](https://github.com/RandomJUser)`

if the email address or GitHub username is included. 

If the email address is not given the author header value must be:

> Random J. User

#### `discussions-to` header

While a SLURP is in **Draft** status, a `discussions-to` header will indicate the URL where the SLURP is being discussed.

#### `created` header

The `created` header records the date that the SLURP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the SLURP was updated with "substantial" changes. This header is only valid for SLURPs of Draft and Active status.

#### `requires` header

SLURPs may have a `requires` header, indicating the SLURP numbers that this SLURP depends on.

## Auxiliary Files

SLURPs may include auxiliary files such as diagrams. Such files must be named `SLURP-XXXX-Y.ext`, where “XXXX” is the SLURP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Assigned Council Member Responsibilities

For each new SLURP proposed, the assigned Council member does the following:

- Read the initial proposal from talk.stake.link to check if it is ready, sound, and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the SLURP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the proposed SLURP isn't ready, the assigned Council member will send it back to the author for revision, along with specific instructions.

Once the proposed SLURP is ready for the repository, the assigned Council member will:

- Assign a SLURP number (generally the number of the next PR, or if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this SLURP)

- Request the PR be merged by the Core Contributors

- Notify the SLURP author via a comment on the SLURP's original talk.stake.link post with the next step

Many SLURPs are written and maintained by developers with write access to the stake.link codebase. The assigned Council members will monitor SLURP changes, and correct any structure, grammar, spelling, or markup mistakes they see.

The assigned Council members don't pass judgment on SLURPs. They merely do the administrative & editorial part.

## History

The SLURP document was derived heavily from the EIP Ethereum Improvement Proposal, Synthetix Improvement Proposal, and Thales Improvement Proposal documents in many places text was simply copied and modified. Any comments about the SLURP document should be directed to the governing Council. The history of the EIP is quoted below from the EIP document  for context:

*"This document (EIP) was derived heavily from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/). In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use..."*

January 30, 2023: SLURP 1 has been drafted and submitted as a PR.


See [the revision history for further details](https://github.com/Thales-Markets/).

### Bibliography

1. [stake.link Discord](https://discord.gg/QZ3KsuJtCx)
2. [stake.link Discourse](https://talk.stake.link)
3. [pull request](https://github.com/stakedotlink/SLURPs/pulls) 
4. [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
5. [Thales's TIP-01](https://github.com/thales-markets/thales-improvement-proposals/blob/main/TIPs/TIP-1.md)
6. [Synthetix's SIP-01](https://sips.synthetix.io/sips/sip-1/)
7. [Bitcoin's BIP-0001](https://github.com/bitcoin/bips)
8. [Python's PEP-0001](https://www.python.org/dev/peps/)


## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
