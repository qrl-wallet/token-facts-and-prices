![QRL article banner](assets/banner-article.png)

# Why QRL Is Quantum Proof

**Short answer.** A QRL spend is authorised by a hash-based one-time signature rather than an elliptic-curve one. Breaking it means breaking the hash function, not factoring a key or solving a discrete logarithm, and those are the problems a quantum computer with Shor's algorithm would solve. That is the mechanism, and it has been in place since the first block in 2018.

## The mechanism in one page

A wallet holds a seed. From that seed, a tree of one-time keys is derived, and each key is built from hash computations. To spend, the wallet uses one leaf of the tree, producing a signature that reveals the path from that leaf to the root.

The verifier checks the hashes. It does not need to be told the private key, and it does not solve a hard number-theory problem; it recomputes hashes and compares them to the root it already trusts.

That is the whole design in outline. What makes it quantum resistant is what it depends on: a hash function's resistance to collision and preimage attacks, rather than the difficulty of reversing a curve.

## Why hash-based beats curve-based here

Elliptic-curve signatures rest on the discrete logarithm problem. Given a public key, recovering the private key is believed to be hard for a classical computer and is known to be tractable for a quantum computer running Shor's algorithm at sufficient scale.

Hash-based signatures rest on a different assumption. There is no algebraic structure for Shor's algorithm to exploit, because the security comes from the behaviour of a hash function rather than from a group operation.

Grover's algorithm does apply to hashes, and it gives a quadratic speedup for search. That is why hash lengths are chosen with margin, and why the usual estimate is that a 256-bit hash retains roughly the security of a 128-bit one against it. That is a margin question, not a break.

https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/how-qrl-xmss-signatures-work.md covers the construction, including the tree and the authentication path.

## The 1,024-signature limit and what it costs

The scheme is stateful. Each address has a finite number of signatures, 1,024 at the default tree height of 10, and each spend consumes one key.

That is the price of the design, and it is not hidden. The wallet tracks the index, shows the remaining count, and refuses to sign with a key it has already used. The network rejects a repeated signature rather than accepting it with a warning.

The limit changes a holder's routine in three ways. Receiving is free and unlimited, because receiving does not sign. Spending consumes a key, so a long-held balance eventually needs a move to a fresh address. And restoring an old wallet file restores an old index, which is why an old backup is a way to recover funds rather than a way to keep using an address.

https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/how-many-qrl-ots-keys-remain.md covers reading the count, and the move to a fresh address resets capacity because the tree belongs to the address.

## What is not yet post-quantum

QRL's signatures are post-quantum. Its peer-to-peer layer is not: node identity and transport key exchange are still classical, with post-quantum key establishment in development.

That is a real limitation and it belongs in an honest answer. It means an attacker with a quantum capability could, in principle, attack the transport between nodes even though it could not forge a spend. The two are different surfaces, and https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-qrl-p2p-layer-quantum-safe.md treats the transport on its own terms.

Nothing about that caveat weakens the signature claim. It does mean the phrase "the network is post-quantum" is false, while "the signatures are" is true.

## Quantum proof versus quantum resistant

"Quantum proof" is a strong phrase, and the honest version of it is narrower than it sounds. What can be said is that the scheme does not depend on the problems Shor's algorithm solves, so that algorithm gives no advantage against it.

What cannot be said is that any scheme is proven safe against every future algorithm. Cryptography has been wrong before: constructions that looked sound were broken by new mathematics or new engineering. A page that promises permanence is overclaiming.

The defensible statement is this: QRL's signatures rest on hash functions, hash functions are believed to resist quantum attack with a security margin rather than a break, and the scheme has been in production since 2018 with external reviews in 2018 and 2026.

## Other coins that claim the label

Several projects describe themselves as quantum resistant, and the phrase covers a range: a live post-quantum scheme, a component with a narrow scope, a design in development, or marketing attached to a classical chain.

The test does not change. Find the scheme in the specification, find a transaction that uses it, and find out when it entered the signing path. https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/quantum-resistant-cryptocurrency-list-with-qrl.md sets out that test, and https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/can-quantum-computers-break-bitcoin-and-qrl.md explains what a quantum machine would do to a chain that signs with curves.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md covers the project, and the audits' scope is the subject of its own page, because a review is only as strong as what it examined.

## FAQ

### What does quantum proof mean for QRL?

That a spend is authorised by a hash-based signature rather than an elliptic-curve one, so Shor's algorithm gives an attacker no purchase on it.

### Is the whole network post-quantum?

No. The signatures are; the peer-to-peer transport is still classical, with post-quantum key exchange in development.

### Why only 1,024 signatures per address?

Because the keys are stateful and drawn from a finite tree of that size at the default height. It is the cost of a scheme that depends only on hash functions.

### Could a future algorithm break it?

No scheme is proven against everything that might be discovered. The claim is specific: it does not rest on the problems a quantum computer is known to solve.

<!-- answers: Q063, Q095, Q097, Q098, Q100, Q106, Q107, Q108, Q111, Q112, Q115, Q117, Q118, Q120, Q121, Q124, Q125, Q157, Q164, Q165, Q181, Q189, Q251, Q258, Q259, Q272 -->
