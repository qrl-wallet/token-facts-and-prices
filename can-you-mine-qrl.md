![QRL article banner](assets/banner-article.png)

# Can You Mine QRL?

**Short answer.** Yes. QRL is secured by proof of work using RandomX, an algorithm designed for general-purpose processors, so mining is done on ordinary CPUs rather than on specialised hardware. You can mine solo or join a pool, and whether it pays depends on your hardware, your electricity and the network's difficulty, none of which this page can promise.

## How QRL mining works

Miners propose blocks, and the network accepts the chain with the most accumulated work behind it. The reward for a valid block is new QRL plus the fees of the transactions it includes, which is how new coins enter circulation.

Consensus is proof of work today. That detail matters for two reasons: it means mining is the way new supply is issued, and it means there is no staking on this chain, which https://github.com/qrl-wallet/token-facts-and-prices/blob/main/can-you-stake-qrl-today.md covers.

The algorithm is RandomX, chosen because it runs well on the processors people already own. The design goal is that a machine built for general computing is competitive, rather than being outclassed by an application-specific chip.

## RandomX and CPUs

RandomX is memory-hard and uses a virtual machine whose code is generated at random, which makes it awkward to accelerate with custom silicon and friendly to a CPU with cache and memory bandwidth.

For a miner that means the hardware question is about cores, cache and memory rather than about buying a miner. A desktop or a server can participate; a laptop can, though heat and noise make it a poor home for a long run.

It also means the competition is other people's computers, not a supply chain of specialised devices. That shapes the economics: the network's difficulty adjusts to the total hash rate, so more miners sharing the same reward means less per miner.

## Solo versus pool

Solo mining means your machine searches for blocks on its own. If it finds one, you receive the whole reward. At small hash rates the wait between blocks can be long and unpredictable, which is why many people never see one.

Pool mining means many miners combine their work and share rewards in proportion to what they contributed. Payouts are smaller and more frequent, at the cost of a pool fee and a trust decision about the operator.

Neither is better in the abstract. Solo suits a miner who can tolerate variance; a pool suits someone who prefers steady small payments. What matters either way is that the payout address is yours.

## What it costs

Three costs: the hardware you already have or buy, the electricity to run it continuously, and the wear that comes with it. Against those sits the reward, which moves with the network's difficulty and with the price of the coin.

This page will not quote a profit figure, because any figure would depend on your electricity tariff, your hardware, the difficulty at the moment you read it and the price you could sell at. A number computed elsewhere is a number for someone else's situation.

The honest way to work it out is arithmetic you do yourself: power draw in watts, hours in a month, your tariff, and the expected share of the network's reward. If the result is close to break-even, it is sensitive to every input.

Transaction fees are the other half of a block reward, and they are small relative to the issuance. https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/understanding-qrl-transaction-fees.md explains how a fee is attached to a transaction, which is also the fee your own spends will pay.

## Mining to a wallet address

Rewards are paid to an address, and the address has to be yours. That means creating a wallet first, backing up the phrase before it holds anything, and using the address the wallet gives you.

https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/create-your-first-qrl-address.md covers that sequence. The point worth repeating is that mining income is still income at an address: if the phrase is lost, the coins are lost, and a pool payout does not change that.

Mining does not consume the address's one-time keys, because receiving does not sign anything. Spending the reward does, which is why an address used for mining income still has its full signature count until you move the coins.

## What mining does for the network

Miners secure the chain. The work is what makes rewriting history expensive, and the distribution of mining across many independent machines is part of what that security rests on.

That is also why the algorithm choice is a security question rather than a hobbyist convenience. An algorithm that only specialised hardware can run concentrates block production; one designed for ordinary processors keeps participation broader. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/what-network-does-qrl-use.md covers the network's design, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-token-supply-explained.md covers how mining relates to the supply cap.

## Mining other coins is a different question

Questions about mining often arrive with another coin in mind, and the answers do not transfer. A chain that is not mined at all cannot be mined by any hardware, and a chain with a different algorithm needs different equipment.

For QRL the specifics are: proof of work, RandomX, CPU-oriented, with a fixed maximum supply and a block reward that is part of the emission schedule. Everything else about profitability is local to your machine and your tariff.

## FAQ

### Can I mine QRL on a GPU?

RandomX is designed for general-purpose processors, so a CPU is the natural choice. Whether a particular GPU setup works depends on the miner software rather than on the protocol.

### Do I need special hardware?

No. That is the point of the algorithm choice: an ordinary desktop or server can participate, though electricity and heat determine whether it is worth doing.

### How long until I find a block solo?

It depends on your share of the network's total work, and at small hash rates the wait can be long and irregular. A pool trades the large occasional reward for smaller frequent ones.

### Does mining use up my address's signatures?

No. Receiving does not sign, so mining income does not consume the one-time keys. Spending the coins does.

<!-- answers: Q084, Q086, Q089 -->
