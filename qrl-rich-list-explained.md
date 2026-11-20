![QRL article banner](assets/banner-article.png)

# QRL Rich List Explained

**Short answer.** A QRL rich list ranks addresses by balance, largest first. It is a view of the chain, not a list of people: the biggest entries are usually exchanges and services holding coins for thousands of customers, so the ranking measures custody rather than wealth.

## What the list is

A rich list is a sorted view of addresses and their balances, generated from public chain data. It exists because every balance on a public chain is visible, and sorting those balances is a trivial query for anyone running an explorer.

The list shows addresses, not identities. There is no name field, no country field and no way to tell from the chain whether two addresses belong to the same person. Everything beyond the address and the amount is inference.

That inference is where readers get into trouble. A high rank looks like a large holder, and it may well be one, but it may equally be a service that pools customer deposits. The list cannot distinguish the two, and neither can anyone reading it from outside.

## How to read a rank

Read a rank as a statement about a single address at a single moment. Balances change with every block, so a position in the list is a snapshot, and snapshots taken days apart can order the same addresses differently.

Three details make a rank interpretable. The balance, which is exact. The address age, visible from its first transaction, which separates long-dormant holdings from active service wallets. And the transaction pattern, where a wallet that receives constantly and pays out constantly looks like a business rather than a saver.

| Pattern | What it usually suggests | What it does not prove |
| --- | --- | --- |
| One large inflow, no outflows | A long-term holding | Who owns it |
| Many small inflows, regular outflows | A service or exchange wallet | Which service |
| Round-number balance, recent activity | An operational wallet | Any intent |
| Very old address, very large balance | Early participation | That the coins are still spendable by that owner |

The last row deserves a note. On QRL, an address can authorise a fixed number of spends, so an old address with a large balance may also have a limited number of signatures left. A rich list does not show that count, which is one more reason a rank is a partial picture.

## Why big addresses are usually not people

Exchanges hold customer coins in a small number of wallets. That is how custodial trading works: deposits go to a pooled address, internal ledgers track who owns what, and withdrawals come out of the same pool. The result is a handful of addresses with balances that dwarf any individual holding.

The same is true of payment processors, mining pools and any service that receives on behalf of others. Their addresses appear at the top of every rich list on every chain, and reading them as single owners produces the wrong conclusion about concentration.

For QRL specifically, the practical implication is that a rich list cannot tell you how concentrated ownership is. It can tell you how concentrated addresses are, which is a different measurement and a much less interesting one.

## What the list cannot tell you

It cannot tell you who owns an address, where they live, or whether they are buying or selling. It cannot tell you whether a balance is spendable, pledged, lost, or held by a service that owes it to somebody else.

It cannot tell you anything about price. A large balance moving does not mean a sale, and a sale does not have to touch a visible address at all. Pages that read price direction from rich-list changes are guessing, which is why [QRL Price and Market Cap Data](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-price-and-market-cap.md) separates the data from the commentary.

It also cannot tell you whether an address is secure. Keys can be lost while the balance remains visible, and a wallet that has never been backed up still shows up in the ranking. [Is the QRL Wallet Safe to Use?](https://github.com/qrl-wallet/signatures-and-comparisons/blob/main/is-qrl-wallet-safe-to-use.md) covers what visibility does not prove. Visibility is not control.

## How to check your own address

Paste your address into a QRL block explorer. QRL addresses begin with Q, and the explorer needs nothing else from you, no login, no connection, no signature.

You will see the balance and the transaction history. The transaction count is not the same as the signatures used: receiving does not consume a key, so an address can take hundreds of payments and still have its full count available. For the remaining count, the wallet is the place to look, because it tracks the index.

If you are checking whether a payment arrived, the explorer is the reference and the wallet display is the convenience, as [Receive QRL in Your Wallet](https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/receive-qrl-in-your-wallet.md) explains. If the two disagree, trust the chain, then let the wallet resync.

For the wider context, [QRL Token Supply Explained](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-token-supply-explained.md) shows why the circulating figure differs from the fixed cap, and [What Network Does QRL Use?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-network-does-qrl-use.md) explains addresses and the explorer in more detail. Both are shorter than this page and answer the questions that usually follow a first look at a rich list.

## FAQ

### Does the rich list show who owns QRL?

No. It shows addresses and balances. Ownership is not recorded on the chain, and any claim about who holds a top address is an inference rather than a fact.

### Why is one address holding so much?

Usually because it is a service. Exchanges and payment processors pool customer coins into a small number of wallets, which is why those addresses dominate every rich list on every chain.

### Can I tell how many signatures an address has left?

Not from a rich list. An explorer shows transactions, and receiving does not spend a key, so the count of payments tells you nothing about the count left. The wallet tracks the index, and a default address starts with 1,024.

### Is a large balance a sign the price will move?

No. Rich-list changes say nothing about price direction, and reading them as a signal is guesswork dressed as analysis.

<!-- answers: none -->
