![QRL article banner](assets/banner-article.png)

# What Network Does QRL Use?

**Short answer.** QRL runs on its own layer-1 blockchain, secured by RandomX proof of work, with addresses that begin with Q. It is not a token on Ethereum, not a sidechain of Bitcoin, and not connected to either. The Zond workstream is a separate network with its own design and no mainnet date.

## The chain

A layer-1 network is a blockchain that runs its own consensus, keeps its own state and validates its own transactions. QRL is one: it has its own genesis block, its own transaction format and its own supply schedule.

That means a QRL transaction is not settled by another chain's miners, and QRL's security does not inherit from a larger network. It comes from the work done on this chain.

The distinction matters practically. A token on Ethereum moves when an Ethereum contract says so, and its rules are whatever that contract encodes. A QRL balance is held at a QRL address, and the rules are the protocol's.

## Consensus

Blocks are produced by proof of work using RandomX, an algorithm designed for general-purpose processors rather than specialised hardware. Miners compete to extend the chain, and the chain with the most accumulated work is the one nodes accept.

Proof of work has consequences a reader should know. There is no staking on this chain, because staking belongs to proof-of-stake consensus. New coins are issued as block rewards. And mining is the activity that secures the network, which is why https://github.com/qrl-wallet/token-facts-and-prices/blob/main/can-you-mine-qrl.md covers the hardware and the economics.

The algorithm choice is not cosmetic. RandomX is memory-hard and awkward to accelerate with custom silicon, which keeps participation within reach of ordinary machines.

## Addresses

QRL addresses begin with Q. The prefix is part of the encoding rather than a label, and it is the quickest check that a withdrawal form is sending to the right network.

Behind an address is a hash-based key with a finite number of one-time signatures, 1,024 at the default tree height. That is the property the whole design exists for: a spend is authorised by a signature that does not rest on elliptic-curve mathematics.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/is-qrl-a-cryptocurrency.md covers why the asset is a coin rather than a token, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-the-qrl-quantum-resistant-ledger.md covers the project.

## The block explorer

A block explorer shows what the chain recorded: blocks, transactions, addresses and balances. For QRL, the explorer is the way to check a payment arrived, to see whether an address has spent, and to read the fee a transaction paid.

It is also the tool that answers questions no summary can. Whether a transaction confirmed, how many coins an address holds, and whether an issuance happened are all visible there, without trusting a page like this one.

What the explorer cannot do is tell you who owns an address. Balances are public; ownership is not recorded, and an address can belong to an exchange holding many customers' coins.

## Receiving and sending on this network

Receiving is passive: the address and its QR code are enough, and receiving does not consume a signature. https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/receive-qrl-in-your-wallet.md covers that side, including what to check when a balance has not appeared.

Sending consumes a one-time key, which is why the wallet shows the remaining count and why running two copies of one wallet is dangerous. The transaction carries a fee, calculated in the smallest unit, and confirmed by nodes rather than by a company.

Finality is a matter of blocks rather than a receipt. A transaction is settled once it is included and the chain has moved on, and the explorer is where you read that rather than the wallet's own claim that it sent something.

## Where Zond fits

Project Zond is a separate network, not a version of this one. Its design is EVM-compatible and proof of stake with ML-DSA signatures, and it runs on a test network with no published mainnet date.

That means two things a reader should hold apart. Zond does not carry QRL balances, and nothing published says it will. And a change described for Zond is not a change to the chain your wallet connects to.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-is-project-zond-for-qrl.md covers the workstream in detail, including the parts of its design that differ from the chain in use today.

## What QRL is not

It is not an ERC-20 token, so there is no contract address to add to an Ethereum wallet and no token approval to sign. A page instructing you to "add QRL as a custom token" is describing something else, usually a token that borrowed the ticker.

It is not a sidechain or a Layer 2, so there is no bridge and no wrapped version that the project operates. A wrapped asset, if one exists somewhere, is a claim on a custodian rather than a QRL balance.

And it is not a bank settlement network. QRL settles its own transactions and nothing else, which is also why the financial-reset narrative around it is false.

## FAQ

### Is QRL an ERC-20 token?

No. It is the native coin of its own layer-1 chain. There is no contract address and no token approval step.

### What secures the network?

Proof of work using RandomX, an algorithm designed for general-purpose processors. Miners extend the chain and the most-work chain wins.

### Where can I see transactions?

On a QRL block explorer, which shows blocks, transactions, addresses and balances. It shows what the chain recorded, not who owns an address.

### Does Zond replace this network?

Zond is a separate design running on a test network. It does not carry QRL balances, and no date has been published for a mainnet.

<!-- answers: Q023, Q177 -->
