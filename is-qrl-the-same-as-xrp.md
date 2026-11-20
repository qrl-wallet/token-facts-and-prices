![QRL article banner](assets/banner-article.png)

# Is QRL the Same as XRP?

**Short answer.** No. QRL and XRP are unrelated projects on separate chains, with different consensus, different supply rules and different signature schemes. The confusion usually starts with a search result or a ticker pattern, not with anything the two projects share.

## Where the confusion comes from

Both tickers are three letters, both appear in the same "quantum" search results, and both get discussed in the same threads about which coins survive a quantum computer. That is enough for a search engine to place them side by side and for a reader to assume a relationship.

The relationship does not exist. There is no partnership, no shared team, no shared supply and no bridge between the chains. QRL is a proof-of-work network with hash-based signatures; the XRP Ledger is a separate network with its own consensus and its own asset.

The more specific confusion, and the one worth correcting carefully, is the assumption that because QRL is quantum resistant, XRP must be too, or that the two are competing versions of the same idea. They are not versions of anything. They were built for different purposes and they secure transactions differently.

## The two projects side by side

| Property | QRL | XRP Ledger |
| --- | --- | --- |
| Chain | Its own layer-1 network | Its own layer-1 network |
| Consensus | Proof of work, RandomX | A federated consensus protocol |
| Supply | Fixed cap, 105,000,000 | Fixed maximum, released over time |
| Signature scheme | XMSS, hash-based | Classical elliptic-curve schemes |
| Quantum resistant signatures | Yes, in the live signing path | No, classical signatures sign transactions |
| Purpose | A quantum-resistant store and transfer chain | Fast settlement and payments |

The row that matters for this comparison is the signature scheme. Everything else is context, and the context explains why the two get compared at all: both are old by crypto standards, both have fixed supplies, and both are discussed as payments infrastructure rather than as platforms for applications.

## Signature schemes, in plain terms

QRL signs with XMSS, a hash-based scheme. Each address owns a tree of one-time keys, the root of that tree is the public key, and a spend reveals one key plus the path that proves it belongs to the tree. Breaking that means breaking the hash function, which is not what a quantum computer running Shor's algorithm does.

The XRP Ledger signs with classical elliptic-curve keys. Those keys are secure against ordinary computers and vulnerable, in principle, to a sufficiently large quantum machine running Shor's algorithm. That is a statement about the mathematical problem the keys rest on, not a prediction about when such a machine will exist.

Research and proposals to add post-quantum signatures exist in many ecosystems, including this one. A proposal is not a deployment. What counts for a holder is the scheme that signs transactions today, and on the XRP Ledger that scheme is classical.

The full comparison, with the questions people actually ask about XRP and quantum computing, is in [Is XRP Quantum Resistant?](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-xrp-quantum-resistant-like-qrl.md).

## What to check before buying either

Identity first. QRL is bought on exchanges that list it, it runs on its own chain, and it has no contract address. If a page asks you to import a token or connect a wallet to claim something, it is not describing QRL.

Supply second. The QRL cap is 105,000,000, and the circulating figure is roughly 79.5 million. Anything that quotes a different cap for this asset is either wrong or describing a different coin with similar letters.

Third, check what you are actually buying. A custodial balance on an exchange is a promise, not a holding. Withdrawing to an address you control is what turns it into a position on the chain, and that step is the same for both assets even though the address formats differ.

Finally, ignore anything that frames the choice as a contest with a foregone winner. The two chains do different jobs, and the quantum question is one property among many rather than a verdict on either.

## Where the longer comparison sits

If your question was specifically whether XRP is quantum resistant, [Is XRP Quantum Resistant?](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-xrp-quantum-resistant-like-qrl.md) answers it directly and stays on the signature question. If your question was what QRL is at all, start with [What Is the QRL Quantum Resistant Ledger?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md) and then read [Why QRL Is Quantum Proof](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/why-qrl-is-quantum-proof.md).

For the supply side, [Is QRL a Cryptocurrency?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-qrl-a-cryptocurrency.md) explains the cap and the circulating figure, and [How to Buy QRL Coin](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/how-to-buy-qrl-coin.md) covers how to acquire the coin without landing on a lookalike. Those two pages are the ones that stop most ticker-level mistakes.

Nothing on this page is a judgement about XRP's usefulness, its team or its price. The comparison is narrow on purpose: which signature scheme secures a transaction, and what that means for the quantum question.

## FAQ

### Are QRL and XRP partners?

No. They are separate projects with separate teams and separate chains. There is no partnership, no shared development and no bridge between them.

### Is XRP quantum resistant like QRL?

Not in its live signing path. The XRP Ledger signs with classical elliptic-curve keys, while QRL signs with XMSS, a hash-based scheme. Proposals to change that are not the same as a deployed scheme.

### Did QRL come from XRP?

No. QRL was designed independently and has run its own chain since 2018. The similarity is a three-letter ticker and a shared place in quantum-resistance discussions.

### Can I hold both?

Yes, they are unrelated assets and holding one does not affect the other. Just check the ticker and the chain when you buy, because lookalike listings exist for both.

<!-- answers: none -->
