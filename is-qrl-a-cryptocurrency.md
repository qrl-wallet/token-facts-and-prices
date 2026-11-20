![QRL article banner](assets/banner-article.png)

# Is QRL a Cryptocurrency?

**Short answer.** Yes. QRL is a cryptocurrency with its own blockchain and its own native coin. It is not a token issued on another chain, it is not a share in a company, and its supply is fixed at 105,000,000 coins rather than adjustable at a team's discretion.

## The short answer, in detail

A cryptocurrency is a digital asset issued and moved by a blockchain's own rules. QRL meets that definition without qualification: the chain issues the coins through mining, validates transfers with its own consensus, and records every balance in its own state. The full description of the chain is in [What Is the QRL Quantum Resistant Ledger?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md).

The distinction that matters most is coin versus token. A token is a contract entry inside somebody else's chain, and its existence depends on that chain continuing to run and on the contract not being changed. A coin on its own chain depends on nothing outside itself.

QRL is the second kind. There is no contract address to import, no bridge that could be paused, and no issuer that could mint more. The rules that created the supply are the same rules every node checks.

That also means the wallet is not an interface to somebody else's account system. It holds keys, talks to QRL nodes, and signs QRL transactions. Nothing in the flow requires an account, an email address or a custodian.

## Coin versus token, in QRL's case

| Question | QRL | A typical token |
| --- | --- | --- |
| Where does it live? | Its own layer-1 chain | A contract on another chain |
| Who issues new units? | The mining protocol, up to a fixed cap | The contract owner, under whatever rules were written |
| What secures a transfer? | QRL's proof-of-work consensus | The host chain's consensus plus the contract |
| How do you hold it? | A wallet file with QRL keys | A wallet that can call the contract |
| What happens if the issuer disappears? | The chain continues | The token may keep working, or may not |

The last row is the practical difference. A token's usefulness depends on a team that can upgrade or abandon a contract. A coin's usefulness depends on nodes that validate blocks, and those nodes are run by anyone who chooses to run one.

## Where the coin exists

QRL exists in three places at once, and they are the same thing seen from different angles: on the chain as balances, in a wallet as keys that control those balances, and on exchanges as claims held by a custodian until you withdraw.

The chain is authoritative. A wallet that shows a balance is reporting what the chain says, and an exchange balance is a promise to send coins when asked. Only the first two are yours in the sense that matters, which is why withdrawing to your own address is the standard step after a purchase.

The coin trades on exchanges that choose to list it, and [How to Buy QRL Coin](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/how-to-buy-qrl-coin.md) covers the steps and the regional differences. There is no presale and no allocation run by the project. If a page offers to sell you coins at a fixed price, it is not the project; the card purchase built into the wallet is the one route the software itself provides.

On-chain, the supply is public. Anyone can add up balances, inspect the largest addresses, or check that the circulating figure quoted on a market site matches what the chain shows. [QRL Price and Market Cap Data](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-price-and-market-cap.md) explains how that circulating figure becomes a market cap. That transparency is a property of the asset, not a feature the project grants.

## What backs it

What backs QRL is the same thing that backs any proof-of-work coin: the cost of producing blocks and the willingness of participants to keep validating them. There is no reserve asset and no redemption promise, and the QRL Foundation is a steward of the project rather than a backer of the coin.

Mining uses RandomX, an algorithm designed for general-purpose processors rather than for specialised hardware.

The development side is public as well. The wallet is MIT-licensed, the source is readable, and the current release is published on the project's GitHub releases page. Its cryptography has been reviewed by external firms in 2018 and again in 2026, and the scope of each review is what the claim rests on.

None of that makes the coin a safe investment. It makes it a functioning cryptocurrency with checkable properties, which is a different and much narrower statement.

## How to check a balance yourself

You do not have to trust a market site or a wallet display. A block explorer shows addresses, transactions and balances directly from the chain, and the numbers there are the ones that count; [What Network Does QRL Use?](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-network-does-qrl-use.md) describes what the explorer covers.

Start with your own address if you hold coins. Paste it into the explorer, confirm the balance and the transaction history, and note the address prefix: QRL addresses begin with Q. If a page asks for anything other than the address, it is not an explorer.

For the wider picture, compare the circulating supply shown by the explorer against the figure on a price site. When they disagree, the chain is right and the price site is behind. [QRL Token Supply Explained](https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-token-supply-explained.md) explains why the maximum and circulating numbers differ.

If the balance is smaller than you expected, check whether the coins are still on an exchange. A custodial balance does not appear in your own address until you withdraw it, and that is the most common explanation for a missing balance.

## FAQ

### Is QRL an ERC-20 token?

No. QRL runs on its own blockchain and has no contract address. Any page that asks you to add a custom token to see a QRL balance is describing a different asset.

### Does QRL have a company behind it?

The chain is not operated by a company, and the coin is not a share. Development happens in public, the wallet is open source, and no entity can mint additional coins beyond the fixed cap.

### Can I mine QRL?

Yes. QRL uses proof-of-work consensus with the RandomX algorithm, which runs on ordinary processors. Mining rewards are issued by the protocol and are subject to the same fixed supply as every other coin.

### Where can I check the circulating supply?

On a QRL block explorer, which reads the chain directly. Market sites usually report a similar figure, but the explorer is the reference when the two disagree.

<!-- answers: Q061, Q068, Q269 -->
