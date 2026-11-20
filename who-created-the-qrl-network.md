![QRL article banner](assets/banner-article.png)

# Who Created the QRL Network?

**Short answer.** QRL was started in 2016 by Dr. Peter Waterland and a group of founding developers, who published the design before the network launched in 2018. It has been maintained as an open-source project since, with a foundation acting as steward rather than as an owner of the chain.

## The origin

The project began in 2016, two years before its first block. That gap is typical of serious cryptography work: a design is written, argued over and implemented before there is a network to point at.

The founding claim was specific. Existing blockchains signed with elliptic-curve cryptography, which a sufficiently large quantum computer would be able to break. QRL's proposal was to sign with hash-based signatures from the first block, accepting the operational cost that comes with them.

That cost is real and visible in the software: a finite number of one-time keys per address, an index the wallet must track, and a wallet file that carries state rather than only a key.

## The whitepaper and design choices

The design documents set out the consensus, the signature scheme and the monetary policy. Proof of work with RandomX was chosen so that mining stays within reach of ordinary processors, and the supply was fixed at a maximum.

The signature choice is the part that defines the project. XMSS is standardised in RFC 8391 and profiled by NIST in SP 800-208, which means the scheme was not invented for the occasion: it is a published construction with a specification others can audit against.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/why-qrl-is-quantum-proof.md covers the reasoning, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-network-does-qrl-use.md covers the network's architecture.

## The gap between design and launch

Two years separated the project's start from its first block, and the reason is visible in what launched: a signature scheme that was not in use at that scale, a wallet that had to manage state no wallet had managed before, and a network that had to run with both from the first block.

That order matters for how the project's claims should be read. The design was published before there was a coin to sell, which is the opposite of launching first and documenting later. A reader checking the record can see the sequence: documents, implementation, then a live chain.

It also explains why the software's unusual behaviour is not an accident. The finite key count and the tracked index are consequences of the scheme chosen in 2016, not features added afterwards.

## Who maintains it now

Development happens in public. The wallet's repository carries the code, the release history and the issue tracker, and the licence is MIT, which means anyone can read, fork or build it.

Stewardship sits with the QRL Foundation, a Swiss non-profit, alongside the operating company. A foundation in that role handles the project's continuity, documentation and relationships; it does not hold the chain, and it cannot rewrite a balance.

That distinction matters when someone claims the project could freeze coins or mint more. Neither is available to a steward of a proof-of-work chain with a fixed cap: there is no administrative key over balances, and new coins come from mining.

## How to verify activity yourself

Four checks take a few minutes and need no trust in a summary.

Look at the release history in the wallet repository, and note the date of the most recent release. Look at the commit history, which shows work between releases. Look at the audits, which name external firms and years. And look at the Zond workstream, which is the project's forward work and is documented separately.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-the-qrl-project-still-active.md walks through those checks, and https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/qrl-security-audit-history.md covers the audits in detail, including what each one examined.

## What decentralised does and does not mean

It does not mean there is no organisation. A foundation exists, developers are employed, and decisions are made by people with names.

It means no single party can change the rules unilaterally or move coins it does not hold. The consensus rules are enforced by the nodes that run the software, the supply is fixed by the protocol, and the code is public enough that a change would be visible.

That is a weaker claim than the word sometimes implies, and a more useful one. It is also checkable: a fork, a release and a commit history are all observable, and none of them requires believing anyone's description of the project.

## Attribution, carefully

Names and dates on this page come from the project's own record rather than from a third-party biography. Where a claim about a person could not be verified from that record, it is not made.

The reason for the caution is practical. Founding stories attract embellishment, and a page that repeats an unverified detail lends it credibility it has not earned. The verifiable core is enough: a founder, a design published before launch, a network running since 2018, and a public repository.

https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/qrl-wallet-source-code-licence.md covers what the licence allows, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md covers what the project is.

## FAQ

### Who founded QRL?

Dr. Peter Waterland, with a group of founding developers. The project began in 2016 and its network launched in 2018.

### Is there a company behind the coin?

There is a foundation and an operating company that steward the project. Neither owns the chain or can move balances, and the supply is fixed by the protocol.

### Can the foundation change the supply?

No. The maximum is part of the protocol, and changing it would require the network's participants to accept a different set of rules.

### How can I check the project is active?

Read the release history, the commit history, the audits and the Zond documentation. Each is public and each takes minutes.

<!-- answers: Q154 -->
