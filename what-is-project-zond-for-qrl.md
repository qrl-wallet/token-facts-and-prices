![QRL article banner](assets/banner-article.png)

# What Is Project Zond for QRL?

**Short answer.** Project Zond is the QRL 2.0 workstream: an EVM-compatible, proof-of-stake network using ML-DSA signatures, running on a test network and separate from the QRL chain in use today. It has no mainnet date, and holding QRL does not entitle you to anything on it.

## What Zond is

Zond is a second network, not an upgrade applied to the first. Its design changes consensus, its execution environment and its signature scheme at once, which is why it is described as a successor rather than a version.

The current QRL chain continues to run as it does: proof of work, XMSS signatures, its own transaction format. Zond would be a different chain with different rules, and the two are not interchangeable at the protocol level.

That distinction is the one most confusion comes from. A question about Zond is not a question about your wallet, and a change described for Zond is not a change coming to the chain you are using.

## What changes

Three changes define the design.

Consensus moves from proof of work to proof of stake, which replaces mining with validators and changes what secures the chain. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/can-you-stake-qrl-today.md covers what that implies, including the fact that staking does not exist on the current chain.

Execution becomes EVM-compatible, which means contracts and tooling written for Ethereum's virtual machine are intended to run there. That is a large practical difference: it opens a tooling ecosystem that QRL's current chain does not share.

Signatures move to ML-DSA, a lattice-based scheme, rather than the hash-based XMSS used today. Both are post-quantum families, and the change is about performance and ecosystem fit rather than about dropping quantum resistance.

## Why EVM compatibility matters

An EVM-compatible chain executes the same contract bytecode as Ethereum, which means wallets, libraries and developer tooling built for that ecosystem can be pointed at it with configuration rather than a rewrite. For a network starting fresh, that is the difference between an empty tooling landscape and a populated one.

The choice carries more than convenience. The account model, the fee market and the way contracts hold value all follow the EVM's conventions rather than those of QRL's current chain, so a user moving between the two would find familiar tools and unfamiliar addresses.

It is also the part that makes a proof-of-stake design practical, because validator tooling for that environment already exists.

## What does not change

There is no mainnet date. The project has not published one, and a page that supplies a date is supplying something it does not have.

There is no migration promise. Nothing in the published material says that QRL coins convert one for one, that a snapshot will happen, or that holding today entitles you to anything on a future network. Treat any such claim, particularly from an account asking for a deposit, as unverified at best.

And the wallet's release series is separate. Zond is not a version of the desktop wallet, and a release note for the wallet is not an announcement about Zond. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-the-qrl-project-still-active.md covers how to read the release history without conflating the two.

## Testnet status

Zond runs on a test network. Test networks exist so that software can be exercised before real value is at stake, and their tokens carry no monetary value.

Practically that means three things. A testnet balance is not a mainnet balance, and a wallet pointed at one shows the other as empty. Rewards earned there cannot be sold. And a project asking you to send real assets to participate in a test is not running a test.

Following the work is free. Reading the repositories and documentation costs nothing and is the way to see what has actually shipped rather than what has been described.

## Why the signature change matters

QRL's current signatures are hash-based, which is what makes them resistant to Shor's algorithm without relying on lattice assumptions. ML-DSA is also post-quantum, standardised separately, and built on different mathematics.

For a user the practical differences are in key and signature sizes, verification cost, and the tooling that supports them. For the network, the change buys compatibility with an ecosystem that is already building around lattice-based schemes.

https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/how-qrl-xmss-signatures-work.md explains the scheme in use today, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/why-qrl-is-quantum-proof.md covers why hash-based signatures were chosen for the first chain.

## How to follow progress

The project's repositories are the primary record: commits, releases and issues show what is being worked on and what has been completed. Documentation describes the design as it stands.

What those sources do not provide is a schedule. A design document can describe a network in detail without implying when it will be live, and in Zond's case that is exactly the situation.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-network-does-qrl-use.md covers the network you can use today, which is the one that holds value and the one the wallet connects to.

## FAQ

### Is Zond live?

No. It runs on a test network. The QRL chain in use today is a separate, live network.

### Will my QRL coins move to Zond?

Nothing published says so. There is no stated conversion, snapshot or one-for-one migration, and any offer built on that assumption should be treated as unverified.

### Is Zond a wallet update?

No. It is a separate network design. The desktop wallet's releases are its own series, and a wallet release is not a Zond announcement.

### What signatures will Zond use?

ML-DSA, a lattice-based post-quantum scheme, rather than the hash-based XMSS used on the current chain.

<!-- answers: Q166, Q180 -->
