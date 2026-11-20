![QRL article banner](assets/banner-article.png)

# QRL Token Supply Explained

**Short answer.** QRL has a fixed maximum supply of 105,000,000 coins, with roughly 79.5 million in circulation. The difference is not a reserve held by anyone: it is coins not yet issued, because new supply enters through mining. Market cap is the price times the circulating figure, which is why sites that use the maximum report a larger number.

## The cap

The maximum is part of the protocol, not a policy the project can revise. A proof-of-work chain with a fixed cap issues coins through block rewards and stops when the cap is reached; nobody can mint beyond it, and no administrative key exists that would allow it.

A cap matters for two reasons. It makes the supply schedule knowable in advance, and it removes a category of risk: an issuer that can create more units at will. QRL has no such issuer.

The cap also shapes the mining economics. Block rewards are issuance, and issuance is finite, so the reward available to miners declines as the remaining supply is issued.

## What is circulating

Roughly 79.5 million coins are in circulation. The figure moves as blocks are mined, so any number quoted on a page is a snapshot of the moment it was written.

Circulating supply is the number that matters for market capitalisation, because it counts coins that exist and can change hands. Coins not yet issued are not held by a person or an entity; they do not exist yet.

That is the point where careless descriptions go wrong. Calling the unissued remainder "locked", "reserved" or "team-held" implies a holder and a decision. There is neither: there is a schedule and a mining process.

## How emission worked

New coins enter as block rewards. A miner proposes a block, the network accepts it, and the reward is created and paid to the address the miner nominated, along with the fees from the transactions in that block.

That mechanism ties issuance to security: the reward is what pays for the work that secures the chain. It also means the supply is auditable on-chain, because every issuance is a transaction with a block behind it.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/can-you-mine-qrl.md covers the algorithm and the hardware, including the fact that RandomX is designed for ordinary processors.

## Where to verify supply

A block explorer shows the chain's balances and issuance, and the project's documentation states the cap. Between those two a reader can check both figures without trusting a summary.

What a page like this cannot do is give you a live number. The cap is stable and worth quoting; the circulating figure is not, and treating a snapshot as permanent is how old numbers spread between sites.

## Why supply matters for market cap

Market capitalisation is arithmetic: price multiplied by circulating supply. With a price and 79.5 million coins, the result is one number; with 105 million, it is about a third larger for the same price.

Both calculations appear in the wild, labelled the same way. When two sites disagree about a cap, check the supply first: the difference is usually there rather than in the price.

The measure itself is a shorthand for size, not a record of money invested. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-price-and-market-cap.md covers that distinction and why a thin market can move a cap without any money entering the network.

## Why the cap is credible

A cap is only worth what enforces it. Here the enforcement is the protocol: a block that pays more than the schedule allows is rejected by the nodes validating it, and no key exists that could instruct them to accept it. That is a stronger position than an announcement, because it is a rule the software applies rather than a statement someone made.

It also makes the schedule predictable in a way discretionary issuance is not. A miner can calculate what a block is worth before starting, and a buyer can calculate what share of the cap has already been issued. The difference between the two figures is the part still to come: roughly 25.5 million coins, about a quarter of the maximum, remain to be issued through mining.

That predictability is why the two numbers on this page are worth quoting separately. The cap does not move. The circulating figure moves every block, and the gap between them closes slowly.

## Distribution, not just totals

A total tells you how many coins exist. It does not tell you who holds them, and the distribution is a separate question with its own limits: an address can belong to an exchange holding thousands of customers' coins. A total also says nothing about how many people hold the coins, which is the question most readers actually have.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-rich-list-explained.md covers what a rich list can and cannot show. The short version is that concentration measured by address overstates concentration by holder, because custodial addresses aggregate balances that belong to many people.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-qrl-a-cryptocurrency.md covers the coin's status as an independent asset rather than a token on another chain, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md covers the project itself.

## FAQ

### What is the maximum QRL supply?

105,000,000 coins, fixed by the protocol.

### How many are in circulation?

Roughly 79.5 million, and the figure rises as blocks are mined. Treat any quoted number as a snapshot with a date.

### Who holds the remaining coins?

Nobody. They have not been issued yet. New supply enters through mining rewards, and there is no reserve or treasury allocation behind the difference.

### Does market cap use the maximum or the circulating supply?

Reputable calculations use circulating supply. Some sites use the maximum, which produces a larger figure for the same price.

<!-- answers: Q071, Q191 -->
